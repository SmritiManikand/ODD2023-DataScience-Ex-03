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

## Diabetes Dataset

## head
<img width="533" alt="s1" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/31334f3f-bd76-475e-8cdc-a42a32083ced">

## describe
<img width="576" alt="s2" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/4bb1c854-1407-4105-b167-2295c1a7a09c">

## isnull.sum
<img width="188" alt="s3" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/9ebd94a5-62c1-43c7-a4eb-cd923aecc27c">

## info
<img width="314" alt="s4" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/b5fc0f02-fc7f-4dba-b6f6-db9d25357d0a">

## box plot
<img width="386" alt="s5" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/0a16f906-3869-4609-ab86-32c63bd4f8dd">

## count plot
<img width="414" alt="s6" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/595d8f14-414e-4a90-83c6-13a2f326f5d5">

## distplot
<img width="413" alt="s7" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/d67d3a7b-e871-4867-b94c-dbb3890089e7">

## histplot
<img width="422" alt="s8" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/919e58d7-b05c-43a9-87fc-babe34e5e33a">

## SuperStore Dataset

## head
<img width="606" alt="s9" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/ed2e97af-67a4-475d-8eb3-f36ecac03eb3">

## describe
<img width="247" alt="s10" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/8b51db60-8877-4bd5-a73c-5361205b97df">

## isnull.sum
<img width="133" alt="s11" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/4a4d018f-5b29-42a4-890b-cf6418826ce0">

## info
<img width="273" alt="s12" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/ededc383-c677-4489-bd54-a93ab8e0b054">

## box plot
<img width="382" alt="s13" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/a126e036-ae49-47aa-849b-aa5049fbd62e">

## count plot
<img width="427" alt="s14" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/61a3dbb0-5fe7-4fb2-92bd-e1700100729e">

## distplot
<img width="418" alt="s15" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/365d8b0e-638d-4880-922d-42a82456097a">

## Employee_sal Dataset

## head
<img width="257" alt="s16" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/db895ae7-33b1-4584-8798-ecf546c48034">

## isnull.sum
<img width="155" alt="s17" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/76f0a291-d1c9-4da5-97a2-fe3212d2b0e4">

## describe
<img width="344" alt="s18" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/e450d596-b769-44fd-8915-92f39af7a116">

## info
<img width="260" alt="s19" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/81125fdb-49eb-4d9a-a9e4-1de34f3416d3">

## box plot
<img width="383" alt="s20" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/d3621a00-dd3f-4d8b-8b68-c0c27205f6fc">

## count plot
<img width="392" alt="s21" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/c063d9c0-7e88-4a17-b72c-d5aefc62628d">

## distplot
<img width="420" alt="s22" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/acc1ec10-3877-4151-84bb-83dfb8bbca3b">

## histplot
<img width="410" alt="s23" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/e23b8f17-2b67-47d5-a713-bee2f4120195">

## Result

Thus we have read the given data and performed the univariate analysis with different types of plots.
