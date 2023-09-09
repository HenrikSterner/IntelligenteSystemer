---
output:
  pdf_document:
    keep_tex: true
    latex_engine: xelatex
  html_document:
    df_print: paged
header-includes:
- \usetheme[sectionpage = none]{metropolis}
title: "Introduktion til Matematisk analyse"
subtitle: "Relevant for maskinlæring og intelligente systemer (DDU)"
author: [Henrik Sterner]
date: "16-08-2023"
fonttheme: "default"
fontsize: 11pt
urlcolor: red
linkstyle: bold
aspectratio: 169
date: 20/08/2023

---


# Introduktion til matematisk analyse relevant for maskinlæring og intelligente systemer

## Af Henrik Sterner
I det følgende ser vi på nogle af de matematiske begreber indenfor grenen af matematik kaldet matematisk analyse, som er relevante for maskinlæring og intelligente systemer. Vi ser på begreber som funktioner, differentialregning, integralregning, vektorer og matricer. 

# Funktioner
Ved en funktion forstår vi en regel, der til hvert element i en mængde $X$ tilknytter et element i en mængde $Y$. 

Vi skriver $f: X \rightarrow Y$ og siger at $f$ er en funktion fra $X$ til $Y$. 

Elementerne i $X$ kaldes for funktionens definitionsmængde. 

Elementerne i $Y$ kaldes for funktionens værdimængde.

# Eksempel
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = x^2$. Her er $X = \mathbb{R}$ og $Y = \mathbb{R}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sin(x)$.Her er $X = \mathbb{R}$ og $Y = [-1,1]$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \frac{1}{x}$.Her er $X = \mathbb{R} \setminus \{0\}$ og $Y = \mathbb{R} \setminus \{0\}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sqrt{x}$.Her er $X = [0,\infty)$ og $Y = [0,\infty)$.

# Kontinuerte funktioner
En funktion $f: X \rightarrow Y$ kaldes kontinuert i $x_0 \in X$, hvis der for ethvert $\epsilon > 0$ findes et $\delta > 0$, således at $|f(x) - f(x_0)| < \epsilon$ for alle $x \in X$ med $|x - x_0| < \delta$. 

En funktion $f: X \rightarrow Y$ kaldes kontinuert, hvis den er kontinuert i alle punkter i $X$.

Groft sagt betyder det, at en funktion er kontinuert, hvis den kan tegnes uden at løfte blyanten fra papiret.

# Eksempel
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = x^2$. Her er $X = \mathbb{R}$ og $Y = \mathbb{R}$. Funktionen er kontinuert i alle punkter i $\mathbb{R}$. 
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sin(x)$.Her er $X = \mathbb{R}$ og $Y = [-1,1]$. Funktionen er kontinuert i alle punkter i $\mathbb{R}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \frac{1}{x}$.Her er $X = \mathbb{R} \setminus \{0\}$ og $Y = \mathbb{R} \setminus \{0\}$. Funktionen er kontinuert i alle punkter i $\mathbb{R} \setminus \{0\}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sqrt{x}$.Her er $X = [0,\infty)$ og $Y = [0,\infty)$. Funktionen er kontinuert i alle punkter i $[0,\infty)$.

# Differentiable funktioner
En funktion $f: X \rightarrow Y$ kaldes differentiabel i $x_0 \in X$, hvis grænseværdien
$$\lim_{x \rightarrow x_0} \frac{f(x) - f(x_0)}{x - x_0}$$
eksisterer.

En funktion $f: X \rightarrow Y$ kaldes differentiabel, hvis den er differentiabel i alle punkter i $X$.

# Eksempel
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = x^2$. Her er $X = \mathbb{R}$ og $Y = \mathbb{R}$. Funktionen er differentiabel i alle punkter i $\mathbb{R}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sin(x)$.Her er $X = \mathbb{R}$ og $Y = [-1,1]$. Funktionen er differentiabel i alle punkter i $\mathbb{R}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \frac{1}{x}$.Her er $X = \mathbb{R} \setminus \{0\}$ og $Y = \mathbb{R} \setminus \{0\}$. Funktionen er differentiabel i alle punkter i $\mathbb{R} \setminus \{0\}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sqrt{x}$.Her er $X = [0,\infty)$ og $Y = [0,\infty)$. Funktionen er differentiabel i alle punkter i $(0,\infty)$.

# Differentialkvotient
Hvis en funktion $f: X \rightarrow Y$ er differentiabel i $x_0 \in X$, så kaldes grænseværdien
$$\lim_{x \rightarrow x_0} \frac{f(x) - f(x_0)}{x - x_0}$$
for differentialkvotienten for $f$ i $x_0$ og betegnes $f'(x_0)$.

# Eksempel
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = x^2$. Her er $X = \mathbb{R}$ og $Y = \mathbb{R}$. Funktionen er differentiabel i alle punkter i $\mathbb{R}$. Differentialkvotienten for $f$ i $x_0$ er $f'(x_0) = 2x_0$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sin(x)$.Her er $X = \mathbb{R}$ og $Y = [-1,1]$. Funktionen er differentiabel i alle punkter i $\mathbb{R}$. Differentialkvotienten for $f$ i $x_0$ er $f'(x_0) = \cos(x_0)$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \frac{1}{x}$.Her er $X = \mathbb{R} \setminus \{0\}$ og $Y = \mathbb{R} \setminus \{0\}$. Funktionen er differentiabel i alle punkter i $\mathbb{R} \setminus \{0\}$. Differentialkvotienten for $f$ i $x_0$ er $f'(x_0) = -\frac{1}{x_0^2}$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sqrt{x}$.Her er $X = [0,\infty)$ og $Y = [0,\infty)$. Funktionen er differentiabel i alle punkter i $(0,\infty)$. Differentialkvotienten for $f$ i $x_0$ er $f'(x_0) = \frac{1}{2\sqrt{x_0}}$.

# Regneregler for differentialkvotienter
Lad $f: X \rightarrow Y$ og $g: X \rightarrow Y$ være differentiable funktioner i $x_0 \in X$. Så gælder følgende regneregler for differentialkvotienter:
- $(f + g)'(x_0) = f'(x_0) + g'(x_0)$
- $(f - g)'(x_0) = f'(x_0) - g'(x_0)$
- $(f \cdot g)'(x_0) = f'(x_0) \cdot g(x_0) + f(x_0) \cdot g'(x_0)$
- $(\frac{f}{g})'(x_0) = \frac{f'(x_0) \cdot g(x_0) - f(x_0) \cdot g'(x_0)}{g(x_0)^2}$
- $(f \circ g)'(x_0) = f'(g(x_0)) \cdot g'(x_0)$

# Eksempel
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = x^2$ og $g: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $g(x) = x^3$. Her er $X = \mathbb{R}$ og $Y = \mathbb{R}$. Funktionerne er differentiable i alle punkter i $\mathbb{R}$. Differentialkvotienten for $f$ i $x_0$ er $f'(x_0) = 2x_0$ og differentialkvotienten for $g$ i $x_0$ er $g'(x_0) = 3x_0^2$. Vi har derfor:
- $(f + g)'(x_0) = f'(x_0) + g'(x_0) = 2x_0 + 3x_0^2$
- $(f - g)'(x_0) = f'(x_0) - g'(x_0) = 2x_0 - 3x_0^2$
- $(f \cdot g)'(x_0) = f'(x_0) \cdot g(x_0) + f(x_0) \cdot g'(x_0) = 2x_0 \cdot x_0^3 + x_0^2 \cdot 3x_0^2 = 2x_0^4 + 3x_0^4$
- $(\frac{f}{g})'(x_0) = \frac{f'(x_0) \cdot g(x_0) - f(x_0) \cdot g'(x_0)}{g(x_0)^2} = \frac{2x_0 \cdot x_0^3 - x_0^2 \cdot 3x_0^2}{x_0^6} = \frac{2x_0^4 - 3x_0^4}{x_0^6} = -\frac{1}{x_0^2}$

# Ekstremumspunkter
Vi kan bruge differentialkvotienten til at finde ekstremumspunkter for en funktion. Dvs. punkter hvor funktionen har et lokalt maksimum eller minimum.

Lad $f: X \rightarrow Y$ være en differentiable funktion. Så er $x_0 \in X$ et ekstremumspunkt for $f$, hvis $f'(x_0) = 0$.



# Sammensatte funktioner
Lad $f: X \rightarrow Y$ og $g: X \rightarrow Y$ være funktioner. Så er den sammensatte funktion $f \circ g: X \rightarrow Y$ givet ved $(f \circ g)(x) = f(g(x))$.

# Eksempel
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = x^2$ og $g: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $g(x) = x^3$. Her er $X = \mathbb{R}$ og $Y = \mathbb{R}$. Den sammensatte funktion $f \circ g: \mathbb{R} \rightarrow \mathbb{R}$ er givet ved $(f \circ g)(x) = f(g(x)) = f(x^3) = (x^3)^2 = x^6$.
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sin(x)$ og $g: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $g(x) = x^3$. Her er $X = \mathbb{R}$ og $Y = [-1,1]$. Den sammensatte funktion $f \circ g: \mathbb{R} \rightarrow \mathbb{R}$ er givet ved $(f \circ g)(x) = f(g(x)) = f(x^3) = \sin(x^3)$.
  
# Differentiering af sammensatte funktioner
Lad $f: X \rightarrow Y$ og $g: X \rightarrow Y$ være differentiable funktioner. Så er den sammensatte funktion $f \circ g: X \rightarrow Y$ differentiable og differentialkvotienten for $f \circ g$ i $x_0$ er givet ved $(f \circ g)'(x_0) = f'(g(x_0)) \cdot g'(x_0)$.

Denne regel kaldes kædereglen og bliver særdeles nyttig i maskinlæring og intelligente systemer.

# Eksempel
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = x^2$ og $g: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $g(x) = x^3$. Her er $X = \mathbb{R}$ og $Y = \mathbb{R}$. Funktionerne er differentiable i alle punkter i $\mathbb{R}$. Differentialkvotienten for $f$ i $x_0$ er $f'(x_0) = 2x_0$ og differentialkvotienten for $g$ i $x_0$ er $g'(x_0) = 3x_0^2$. Vi har derfor:
- $(f \circ g)'(x_0) = f'(g(x_0)) \cdot g'(x_0) = f'(x_0^3) \cdot g'(x_0) = 2x_0^3 \cdot 3x_0^2 = 6x_0^5$
- Lad $f: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $f(x) = \sin(x)$ og $g: \mathbb{R} \rightarrow \mathbb{R}$ være givet ved $g(x) = x^3$. Her er $X = \mathbb{R}$ og $Y = [-1,1]$. Funktionerne er differentiable i alle punkter i $\mathbb{R}$. Differentialkvotienten for $f$ i $x_0$ er $f'(x_0) = \cos(x_0)$ og differentialkvotienten for $g$ i $x_0$ er $g'(x_0) = 3x_0^2$. Vi har derfor:
- $(f \circ g)'(x_0) = f'(g(x_0)) \cdot g'(x_0) = f'(x_0^3) \cdot g'(x_0) = \cos(x_0^3) \cdot 3x_0^2$

# Funktioner af flere variable
Indtil nu har vi kun set på funktioner af én variabel. Vi kan også betragte funktioner af flere variable.

En funktion $f: X \rightarrow Y$ kaldes en funktion af to variable, hvis $X \subseteq \mathbb{R}^2$ og $Y \subseteq \mathbb{R}$.

En funktion $f: X \rightarrow Y$ kaldes en funktion af tre variable, hvis $X \subseteq \mathbb{R}^3$ og $Y \subseteq \mathbb{R}$.

En funktion $f: X \rightarrow Y$ kaldes en funktion af $n$ variable, hvis $X \subseteq \mathbb{R}^n$ og $Y \subseteq \mathbb{R}$.

# Eksempler på funktioner af flere variable
- Lad $f: \mathbb{R}^2 \rightarrow \mathbb{R}$ være givet ved $f(x,y) = x^2 + y^2$. Her er f en funktion af to variable.
- Lad $f: \mathbb{R}^3 \rightarrow \mathbb{R}$ være givet ved $f(x,y,z) = x^2 + y^2 + z^2$. Her er f en funktion af tre variable.
- Lad $f: \mathbb{R}^n \rightarrow \mathbb{R}$ være givet ved $f(x_1,x_2,\ldots,x_n) = x_1^2 + x_2^2 + \ldots + x_n^2$. Her er f en funktion af $n$ variable.

# Partielle differentialkvotienter
For at kunne differentiere en funktion af flere variable, skal vi indføre begrebet partielle differentialkvotienter.

Lad $f: X \rightarrow Y$ være en funktion af to variable, hvor $X \subseteq \mathbb{R}^2$ og $Y \subseteq \mathbb{R}$. Så er den partielle differentialkvotient af $f$ i $(x_0,y_0) \in X$ med hensyn til $x$ givet ved:
$$\frac{\partial f}{\partial x}(x_0,y_0) = \lim_{h \rightarrow 0} \frac{f(x_0 + h,y_0) - f(x_0,y_0)}{h}$$

Den partielle differentialkvotient af $f$ i $(x_0,y_0) \in X$ med hensyn til $y$ givet ved:
$$\frac{\partial f}{\partial y}(x_0,y_0) = \lim_{h \rightarrow 0} \frac{f(x_0,y_0 + h) - f(x_0,y_0)}{h}$$

# Eksempel: Udregning af partielle differentialkvotienter 
Lad $f: \mathbb{R}^2 \rightarrow \mathbb{R}$ være givet ved $f(x,y) = x^2 + y^2$. Her er $X = \mathbb{R}^2$ og $Y = \mathbb{R}$. Funktionen er differentiable i alle punkter i $\mathbb{R}^2$. Den partielle differentialkvotient af $f$ i $(x_0,y_0) \in \mathbb{R}^2$ med hensyn til $x$ er givet ved:
$$\frac{\partial f}{\partial x}(x_0,y_0) =  \lim_{h \rightarrow 0} \frac{f(x_0 + h,y_0) - f(x_0,y_0)}{h}$$ 
$$ = \lim_{h \rightarrow 0} \frac{(x_0 + h)^2 + y_0^2 - x_0^2 - y_0^2}{h} $$ 
$$ = \lim_{h \rightarrow 0} \frac{x_0^2 + 2x_0h + h^2 + y_0^2 - x_0^2 - y_0^2}{h} $$ 
$$ = \lim_{h \rightarrow 0} \frac{2x_0h + h^2}{h} = \lim_{h \rightarrow 0} 2x_0 + h = 2x_0$$

# Eksempel: Udregning af partielle differentialkvotienter 
og tilsvarende er den partielle differentialkvotient af $f$ i $(x_0,y_0) \in \mathbb{R}^2$ med hensyn til $y$ givet ved:
$$\frac{\partial f}{\partial y}(x_0,y_0) =  \lim_{h \rightarrow 0} \frac{f(x_0,y_0 + h) - f(x_0,y_0)}{h}$$
$$ = \lim_{h \rightarrow 0} \frac{x_0^2 + (y_0 + h)^2 - x_0^2 - y_0^2}{h} $$
$$ = \lim_{h \rightarrow 0} \frac{x_0^2 + y_0^2 + 2y_0h + h^2 - x_0^2 - y_0^2}{h} $$
$$ = \lim_{h \rightarrow 0} \frac{2y_0h + h^2}{h} = \lim_{h \rightarrow 0} 2y_0 + h = 2y_0$$

# Eksempel: Udregning af partielle differentialkvotienter
Her et eksempel med tre variable. Lad $f: \mathbb{R}^3 \rightarrow \mathbb{R}$ være givet ved $f(x,y,z) = x^2 + y^2 + z^2$. Her er $X = \mathbb{R}^3$ og $Y = \mathbb{R}$. Funktionen er differentiable i alle punkter i $\mathbb{R}^3$. 
# Eksempel: Udregning af partielle differentialkvotienter mh.t. x

Den partielle differentialkvotient af $f$ i $(x_0,y_0,z_0) \in \mathbb{R}^3$ med hensyn til $x$ er givet ved:
$$\frac{\partial f}{\partial x}(x_0,y_0,z_0) =  \lim_{h \rightarrow 0} \frac{f(x_0 + h,y_0,z_0) - f(x_0,y_0,z_0)}{h}$$
$$ = \lim_{h \rightarrow 0} \frac{(x_0 + h)^2 + y_0^2 + z_0^2 - x_0^2 - y_0^2 - z_0^2}{h} $$
$$ = \lim_{h \rightarrow 0} \frac{x_0^2 + 2x_0h + h^2 + y_0^2 + z_0^2 - x_0^2 - y_0^2 - z_0^2}{h} $$
$$ = \lim_{h \rightarrow 0} \frac{2x_0h + h^2}{h} = \lim_{h \rightarrow 0} 2x_0 + h = 2x_0$$

Tilsvarende udregnes den partielle differentialkvotient af $f$ i $(x_0,y_0,z_0) \in \mathbb{R}^3$ med hensyn til $y$ og $z$.




