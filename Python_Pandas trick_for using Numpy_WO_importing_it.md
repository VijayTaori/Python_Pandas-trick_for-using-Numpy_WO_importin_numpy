
# Tutorial to use numpy in pandas without importing numpy


```python
import pandas as pd
```


```python
my_list = [1, 'two', 3.0, pd.np.NaN]
my_list
```




    [1, 'two', 3.0, nan]




```python
my_list2 = [1, 'two', 3.0, pd.np.nan]
my_list2
```




    [1, 'two', 3.0, nan]




```python
titanic = pd.read_csv('titanic_train.csv')
# Find the null values in column 'Age'
```


```python
# Pandas way
pd.isnull(titanic['Age']).sum()
```




    177




```python
# Numpy way
pd.np.isnan(titanic['Age']).sum()
```




    177


