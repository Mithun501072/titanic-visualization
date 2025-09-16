# Titanic Dataset Visualization

# Install & Import Libraries
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd

# Load the Titanic dataset (from Seaborn)
df = sns.load_dataset("titanic")
df.head()

# Survival rate by Passenger Class (Bar Plot)
sns.barplot(x="pclass", y="survived", data=df)
plt.title("Survival Rate by Passenger Class")
plt.savefig("survival_by_pclass.png")
plt.show()

# Age Distribution by Class (Box Plot)
sns.boxplot(x="pclass", y="age", data=df)
plt.title("Age Distribution by Class")
plt.savefig("age_boxplot_by_pclass.png")
plt.show()

# Fare Distribution by Class (Violin Plot)
sns.violinplot(x="pclass", y="fare", data=df)
plt.title("Fare Distribution by Class")
plt.savefig("fare_violin_by_pclass.png")
plt.show()

# Age Density by Survival (KDE Plot)
sns.kdeplot(data=df, x="age", hue="survived", fill=True)
plt.title("Age Density by Survival")
plt.savefig("age_kde_by_survival.png")
plt.show()

# Scatter Plot (Swarm-like) - Age vs Fare
sns.scatterplot(data=df, x="age", y="fare", hue="survived", alpha=0.6)
plt.title("Age vs Fare Scatter Plot")
plt.savefig("age_vs_fare_scatter.png")
plt.show()

import seaborn as sns
import pandas as pd

# Load Titanic dataset directly from seaborn
df = sns.load_dataset("titanic")

# Save it as CSV so you can download
df.to_csv("titanic_seaborn.csv", index=False)

Bar Plot – Shows survival rate for each passenger class (1st, 2nd, 3rd).
People in 1st class had higher chances of survival.

Box Plot – Shows the spread of passenger ages in each class.
Higher classes had older passengers on average.

Violin Plot – Shows how fares (ticket prices) are distributed in each class.
1st class tickets were much more expensive than others.

KDE Plot – Smooth curve showing age distribution for survivors vs non-survivors.
Many young children had better survival chances.

Scatter Plot (swarm-like) – Age vs Fare with small random spread.
Younger passengers bought cheaper tickets, but some older passengers paid very high fares.

# Observations
From the above, we can say:
1st class passengers had better survival rates.
Younger kids survived more often than adults.
Ticket price was strongly linked with survival (richer passengers had higher chances).














