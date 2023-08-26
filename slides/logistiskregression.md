---
title: Logistisk regression i Python
subtitle: Introduktion til Logistisk Regression i Python
author: Henrik Sterner
fonttheme: "default"    
lheader: "Intelligente Systemer"
rheader: "Henrik Sterner (henrik.sterner@gmail.com)"
---


# Introduktion til Logistisk Regression i Python
## Af Henrik Sterner (henrik.sterner@gmail.com)
I det følgende introduceres logistisk regression og hvordan vi kan bruge det i Python. 



# Hvad er logistisk regression?
Logistisk regression er en metode til at forudsige sandsynligheden for at en given observation tilhører en given klasse.
Eksempler er mange:
* Er en given e-mail spam?
* Er en given transaktion svindel?
* Er en given patient syg?
* Er en given kunde tilbøjelig til at købe et produkt?
* Er en given kunde tilbøjelig til at opsige sit abonnement?
* Har en given kunde en høj sandsynlighed for at købe et produkt?

# Hvorfor logistisk regression?
Logistisk regression er en simpel og hurtig metode til at forudsige sandsynligheden for at en given observation tilhører en given klasse.
* Logistisk regression er hurtig at træne og kan derfor bruges til at træne modeller på store datasæt.  
* Logistisk regression er hurtig at bruge til at forudsige sandsynligheder for nye observationer.
* Modsat lineær regression er logistisk regression ikke begrænset til at forudsige værdier mellem 0 og 1.

# Hvordan virker logistisk regression?
Logistisk regression er en udvidelse af lineær regression.
* Lineær regression: $$y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_n x_n$$
* Logistisk regression: $$y = \frac{1}{1 + e^{-(\beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_n x_n)}},$$
hvor $y$ er sandsynligheden for at en given observation tilhører en given klasse.
