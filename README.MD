# Aggregates multiple columns of a DataFrame

```python
pip install a-pandas-ex-mindex-aggregate
```

```python

from a_pandas_ex_mindex_aggregate import pd_add_mindex_aggregate
import pandas as pd
pd_add_mindex_aggregate()
df = pd.read_csv("https://github.com/pandas-dev/pandas/raw/main/doc/data/titanic.csv")

     PassengerId  Survived  Pclass  ...     Fare Cabin  Embarked
0              1         0       3  ...   7.2500   NaN         S
1              2         1       1  ...  71.2833   C85         C
2              3         1       3  ...   7.9250   NaN         S
3              4         1       1  ...  53.1000  C123         S
4              5         0       3  ...   8.0500   NaN         S
..           ...       ...     ...  ...      ...   ...       ...
886          887         0       2  ...  13.0000   NaN         S
887          888         1       1  ...  30.0000   B42         S
888          889         0       3  ...  23.4500   NaN         S
889          890         1       1  ...  30.0000  C148         C
890          891         0       3  ...   7.7500   NaN         Q
[891 rows x 12 columns]


df.d_multiindex_aggregate(['Fare', 'Age'])

              PassengerId Survived  ...          Cabin Embarked
Fare     Age                        ...                        
0.0000   19.0       [303]      [0]  ...          [nan]      [S]
         25.0       [272]      [1]  ...          [nan]      [S]
         36.0       [180]      [0]  ...          [nan]      [S]
         38.0       [823]      [0]  ...          [nan]      [S]
         39.0       [807]      [0]  ...          [A36]      [S]
                   ...      ...  ...            ...      ...
263.0000 23.0        [89]      [1]  ...  [C23 C25 C27]      [S]
         24.0       [342]      [1]  ...  [C23 C25 C27]      [S]
         64.0       [439]      [0]  ...  [C23 C25 C27]      [S]
512.3292 35.0  [259, 738]   [1, 1]  ...    [nan, B101]   [C, C]
         36.0       [680]      [1]  ...  [B51 B53 B55]      [C]
[815 rows x 10 columns]

```
