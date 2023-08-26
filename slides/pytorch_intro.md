# Introduktion til PyTorch
## Af Henrik Sterner

Pytorch er et bibliotek til maskinlæring, der er udviklet af Facebook. Det er et af de mest populære biblioteker til maskinlæring, og det er også et af de nyeste. Det er udviklet i Python, og det er derfor nemt at bruge i forbindelse med andre Python-biblioteker. Det er også nemt at bruge på GPU, hvilket gør det hurtigt at træne modeller.

Pytorch er baseret på NumPy, og det er derfor nemt at bruge NumPy-arrays i forbindelse med Pytorch. Det er også nemt at konvertere mellem NumPy-arrays og Pytorch-tensorer.

# Installation
Pytorch kan installeres med pip eller conda. Hvis du har en CUDA-kompatibel GPU, kan du installere en version af Pytorch, der er optimeret til GPU. Hvis du ikke har en CUDA-kompatibel GPU, kan du installere en version af Pytorch, der bruger CPU'en.

# Tensors
Tensors er en generalisering af vektorer og matricer. De kan have et vilkårligt antal dimensioner. En tensor med en dimension er en vektor, en tensor med to dimensioner er en matrix, og en tensor med tre dimensioner er en tredimensionel matrix. En tensor med fire dimensioner er en firdimensionel matrix, og så videre.  

Tensors kan repræsentere mange forskellige typer data. De kan repræsentere billeder, lyd, tekst, tal og meget andet. De kan også repræsentere modeller, der er trænet til at løse forskellige opgaver.

# Tensors i Pytorch
I Pytorch repræsenteres tensors af klassen `torch.Tensor`. Denne klasse har mange metoder, der kan bruges til at manipulere tensors. Den har også mange attributter, der kan bruges til at få information om en tensor.

# Oprettelse af tensors
Der er mange måder at oprette en tensor på. En tensor kan oprettes fra en liste, en NumPy-array, en anden tensor eller en række andre typer objekter. En tensor kan også oprettes med tilfældige værdier eller med nulværdier. En tensor kan også oprettes med en bestemt datatype, og den kan oprettes på GPU'en.

# Oprettelse af en tensor fra en liste
En tensor kan oprettes fra en liste med `torch.tensor`. Hvis listen indeholder tal, vil typen af tensor være `torch.float32`. Hvis listen indeholder heltal, vil typen af tensor være `torch.int64`.

```python
import torch

x = torch.tensor([1, 2, 3])
print(x)
print(x.dtype)
```
    
    ```
    tensor([1, 2, 3])
    torch.int64
    ```

# Oprettelse af en tensor fra en NumPy-array
En tensor kan oprettes fra en NumPy-array med `torch.from_numpy`. Hvis NumPy-arrayet indeholder tal, vil typen af tensor være `torch.float32`. Hvis NumPy-arrayet indeholder heltal, vil typen af tensor være `torch.int64`.

```python
import numpy as np
import torch

x = torch.from_numpy(np.array([1, 2, 3]))
print(x)
print(x.dtype)
```
    
    ```
    tensor([1, 2, 3])
    torch.int64
    ```

# Oprettelse af en tensor fra en anden tensor
En tensor kan oprettes fra en anden tensor med `torch.tensor`. Hvis den anden tensor indeholder tal, vil typen af den nye tensor være `torch.float32`. Hvis den anden tensor indeholder heltal, vil typen af den nye tensor være `torch.int64`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = torch.tensor(x)
print(y)
print(y.dtype)
```
    
    ```
    tensor([1, 2, 3])
    torch.int64
    ```

# Oprettelse af en tensor med tilfældige værdier
En tensor kan oprettes med tilfældige værdier med `torch.rand`. Hvis der ikke angives nogen argumenter, vil typen af tensor være `torch.float32`.

```python
import torch

x = torch.rand(2, 3)
print(x)
print(x.dtype)
```
    
    ```
    tensor([[0.8147, 0.0380, 0.4192],
            [0.5948, 0.9617, 0.7922]])
    torch.float32
    ```

# Oprettelse af en tensor med nulværdier
En tensor kan oprettes med nulværdier med `torch.zeros`. Hvis der ikke angives nogen argumenter, vil typen af tensor være `torch.float32`.

```python
import torch

x = torch.zeros(2, 3)
print(x)
print(x.dtype)
```
    
    ```
    tensor([[0., 0., 0.],
            [0., 0., 0.]])
    torch.float32
    ```

# Oprettelse af en tensor med en bestemt datatype
En tensor kan oprettes med en bestemt datatype med `torch.zeros`. Hvis der ikke angives nogen argumenter, vil typen af tensor være `torch.float32`.

```python
import torch

x = torch.zeros(2, 3, dtype=torch.int64)
print(x)
print(x.dtype)
```
    
    ```
    tensor([[0, 0, 0],
            [0, 0, 0]])
    torch.int64
    ```

# Oprettelse af en tensor på GPU'en
En tensor kan oprettes på GPU'en med `torch.zeros`. Hvis der ikke angives nogen argumenter, vil typen af tensor være `torch.float32`.

```python
import torch

x = torch.zeros(2, 3, device='cuda')
print(x)
print(x.device)
```
    
    ```
    tensor([[0., 0., 0.],
            [0., 0., 0.]], device='cuda:0')
    cuda:0
    ```

# Attributter
En tensor har mange attributter, der kan bruges til at få information om en tensor. Nogle af de mest brugte attributter er `dtype`, `device`, `shape` og `size`.

# Attributten `dtype`
Attributten `dtype` kan bruges til at få typen af en tensor. Typen af en tensor kan være `torch.float32`, `torch.int64` eller en anden type.

```python
import torch

x = torch.tensor([1, 2, 3])
print(x.dtype)
```
    
    ```
    torch.int64
    ```

# Attributten `device`
Attributten `device` kan bruges til at få enheden, som en tensor er placeret på. En tensor kan være placeret på CPU'en eller på GPU'en.

```python
import torch

x = torch.tensor([1, 2, 3])
print(x.device)
```
    
    ```
    cpu
    ```

# Attributten `shape`
Attributten `shape` kan bruges til at få størrelsen af en tensor. Størrelsen af en tensor er en tuple med størrelsen af hver dimension.

```python
import torch

x = torch.tensor([[1, 2, 3], [4, 5, 6]])
print(x.shape)
```
    
    ```
    torch.Size([2, 3])
    ```

# Attributten `size`
Attributten `size` kan bruges til at få størrelsen af en tensor. Størrelsen af en tensor er en tuple med størrelsen af hver dimension.

```python
import torch

x = torch.tensor([[1, 2, 3], [4, 5, 6]])
print(x.size())
```
    
    ```
    torch.Size([2, 3])
    ```

Der er ingen forskel på at bruge `shape` og `size`.

# Metoder
En tensor har mange metoder, der kan bruges til at manipulere en tensor. Nogle af de mest brugte metoder er `reshape`, `squeeze`, `unsqueeze`, `permute`, `transpose`, `view`, `item`, `tolist`, `numpy`, `to`, `cuda`, `cpu`, `float`, `double`, `long`, `half`, `int`, `short`, `char`, `byte`, `bool`, `abs`, `add`, `sub`, `mul`, `div`, `pow`, `exp`, `log`, `sqrt`, `sin`, `cos`, `tan`, `asin`, `acos`, `atan`, `sinh`, `cosh`, `tanh`, `asinh`, `acosh`, `atanh`, `sigmoid`, `relu`, `softmax`, `argmax`, `argmin`, `max`, `min`, `mean`, `sum`, `prod`, `norm`, `dot`, `t`

# Metoden `reshape`
Metoden `reshape` kan bruges til at ændre størrelsen af en tensor. Den nye størrelse skal være kompatibel med den gamle størrelse. Det vil sige, at antallet af elementer skal være det samme.

```python
import torch

x = torch.tensor([[1, 2, 3], [4, 5, 6]])
y = x.reshape(3, 2)
print(y)
```
    
    ```
    tensor([[1, 2],
            [3, 4],
            [5, 6]])
    ```

# Metoden `squeeze`
Metoden `squeeze` kan bruges til at fjerne dimensioner med størrelse 1 fra en tensor.

```python
import torch

x = torch.tensor([[[1, 2, 3]]])
y = x.squeeze()
print(y)
```
    
    ```
    tensor([1, 2, 3])
    ```

# Metoden `unsqueeze`
Metoden `unsqueeze` kan bruges til at tilføje dimensioner med størrelse 1 til en tensor.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.unsqueeze(0)
print(y)
```
    
    ```
    tensor([[1, 2, 3]])
    ```

# Metoden `permute`
Metoden `permute` kan bruges til at ændre rækkefølgen af dimensioner i en tensor.

```python
import torch

x = torch.tensor([[[1, 2, 3], [4, 5, 6]]])
y = x.permute(2, 0, 1)
print(y)
```
    
    ```
    tensor([[[1, 4]],
    
            [[2, 5]],
    
            [[3, 6]]])
    ```

# Metoden `transpose`
Metoden `transpose` kan bruges til at bytte rækkefølgen af to dimensioner i en tensor.

```python
import torch

x = torch.tensor([[[1, 2, 3], [4, 5, 6]]])

y = x.transpose(0, 1)
print(y)
```
    
    ```
    tensor([[[1, 2, 3]],
    
            [[4, 5, 6]]])
    ```

# Metoden `view`
Metoden `view` kan bruges til at ændre størrelsen af en tensor. Den nye størrelse skal være kompatibel med den gamle størrelse. Det vil sige, at antallet af elementer skal være det samme.

```python
import torch

x = torch.tensor([[1, 2, 3], [4, 5, 6]])
y = x.view(3, 2)
print(y)
```
    
    ```
    tensor([[1, 2],
            [3, 4],
            [5, 6]])
    ```

# Metoden `item`
Metoden `item` kan bruges til at få værdien af en tensor, der kun indeholder ét element.

```python
import torch

x = torch.tensor([1])
y = x.item()
print(y)
```
    
    ```
    1
    ```

# Metoden `tolist`
Metoden `tolist` kan bruges til at konvertere en tensor til en liste.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.tolist()
print(y)
```
    
    ```
    [1, 2, 3]
    ```

# Metoden `numpy`
Metoden `numpy` kan bruges til at konvertere en tensor til en NumPy-array.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.numpy()
print(y)
```
    
    ```
    [1 2 3]
    ```

# Metoden `to`
Metoden `to` kan bruges til at flytte en tensor til en anden enhed. En tensor kan flyttes til CPU'en eller til GPU'en.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.to('cuda')
print(y)
print(y.device)
```
    
    ```
    tensor([1, 2, 3], device='cuda:0')
    cuda:0
    ```

# Metoden `cuda`
Metoden `cuda` kan bruges til at flytte en tensor til GPU'en.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.cuda()
print(y)
print(y.device)
```
    
    ```
    tensor([1, 2, 3], device='cuda:0')
    cuda:0
    ```

# Metoden `cpu`
Metoden `cpu` kan bruges til at flytte en tensor til CPU'en.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.cuda()
z = y.cpu()
print(z)

print(z.device)
```
    
    ```
    tensor([1, 2, 3])
    cpu
    ```

# Metoden `float`
Metoden `float` kan bruges til at konvertere en tensor til typen `torch.float32`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.float()
print(y)
print(y.dtype)
```
    
    ```
    tensor([1., 2., 3.])
    torch.float32
    ```

# Metoden `double`
Metoden `double` kan bruges til at konvertere en tensor til typen `torch.float64`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.double()
print(y)
print(y.dtype)
```
    
    ```
    tensor([1., 2., 3.], dtype=torch.float64)
    torch.float64
    ```

# Metoden `long`
Metoden `long` kan bruges til at konvertere en tensor til typen `torch.int64`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.long()
print(y)
print(y.dtype)
```
    
    ```
    tensor([1, 2, 3])
    torch.int64
    ```

# Metoden `half`
Metoden `half` kan bruges til at konvertere en tensor til typen `torch.float16`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.half()
print(y)
print(y.dtype)
```
    
    ```
    tensor([1., 2., 3.], dtype=torch.float16)
    torch.float16
    ```

# Metoden `int`
Metoden `int` kan bruges til at konvertere en tensor til typen `torch.int32`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.int()
print(y)
print(y.dtype)
```
    
    ```
    tensor([1, 2, 3], dtype=torch.int32)
    torch.int32
    ```

# Metoden `short`
Metoden `short` kan bruges til at konvertere en tensor til typen `torch.int16`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.short()
print(y)

print(y.dtype)
```
    
    ```
    tensor([1, 2, 3], dtype=torch.int16)
    torch.int16
    ```

# Metoden `char`
Metoden `char` kan bruges til at konvertere en tensor til typen `torch.int8`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.char()
print(y)

print(y.dtype)
```
    
    ```
    tensor([1, 2, 3], dtype=torch.int8)
    torch.int8
    ```

# Metoden `byte`
Metoden `byte` kan bruges til at konvertere en tensor til typen `torch.uint8`.

```python
import torch

x = torch.tensor([1, 2, 3])
y = x.byte()

print(y)
print(y.dtype)
```
    
    ```
    tensor([1, 2, 3], dtype=torch.uint8)
    torch.uint8
    ```

