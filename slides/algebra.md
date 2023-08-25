

# Introduktion til Lineær algreba til maskinelæring
## Af Henrik Sterner (hst@nextkbh.dk)
I det følgende vil vi gennemgå de grundlæggende begreber indenfor lineær algebra, som er nødvendige for at forstå maskinelæring. Vi vil gennemgå de grundlæggende begreber og operationer på vektorer, matricer og tensorer. Vi vil også gennemgå de grundlæggende operationer på matricer, som er nødvendige for at forstå maskinelæring. 

# Vektorer
En vektor er en liste af tal. Vi kan repræsentere en vektor som en liste af tal, som vist i eksemplet nedenfor. Herunder eksempel på tre vektorer, som vi kalder $x$, $y$ og $z$:

$$x = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}, y = \begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix}, z = \begin{bmatrix} 7 \\ 8 \\ 9 \end{bmatrix}$$

Vi kan også repræsentere en vektor som en liste af tal, som vist i eksemplet nedenfor. Herunder eksempel på tre vektorer, som vi kalder $x$, $y$ og $z$:

$$x = \begin{bmatrix} 1 & 2 & 3 \end{bmatrix}, y = \begin{bmatrix} 4 & 5 & 6 \end{bmatrix}, z = \begin{bmatrix} 7 & 8 & 9 \end{bmatrix}$$

# Matematisk definition af vektorer i n-dimensioner
Lad $x$ være en vektor i $n$-dimensioner. Vi kan repræsentere $x$ som en liste af $n$ tal: 
$$x = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix}$$
Her er $x_i$ er det $i$'te element i vektoren $x$. 
Denne notation kaldes kolonnenotation. 

Vi kan også repræsentere $x$ som en liste af $n$ tal:
$$x = \begin{bmatrix} x_1 & x_2 & \cdots & x_n \end{bmatrix}$$
Denne notation kaldes rækkenotation.

# Vigtige operationer på vektorer
Vi kan udføre en række operationer på vektorer. De vigtigste operationer er:
- Addition af vektorer
- Subtraktion af vektorer
- Multiplikation af en vektor med en skalar
- Beregning af prikprodukt
- Beregning af krydsprodukt
- Beregning af vektorlængde
- Beregning af vinkel mellem to vektorer

# Addition af vektorer
Vi kan addere to vektorer ved at addere de tilsvarende elementer i vektorerne. Den generelle notation er: 
$$x + y = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} + \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix} = \begin{bmatrix} x_1 + y_1 \\ x_2 + y_2 \\ \vdots \\ x_n + y_n \end{bmatrix}$$

Eksempelvis er summen af vektorerne $x$ og $y$ givet ved:
$$x + y = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} + \begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix} = \begin{bmatrix} 1 + 4 \\ 2 + 5 \\ 3 + 6 \end{bmatrix} = \begin{bmatrix} 5 \\ 7 \\ 9 \end{bmatrix}$$

# Subtraktion af vektorer
Vi kan subtrahere to vektorer ved at subtrahere de tilsvarende elementer i vektorerne. Den generelle notation er:
$$x - y = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} - \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix} = \begin{bmatrix} x_1 - y_1 \\ x_2 - y_2 \\ \vdots \\ x_n - y_n \end{bmatrix}$$

Eksempelvis er differencen mellem vektorerne $x$ og $y$ givet ved:
$$x - y = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} - \begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix} = \begin{bmatrix} 1 - 4 \\ 2 - 5 \\ 3 - 6 \end{bmatrix} = \begin{bmatrix} -3 \\ -3 \\ -3 \end{bmatrix}$$

# Multiplikation af en vektor med en skalar
Vi kan multiplicere en vektor med en skalar ved at multiplicere hvert element i vektoren med skalarværdien. Den generelle notation er:

$$\alpha x = \alpha \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} = \begin{bmatrix} \alpha x_1 \\ \alpha x_2 \\ \vdots \\ \alpha x_n \end{bmatrix}$$

Eksempelvis er produktet af vektoren $x$ og skalarværdien $\alpha$ givet ved:

$$\alpha x = 2 \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} = \begin{bmatrix} 2 \cdot 1 \\ 2 \cdot 2 \\ 2 \cdot 3 \end{bmatrix} = \begin{bmatrix} 2 \\ 4 \\ 6 \end{bmatrix}$$

# Prikprodukt
Vi kan beregne prikproduktet af to vektorer ved at multiplicere de tilsvarende elementer i vektorerne og derefter summe disse produkter. Den generelle notation er:

$$x \cdot y = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} \cdot \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix} = x_1 y_1 + x_2 y_2 + \cdots + x_n y_n$$

Eksempelvis er prikproduktet af vektorerne $x$ og $y$ givet ved:

$$x \cdot y = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} \cdot \begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix} = 1 \cdot 4 + 2 \cdot 5 + 3 \cdot 6 = 4 + 10 + 18 = 32$$

# Længden af en vektor
Vi kan beregne længden af en vektor ved at kvadrere hvert element i vektoren, summe disse kvadrater og derefter tage kvadratroden af summen. Den generelle notation er:

$$\| x \| = \sqrt{x_1^2 + x_2^2 + \cdots + x_n^2}$$

Eksempelvis er længden af vektoren $x$ givet ved:

$$\| x \| = \sqrt{1^2 + 2^2 + 3^2} = \sqrt{1 + 4 + 9} = \sqrt{14}$$

# Vinkel mellem to vektorer
Vi kan beregne vinklen mellem to vektorer ved at beregne prikproduktet af de to vektorer og derefter dividere med produktet af længden af de to vektorer. Den generelle notation er:

$$\cos \theta = \frac{x \cdot y}{\| x \| \| y \|}$$

Eksempelvis er vinklen mellem vektorerne $x$ og $y$ givet ved:

$$\cos \theta = \frac{x \cdot y}{\| x \| \| y \|} = \frac{32}{\sqrt{14} \sqrt{77}} = \frac{32}{\sqrt{1078}}$$


# Lineært uafhængige vektorer
To vektorer $x$ og $y$ er lineært uafhængige, hvis ingen af vektorerne kan skrives som en linearkombination af den anden vektor. Dvs. at der ikke findes en skalarværdi $\alpha$, således at:
$$x = \alpha y \quad \text{eller} \quad y = \alpha x$$
hvor $\alpha$ er en skalarværdi.

# Krydsprodukt af to vektorer
Vi kan beregne krydsproduktet af to lineært uafhænige vektorer i n-dimensioner på følgende måde:

$$x \times y = \begin{bmatrix} x_1 \\ x_2 \\ \vdots \\ x_n \end{bmatrix} \times \begin{bmatrix} y_1 \\ y_2 \\ \vdots \\ y_n \end{bmatrix} = \begin{bmatrix} x_2 y_3 - x_3 y_2 \\ x_3 y_1 - x_1 y_3 \\ \vdots \\ x_{n-1} y_n - x_n y_{n-1} \\ x_n y_1 - x_1 y_n \end{bmatrix}$$

Krydsproduktet giver en vektor, som står vinkelret på de to vektorer, som indgår i krydsproduktet.

Eksempelvis er krydsproduktet af vektorerne $x$ og $y$ givet ved:

$$x \times y = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix} \times \begin{bmatrix} 4 \\ 5 \\ 6 \end{bmatrix} = \begin{bmatrix} 2 \cdot 6 - 3 \cdot 5 \\ 3 \cdot 4 - 1 \cdot 6 \\ 1 \cdot 5 - 2 \cdot 4 \end{bmatrix} = \begin{bmatrix} -3 \\ 6 \\ -3 \end{bmatrix}$$

# Matricer
En matrix er en tabel af tal. Vi kan repræsentere en matrix som en tabel af tal, som vist i eksemplet nedenfor. En n x m matrix er en matrix med n rækker og m kolonner:

$$X=\begin{bmatrix} x_{11} & x_{12} & \cdots & x_{1m} \\ x_{21} & x_{22} & \cdots & x_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} & x_{n2} & \cdots & x_{nm} \end{bmatrix}$$

her er $x_{ij}$ det element, som står i $i$'te række og $j$'te kolonne i matricen $X$.

# Eksempler på matricer
Givet vores to vektorer $x$ og $y$ kan vi repræsentere dem som en matrix:

$$X=\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$$
Her er n=2 og m=3.

Givet vores tre vektorer $x$, $y$ og $z$ kan vi repræsentere dem som en matrix:

$$X=\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}$$
Her er n=3 og m=3.

# Operationer på matricer
Vi kan udføre en række operationer på matricer. De vigtigste operationer er:
* Addition af matricer 
* Subtraktion af matricer
* Multiplikation af en matrix med en skalar
* Multiplikation af to matricer
* Transponering af en matrix
* Beregning af determinant
* Beregning af invers matrix

# Addition af matricer
Vi kan addere to matricer ved at addere de tilsvarende elementer i matricerne. Lad $X$ være en n x m matrix og $Y$ være en n x m matrix. Den generelle notation er:

$$X + Y = \begin{bmatrix} x_{11} & x_{12} & \cdots & x_{1m} \\ x_{21} & x_{22} & \cdots & x_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} & x_{n2} & \cdots & x_{nm} \end{bmatrix} + \begin{bmatrix} y_{11} & y_{12} & \cdots & y_{1m} \\ y_{21} & y_{22} & \cdots & y_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ y_{n1} & y_{n2} & \cdots & y_{nm} \end{bmatrix}$$
$$= \begin{bmatrix} x_{11} + y_{11} & x_{12} + y_{12} & \cdots & x_{1m} + y_{1m} \\ x_{21} + y_{21} & x_{22} + y_{22} & \cdots & x_{2m} + y_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} + y_{n1} & x_{n2} + y_{n2} & \cdots & x_{nm} + y_{nm} \end{bmatrix}$$

# Eksempel på addition af matricer
Givet matricerne $X$ og $Y$:

$$X=\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}, Y=\begin{bmatrix} 7 & 8 & 9 \\ 10 & 11 & 12 \end{bmatrix}$$

kan vi beregne summen af matricerne $X$ og $Y$:

$$X + Y = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix} + \begin{bmatrix} 7 & 8 & 9 \\ 10 & 11 & 12 \end{bmatrix} = \begin{bmatrix} 1 + 7 & 2 + 8 & 3 + 9 \\ 4 + 10 & 5 + 11 & 6 + 12 \end{bmatrix}$$
$$ = \begin{bmatrix} 8 & 10 & 12 \\ 14 & 16 & 18 \end{bmatrix}$$

# Subtraktion af matricer
Vi kan subtrahere to matricer ved at subtrahere de tilsvarende elementer i matricerne. Lad $X$ være en n x m matrix og $Y$ være en n x m matrix. Den generelle notation er:

$$X - Y = \begin{bmatrix} x_{11} & x_{12} & \cdots & x_{1m} \\ x_{21} & x_{22} & \cdots & x_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} & x_{n2} & \cdots & x_{nm} \end{bmatrix} - \begin{bmatrix} y_{11} & y_{12} & \cdots & y_{1m} \\ y_{21} & y_{22} & \cdots & y_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ y_{n1} & y_{n2} & \cdots & y_{nm} \end{bmatrix}$$
$$= \begin{bmatrix} x_{11} - y_{11} & x_{12} - y_{12} & \cdots & x_{1m} - y_{1m} \\ x_{21} - y_{21} & x_{22} - y_{22} & \cdots & x_{2m} - y_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} - y_{n1} & x_{n2} - y_{n2} & \cdots & x_{nm} - y_{nm} \end{bmatrix}$$

# Eksempel på subtraktion af to matricer
Givet matricerne $X$ og $Y$:

$$X=\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}, Y=\begin{bmatrix} 7 & 8 & 9 \\ 10 & 11 & 12 \end{bmatrix}$$

kan vi beregne differencen mellem matricerne $X$ og $Y$:

$$X - Y = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix} - \begin{bmatrix} 7 & 8 & 9 \\ 10 & 11 & 12 \end{bmatrix} = \begin{bmatrix} 1 - 7 & 2 - 8 & 3 - 9 \\ 4 - 10 & 5 - 11 & 6 - 12 \end{bmatrix}$$
$$ = \begin{bmatrix} -6 & -6 & -6 \\ -6 & -6 & -6 \end{bmatrix}$$

# Multiplikation af en matrix med en skalar
Vi kan multiplicere en matrix med en skalar ved at multiplicere hvert element i matricen med skalarværdien. Lad $X$ være en n x m matrix og $\alpha$ være en skalarværdi. Den generelle notation er:

$$\alpha X = \alpha \begin{bmatrix} x_{11} & x_{12} & \cdots & x_{1m} \\ x_{21} & x_{22} & \cdots & x_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} & x_{n2} & \cdots & x_{nm} \end{bmatrix} = \begin{bmatrix} \alpha x_{11} & \alpha x_{12} & \cdots & \alpha x_{1m} \\ \alpha x_{21} & \alpha x_{22} & \cdots & \alpha x_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ \alpha x_{n1} & \alpha x_{n2} & \cdots & \alpha x_{nm} \end{bmatrix}$$

# Eksempel på multiplikation af en matrix med en skalar 
Givet matricen $X$:

$$X=\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$$

kan vi beregne produktet af matricen $X$ og skalarværdien $\alpha=8$:

$$\alpha X = 8 \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix} = \begin{bmatrix} 8 \cdot 1 & 8 \cdot 2 & 8 \cdot 3 \\ 8 \cdot 4 & 8 \cdot 5 & 8 \cdot 6 \end{bmatrix} = \begin{bmatrix} 8 & 16 & 24 \\ 32 & 40 & 48 \end{bmatrix}$$

# Identitetsmatricen
Identitetsmatricen er en kvadratisk matrix, hvor alle elementer på diagonalen er lig med 1 og alle andre elementer er lig med 0. Identitetsmatricen er en kvadratisk matrix, som har den egenskab, at produktet af en matrix og identitetsmatricen er lig med den oprindelige matrix. Lad $X$ være en n x n matrix. Den generelle notation er:

$$I = \begin{bmatrix} 1 & 0 & \cdots & 0 \\ 0 & 1 & \cdots & 0 \\ \vdots & \vdots & \ddots & \vdots \\ 0 & 0 & \cdots & 1 \end{bmatrix}$$

# Invertible matricer
En matrix $X$ er invertibel, hvis der findes en matrix $Y$, således at:

$$X Y = Y X = I$$

I kaldes identitetsmatricen.

# Transponering af en matrix
Givet en matrix $X$ kan vi beregne den transponerede matrix $X^T$ ved at bytte om på rækker og kolonner. Lad $X$ være en n x m matrix. Den generelle notation er:

$$X^T = \begin{bmatrix} x_{11} & x_{12} & \cdots & x_{1m} \\ x_{21} & x_{22} & \cdots & x_{2m} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} & x_{n2} & \cdots & x_{nm} \end{bmatrix}^T = \begin{bmatrix} x_{11} & x_{21} & \cdots & x_{n1} \\ x_{12} & x_{22} & \cdots & x_{n2} \\ \vdots & \vdots & \ddots & \vdots \\ x_{1m} & x_{2m} & \cdots & x_{nm} \end{bmatrix}$$

# Eksempel på transponering af en matrix
Givet matricen $X$:

$$X=\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}$$

kan vi beregne den transponerede matrix $X^T$:

$$X^T = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}^T = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}$$


# Determinanten af en matrix: Hvad er det?

Determinanten af en matrix er en operation på en kvadratisk matrix, som giver et tal. Determinanten af en matrix er en måde at beregne om en matrix er invertibel. 

- Hvis determinanten af en matrix er forskellig fra nul, så er matricen invertibel. 
- Hvis determinanten af en matrix er lig med nul, så er matricen ikke invertibel.



# Determinanten af en matrix
Vi kan beregne determinanten af en kvadratisk matrix ved at beregne summen af produkterne af elementerne i en række og deres såkaldte kofaktorer. Lad $X$ være en n x n matrix. Den generelle notation er:

$$\det X = \begin{vmatrix} x_{11} & x_{12} & \cdots & x_{1n} \\ x_{21} & x_{22} & \cdots & x_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ x_{n1} & x_{n2} & \cdots & x_{nn} \end{vmatrix} = \sum_{i=1}^n x_{1i} C_{1i}$$

Hvor $C_{1i}$ er kofaktoren for elementet $x_{1i}$:

$$C_{1i} = (-1)^{1+i} M_{1i}$$

## Determinanten af en matrix fortsat

Her er $M_{1i}$ minorværdien for elementet $x_{1i}$:

$$M_{1i} = \begin{vmatrix} x_{22} & \cdots & x_{2i-1} & x_{2i+1} & \cdots & x_{2n} \\ \vdots & \ddots & \vdots & \vdots & \ddots & \vdots \\ x_{n2} & \cdots & x_{ni-1} & x_{ni+1} & \cdots & x_{nn} \end{vmatrix}$$

# Eksempel på beregning af determinanten af en matrix
Determinanten af matricen $X$:

$$X=\begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{bmatrix}$$

Vi starter med at beregne kofaktorerne:

$$C_{11} = (-1)^{1+1} M_{11} = 1 \cdot \begin{vmatrix} 5 & 6 \\ 8 & 9 \end{vmatrix} = 1 \cdot (5 \cdot 9 - 6 \cdot 8)$$ 
$$ = 1 \cdot (45 - 48) = 1 \cdot (-3) = -3$$

$$C_{12} = (-1)^{1+2} M_{12} = -1 \cdot \begin{vmatrix} 4 & 6 \\ 7 & 9 \end{vmatrix} = -1 \cdot (4 \cdot 9 - 6 \cdot 7) $$
$$ = -1 \cdot (36 - 42) = -1 \cdot (-6) = 6$$

$$C_{13} = (-1)^{1+3} M_{13} = 1 \cdot \begin{vmatrix} 4 & 5 \\ 7 & 8 \end{vmatrix} = 1 \cdot (4 \cdot 8 - 5 \cdot 7) $$  
$$=  1 \cdot (32 - 35) = 1 \cdot (-3) = -3$$

Derefter beregner vi determinanten af matricen $X$:

$$\det X = \begin{vmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \\ 7 & 8 & 9 \end{vmatrix} $$
$$ = 1 \cdot C_{11} + 2 \cdot C_{12} + 3 \cdot C_{13}$$ 
$$ = 1 \cdot (-3) + 2 \cdot 6 + 3 \cdot (-3) = 0$$

# Invers matrix
Vi kan beregne den inverse matrix ved at beregne kofaktorerne for hver enkelt element i matricen og derefter transponere matricen. Lad $X$ være en n x n matrix: 

$$X^{-1} = \frac{1}{\det X} \begin{bmatrix} C_{11} & C_{21} & \cdots & C_{n1} \\ C_{12} & C_{22} & \cdots & C_{n2} \\ \vdots & \vdots & \ddots & \vdots \\ C_{1n} & C_{2n} & \cdots & C_{nn} \end{bmatrix}^T$$

# Eksempel på beregning af invers matrix
Givet matricen $Z$:

$$Z=\begin{bmatrix} 4 & 0 & 1 \\ 3 & 3 & 2 \\ 1 & 0 & 9 \end{bmatrix}$$

kan vi beregne den inverse matrix:

$$Z^{-1} = \frac{1}{\det Z} \begin{bmatrix} C_{11} & C_{21} & C_{31} \\ C_{12} & C_{22} & C_{32} \\ C_{13} & C_{23} & C_{33} \end{bmatrix}^T$$

Vi starter med at beregne determinanten af matricen $Z$:

$$\det Z = \begin{vmatrix} 4 & 0 & 1 \\ 3 & 3 & 2 \\ 1 & 0 & 9 \end{vmatrix} = 4 \cdot \begin{vmatrix} 3 & 2 \\ 0 & 9 \end{vmatrix} - 0 \cdot \begin{vmatrix} 3 & 2 \\ 1 & 9 \end{vmatrix} + 1 \cdot \begin{vmatrix} 3 & 3 \\ 1 & 0 \end{vmatrix}$$
$$= 4 \cdot (3 \cdot 9 - 2 \cdot 0) - 0 \cdot (3 \cdot 9 - 2 \cdot 1) + 1 \cdot (3 \cdot 0 - 3 \cdot 1) = 4 \cdot (27 - 0) - 0 \cdot (27 - 2) + 1 \cdot (0 - 3)$$
$$= 4 \cdot 27 - 0 \cdot 25 + 1 \cdot (-3) = 108 - 0 - 3 = 105$$

Vi bemærker, at determinanten af matricen $Z$ er forskellig fra nul, så matricen er invertibel. 

# Eksempel på beregning af invers matrix - fortsat: Beregning af kofaktorer
Vi fortsætter med at beregne kofaktorerne for hver enkelt element i matricen $Z$:

$$C_{11} = (-1)^{1+1} M_{11} = 1 \cdot \begin{vmatrix} 3 & 2 \\ 0 & 9 \end{vmatrix} = 1 \cdot (3 \cdot 9 - 2 \cdot 0) =   27$$

$$C_{12} = (-1)^{1+2} M_{12} = -1 \cdot \begin{vmatrix} 3 & 2 \\ 1 & 9 \end{vmatrix} = -1 \cdot (3 \cdot 9 - 2 \cdot 1) =   -25$$

$$C_{13} = (-1)^{1+3} M_{13} = 1 \cdot \begin{vmatrix} 3 & 3 \\ 1 & 0 \end{vmatrix} = 1 \cdot (3 \cdot 0 - 3 \cdot 1) =   -3$$

# Eksempel på beregning af invers matrix - fortsat: Beregning af kofaktorer
$$C_{21} = (-1)^{2+1} M_{21} = -1 \cdot \begin{vmatrix} 0 & 1 \\ 0 & 9 \end{vmatrix} = -1 \cdot (0 \cdot 9 - 1 \cdot 0) = 0$$

$$C_{22} = (-1)^{2+2} M_{22} = 1 \cdot \begin{vmatrix} 4 & 1 \\ 1 & 9 \end{vmatrix} = 1 \cdot (4 \cdot 9 - 1 \cdot 1)  = 35$$

$$C_{23} = (-1)^{2+3} M_{23} = -1 \cdot \begin{vmatrix} 4 & 0 \\ 1 & 0 \end{vmatrix} = -1 \cdot (4 \cdot 0 - 0 \cdot 0)  = 0$$

# Eksempel på beregning af invers matrix - fortsat: Beregning af kofaktorer
$$C_{31} = (-1)^{3+1} M_{31} = 1 \cdot \begin{vmatrix} 0 & 1 \\ 3 & 2 \end{vmatrix} = 1 \cdot (0 \cdot 2 - 1 \cdot 3) = -3$$

$$C_{32} = (-1)^{3+2} M_{32} = -1 \cdot \begin{vmatrix} 4 & 1 \\ 3 & 2 \end{vmatrix} = -1 \cdot (4 \cdot 2 - 1 \cdot 3) = -5$$

$$C_{33} = (-1)^{3+3} M_{33} = 1 \cdot \begin{vmatrix} 4 & 0 \\ 3 & 3 \end{vmatrix} = 1 \cdot (4 \cdot 3 - 0 \cdot 3)  = 12$$

# Eksempel på beregning af invers matrix - fortsat: Beregning af den inverse matrix

Vi kan nu beregne den inverse matrix:

$$Z^{-1} = \frac{1}{\det Z} \begin{bmatrix} C_{11} & C_{21} & C_{31} \\ C_{12} & C_{22} & C_{32} \\ C_{13} & C_{23} & C_{33} \end{bmatrix}^T$$

$$= \frac{1}{105} \begin{bmatrix} 27 & 0 & -3 \\ -25 & 35 & -5 \\ -3 & 0 & 12 \end{bmatrix}^T = \frac{1}{105} \begin{bmatrix} 27 & -25 & -3 \\ 0 & 35 & 0 \\ -3 & -5 & 12 \end{bmatrix}$$

Den endelige matrix er:

$$Z^{-1} = \frac{1}{105} \begin{bmatrix} 27 & -25 & -3 \\ 0 & 35 & 0 \\ -3 & -5 & 12 \end{bmatrix}$$


























