# Monday, 6/23/25

## Part 2: Plotting

Dataset used in class examples:`taxis.csv`, https://drive.google.com/file/d/1yzcou-mgYXhanO_gP69TZyEC_2S5sm0f/view?usp=sharing

Code from class:

```
import seaborn as sns

# create a histogram for fare
sns.displot(data = taxis, x = "fare")
plt.show()

# create a bar plot for pickup_borough
sns.displot(data = taxis, x = "pickup_borough")
plt.show()

import seaborn as sns
import matplotlib.pyplot as plt

# Create a histogram of the "total_bill" variable
sns.displot(data=tips, x="total_bill")
plt.show()

# Create a histogram of the "total_bill" variable colored by "smoker" and faceted by "time"
sns.displot(data=tips, x="total_bill",hue = "smoker", col="time", kind = "hist")
plt.show()

sns.displot(data=tips, x = "tip", hue="time", kind="kde")
plt.show()

# Create a scatterplot of "total_bill" vs "tip"
sns.relplot(
    data=tips,
    x="total_bill", y="tip"
)
plt.show()

# Create a scatterplot of "total_bill" vs "tip" colored by "smoker", faceted by "time", with marker style determined by "smoker" and size of the marker determined by "size"
sns.relplot(
    data=tips,
    x="total_bill", y="tip", col="time",
    hue="smoker", style="smoker", size="size"
)
plt.show()

sns.relplot(
    data=penguins,
    x="bill_length_mm", y="bill_depth_mm", col="sex",
    hue="species", style="island", size="body_mass_g"
)
plt.show()

# Create a barplot of "day" by "total_bill" colored by "smoker"
sns.catplot(data=tips, kind="bar", x="day", y="total_bill", hue="smoker")
plt.show()

sns.catplot(data = penguins, x = "species", y = "body_mass_g", kind = "box", hue="sex")
plt.show()
```

Documentation for functions:
* `displot`: https://seaborn.pydata.org/generated/seaborn.displot.html
* `relplot`: https://seaborn.pydata.org/generated/seaborn.relplot.html
* `catplot`: https://seaborn.pydata.org/generated/seaborn.catplot.html

Do the following with the survey data:

1. Create a plot for each of the variables in the survey dataset.
1. There are many different kinds of plots you can make with the `displot()` function. What happens when you use an x and y variable? 
1. Test out other displot options based on this document: https://seaborn.pydata.org/tutorial/distributions.html 
1. Try creating a scatterplot based on two different variables.
1. Try making different kinds of plots (changing colors, changing variables, etc)
1. Which plot do you find most interesting?

