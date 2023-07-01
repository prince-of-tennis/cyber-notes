## basic 
### importing
```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import os
from sklearn.model_selection import train_test_split
from sklearn import linear_model
from sklearn.metrics import accuracy_score, confusion_matrix
from google.colab import drive
drive.mount('/content/drive')
#uploaded = files.upload()
filepath = '/content/drive/My Drive/Tai-Yu Chen'
os.chdir(filepath)
```

### prelim info
```python
print(data.shape)
data.describe()
```

## visualizing data/plotting
### histogram
```python
import matplotlib.pyplot as plt
plt.figure(figsize=(10,6))
plt.hist(medical_data['bmi'], edgecolor = 'black')
plt.xlabel('bmi')
plt.show()
```
### box plot (1 attribute)
```python
plt.figure(figsize=(15,4))
sns.boxplot(x=medical_data['bmi'])
```
### scatter plot (2 attributes)
```python
plt.figure(figsize=(12,10))
sns.scatterplot(medical_data['bmi'], medical_data['charges'], hue=medical_data['sex'])
plt.show()
```

### pie charts
```python
categories = data.groupby(by='category',as_index=False).agg({'unique_col':'count'})
plt.pie(x=categories['unique_col'], labels=categories['category']);
```
## creating models

