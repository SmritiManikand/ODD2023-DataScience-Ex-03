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


<img width="518" alt="s1" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/1e1f9bec-94d7-4c18-b952-6c1604c585c0">


<img width="571" alt="s2" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/fc6c7152-5f4b-4c4f-9f4d-b298f3536a32">


<img width="175" alt="s3" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/53047eaf-1eae-45cd-a9cf-dc70508075f6">


<img width="301" alt="s4" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/7ea54d91-a412-4f26-99af-0ae656fb2fab">


<img width="370" alt="s5" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/60174195-14a7-4f01-ad10-6d4f6b93da02">


<img width="420" alt="s6" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/5bb3ede2-c910-4e78-bf27-717180c5f9d5">


<img width="420" alt="s7" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/ab03d98b-4e8e-4dcc-b4f1-358bae5b071c">


<img width="408" alt="s8" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/8722cf1e-3a64-452d-9fcb-45985fb08cad">


<img width="601" alt="s9" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/890c3466-b12c-4cbe-aab9-a3770661e0cd">


<img width="227" alt="s10" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/6085b7e4-964c-4600-a68d-3c60b70d9842">


<img width="134" alt="s11" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/cbc58548-7676-48e5-97e4-ac9ba82c05d7">


<img width="249" alt="s12" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/a21264a3-1602-41f1-b572-91bdddfaa769">


<img width="371" alt="s13" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/416ebbef-adbd-4f81-bce5-ac1a63201eb8">


<img width="429" alt="s14" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/a6d0cd96-f705-49fd-a2f1-7b16b8eb6bec">


<img width="424" alt="s15" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/9bf84963-5954-4a1c-813d-3615dc64b9bb">


<img width="258" alt="s16" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/00d74167-784b-4f60-b6a0-480e511c9ca2">


<img width="148" alt="s17" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/fb858e1a-cb00-471c-9509-4874d880f5a3">


<img width="331" alt="s18" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/6529252b-9256-472a-9fa5-171ef018f4d0">


<img width="283" alt="s19" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/9270c9ca-adf5-4352-b66a-b8442f22e735">


<img width="383" alt="s20" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/ae2ee04d-ef8b-4c7c-8a49-d2516101aed6">


<img width="401" alt="s21" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/14264410-5fef-41da-a9f0-f2e498297755">


<img width="414" alt="s22" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/29b0177c-9f89-4ad7-806e-3ff2e6bf522f">


<img width="406" alt="s23" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/3a206dfb-0c07-4e25-9dfb-8754ab063c2c">


## Result

Thus we have read the given data and performed the univariate analysis with different types of plots.
