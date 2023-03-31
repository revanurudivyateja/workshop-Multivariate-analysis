import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib.pyplot as plt

import io

from google.colab import files

uploaded = files.upload()

dd = pd.read_csv(io.BytesIO(uploaded['FlightInformation.csv']))

print(dd)
Types of Bivariate Analysis:
(i) Numerical & Numerical

sns.scatterplot (dd['Date_of_Journey'],dd['Dep_Time'])

1
(ii) Numerical & Categorical

sns.barplot (x=dd['Duration'],y=dd['Price'])

2

sns.barplot(x=dd["Arrival_Time"],y=dd["Price"],data=dd)

3

states=dd.loc[:,["Duration","Price"]]

states=states.groupby(by=["Duration"]).sum().sort_values(by="Price")

sns.barplot(x=states.index,y="Price",data=states)

plt.xticks(rotation = 90)

plt.xlabel=("Duration")

plt.ylabel=("Price")

plt.show()

4
Multivariate Analysis

dd.corr()

data = np.random.randint(low = 1, high = 100, size = (10, 10))

print("The data to be plotted:\n")

print(data)

hm = sns.heatmap(data = data)

plt.show()

5
RESULT:

Thus, Bivariate/Multivariate Analysis is performed successfully.
