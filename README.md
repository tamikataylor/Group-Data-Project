# Group Data Project 

Tamika Taylor,
Daniil Sagun,
Pierce Myers,
Nrusimha Ayyalasomayajula,
Isabella Ecklund

# Mushroom Toxicity

# Motivation
We decided to do our group project on mushroom toxicity. The reason being that some of us are avid cooks that enjoy cooking with different varieties of mushrooms and embrace the idea of being able to forage for them ourselves. Especially since they grow abundantly here in the PNW. To see if there were any correlations between a mushroom's toxicity and its characteristics, we looked at Heat Maps, Logistical Regression, and Cross Tabulation Maps. 

# Data
To obtain our data we used Kaggle. The data did not require any cleaning just some manipulation within the Juypter notebooks. The mushroom notebook contained 22 different characteristics. However, we decided to focus on three of them being: Odor, Spore Print Color, and the Cap Color. First, we looked at Heat Maps to determine the first impressions of the data and what had the highest correlations. Next, we attempted the Logistical Regression, however, due to the high number of variances in the characteristics typical logistical regression did not work. Instead, we looked at the cross-tabulation maps using the logistical regression to get a better visual between the character types and the edibility of the mushrooms.

# Heat Maps for Exploratory Analysis

![Correlation Between Mushroom Odor and Edibility](https://github.com/tamikataylor/Group-Data-Project/blob/main/HM%20Odor.png)

Key for Odor:
a - Almond,
l - Anise,
c - Creosote,
y - Fishy,
f - Foul,
m - Musty,
p - Pungent,
s - Spicy,
n - None

![Correlation Between Mushroom Spore Print Color and Edibility](https://github.com/tamikataylor/Group-Data-Project/blob/main/HM%20SPC.png)

Key for Spore Print Color:
k - Black,
n - Brown,
b - Buff,
h - Chocolate,
r - Green,
o - Orange, 
u - Purple,
w - White,
y - Yellow

![Correlation Between Mushroom Cap Color and Edibility](https://github.com/tamikataylor/Group-Data-Project/blob/main/HM%20CP.png)

Key for Cap Color: 
n - Brown,
b - Buff,
c - Cinnamon,
g - Gray,
r - Green,
p - Pink,
u - Purple,
e - Red,
w - White,
y - Yellow

In our exploratory analysis we used heat maps to look at the general correlations. Right of the bat for the spore print and odor you can see some strong correlations as well as ones that have zero correlation. The first one being for odor n (none), edible mushrooms are more likely to have no odor. For the spore print color h (chocolate) there is a good chance that it was more poisonous. However, for cap color there were no major correlations. 

# Logistical Regression with Cross Tabulation

Max(poison)-spore print color-r(green) 3.66 100% poison

Min(edible)-Odor-n(none) -4.18 96.6% edible

Best edible predictors:

Odor- a(almond) -2.96 100% edible

Odor- i(anise) -2.96 100% edible

Cross Tab Tabel of Odor 

![Odor vs. Toxicity](https://github.com/tamikataylor/Group-Data-Project/blob/main/Screen%20Shot%202020-12-16%20at%2010.41.18%20AM.png)

![Odor vs. Toxicity](https://github.com/tamikataylor/Group-Data-Project/blob/main/CT%20Odor.png)

Key for Odor:
a - Almond,
l - Anise,
c - Creosote,
y - Fishy,
f - Foul,
m - Musty,
p - Pungent,
s - Spicy,
n - None

![Spore Print Color vs. Toxicity](https://github.com/tamikataylor/Group-Data-Project/blob/main/CT%20SPC.png)

Key for Spore Print Color:
k - Black,
n - Brown,
b - Buff,
h - Chocolate,
r - Green,
o - Orange, 
u - Purple,
w - White,
y - Yellow

![Cap Color vs. Toxicity](https://github.com/tamikataylor/Group-Data-Project/blob/main/CT%20CC.png)

Key for Cap Color: 
n - Brown,
b - Buff,
c - Cinnamon,
g - Gray,
r - Green,
p - Pink,
u - Purple,
e - Red,
w - White,
y - Yellow

For our actual analysis of data, we looked at the Logistical Regression of the three characteristics. However, since there are so many different variables for each characteristic, traditional regression did not work. We weren’t looking at numbers but rather colors and smells so we needed a graph that could compare those simultaneously. So instead we used Cross Tabulation maps. These gave a us a much better picture of what the correlation was between edible and poisonous. First, we created cross tab tables using pandas and then plotted them. From that data we are able to see that there are no major correlations in the cap color, but the odor and spore print color have higher correlations. 

# Conclusion

From our data we were able to find some correlation between the odor, spore print color and class of mushroom. However, for the cap color, it appears that there is not much of a distinction between the colors of the mushroom and its toxicity. The only colors that were edible were green and purple. The rest of the colors were more even and had a tendency to be either or. For odor, if the mushroom smells like almonds or anise then they were edible and if there was none it was most likely edible, for all other scents they were poisonous. For the spore color print, there was greater variability. For the colors buff, orange, purple, and yellow those were edible. For green, those were poisonous. If the print color was brown or black it was most likely edible, chocolate was most likely poisonous and white had a greater proclivity for being poisonous rather than edible. 

# Source 
https://www.kaggle.com/uciml/mushroom-classification
