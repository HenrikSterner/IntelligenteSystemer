# Introduktion til maskinelæring og kunstig intelligens ved brug af Python og scipy
## Af Henrik Sterner (henrik.sterner@gmail.com)

scipy er en samling af Python-biblioteker til videnskabelig programmering. Det er gratis og open source.

# scipy er tilgængelig på flere måder
scipy er en del af Anaconda, som er en distribution af Python, der er gratis og open source. Anaconda kan hentes [her](https://www.anaconda.com/products/individual).

scipy er også en del af Google Colab, som er en online udgave af Jupyter Notebook. Google Colab kan hentes [her](https://colab.research.google.com/).

# knn-algoritmen i scipy
Vi vil bruge scipy til at implementere knn-algoritmen. Vi starter med at importere de biblioteker, som vi skal bruge.

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn import datasets
from sklearn.neighbors import KNeighborsClassifier
```
