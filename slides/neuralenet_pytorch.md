# Introduktion til neurale netværk i PyTorch
## Af Henrik Sterner (henrik.sterner@gmail.com)

Med et grundlæggende kendskab til pytorch er vi nu klar til at kigge på neurale netværk. Vi vil starte med at kigge på et simpelt neuralt netværk, som vi træner på cifar10 datasættet. Vi vil derefter kigge på hvordan vi kan bruge et fortrænet netværk til at lave transfer learning. Til sidst vil vi kigge på hvordan vi kan bruge et neuralt netværk til at generere billeder.

## Hvad er et neuralt netværk?

Et neuralt netværk er en matematisk model, der er inspireret af den måde, hvorpå neuroner i hjernen er forbundet. Et neuralt netværk består af en række lag, hvor hvert lag består af en række neuroner. Hvert neuron i et lag er forbundet til alle neuroner i det forrige lag. Hvert forbindelse mellem to neuroner har en vægt, som bestemmer hvor meget værdi der sendes fra den ene neuron til den anden. Hver neuron har også en bias, som er en konstant, der lægges til den værdi, som sendes fra de forrige neuroner.

# Et meget simpelt neuralt netværk

Vi konstruerer i første omgang et meget simpelt neuralt netværk, som har et input lag og et output lag for at illustrere hvordan et neuralt netværk fungerer. 

Vi starter med at importere de pakker, som vi skal bruge.

```python
import torch
import torch.nn as nn
import torch.nn.functional as F
import torch.optim as optim
```

Vi definerer nu et neuralt netværk, som har et input lag med 3 neuroner og et output lag med 2 neuroner. Vi bruger `nn.Linear` til at definere lagene. `nn.Linear` tager to argumenter, nemlig antallet af neuroner i det forrige lag og antallet af neuroner i det efterfølgende lag. Vi bruger `nn.Linear` til at definere et lag, som vi gemmer i variablen `fc1`. Vi bruger `nn.Linear` til at definere et lag, som vi gemmer i variablen `fc2`.

```python
fc1 = nn.Linear(3, 2)
fc2 = nn.Linear(2, 2)
```

Vi definerer nu et input, som består af en enkelt vektor med 3 elementer. Vi bruger `torch.tensor` til at definere inputtet. Vi bruger `torch.tensor` til at definere et tensor objekt, som vi gemmer i variablen `x`. Vi bruger `torch.tensor` til at definere et tensor objekt, som vi gemmer i variablen `y`.

```python
x = torch.tensor([1.0, 2.0, 3.0])
y = torch.tensor([1.0, 0.0])
```

Vi bruger nu `fc1` til at beregne outputtet fra det første lag. Vi bruger `fc1` til at beregne et tensor objekt, som vi gemmer i variablen `z1`.

```python
z1 = fc1(x)
```

Vi bruger nu `F.relu` til at beregne outputtet fra det første lag. Vi bruger `F.relu` til at beregne et tensor objekt, som vi gemmer i variablen `a1`.

```python
a1 = F.relu(z1)
```

Vi bruger nu `fc2` til at beregne outputtet fra det andet lag. Vi bruger `fc2` til at beregne et tensor objekt, som vi gemmer i variablen `z2`.

```python
z2 = fc2(a1)
```

Vi bruger nu `F.softmax` til at beregne outputtet fra det andet lag. Vi bruger `F.softmax` til at beregne et tensor objekt, som vi gemmer i variablen `a2`.

```python
a2 = F.softmax(z2, dim=0)
```
Her er `dim=0` et argument, som fortæller `F.softmax` at vi vil beregne softmax for hver kolonne i `z2`. Hvis vi havde brugt `dim=1` ville vi beregne softmax for hver række i `z2`.

softmax er en funktion, som tager en vektor som input og returnerer en vektor, hvor alle elementer er mellem 0 og 1 og hvor summen af alle elementer er 1. softmax er defineret som følger:

$$
\text{softmax}(z_i) = \frac{e^{z_i}}{\sum_{j=1}^n e^{z_j}}
$$



Vi kan nu se på outputtet fra det andet lag.

```python
a2
```
