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

Nu kan vi hente data fra scikit-learn. Vi bruger boston-huspriserne, som er et datasæt med 506 rækker og 13 kolonner. Vi bruger kun de første to kolonner, som er kriminalitet og andel af befolkningen, der er lavindkomst.

```python
boston = datasets.load_boston()
X = boston.data[:, :2]
y = boston.target
```

Vi kan nu visualisere data. Vi bruger matplotlib til at lave et scatterplot.

```python
plt.scatter(X[:, 0], X[:, 1], c=y)
plt.xlabel('Kriminalitet')
plt.ylabel('Lavindkomst')
plt.show()
```

![scatterplot](https://raw.githubusercontent.com/henrist/intelligente-systemer/main/slides/scipy/scatterplot.png)

