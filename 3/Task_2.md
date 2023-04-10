```python
# В первом ящике находится 8 мячей, из которых 5 - белые. Во втором ящике - 12 мячей, из которых 5 белых. 
# Из первого ящика вытаскивают случайным образом два мяча, из второго - 4. 
# Какова вероятность того, что 3 мяча белые?
```


```python
import numpy as np
from math import factorial as fl

# сочетания
def combinations(n, k):
    return fl(n) / (fl(k) * fl(n - k))

```


```python
t1=combinations(8, 2)
t2=combinations(12, 4)
```


```python
# a)

a1=combinations(5, 2)
a2=combinations(5, 1)
b2=combinations(7, 3)
p1=a1/t1
p2=(a2*b2)/t2
pa=p1*p2
print("2 из 2х белые и 1 из 4х белый, P = ",pa)
```

    2 из 2 белые и 1 из 4 белый, P =  0.12626262626262627
    


```python
# b)

a1=combinations(5, 1)
b1=combinations(3, 1)
a2=combinations(5, 2)
b2=combinations(7, 2)
p1=(a1*b1)/t1
p2=(a2*b2)/t2
pb=p1*p2
print("1 из 2х белый и 2 из 4 белые, P = ",pb)
```

    1 из 2х белый и 2 из 4 белые, P =  0.22727272727272727
    


```python
# c)

a1=combinations(3, 2)
a2=combinations(5, 3)
b2=combinations(7, 1)
p1=a1/t1
p2=(a2*b2)/t2
pc=p1*p2
print("0 из 2х белые и 3 из 4х белые, P = ",pc)
```

    0 из 2х белые и 3 из 4х белые, P =  0.01515151515151515
    


```python
p=pa+pb+pc
print("Вероятность того, что 3 мяча белые P = ",p)
```

    Вероятность того, что 3 мяча белые P =  0.3686868686868687
    


```python

```
