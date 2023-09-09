# Introduktion til sandsynlighedsregning i Python
## Af Henrik Sterner (henrik.sterner@gmail.com)

Sandsynlighedsregning er en måde at beskrive usikkerhed på, som er matematisk
veldefineret. Sandsynlighedsregning spiller en central rolle i mange aspekter af maskinlæring, og derfor er det vigtigt at have en grundlæggende forståelse af sandsynlighedsregning.

Vi viser hvorledes sandsynlighedsregning kan implementeres i Python ved hjælp af biblioteket `numpy`.

# Sandsynlighedsregning - centrale begreber
- Udfaldsrum
- Hændelser
- Sandsynlighedsfunktioner
- Sandsynlighedsmål
- Stokastiske variable
- Betinget sandsynlighed
- Uafhængighed
- Bayes regel
- Forventningsværdi
- Varians
- Kovarians
- Korrelation
- Markov uligheden
- Chebyshevs ulighed
- Lov om den itererede forventning
- Lov om den totale sandsynlighed
- Lov om den itererede sandsynlighed
- Centrale grænseværdisætning
- Lov om store tal

# Udfaldsrum og hændelser
Et udaldsrum er en mængde af mulige udfald. Et udfald er en mulig hændelse.
Eksempler på udfaldsrum: 
* Hvis vi kaster en mønt, så er udfaldsrummet $\{P,K\}$. P står for plat, og K står for krone.
* Hvis vi kaster to mønter, så er udfaldsrummet $\{(P,P),(P,K),(K,P),(K,K)\}$. 
* Et udfaldsrum kan være uendeligt stort, f.eks. hvis vi kaster en terning, så er udfaldsrummet $\{1,2,3,4,5,6\}$.
* Hvis vi kaster to terninger, så er udfaldsrummet $\{(1,1),(1,2),(1,3),\ldots,(6,6)\}$.
* Hvis vi kaster to terninger, og vi er interesserede i summen af øjnene, så er udfaldsrummet $\{2,3,4,\ldots,12\}$.

# Hændelser
En hændelse er en delmængde af udfaldsrummet. Eksempler på hændelser:
* Hvis vi kaster en mønt, så er hændelsen $\{P\}$.
* Hvis vi kaster to mønter, så er hændelsen $\{(P,P),(P,K)\}$.
* Hvis vi kaster to terninger, så er hændelsen $\{(1,1),(1,2),(1,3),\ldots,(6,6)\}$.
* Hvis vi kaster to terninger, og vi er interesserede i summen af øjnene, så er hændelsen $\{2,3,4,\ldots,12\}$.
* Hvis vi kaster to terninger, og vi er interesserede i summen af øjnene, og summen er større end 10, så er hændelsen $\{11,12\}$.
* Hvis vi kaster to terninger, og vi er interesserede i summen af øjnene, og summen er større end 10, og den første terning viser 6, så er hændelsen $\{11\}$.

# Hændelser og udaldsrum i Python
Vi kan repræsentere et udfaldsrum som en liste:
```python
U = [1,2,3,4,5,6]
```
Vi kan repræsentere en hændelse som en liste:
```python
A = [1,2,3]
```
Vi kan teste om et element er i en liste ved hjælp af `in`:
```python
1 in A
```
Vi kan teste om en liste er en delmængde af en anden liste ved hjælp af `issubset`:
```python
A.issubset(U)
```

  
# Matematisk definition af udaldsrum og hændelser
Et udfaldsrum er en mængde $U$. En hændelse er en delmængde af $U$.
Hvis $A$ er en hændelse, så er $A \subseteq U$. Det læses som at $A$ er en delmængde af $U$. Men $A$ kan også være lig med $U$. I så fald siger vi at $A$ er en sikker hændelse. Hvis $A$ er den tomme mængde, så siger vi at $A$ er en umulig hændelse.

# Sandsynlighedsfunktioner
Lad $U$ være et udfaldsrum bestående af udfald $u_1,u_2,\ldots,u_n$.
En sandsynlighedsfunktion er en funktion $P$ som tager en hændelse $A$ som input og returnerer et tal $P(A)$ som er sandsynligheden for at hændelsen $A$ indtræffer. Sandsynligheden $P(A)$ skal opfylde følgende betingelser:
* $P(A) \geq 0$ for alle hændelser $A$.
* $P(U) = 1$.

Udfaldsrummet sammen med sandsynlighedsfunktionen kaldes et sandsynlighedsrum eller et sandsynlighedsfelt

# Disjunkte hændelser
Sætning: To hændelser $A$ og $B$ er disjunkte hvis $A \cap B = \emptyset$. Det betyder at $A$ og $B$ ikke har nogen fælles udfald. Hvis $A$ og $B$ er disjunkte, så er sandsynligheden for at enten $A$ eller $B$ indtræffer givet ved:
$$P(A \cup B) = P(A) + P(B)$$

Bevis: Lad $A$ og $B$ være disjunkte. Så er $A \cap B = \emptyset$. Derfor er $A \cup B = A \cup B \cup \emptyset = A \cup B \cup (A \cap B) = (A \cup B) \cap (A \cup B) = A \cup B$. Derfor er $P(A \cup B) = P(A \cup B) = P(A \cup B) + P(\emptyset) = P(A \cup B) + P(A \cap B) = P(A) + P(B)$.

# Disjunkte hændelser i Python
Vi kan teste om to lister er disjunkte i numpy ved hjælp af `intersection`:

```python
A = [1,2,3]
B = [4,5,6]
print(A.intersection(B) == set())
```

# Komplementære hændelser
Definition: Lad $A$ være en hændelse. Så er den komplementære hændelse $\bar{A}$ givet ved:

$$\bar{A} = U \setminus A$$

Det betyder at $\bar{A}$ er alle de udfald som ikke er i $A$.

# Komplementære hændelser i Python
Vi kan finde den komplementære hændelse til en liste ved hjælp af `difference`:

```python
A = [1,2,3]
U = [1,2,3,4,5,6]
print(U.difference(A))
```

# Komplementære hændelser og sandsynlighedsfunktioner
Sætning: Lad $A$ være en hændelse. Så er sandsynligheden for at $A$ ikke indtræffer givet ved:
$$P(\bar{A}) = 1 - P(A)$$

Vi kan bevise sætningen ved at bruge at $A$ og $\bar{A}$ er disjunkte og at $A \cup \bar{A} = U$.

Da gælder at $P(U) = P(A \cup \bar{A}) = P(A) + P(\bar{A})$. Derfor er $P(\bar{A}) = P(U) - P(A) = 1 - P(A)$.

# Sandsynlighedsfunktioner i Python
Vi kan repræsentere en sandsynlighedsfunktion som en dictionary:

```python
P = {1: 1/6, 2: 1/6, 3: 1/6, 4: 1/6, 5: 1/6, 6: 1/6}
```

Vi kan finde sandsynligheden for en hændelse ved at summere sandsynlighederne for de udfald som er i hændelsen:

```python 
A = [1,2,3]
print(sum([P[u] for u in A]))
```

# Uafhængige hændelser
Definition: Lad $A$ og $B$ være hændelser. Så er $A$ og $B$ uafhængige hvis:
$$P(A \cap B) = P(A) \cdot P(B)$$

# Eksempel på uafhængige og ikke uafhængige hændelser
- Hvis vi kaster to terninger A og B, så er hændelsen at A viser 1 og hændelsen at B viser 2 uafhængige. De er uafhængige fordi ene terning ikke påvirker den anden terning.
- Hvis vi kaster to terninger A og B, så er hændelsen at A viser 1 og hændelsen at summen af øjnene er 2 ikke uafhængige. De er ikke uafhængige fordi hvis A viser 1, så er summen af øjnene mindst 2.

# Uafhængige hændelser i Python
Vi kan teste om to hændelser er uafhængige ved at teste om $P(A \cap B) = P(A) \cdot P(B)$:

```python
A = [1,2,3]
B = [4,5,6]
print(sum([P[u] for u in A.intersection(B)]) == sum([P[u] for u in A]) * sum([P[u] for u in B]))
```

# Sandsynligheden for uafhængige hændelser
Sætning: Lad $A$ og $B$ være uafhængige hændelser. Så er sandsynligheden for at begge hændelser indtræffer givet ved:
$$P(A \cap B) = P(A) \cdot P(B)$$
Det kan vi bevise ved at bruge at $A$ og $\bar{A}$ er disjunkte og at $A \cup \bar{A} = U$. Da gælder at $P(U) = P(A \cup \bar{A}) = P(A) + P(\bar{A})$. Derfor er $P(\bar{A}) = P(U) - P(A) = 1 - P(A)$.
Dvs. at $P(A) = 1 - P(\bar{A})$. Vi kan bruge det til at vise at $P(A \cap B) = P(A) \cdot P(B)$:
$$P(A \cap B) = P(A) \cdot P(B) = (1 - P(\bar{A})) \cdot P(B) = P(B) - P(\bar{A}) \cdot P(B) = P(B) - P(\bar{A} \cap B) = P(B) - P((A \cup B) \cap \bar{A}) = P(B) - P(A \cap B \cup B \cap \bar{A}) = P(B) - P(A \cap B) - P(B \cap \bar{A})$$
Derfor er $P(A \cap B) = P(A) \cdot P(B)$.

# Sandsynligheden for uafhængige hændelser i Python
Vi kan udregne sandsynligheden for uafhængige hændelser ved at bruge at $P(A \cap B) = P(A) \cdot P(B)$:

```python
A = [1,2,3]
B = [4,5,6]
print(sum([P[u] for u in A.intersection(B)]) == sum([P[u] for u in A]) * sum([P[u] for u in B]))
```

# Betinget sandsynlighed
Definition: Lad $A$ og $B$ være hændelser. Så er den betingede sandsynlighed for at $A$ indtræffer givet at $B$ indtræffer givet ved:
$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$

Det l


