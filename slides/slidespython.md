# Introduktion til Grundlæggende Python

- Python: Et populært og læsbar programmeringssprog
- Bruges bredt indenfor udvikling, automatisering og dataanalyse
- Udo

# Hvad er Python?

- Python er et programmeringssprog
- Python er et højniveausprog
- Python er et objektorienteret sprog
- Python er et dynamisk typet sprog
- Python er et open source sprog
- Python er et sprog med mange biblioteker
  
# Datascience biblioteker med Python
Vi vender tilbage til disse biblioteker senere i kurset:
- Numpy: Matematik og videnskabelige beregninger
- Pandas: Dataanalyse og datahåndtering
- Matplotlib: Visualisering af data
- Scikit-learn: Maskinlæring
- TensorFlow: Maskinlæring og deep learning
- PyTorch: Maskinlæring og deep learning

# Overblik over hvad vi skal igennem
- Introduktion til variabler i Python
- Datatyper i Python
- Brugerinput i Python
- Strengformatering i Python
- Betinget udførelse af kode i Python
- Løkker i Python
- Funktioner i Python
- Objektorienteret programmering i Python
- Fejlhåndtering i Python
- Filhåndtering i Python


# Introduktion til variabler og datatyper i Python

- Variabler gemmer værdier til brug i programmet
- Navngivne lagerpladser til forskellige typer af data
- Python bruger dynamisk typetildeling
- Variabler behøver ikke erklæres med en bestemt type
- Data i variabler kan ændres undervejs i programmet


## Variabelnavne
```python
navn = "Alice"
alder = 30
point_1 = 95.5
er_student = True
```

## Navngivningsregler for variabler

- Variabelnavne kan indeholde bogstaver, tal og understregning
- Variabelnavne må ikke starte med et tal
- Variabelnavne må ikke indeholde mellemrum
- Variabelnavne må ikke indeholde specialtegn
- Variabelnavne må ikke være Python nøgleord
- Variabelnavne bør være sigende
- Variabelnavne kan være på engelsk


## Datatyper i Python
```python
tekst = "Hej verden"
heltal = 42
decimaltal = 3.14
sandt_eller_falsk = True
```

## Streng (Tekst)
```python
besked = "Velkommen til Python"
underbesked = besked[8:12]
længde = len(besked)
```

## Heltal
```python
alder = 25
højde = -160
antal_børn = 3
```

## Sandt eller Falsk (Boolean)
```python
er_solopgang = True
er_nedbør = False
```

## Listetyper
```python
farver = ["rød", "grøn", "blå"]
tal = [1, 2, 3, 4, 5]
blandet = ["æble", 3, True]
```

## Tupletyper
```python
koordinater = (3, 7)
datarække = (1, "tekst", True)
```

# Dictionarietyper
```python
person = {
    "navn": "Alice",
    "alder": 30,
    "er_student": True
}
navn = person["navn"]
```

# Variabelskift
```python
a = 5
b = 7
a, b = b, a
print("a:", a)  # Resultat: 7
print("b:", b)  # Resultat: 5
```

# Global og Lokal Variabel
```python
global_var = 10
def funktion():
    lokal_var = 5
    print(global_var)
    print(lokal_var)
```

# Typekonvertering
```python
alder = 25
alder_tekst = str(alder)
pris = "9.99"
pris_decimal = float(pris)
```

# Indbyggede Funktioner til Typer
```python
længde = len("Hej verden")
maksimum = max([4, 7, 2, 9])
minimum = min([4, 7, 2, 9])
```

# Variabler som Referencer
```python
liste_a = [1, 2, 3]
liste_b = liste_a
liste_a.append(4)
print(liste_b)  # Resultat: [1, 2, 3, 4]
```

# Identitet og Lighed
```python	
a = [1, 2, 3]
b = [1, 2, 3]
print(a is b)  # Resultat: False
print(a == b)  # Resultat: True
```

# Typekontrol med isinstance()
```python
x = 5
if isinstance(x, int):
    print("x er et heltal")
else:
    print("x er ikke et heltal")
``` 

``` lav 10 slides om brugerinput i python ``

# Brugerinput
```python
navn = input("Hvad hedder du? ")
alder = int(input("Hvor gammel er du? "))
```

# Brugerinput med Fejlhåndtering
```python 
while True:
    try:
        alder = int(input("Hvor gammel er du? "))
        break
    except ValueError:
        print("Indtast venligst et heltal")
```

# Strengformatering
```python
navn = "Alice"
alder = 30
print("Hej, jeg hedder " + navn + " og er " + str(alder) + " år gammel")
print("Hej, jeg hedder %s og er %d år gammel" % (navn, alder))
print("Hej, jeg hedder {} og er {} år gammel".format(navn, alder))
print(f"Hej, jeg hedder {navn} og er {alder} år gammel")
```

# Metoder på strenge
```python
besked = "Hej verden"
print(besked.upper())  # Resultat: HEJ VERDEN
print(besked.lower())  # Resultat: hej verden
print(besked.capitalize())  # Resultat: Hej verden
print(besked.replace("Hej", "Hello"))  # Resultat: Hello verden
```

# Flere metoder på strenge
```python
besked = "Hej verden"
print(besked.startswith("Hej"))  # Resultat: True
print(besked.endswith("Hej"))  # Resultat: False
print(besked.find("verden"))  # Resultat: 4
print(besked.find("ikke"))  # Resultat: -1
```
# Brugen af split og join
```python
besked = "Hej verden"
ord = besked.split(" ")
print(ord)  # Resultat: ["Hej", "verden"]
ny_besked = " ".join(ord)
print(ny_besked)  # Resultat: Hej verden
```

# Brugen af strip
```python
besked = "   Hej verden   "
print(besked.strip())  # Resultat: Hej verden
```

# Brugen af format
```python
navn = "Alice"
alder = 30
print("Hej, jeg hedder {} og er {} år gammel".format(navn, alder))
print("Hej, jeg hedder {0} og er {1} år gammel".format(navn, alder))
print("Hej, jeg hedder {navn} og er {alder} år gammel".format(navn=navn, alder=alder))
print(f"Hej, jeg hedder {navn} og er {alder} år gammel")
```

# Brugen af format med tal

```python
tal = 3.14159265359
print("{:.2f}".format(tal))  # Resultat: 3.14
print("{:.4f}".format(tal))  # Resultat: 3.1416
print("{:e}".format(tal))  # Resultat: 3.141593e+00
print("{:d}".format(42))  # Resultat: 42
print("{:b}".format(42))  # Resultat: 101010
print("{:x}".format(42))  # Resultat: 2a
```

# Betinget udførelse af kode
```python
if alder >= 18:
    print("Du er myndig")
else:
    print("Du er ikke myndig")
```

# Betinget udførelse af kode med elif
```python
if alder < 0:
    print("Ugyldig alder")
elif alder < 18:
    print("Du er ikke myndig")
else:
    print("Du er myndig")
```

# Betinget udførelse af kode med flere betingelser
```python
if alder < 0:
    print("Ugyldig alder")
elif alder < 18:
    print("Du er ikke myndig")
elif alder < 67:
    print("Du er i arbejde")
else:
    print("Du er på pension")
```

# Betinget udførsel med flere instruktioner

```python
if alder < 0:
    print("Ugyldig alder")
elif alder < 18:
    print("Du er ikke myndig")
    print("Du må ikke købe alkohol")
elif alder < 67:
    print("Du er i arbejde")
    print("Du må gerne købe alkohol")
else:
    print("Du er på pension")
    print("Du må gerne købe alkohol")
```

# Intro til løkker

- Løkker bruges til at gentage kode
- Løkker bruges til at udføre kode et bestemt antal gange
- Løkker bruges til at udføre kode indtil en betingelse er opfyldt
- Løkker bruges til at udføre kode på hvert element i en liste
- Løkker bruges til at udføre kode på hvert bogstav i en streng
- Løkker bruges til at udføre kode på hvert bogstav i en fil
- Mange andre ting

# While-løkker
```python
i = 0
while i < 10:
    print(i)
    i += 1
```

# For-løkker
```python
for i in range(10):
    print(i)
```

# For-løkker med liste
```python
farver = ["rød", "grøn", "blå"]
for farve in farver:
    print(farve)
```

# For-løkker med streng
```python
besked = "Hej verden"
for bogstav in besked:
    print(bogstav)
```
# Løkker indeni løkker
```python
for i in range(3):
    for j in range(3):
        print(i, j)
```

# While løkker indeni while løkker
```python
i = 0
while i < 3:
    j = 0
    while j < 3:
        print(i, j)
        j += 1
    i += 1
```

# While løkker indeni for løkker
```python
for i in range(3):
    j = 0
    while j < 3:
        print(i, j)
        j += 1
```

# For løkker indeni while løkker
```python
i = 0
while i < 3:
    for j in range(3):
        print(i, j)
    i += 1
```

# Listecomprehension med for løkker
```python
liste = [i for i in range(10)]
print(liste)  # Resultat: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
```

# Listecomprehension med for løkker og betingelse
```python
liste = [i for i in range(10) if i % 2 == 0]
print(liste)  # Resultat: [0, 2, 4, 6, 8]
```

# Listecomprehension med for løkker og flere løkker
```python
liste = [(i, j) for i in range(3) for j in range(3)]
print(liste)  # Resultat: [(0, 0), (0, 1), (0, 2), (1, 0), (1, 1), (1, 2), (2, 0), (2, 1), (2, 2)]
```

# Listecomprehension med for løkker og flere løkker og betingelse
```python
liste = [(i, j) for i in range(3) for j in range(3) if i != j]
print(liste)  # Resultat: [(0, 1), (0, 2), (1, 0), (1, 2), (2, 0), (2, 1)]
```

#















