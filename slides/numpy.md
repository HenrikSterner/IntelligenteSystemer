# Numpy i prakis af Henrik Sterner (hst@nextkbh.dk)
Numpy er et bibliotek til Python, som gør det muligt at arbejde med matricer og vektorer. Det er en forudsætning for at kunne arbejde med maskinelæring, da mange af de algoritmer vi skal arbejde med er baseret på matricer og vektorer.

Numpy tilbyder også en række funktioner til matematiske, statistiske og logiske operationer på arrays.

# Hvorfor bruge NumPy?
* NumPy er meget hurtigere end at bruge Python-lister til matematiske operationer.
* Det er også mere bekvemt og lettere at læse.
* NumPy er et standardbibliotek i Python, så det er tilgængeligt i stort set alle Python-distributioner.

# Installation af Numpy i Google Colab
Numpy er en del af Google Colab, så hvis du bruger Google Colab, så har du også Numpy. Hvis du ikke bruger Google Colab, så kan du installere Numpy ved at skrive følgende i en terminal:


# Installation af Numpy via Anaconda
Numpy er en del af Anaconda, så hvis du har installeret Anaconda, så har du også Numpy. Hvis du ikke har installeret Anaconda, så kan du installere Numpy ved at skrive følgende i en terminal:
```bash
pip install numpy
```
Numpy importeres på følgende måde:
```python
import numpy as np
```

# Arrays i numpy
Et array er en samling af elementer, som har samme datatype. Et array kan have en eller flere dimensioner. Et array med en dimension kaldes en vektor, et array med to dimensioner kaldes en matrix.

# Definition af en vektor 
En vektor er en samling af tal, som er ordnet efter en bestemt rækkefølge. En vektor kan repræsenteres som en kolonne eller en række. En vektor med n elementer kan repræsenteres som en n x 1 matrix eller en 1 x n matrix.

$$ \vec{v} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} $$

Her er $v_1, v_2, \ldots, v_n$ reelle tal, som kaldes vektorens komponenter. 

Ved $n=2$ og $n=3$ kan en vektor repræsenteres som en pil, hvor længden af pilen er lig med vektorens længde og retningen af pilen er lig med vektorens retning.

# Eksempler på vektorer
En vektor i 2d: 
$$ \vec{v} = \begin{bmatrix} 7 \\ 4 \end{bmatrix} $$
En vektor i 3d: 
$$ \vec{v} = \begin{bmatrix} 65 \\ 1 \\ -3 \end{bmatrix} $$
En vektor i 4d:
$$ \vec{v} = \begin{bmatrix} -5 \\ 56 \\ 7 \\ 4 \end{bmatrix} $$

# Vektorer i Python
I Python kan en vektor repræsenteres som en liste. For at kunne arbejde med vektorer i Python skal vi importere numpy-biblioteket. 
```python
import numpy as np
```
Vi kan nu repræsentere en vektor som en liste og konvertere den til et numpy array:
```python
v = [7, 4]
v = np.array(v)
w = np.array([65, 1, -3])
u = np.array([-5, 56, 7, 4])
```

# Udskrive vektoren
Vi kan nu udskrive vektoren:
```python  
print(v)
```
```bash
[7 4]
```
Vi kan udskrive vektorens komponenter:
```python
print(v[0])
print(v[1])
```
```bash
7
4
```

# Længden af en vektor i 2d
Længden af en vektor i 2d kan beregnes ved hjælp af Pythagoras' læresætning:
$$ \|\vec{v}\| = \sqrt{v_1^2 + v_2^2} $$
I Python kan vi beregne længden af en vektor ved hjælp af funktionen `linalg.norm`:
```python
print(np.linalg.norm(v))
```
```bash
8.06225774829855
```

# Længden af en vilkårlig vektor
Længden af en vektor kan beregnes ved hjælp af Pythagoras' læresætning:
$$ \|\vec{v}\| = \sqrt{v_1^2 + v_2^2 + \cdots + v_n^2} $$
I Python kan vi beregne længden af en vektor ved hjælp af funktionen `linalg.norm`:
```python
print(np.linalg.norm(v))
print(np.linalg.norm(w))
print(np.linalg.norm(u))
```
```bash
8.06225774829855
65.007575322837
58.137767414994535
```

# Addition af vektorer
To vektorer kan adderes ved at addere deres komponenter:
$$ \vec{v} + \vec{w} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} + \begin{bmatrix} w_1 \\ w_2 \\ \vdots \\ w_n \end{bmatrix} = \begin{bmatrix} v_1 + w_1 \\ v_2 + w_2 \\ \vdots \\ v_n + w_n \end{bmatrix} $$

I Python kan vi addere to vektorer ved at bruge operatoren `+`:
```python
print(v + w)
```
```bash
[72  5 -3]
```

# Subtraktion af vektorer
To vektorer kan subtraheres ved at subtrahere deres komponenter:
$$ \vec{v} - \vec{w} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} - \begin{bmatrix} w_1 \\ w_2 \\ \vdots \\ w_n \end{bmatrix} = \begin{bmatrix} v_1 - w_1 \\ v_2 - w_2 \\ \vdots \\ v_n - w_n \end{bmatrix} $$
I Python kan vi subtrahere to vektorer ved at bruge operatoren `-`:
```python
print(v - w)
```
```bash
[-58   3   7]
```

# Multiplikation af en vektor med en skalar
En vektor kan multipliceres med en skalar ved at multiplicere alle dens komponenter med skalarværdien:
$$ a \cdot \vec{v} = a \cdot \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} = \begin{bmatrix} a \cdot v_1 \\ a \cdot v_2 \\ \vdots \\ a \cdot v_n \end{bmatrix} $$
I Python kan vi multiplicere en vektor med en skalar ved at bruge operatoren `*`:
```python
print(2 * v)
```
```bash
[14  8]
```

# Multiplikation af to vektorer
To vektorer kan multipliceres ved at multiplicere deres komponenter:
$$ \vec{v} \cdot \vec{w} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} \cdot \begin{bmatrix} w_1 \\ w_2 \\ \vdots \\ w_n \end{bmatrix} = \begin{bmatrix} v_1 \cdot w_1 \\ v_2 \cdot w_2 \\ \vdots \\ v_n \cdot w_n \end{bmatrix} $$
Dette kaldes også for skalarproduktet af $\vec{v}$ og $\vec{w}$.
I Python kan vi multiplicere to vektorer ved at bruge funktionen `multiply`:
```python
print(np.multiply(v, w))
```
```bash
[455   4 -12]
```
# Division af en vektor med en skalar
En vektor kan divideres med en skalar ved at dividere alle dens komponenter med skalarværdien:
$$ \frac{1}{a} \cdot \vec{v} = \frac{1}{a} \cdot \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} = \begin{bmatrix} \frac{1}{a} \cdot v_1 \\ \frac{1}{a} \cdot v_2 \\ \vdots \\ \frac{1}{a} \cdot v_n \end{bmatrix} $$
I Python kan vi dividere en vektor med en skalar ved at bruge operatoren `/`:
```python
print(v / 2)
```
```bash
[3.5 2. ]
```

# Krydsproduktet af to vektorer
Krydsproduktet af to vektorer er en vektor, som står vinkelret på de to vektorer. Krydsproduktet af to vektorer er givet ved:
$$ \vec{v} \times \vec{w} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} \times \begin{bmatrix} w_1 \\ w_2 \\ \vdots \\ w_n \end{bmatrix} = \begin{bmatrix} v_2 \cdot w_3 - v_3 \cdot w_2 \\ v_3 \cdot w_1 - v_1 \cdot w_3 \\ v_1 \cdot w_2 - v_2 \cdot w_1 \end{bmatrix} $$
I Python kan vi beregne krydsproduktet af to vektorer ved at bruge funktionen `cross`:
```python
print(np.cross(v, w))
```
```bash
[  7  228 -261]
```

# Prikproduktet mellem to vektorer
Prikproduktet mellem to vektorer er en skalar, som er givet ved:
$$ \vec{v} \cdot \vec{w} = \begin{bmatrix} v_1 \\ v_2 \\ \vdots \\ v_n \end{bmatrix} \cdot \begin{bmatrix} w_1 \\ w_2 \\ \vdots \\ w_n \end{bmatrix} = v_1 \cdot w_1 + v_2 \cdot w_2 + \cdots + v_n \cdot w_n $$
I Python kan vi beregne prikket mellem to vektorer ved at bruge funktionen `dot`:
```python
print(np.dot(v, w))
```
```bash
455
```

# Tolkning af prikproduktet
Vi kan tolke prikproduktet som længden af den projektion af $\vec{v}$ på $\vec{w}$, som er parallel med $\vec{w}$:
$$ \vec{v} \cdot \vec{w} = \|\vec{v}\| \cdot \|\vec{w}\| \cdot \cos(\theta) $$
hvor $\theta$ er vinklen mellem $\vec{v}$ og $\vec{w}$.
Ved at isolere $\cos(\theta)$ får vi:
$$ \cos(\theta) = \frac{\vec{v} \cdot \vec{w}}{\|\vec{v}\| \cdot \|\vec{w}\|} $$
Hvis $\theta$ er mindre end $90^\circ$, så er $\cos(\theta)$ positiv, og hvis $\theta$ er større end $90^\circ$, så er $\cos(\theta)$ negativ. Hvis $\theta$ er lig med $90^\circ$, så er $\cos(\theta)$ lig med $0$.

# Eksponering af en vektor
Eksponering af en vektor er en vektor, som er givet ved:
$$ \exp(\vec{v}) = \begin{bmatrix} e^{v_1} \\ e^{v_2} \\ \vdots \\ e^{v_n} \end{bmatrix} $$
I Python kan vi beregne eksponeringen af en vektor ved at bruge funktionen `exp`:
```python
print(np.exp(v))
```
```bash
[1096.63315843   54.59815003]
```

# Logaritmen af en vektor
Logaritmen af en vektor er en vektor, som er givet ved:
$$ \log(\vec{v}) = \begin{bmatrix} \log(v_1) \\ \log(v_2) \\ \vdots \\ \log(v_n) \end{bmatrix} $$
I Python kan vi beregne logaritmen af en vektor ved at bruge funktionen `log`:
```python
print(np.log(v))
```
```bash
[1.94591015 1.38629436]
```

# Sinus af en vektor
Sinus af en vektor er en vektor, som er givet ved:
$$ \sin(\vec{v}) = \begin{bmatrix} \sin(v_1) \\ \sin(v_2) \\ \vdots \\ \sin(v_n) \end{bmatrix} $$
I Python kan vi beregne sinus af en vektor ved at bruge funktionen `sin`:
```python
print(np.sin(v))
```
```bash
[0.6569866  -0.7568025 ]
```

# Cosinus af en vektor
Cosinus af en vektor er en vektor, som er givet ved:
$$ \cos(\vec{v}) = \begin{bmatrix} \cos(v_1) \\ \cos(v_2) \\ \vdots \\ \cos(v_n) \end{bmatrix} $$
I Python kan vi beregne cosinus af en vektor ved at bruge funktionen `cos`:
```python
print(np.cos(v))
```
```bash
[ 0.75390225 -0.65364362]
```

# Tangens af en vektor
Tangens af en vektor er en vektor, som er givet ved:
$$ \tan(\vec{v}) = \begin{bmatrix} \tan(v_1) \\ \tan(v_2) \\ \vdots \\ \tan(v_n) \end{bmatrix} $$
I Python kan vi beregne tangens af en vektor ved at bruge funktionen `tan`:
```python
print(np.tan(v))
```
```bash
[ 0.87144798 -1.15782128]
```

# Indexing af vektorer i numpy
Vi kan indexere vektorer på samme måde som vi indexere lister i Python:
```python
print(v[0])
print(v[1])
```
```bash
7
4
```

# Slicing af vektorer i numpy
Vi kan slice vektorer på samme måde som vi slicer lister i Python ved brug af `:`. Herunder en generel formel for slicing af vektorer:
```python
print(v[start:stop:step])
```
- start: startindeks
- stop: stopindeks
- step: skridt

# Eksempel på slicing af vektorer
Givet vektoren:
```python
v = np.array([7, 4, 2, 6, 8, 9, 1, 3, 5])
```
Så kan vi slice vektoren på følgende måde:
```python
print(v[0:3]) # [7 4 2]
print(v[3:6]) #  [6 8 9]
print(v[6:9]) # [1 3 5]
print(v[0:9:3]) # [7 6 1]

```
# : i slicing af vektorer
Hvis vi udelader startindeks, så sættes startindeks til 0:
```python
print(v[:3]) # [7 4 2]
```
Hvis vi udelader stopindeks, så sættes stopindeks til længden af vektoren:
```python
print(v[3:]) # [6 8 9 1 3 5]
```
Hvis vi udelader skridt, så sættes skridt til 1:
```python
print(v[0:9:1]) # [7 4 2 6 8 9 1 3 5]
print(v[0:9]) # [7 4 2 6 8 9 1 3 5]
```
# Broadcasting i numpy
Numpy understøtter broadcasting, som betyder at vi kan udføre operationer på vektorer med forskellige længder. Hvis vi eksempelvis vil lægge en vektor til en skalar, så vil numpy automatisk kopiere vektoren, så den får samme længde som skalarværdien:
```python
print(v + 2) # [ 9  6  4  8 10 11  3  5  7]
```
Hvis vi vil lægge to vektorer sammen, så skal de have samme længde:
```python
print(v + np.array([1, 2, 3, 4, 5, 6, 7, 8, 9])) # [ 8  6  5 10 13 15  8 11 14]
```




# Definition af en matrix
En matrix er en samling af tal, som er ordnet i rækker og kolonner. En matrix med m rækker og n kolonner kan repræsenteres som en m x n matrix.
$$ \vec{v} = \begin{bmatrix} v_1 & v_2 & \cdots & v_n \end{bmatrix} $$

