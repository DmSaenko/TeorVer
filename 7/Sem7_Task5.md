```python
Задача 5. Заявляется, что партия изготавливается со средним арифметическим 2,5 см. Проверить
данную гипотезу, если известно, что размеры изделий подчинены нормальному закону
распределения. Объем выборки 10, уровень статистической значимости 5%
2.51, 2.35, 2.74, 2.56, 2.40, 2.36, 2.65, 2.7, 2.67, 2.34
```


```python
import numpy as np
import scipy.stats as stats
```


```python
X = np.array([2.51, 2.35, 2.74, 2.56, 2.40, 2.36, 2.65, 2.7, 2.67, 2.34])

mean = X.mean()
std = X.std(ddof=1)

t_fact = (mean - 2.5) / std * np.sqrt(len(X))
t_fact
```




    0.563061366180296




```python
По таблице для критерия Стьюдента находим t = 1.833 (для = 0.05 и 9 степенями свободы).
Так как t > t_fact (1.833 > 0.56), то гипотеза верна и изделия соответствуют заявленному размеру.
```


```python
n = 10
m = 2.5

t = stats.t.ppf(0.975, 9)
print(f"t теор = {t:.2f}")

t = (mean - m) * np.sqrt(n) / std
print(f"t рассч = {t:.3f}")

```

    t теор = 2.26
    t рассч = 0.563
    


```python
так как t теор > t рассч, считаем что нулевая гипотеза верна
```


```python

```
