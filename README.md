# Ex:03 Univariate Analysis

## Aim

To read the given data and perform the univariate analysis with different types of plots.

## Explanation

Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

## Algorithm

Step 1:
Read the given data.

Step 2:
Get the information about the data.

Step 3:
Remove the null values from the data.

Step 4:
Mention the datatypes from the data.

Step 5:
Count the values from the data.

Step 6:
Do plots like boxplots,countplot,distribution plot,histogram plot.

## Code

```
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('diabetes.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x="Glucose",data=df)
Glucose_q1 = df['Glucose'].quantile(0.25)
Glucose_q3 = df['Glucose'].quantile(0.75)
Glucose_IQR = Glucose_q3 - Glucose_q1
Glucose_low = Glucose_q1 - 1.5 * Glucose_IQR
Glucose_high = Glucose_q3 + 1.5 * Glucose_IQR
df=df[((df['Glucose']>=Glucose_low)&(df['Glucose']<=Glucose_high))]
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)

import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('SuperStore.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
df['Postal Code']=df['Postal Code'].fillna(method='ffill')
sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x="Postal Code",data=df)

import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('employeesal.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x='Experience_Years',data=df)
sns.countplot(x="Experience_Years",data=df)
sns.distplot(df['Experience_Years'])
sns.histplot(x="Experience_Years",data=df)

```
## Output


<img width="518" alt="s1" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/c726f2fe-4e74-42a3-9c71-1bbeabd0573a">

<img width="571" alt="s2" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/5306af07-ad67-4747-92fb-3ad9ef3c4ad1">

<img width="175" alt="s3" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/52081a32-816f-441a-993f-05c9a6d5387f">

<img width="301" alt="s4" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/031a494c-b501-4fc7-b989-c62e9158fb1f">

<img width="370" alt="s5" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/5d44f454-f617-430f-8c21-037038713b3d">

<img width="420" alt="s6" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/81eee264-fd5f-4806-b232-ca9f14ccf852">

<img width="420" alt="s7" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/0dd40d13-747b-4711-9589-5d56ad3cefed">

<img width="408" alt="s8" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/3c72a7a7-4bc0-439b-bbf2-40cc47318aec">

<img width="601" alt="s9" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/cbe412fc-be38-4ff3-b8ad-2542f9f025e1">

<img width="227" alt="s10" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/56b4ed00-2c24-4c24-9dd9-8a25936a2158">

<img width="134" alt="s11" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/aa56d361-077e-4c00-b819-83f2d4e5ce61">

<img width="249" alt="s12" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/f396262c-78d2-4076-8014-a188f476907a">

<img width="371" alt="s13" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/0d66dfbe-838a-4abe-8124-ee1c8466de0b">

<img width="429" alt="s14" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/33ef97d1-bb12-455e-81c3-c1b9465b9b6b">

<img width="424" alt="s15" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/5d879cdc-d4ec-4d0c-a3fc-b2c5c9836fa2">

<img width="258" alt="s16" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/0510b405-cb39-4a34-a6d2-00aaabf2c954">

<img width="148" alt="s17" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/632e35a3-4216-4003-b9a4-2b76a41efe22">

<img width="331" alt="s18" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/69116c46-038e-49e8-ae60-9da4625e8249">

<img width="283" alt="s19" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/002ee24a-a320-497e-a03a-6de556928b67">

<img width="383" alt="s20" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/1293afb9-a6b4-45f1-a0da-7abf2bb807c5">

<img width="401" alt="s21" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/1affb1ad-833f-4dab-a9c6-e3e6b84044c9">

<img width="414" alt="s22" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/eb2d5ebd-c432-47e8-9673-2d826a592864">

<img width="406" alt="s23" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/54312d5b-1845-4ca8-a356-9a2ec05478c7">

## Result

Thus we have read the given data and performed the univariate analysis with different types of plots.
