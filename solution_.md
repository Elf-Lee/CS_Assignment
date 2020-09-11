# Solution 

From MeifangLi-13043390

- MCC Van Dyke et al., 2019
- JT Harvey, Applied Ergonomics, 2002
- DW Ziegler et al., 2005


```python
import numpy as np
import pandas as pd
from matplotlib import pyplot as plt

%matplotlib inline
```


```python
df = pd.read_csv('https://raw.githubusercontent.com/Elf-Lee/CS_Assignment/master/istherecorrelation.csv', sep=';')
```


```python
df.columns = ['Year', 'WO[x1000]', 'NL Beer consumption [x1000 hectoliter]']
```


```python
fig, axs = plt.subplots(1, 2, constrained_layout=True, dpi=300)
axs[0].plot(df['Year'], df['WO[x1000]'], color= "blue")
axs[0].set_title('subplot 1')
axs[0].set_xlabel('Year')
axs[0].set_ylabel('WO[x1000]')
fig.suptitle('IS THERE CORRELATION', fontsize=16)

axs[1].plot(df['Year'], df['NL Beer consumption [x1000 hectoliter]'], color="red")
axs[1].set_xlabel('Year')
axs[1].set_title('sublpot 2')
axs[1].set_ylabel('NL Beer consumption [x1000 hectoliter]')

plt.show()
```


![png](output_5_0.png)

