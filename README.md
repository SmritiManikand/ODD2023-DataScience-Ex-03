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


<img width="629" alt="s0" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/7515ae94-d46d-4fca-a9ec-5a2148035b69">


<img width="345" alt="s1" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/1ad94326-6f88-4e25-9c42-4dab684a42e1">


<img width="432" alt="s2" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/43225bbf-5a45-4015-bea2-59e9b986516b">


<img width="416" alt="s3" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/98aa9edb-60db-4ca8-bed0-b770104f3032">


<img width="408" alt="Screenshot 2023-10-07 205039" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/eb595e70-0ed1-4d09-9b8f-6dbfddd1b1ad">


<img width="615" alt="Screenshot 2023-10-07 205101" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/685c6efc-ac6f-4622-ac05-70a9c9a8ff87">


<img width="153" alt="Screenshot 2023-10-07 205126" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/a8874675-73eb-4018-993b-999a206e0ddb">


<img width="254" alt="Screenshot 2023-10-07 205139" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/f033cbe5-59bb-4271-87bf-47a4c66f7777">


<img width="384" alt="Screenshot 2023-10-07 205152" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/7cea6049-ac66-4c56-bf9b-6737627c8d47">


<img width="434" alt="Screenshot 2023-10-07 205206" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/15d52e3a-2876-4566-8e7d-ded0d426059b">


<img width="432" alt="Screenshot 2023-10-07 205220" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/335793e8-0ea2-409f-952b-d39d93ee25ba">


<img width="280" alt="Screenshot 2023-10-07 205235" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/25c0a608-8aba-41d1-99ac-a7d808142276">


<img width="333" alt="Screenshot 2023-10-07 205305" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/01395bf1-44f5-424b-98f0-14417b9eeb36">


<img width="265" alt="Screenshot 2023-10-07 205318" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/9ae9265d-d238-4c37-9f29-bdfda7664093">


<img width="375" alt="Screenshot 2023-10-07 205340" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/d6c70a0e-1f50-4ec2-a24a-2b9c9c9632ef">


<img width="416" alt="Screenshot 2023-10-07 205353" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/cf780321-772d-401b-8899-28de4fa45b08">


<img width="427" alt="Screenshot 2023-10-07 205405" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/8c86565a-dcf4-4182-92e2-a8f6ee459303">


<img width="421" alt="Screenshot 2023-10-07 205417" src="https://github.com/SmritiManikand/ODD2023-DataScience-Ex-03/assets/113674204/dd5c5e02-6bfe-4fc8-96a0-3a95a3400b8a">


## Result

Thus we have read the given data and performed the univariate analysis with different types of plots.
