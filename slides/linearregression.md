# Introduktion til Lineær Regression i Python
## Af Henrik Sterner (henrik.sterner@gmail.com)

Lineær regression er en metode til at finde en lineær funktion, der passer til et datasæt. Den lineære funktion kan bruges til at forudsige værdier for nye data.

# Et eksempel på lineær regression: Verdensrekord i 100 meter løb
Herunder er vist tiderne for de 100 meter løb, der er blevet sat i OL siden 1896, indlæst i python. Tiderne er i sekunder.
    
    ```python
    import numpy as np
    import matplotlib.pyplot as plt

    years = np.array([1896, 1900, 1904, 1908, 1912, 1920, 1924, 1928, 1932, 1936, 1948, 1952, 1956, 1960, 1964, 1968, 1972, 1976, 1980, 1984, 1988, 1992, 1996, 2000, 2004, 2008, 2012, 2016])

    times = np.array([12.0, 11.0, 11.0, 10.8, 10.8, 10.8, 10.6, 10.8, 10.3, 10.3, 10.3, 10.4, 10.5, 10.2, 10.0, 9.95, 10.14, 10.06, 10.25, 9.99, 9.92, 9.96, 9.84, 9.87, 9.85, 9.69, 9.63, 9.81, 9.58])
    ```

# Et eksempel på lineær regression: Hvad er verdensrekorden i 100 meter løb i 2100?
Vi kan bruge lineær regression til at forudsige, hvad verdensrekorden i 100 meter løb vil være i 2100. Vi kan gøre det ved at finde en lineær funktion, der passer til datasættet, og så bruge den til at forudsige tiden for 2100.
Herunder viser vi det i python og ved brug af `LinearRegression`-klassen fra `sklearn.linear_model`-modulet.:
    
        ```python
        from sklearn.linear_model import LinearRegression
    
        model = LinearRegression()
        model.fit(years.reshape(-1, 1), times)
    
        print(model.predict([[2100]]))
        ```
    
        ```
        [9.52636364]
        ```
`reshape(-1, 1)`  ændrer formen på `years` fra en vektor til en matrix med én kolonne. Det er nødvendigt, fordi `LinearRegression`-klassen forventer, at `years` er en matrix med én kolonne.

# Et eksempel på lineær regression: Hvad er verdensrekorden i 100 meter løb i 2200 og 2300?
Herunder viser vi det i python og ved brug af `LinearRegression`-klassen fra `sklearn.linear_model`-modulet.:
    
        ```python
        from sklearn.linear_model import LinearRegression
    
        model = LinearRegression()
        model.fit(years.reshape(-1, 1), times)
    
        print(model.predict([[2200], [2300]]))
        ```
    
        ```
        [8.38636364 7.24636364]
        ```
Hvad er problemet med at bruge lineær regression til at forudsige verdensrekorden i 100 meter løb i 2200 og 2300?

# Matematikken bag lineær regression i to variable
Lad os antage, at vi har et datasæt med $n$ datapunkter. Hvert datapunkt har en $x$-værdi og en $y$-værdi. Vi kan repræsentere datasættet som en liste af $n$ par $(x_i, y_i)$, hvor $x_i$ er $x$-værdien for det $i$'te datapunkt, og $y_i$ er $y$-værdien for det $i$'te datapunkt.
Da handler lineær regression om at finde en lineær funktion $f(x) = ax + b$, der passer til datasættet. Funktionen $f(x)$ kaldes en lineær model. Lineær regression handler om at finde værdierne af $a$ og $b$, der gør, at lineær modellen passer bedst muligt til datasættet.

# Matematikken bag lineær regression i to variable: Hvordan måler vi, hvor godt en lineær model passer til et datasæt?
Vi kan måle, hvor godt en lineær model passer til et datasæt, ved at måle, hvor langt datapunkterne er fra modellen. Hvis datapunkterne er langt fra modellen, passer modellen ikke godt til datasættet. Hvis datapunkterne er tæt på modellen, passer modellen godt til datasættet.

Denne metode kaldes mindste kvadraters metode. 

# Mindste kvadraters metode
Mindste kvadraters metode går ud på at finde den lineære model, der gør, at summen af kvadraterne på afstandene fra datapunkterne til modellen er mindst mulig. Dvs. minimere:

$$\sum_{i=1}^n (y_i - f(x_i))^2$$

Erstattes $f(x_i)$ med $ax_i + b$, får vi:

$$\sum_{i=1}^n (y_i - (ax_i + b))^2$$

Hvordan finder vi $a$ og $b$, der gør, at summen af kvadraterne på afstandene fra datapunkterne til modellen er mindst mulig?

# Lad os finde $a$ og $b$ ved at differentiere
- Vi differentierer summen af kvadraterne på afstandene fra datapunkterne til modellen med hensyn til $a$ og $b$.
- Vi sætter de afledte lig med 0.
- Vi løser de to ligninger med hensyn til $a$ og $b$.
- Vi får en formel for $a$ og en formel for $b$.
- Vi indsætter $a$ og $b$ i modellen $f(x) = ax + b$.
- Vi har nu en lineær model, der passer til datasættet.

# Formler for $a$ og $b$
Differentier summen af kvadraterne på afstandene fra datapunkterne til modellen med hensyn til $a$ og $b$:

$$\frac{\partial}{\partial a} \sum_{i=1}^n (y_i - (ax_i + b))^2 = 0$$

Hvilket giver:
$$\sum_{i=1}^n 2(y_i - (ax_i + b))(-x_i) = 0$$
Her har vi brugt kædereglen:
$$\frac{\partial}{\partial a} (y_i - (ax_i + b))^2 = 2(y_i - (ax_i + b))\frac{\partial}{\partial a} (y_i - (ax_i + b))$$

