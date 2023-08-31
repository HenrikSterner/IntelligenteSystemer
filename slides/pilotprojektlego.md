# Intelligente systemer med Lego Spike Prime og Python

## Af Henrik Sterner (hst@nextkbh.dk) og Nanna Kari  (nakj@nextkbh.dk)


Følgende dokument indeholder en beskrivelse af et pilotprojekt, hvor eleverne skal arbejde med intelligente systemer ved hjælp af Lego Spike Prime og Python. Projektet er udviklet af Nanna Kari og Henrik Sterner, som er undervisere på forløbet.

## Introduktion
Der findes mange forskellige definitioner på intelligente systemer. En af de mest udbredte er, at intelligente systemer er systemer, der kan lære af erfaring. Det vil sige, at systemet kan forbedre sin performance ved at analysere data og finde mønstre i data.

## Rammer for projektet
Vi skal arbejde med at udvikle intelligente systemer, der kan analysere data og finde mønstre i data ved brug af Lego Spike Prime og Python. 

I bestemmer helt selv hvilke data, I vil arbejde med. Det kan være lyd, billeder, bevægelse, temperatur, lys, afstand, farver, tryk, berøring, osv. I kan også arbejde med flere forskellige typer af data.

I skal arbejde med at udvikle et system, der kan analysere data og finde mønstre i data. Systemet skal kunne reagere på mønstrene. Det kan f.eks. være ved at systemet kan sige noget, bevæge sig, lyse, osv.

I skal arbejde med at udvikle systemet i Python. I skal bruge Lego Spike Prime til at indsamle data og til at reagere på mønstrene.

## Intelligente algoritmer KNN og K-means
I kan overveje (men det er ikke et krav) at arbejde med de intelligente algoritmer KNN og K-means, som vi indtil videre har arbejdet med i undervisningen: 

* KNN er en algoritme, der kan lære at genkende mønstre i data. Algoritmen kan f.eks. lære at genkende mønstre i lyd, billeder, lokationsdata og reagere på disse input.
* K-means er en algoritme, der kan lære at gruppere data. Algoritmen kan f.eks. lære at gruppere lyd, billedero og lokationsdata og reagere på disse input.
  

I kan læse mere om algoritmerne på følgende links:

## Til inspiration: Eksempler på intelligente systemer
Eksempler på intelligente lego systemer I kan lave med Lego Spike Prime og Python:

* Et system, der kan lære at genkende mønstre i lyd og reagere på mønstrene.
* Objektgenkendelse og Sorteringsrobot: Byg en robot ved hjælp af LEGO SPIKE Prime, der kan genkende og sortere forskellige objekter baseret på deres egenskaber. Træn KNN-algoritmen med prøver af forskellige objekter og programmer derefter robotten til at bruge dens sensorer (såsom farve- eller afstandssensorer) til at identificere og sortere objekter i passende kategorier.
* Håndgestusstyrede Robot:
* Byg en robot, der kan styres ved hjælp af håndgestus. Træn KNN-modellen til at genkende specifikke håndgestus, der opfanges af SPIKE Prime's sensorer, såsom accelerometre eller gyroscopes. Dette kan involvere enkle gestus for grundlæggende bevægelse eller mere komplekse gestus for specifikke kommandoer.
* Indendørs Navigation og Kortlægning: Udvikl en robot, der kan navigere gennem en given miljø og oprette et kort over omgivelserne. Brug KNN-algoritmen til at hjælpe robotten med at bestemme dens placering baseret på sensorisk input og landemærker. Dette projekt vil integrere SPIKE Prime's sensorer som farvesensorer til linjeføring og ultralydssensorer til forhindringsundgåelse.
* Musikgenreklassifikator: Byg en robot, der kan lytte til musik og klassificere sange i forskellige genrer. Træn KNN-modellen ved hjælp af lydfunktioner udtrukket fra forskellige sange. Robotten kan derefter bruge en mikrofon til at lytte til musik og klassificere den i genrer som rock, pop, jazz osv. baseret på det den har lært.
* Plantevelfærdsmonitoreringsrobot: Skab en robot, der bevæger sig rundt i en have eller en samling af potteplanter og overvåger deres helbred. Træn KNN-algoritmen til at skelne mellem sunde og usunde planter baseret på visuelle spor, fanget af et kamera knyttet til robotten. Robotten kan derefter bruge denne viden til at advare gartnere eller udføre opgaver som vanding af specifikke planter.

Ved brug af k-means kan I eksemplevis lave følgende:

*Farveklassifikation og Sortering: Byg en robot, der kan sortere objekter efter farve ved hjælp af K-Means-algoritmen. Træn K-Means-modellen med RGB-værdierne af forskellige farver, og brug farvesensoren på LEGO SPIKE Prime til at registrere farverne på objekter og sortere dem i de korrekte kategorier.
* Klyngebaseret Ruteplanlægning: Udvikl en robot, der kan planlægge sin rute ved at identificere klynger af forhindringer ved hjælp af K-Means. Ved at analysere afstande mellem hindringerne kan robotten vælge en rute med færrest forhindringer.
* Objektfordeling i et Område: Byg en robot, der kan identificere og opdele områder baseret på de forskellige objekter i området. Brug K-Means til at gruppere objekterne i klynger og programmer robotten til at bevæge sig til hver klynge og udføre en bestemt opgave.
* Farvebaseret Kunstværk: Skab en interaktiv kunstrobot ved at udnytte K-Means til at opdele farvespektret i forskellige klynger. Lad robotten vælge farver fra disse klynger og skabe farverige kunstværker ved at male eller tegne på en overflade.
* Støjreduktion i Sensordata: Anvend K-Means til at reducere støj i sensordata, som din LEGO SPIKE-robot indsamler. Træn modellen med kendte støjmønstre, og lad robotten filtrere og rense sensordata i realtid ved hjælp af K-Means for mere pålidelig opfattelse af omgivelserne.

# Sensorinput fra Lego Spike Prime
Som udgangspunkt har robotterne følgende sensorer til rådiged:

* 6-akset accelerometer
* 6-akset gyroskop
* 3-akset magnetometer
* 2 motorer
* 4 farvesensorer
* 2 tryksensorer
* 2 berøringssensorer
* 2 afstandssensorer
* 1 mikrofon
* 1 højttaler

I kan læse mere om sensorerne på følgende link: https://education.lego.com/en-us/support/spike-prime/teacher-guides/sensors

# Rapport
I skal skrive en rapport, der beskriver jeres arbejde med projektet. Rapporten må max fylde 4-6 sider pr gruppe og skal struktureres efter de 7 faser i den iterative designproces:
- Fase 1: Forståelse af problemet. I skal beskrive jeres problemstilling og jeres overvejelser omkring problemstillingen.
- Fase 2: Udvikling af løsning. I skal beskrive jeres overvejelser omkring udviklingen af løsningen.
- Fase 3: Implementering af løsning. I skal beskrive jeres overvejelser omkring implementeringen af løsningen.
- Fase 4: Test af løsning. I skal beskrive jeres overvejelser omkring test af løsningen.
- Fase 5: Evaluering af løsning. I skal beskrive jeres overvejelser omkring evaluering af løsningen.
- Fase 6: Refleksion over projektet. I skal beskrive jeres overvejelser omkring projektet og jeres læring samt i hvor høj grad jeres system er intelligent.
- Fase 7: Konklusion. I skal beskrive jeres konklusioner på projektet.



