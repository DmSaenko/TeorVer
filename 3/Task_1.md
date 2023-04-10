```python
#1. Даны значения зарплат из выборки выпускников: 100, 80, 75, 77, 89, 33, 45, 25, 65, 17, 30, 24, 57, 55, 70, 75, 65, 84, 90, 150. 
#   Посчитать (желательно без использования статистических методов наподобие std, var, mean) 
#   среднее арифметическое, среднее квадратичное отклонение, 
#   смещенную и несмещенную оценки дисперсий для данной выборки.
    
    
```


```python
import numpy as np
import pandas as pd
from math import factorial as fl

def combinations(k, n):
    return fl(n) / (fl(k) * fl(n - k))

salaries = np.array([100, 80, 75, 77, 89, 33, 45, 25, 65, 17, 30, 24, 57, 55, 70, 75, 65, 84, 90, 150])

```


```python
salaries_mean = salaries.sum() / salaries.size  
```


```python
# Среднее арифметическое:

np.mean(salaries)
    
```




    65.3




```python
# Cреднее квадратичное отклонение
(np.sum((salaries - salaries_mean)**2) / salaries.size)**0.5

```




    30.823854398825596




```python
# Cмещенная дисперсия
np.sum((salaries - salaries_mean)**2) / salaries.size

```




    950.11




```python
# Несмещенная дисперсия
np.sum((salaries - salaries_mean)**2) / (salaries.size - 1)

```




    1000.1157894736842




```python

```


```python

```


```python

```
