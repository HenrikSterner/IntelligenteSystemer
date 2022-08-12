# Kunstig Intelligente Systemer: En introduktion til maskinelæring i Python
Kunstig intelligens i form af machine learning (maskinlæring) og deep learning (dyb læring) på neurale netværk transformerer alle aspekter af vores samfund i disse år – ikke mindst vores forståelse af verdenen og af os selv.  
Det er et ekstremt spændende felt, hvor grænserne næsten dagligt rykkes for hvad vi troede var muligt for blot få år siden. Denne udvikling tager kun til i de kommende år i takt med, at stadig større datamængder bliver tilgængelige og at microchips/computere bliver stadig mindre, hurtigere og mere allestedsnærværende. 

Nærværende side beskriver et undervisningsforløb der har til formål at give jer en praktisk introduktion til algoritmerne, metoderne og værktøjerne bag machine learning og deep learning med henblik på at gøre jer i stand til at designe og udvikle systemer/prototyper, der tager selvstændige data-drevne beslutninger på baggrund af modeller, som vi har trænet. Dvs. ved at få computeren til at lære fra data skabes systemer, der er i stand til at imitere menneskelig intelligens. 

Herunder nogle bud på systemer, som vi kan udvikle prototyper af. Listen er langt fra udtømmende og kan udvides/tones efter ønske/det andet valgtema:
- Billedsegmentering og objektklassificering, som vi kan bruge i konstruktion af selvkørende biler/robotter, identifikation af tumorer ud fra MR-skanninger, ansigtsgenkendelse, kunstig intelligente modstandere/NPC’er i spil, etc.
- Anbefalingssystemer, der giver  bud på din næste film på Netflix, hvilken trøje du skal købe eller hvem din nye kæreste skal være ;-), etc.
- Naturlig sprogprocessering, der tilbyder at automatisere analysen af tekster med henblik på at forstå de udtrykte følelser, meninger og intentioner, udvikle chatbots og virtuelle assistenter, talegenkendelse, identificere fake news, modellering af psykologiske profiler ud fra SoMe data, etc.
- Forudsigelsessystemer, der muligvis kan forudsige hvordan aktierne udvikler sig, hvem der vinder den næste Premier League kamp, klimaets tilstand i de kommende år, etc.
Som listen indikerer er det væsentligt at forholde sig kritisk til fagets muligheder og begrænsninger herunder de indlejrede bias. Nettet flyder i øvrigt over med store, frit tilgængelige datasæt, som vi i første omgang kan træne vores modeller på. 

## Forudsætninger
For at kunne forstå, implementere og anvende algoritmer indenfor maskinelæring forudsættes en god forståelse for emner både indenfor datalogi og matematik. Fundamentet for ML består af:
- Programmering (vi bruger Python primært)
- Sandsynlighedsteori og statistik 
- Lineær algebra (operationer på vektorer, matricer og tensorer)
- Calculus og vektorcalculus (funktioner af flere variable)
Vi introducerer den nødvendige teori når det er nødvendigt og kun i det omfang det er nødvendigt. For en uddybende teoretisk forståelse af de matematiske begreber kilde eksempelvis i (ML)

## Grundbog og øvelser
Vi bruger uddrag af følgende to gratis og opensource bøger: 
1. (PY) [A Whirlwind Tour of Python](https://jakevdp.github.io/WhirlwindTourOfPython/) af Jake VanderPlas. 
2. (PD) [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/) af Jake VanderPlas.
3. (DI) [Dive into Deep Learning](https://d2l.ai/) af Aston Zhang et al.
4. (ØP) [Øvelser og projekter](https://github.com/HenrikSterner/PythonExercises/blob/main/exercises/exercises.ipynb) af Henrik Sterner.
5. (ØP2) [Nybegynder Øvelser] (https://github.com/HenrikSterner/PythonExercises/blob/main/exercises/easyexercises.ipynb)
6. (ML) [Mathematics for machine learning](https://mml-book.github.io/) af Deisenroth et al.
7. (ML2) [Probabilistic Machine Learning: An Introduction](https://probml.github.io/pml-book/book1.html)
8. (NP) [Numpy øvelser](https://github.com/rougier/numpy-100/blob/master/100_Numpy_exercises.ipynb) med [svar](https://github.com/rougier/numpy-100/blob/master/100_Numpy_exercises_with_solutions.md)
9. (MP) [Matplotlib øvelser](https://pynative.com/python-matplotlib-exercise/) med indlejrede svar.


Bøgerne er gratis, og rummer en række kapitler i jupyter-formatet, som gør det muligt at kombinere tekst og kode. Derudover vil der være uddrag fra andre bøger og materialer fra nettet. 
(PY) og (PD) er primær litteratur mens resterende er sekundær litteratur. (ML) og (ML2) er supplerende litteratur til dem som gerne vil have en bedre forståelse af matematikken bag. 

## Slides
Mine slides er tilgængelige [her](https://github.com/HenrikSterner/IntelligenteSystemer/blob/main/slides/maskinel%C3%A6ring.pptx) (kryperet - password udleveres ved start).

## Software
Man kan vælge at køre online uden at skulle installere noget og dokumenter kan nemt deles:
- [Google Colab](https://colab.research.google.com/)

Alternativt kan man bruge 
- [Anaconda](https://www.anaconda.com/products/individual) 
- [Jupyter-plugin til Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.jupyter). Kan bare hentes under plugin i vscode.

Begge løsninger giver mulighed for at skrive Python (i jupyter-format) og tilhørende biblioteker numpy, scikit, matplotlib, streamlit etc.

Derudover kommer vi til at bruge Python til Processing, da det ofte er særdeles nemt at visualisere algoritmer i to dimensioner:
- [Processing in Python](https://py.processing.org/)


## Undervisningsplan
Planen er tentativ og kan ændres. Den indleder med et crash course i Python. 
Lineær algebra og sandsynlighedsregning, som er centrale forudsætninger for at forstå maskinelæring, vil også blive introduceret undervejs.

Modul Nr       | Kapitel     | Indhold                     | Øvelser     |
----------- | ----------- | ----------------------------| ----------- |
1 |PY:1-6 | Python I: Variabler, sekvens og selektion | ØP2: 1-13, ØP:1-6     |
2 |PY:7-11 | Python II: Iterationer, funktioner, fejl og lister  |ØP2: 1-13,ØP:7-14,18-26,33,37 |
3 |PY:16,PD:2 | Python III: Numpy  |ØP: 43-48 (eksl. 47),mindst 10 fra (NP) |
4 |PY:16,PD:4 | Python IV: Matplotlib  |ØP: 43-48(eksl. 47), alle 10 fra (MP) |
5-6 |PD:5(kNN)  | KNN-algoritmen | [Projekt](https://github.com/HenrikSterner/PythonExercises/blob/main/projects/ML_knn.md) |
7-8 |PD:5(kNN) | K-means algoritmen |[Projekt](https://github.com/HenrikSterner/PythonExercises/blob/main/projects/ML_kmeans.md) |
9-10 |PD:5(Linear regression..) | Lineær regression |[Projekt](https://github.com/HenrikSterner/PythonExercises/blob/main/projects/ML_LinReg.md)|
11 |PD:5(Decision Trees..) | Beslutningstræer og Randomiseret skove ||
12 |PD:5(Naive Bayes..)  | Naiv Bayes-algoritmen | |
13-14 | | Logistisk regression |  |
15 | | Perceptroner |  |
16 | | Lineært Neurale netværk |  |
17 | | Multilinære Neurale netværk |  |
18 | | Neurale netværk |  |
19 | | Dyb læring |  |
20 | | Convolutional neurale netværk |  |

