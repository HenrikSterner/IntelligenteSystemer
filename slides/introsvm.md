# Supporting vector machines

## Af Henrik Sterner (hst@nextkbh.dk)

## Introduktion
I det følgende vil vi se på en af de mest anvendte algoritmer indenfor maskinlæring, nemlig **supporting vector machines** (SVM). SVM er en algoritme, som kan bruges til både klassifikation og regression. Men typisk bedst til klassifikation. 

SVM er en **supervised learning** algoritme, hvilket betyder, at den skal bruge et datasæt, hvor der er en række eksempler på, hvordan data ser ud, og hvordan det skal klassificeres.

## Ikke-probalistisk klassifikation
SVM er en **non-probabilistic** algoritme, hvilket betyder, at den ikke giver en sandsynlighed for, at et givent datapunkt hører til en given klasse. Den giver i stedet en binær klassifikation, dvs. den siger, om et givent datapunkt hører til en given klasse eller ej.

Mere konkret vil SVM finde en **decision boundary** mellem to klasser, som er den linje, som ligger lige midt imellem de to klasser. Hvis et datapunkt ligger på den ene side af denne linje, vil det blive klassificeret som tilhørende den ene klasse, og hvis det ligger på den anden side, vil det blive klassificeret som tilhørende den anden klasse.

## Hvad med i forhold til regression?
I forhold til regression vil SVM finde en linje, som passer bedst muligt til datapunkterne. Denne linje vil blive brugt til at forudsige, hvad et givent datapunkt vil have som værdi.

## Et simpelt eksempel
Lad os se på et simpelt eksempel. Vi har et datasæt med to features, $x_1$ og $x_2$, og vi vil gerne klassificere datapunkterne i to klasser, $y=0$ og $y=1$. Vi har følgende datasæt genereret med python:

```python
import numpy as np
import matplotlib.pyplot as plt

# Generate data
np.random.seed(1)
x1 = np.random.normal(0, 1, 100)
x2 = np.random.normal(0, 1, 100)
y = np.zeros(100)
y[(x1 > 0) & (x2 > 0)] = 1
y[(x1 < 0) & (x2 < 0)] = 0
```

Vi kan se, at der er to klart adskilte klasser, som er adskilt af en linje, som går igennem origo. Vi kan se, at alle datapunkter, som ligger i øverste højre kvadrant, er klassificeret som $y=1$, og alle datapunkter, som ligger i nederste venstre kvadrant, er klassificeret som $y=0$.

```python
# Plot data
plt.scatter(x1, x2, c=y)
plt.show()
```

Vi kan nu afprøve SVM på dette datasæt. Vi bruger scikit-learn til at lave en SVM model, og vi bruger en **linear kernel**. Vi bruger en linear kernel, fordi vi kan se, at vores data er lineært separabelt, dvs. at vi kan adskille de to klasser med en linje.

```python
from sklearn.svm import SVC

# Fit SVM model
model = SVC(kernel='linear')
model.fit(np.vstack((x1, x2)).T, y)
```



