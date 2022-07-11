# Kunstig Intelligente Systemer: En introduktion til maskinelæring i Python
Kunstig intelligens i form af machine learning (maskinlæring) og deep learning (dyb læring) på neurale netværk transformerer alle aspekter af vores samfund i disse år – ikke mindst vores forståelse af verdenen og af os selv.  
Det er et ekstremt spændende felt, hvor grænserne næsten dagligt rykkes for hvad vi troede var muligt for blot få år siden. Denne udvikling tager kun til i de kommende år i takt med, at stadig større datamængder bliver tilgængelige og at microchips/computere bliver stadig mindre, hurtigere og mere allestedsnærværende. 

Nærværende side beskriver et undervisningsforløb der har til formål at give jer en praktisk introduktion til algoritmerne, metoderne og værktøjerne bag machine learning og deep learning med henblik på at gøre jer i stand til at designe og udvikle systemer/prototyper, der tager selvstændige data-drevne beslutninger på baggrund af modeller, som vi har trænet. Dvs. ved at få computeren til at lære fra data skabes systemer, der er i stand til at imitere menneskelig intelligens. 

Herunder nogle bud på systemer, som vi kan udvikle prototyper af. Listen er langt fra udtømmende og kan udvides/tones efter ønske/det andet valgtema:
•	Billedsegmentering og objektklassificering, som vi kan bruge i konstruktion af selvkørende biler/robotter, identifikation af tumorer ud fra MR-skanninger, ansigtsgenkendelse, kunstig intelligente modstandere/NPC’er i spil, etc.
•	Anbefalingssystemer, der giver  bud på din næste film på Netflix, hvilken trøje du skal købe eller hvem din nye kæreste skal være ;-), etc.
•	Naturlig sprogprocessering, der tilbyder at automatisere analysen af tekster med henblik på at forstå de udtrykte følelser, meninger og intentioner, udvikle chatbots og virtuelle assistenter, talegenkendelse, identificere fake news, modellering af psykologiske profiler ud fra SoMe data, etc.
•	Forudsigelsessystemer, der muligvis kan forudsige hvordan aktierne udvikler sig, hvem der vinder den næste Premier League kamp, klimaets tilstand i de kommende år, etc.
Som listen indikerer er det væsentligt at forholde sig kritisk til fagets muligheder og begrænsninger herunder de indlejrede bias. Nettet flyder i øvrigt over med store, frit tilgængelige datasæt, som vi i første omgang kan træne vores modeller på. 

# Forudsætninger
For at kunne forstå, implementere og anvende algoritmer indenfor maskinelæring forudsættes en god forståelse for emner både indenfor datalogi og matematik. Herunder

# Grundbog og øvelser
Vi bruger uddrag af følgende to gratis og opensource bøger: 
1. (PY) [A Whirlwind Tour of Python](https://jakevdp.github.io/WhirlwindTourOfPython/) af Jake VanderPlas. 
2. (PD) [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) af Jake VanderPlas.
3. (DI) [Dive into Deep Learning](https://d2l.ai/) af Aston Zhang et al.
4. (ØP) [Øvelser og projekter](https://github.com/HenrikSterner/PythonForDataScience/blob/master/exercises/exercises.ipynb) af Henrik Sterner.


Bøgerne er gratis, og rummer en række kapitler i jupyter-formatet, som gør det muligt at kombinere tekst og kode. Derudover vil der være uddrag fra andre bøger og materialer fra nettet.

# Software
Man kan vælge at køre online uden at skulle installere noget og dokumenter kan nemt deles:
- [Google Colab](https://colab.research.google.com/)

Alternativt kan man bruge 
- [Anaconda](https://www.anaconda.com/products/individual) 
- [Jupyter-plugin til Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter). Kan bare hentes under plugin i vscode.

Begge løsninger giver mulighed for at skrive Python (i jupyter-format) og tilhørende biblioteker numpy, scikit, matplotlib, streamlit etc.

Derudover kommer vi til at bruge Python til Processing, da det ofte er særdeles nemt at visualisere algoritmer i to dimensioner:
- [Processing in Python](https://py.processing.org/)


# Undervisningsplan
Planen er tentativ og kan ændres. Den indleder med et crash course i Python, lineær algebra og sandsynlighedsregning, som er centrale forudsætninger for at forstå maskinelæring.

Modul Nr       | Kapitel     | Indhold                     | Øvelser     |
----------- | ----------- | ----------------------------| ----------- |
1 |PY:1-6 | Python I: Variabler, sekvens og selektion | ØP:1-6     |
2 |PY:7-11 | Python II: Iterationer, funktioner, fejl og lister  |ØP:7-14,21-25,33 |
3 |PY:16,PD:2 | Python III: Numpy  | 43-48|
4 |PY:16,PD:4 | Python IV: Matplotlib  |43-48 |
5 | [Projekt](https://github.com/HenrikSterner/PythonExercises/blob/main/projects/ML_knn.md) | **Aflevering af ML-Projekt: kNN algoritmen** | Arbejde med projekt |
6 | | Lineær algebra I: Vektorer  |  |
7 | | Lineær algebra II: Matricer  |  |
8 | | **ML-Projekt: Aflevering af k-means algoritmen** | |
9 | | Deskriptiv statistik |  |
10 | | Beslutningstræer ||
11 | | ML-Projekt: Randomiseret skove | |
12 | | Sandsynlighedsregning, Bayes sætning||
13 | | ML-Projekt: Naiv Bayes algoritme | |
14 | | Lineær regression | |
15 | | Logistisk regression |  |
16 | | ML-Projekt: Regression | |
17 | | Perceptroner |  |
18 | | Lineært Neurale netværk |  |
19 | | Multilinære Neurale netværk |  |
20 | | ML-projekt: Neurale netværk |  |
21 | | Dyb læring |  |
22 | | Convolutional neurale netværk |  |

