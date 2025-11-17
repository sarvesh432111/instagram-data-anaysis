import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

df = pd.read_csv("instagram.csv")
df.columns = df.columns.str.lower().str.replace(" ", "_")

sns.histplot(df["followers"], bins=20)
plt.show()

sns.scatterplot(x=df["followers"], y=df["likes"])
plt.show()

sns.barplot(x=df["username"], y=df["posts"])
plt.xticks(rotation=90)
plt.show()
