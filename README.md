import pandas as pd

import numpy as np

import seaborn as sns

import matplotlib.pyplot as plt

import io

from google.colab import files

uploaded = files.upload()

dd = pd.read_csv(io.BytesIO(uploaded['FlightInformation.csv']))

print(dd)
https://github.com/sadulla018/workshop-Multivariate-analysis/blob/main/README.md#types-of-bivariate-analysis
