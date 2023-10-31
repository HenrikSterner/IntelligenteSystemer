# Introduktion til polynomiel regression i Python og numpy

## Af Henrik Sterner (henrik.sterner@gmail.com)

Polynomiel regression er en udvidelse af lineær regression, hvor den afhængige variabel er en funktion af en polynomiel funktion af den uafhængige variabel. 

I det følgende introduceres polynomiel regression og hvordan det kan implementeres i Python ved brug af numpy.

# Indhold

- Hvad er et polynomium?
- Graden af et polynomium
- Polynomiel regression
- Eksempel på polynomiel regression
- Beregning af polynomiel regression i Python ved brug af numpy
- Visualisering af polynomiel regression i Python ved brug af matplotlib
- Eksempel på polynomiel regression med flere variable
- Beregning af polynomiel regression med flere variable i Python ved brug af numpy

# Hvad er et polynomium?

Et polynomium er en funktion, der er givet ved en sum af potenser af en variabel, hvor koefficienterne er reelle tal. Her nogle eksempler:

$$f(x) = 3x^2 + 2x + 1$$

$$g(x) = 5x^3 + 4x^2 + 3x + 2$$

$$h(x) = 7x^4 + 6x^3 + 5x^2 + 4x + 3$$

# Matematisk notation

Ved et polynomium af grad $n$ forstås en funktion $f(x)$, der er givet ved:

$$f(x) = a_n x^n + a_{n-1} x^{n-1} + \ldots + a_2 x^2 + a_1 x + a_0$$

hvor $a_n, a_{n-1}, \ldots, a_2, a_1, a_0$ er reelle tal og $a_n \neq 0$.

# Graden af et polynomium

Ved graden af et polynomium forstås den højeste potens af variablen i polynomiet. 

Eksempelvis er graden af polynomiet $f(x) = 3x^2 + 2x + 1$ lig 2, da den højeste potens af variablen $x$ er 2.

# Polynomiel regression

Polynomiel regression er en udvidelse af lineær regression, hvor den afhængige variabel er en funktion af en polynomiel funktion af den uafhængige variabel.

Fordelene ved polynomiel regression er, at den kan tilpasses til en bred vifte af funktioner, og at den kan tilpasses til data, der ikke er lineært fordelt.

# Eksempel på polynomiel regression
Betragt følgende datasæt:

| x | y |
|---|---|
| 1 | 1 |
| 2 | 4 |
| 3 | 9 |
| 4 | 16 |
| 5 | 25 |
| 6 | 36 |

# Eksempel på polynomiel regression i numpy

Først importeres numpy:

```python
import numpy as np
```

Dernæst defineres datasættet:

```python
x = np.array([1, 2, 3, 4, 5, 6])
y = np.array([1, 4, 9, 16, 25, 36])
```

# Eksempel på polynomiel regression i numpy

Herefter beregnes polynomiel regression:

```python
p = np.polyfit(x, y, 2)
```

Her er $p$ en vektor med koefficienterne i polynomiet.

```python
p = [ 1.00000000e+00 -1.59471172e-14  1.00000000e+00]
```
Det vil sige, at polynomiet er givet ved:

$$f(x) = 1.00000000e+00 x^2 -1.59471172e-14 x + 1.00000000e+00$$

Her betyder e+00, at der skal flyttes 0 decimaler til højre, og e-14 betyder, at der skal flyttes 14 decimaler til venstre. Dvs. tilnærmet:

$$f(x) = x^2 + 1$$

# Visualisering af polynomiel regression i Python ved brug af matplotlib

Først importeres matplotlib:

```python
x = np.array([1, 2, 3, 4, 5, 6])
y = np.array([1, 4, 9, 16, 25, 36])
p = np.polyfit(x, y, 2)
plt.scatter(x, y)
plt.plot(x, np.polyval(p, x))
plt.show()
``` 












