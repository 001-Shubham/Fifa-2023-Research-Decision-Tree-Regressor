# Fifa-2023-Research-Decision-Tree-Regression
Builded a Regression Model on a Dataset 'Fifa 2023 Research' which can be downloaded from the given link.
https://www.kaggle.com/datasets/babatundezenith/fifa-archive?select=Fifa_23_Players_Data.csv

Used Recurssive Feature Elimination(RFE) feature selection method to get the features that are majorly correlated with the Label Feature i.e. Value(in Euro).

Engineered the Model to show the Relationship between Value(in Euro) and the Multiple Features using Decision Tree Regressor.

# Data
1. The Data contains 17529 records and 89 features that ultimately lead in deciding a Player's  Value(in Euro).
2. No NULL Values.
3. Dropped the irrelevant Features.
4. Data Cleaning has been referred by the a code available on Kaggle by EMIR T. and you can access it through the link.
https://www.kaggle.com/code/emirtatlc/fifa-23-players-eda-data-cleaning

# EDA

### CountPlot of Overall.

![CountPlot Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/3a13998d-a6fd-44a9-ae59-b181bec46ae9)

Players with Overall Rating are Maximum in the range of 62-70 out of 100 being 47 as min and 91 as max...!
   
### Distribution of Overall.

![DistPlot Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/62f84779-b768-458e-b4e7-85c04f88f9d5)

The DistPlot shows the Distribution of Overall.

### Scatter Plot of Overall vs Value(in_Euro).

![Overall vs Value](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/5fa3d40f-0e82-4670-8aeb-87db5f58cf68)

Here's an exponential growth in Value(in Euro) of a Player as Overall i.e. Overall Rating of a player increases...

### Countplot of Number of Players from Each Country.

![Countries countplot](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/63ce6bd5-b6c9-4f34-98a5-452f159c15f4)

And says that England has most Players in Fifa 2k23 following by Germany and then Spain...
India has almost 200 players...

### Distribution of Age.

![Dist plot of Age](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/adf0a00b-7287-4830-8bc3-75c7ae5358b5)

Shows a idea of Distribution of Age where Age need not to show or follow Normal Distribution.

### Scatter Plot of Potential vs Overall.

![Potential vs Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/0e189c7c-23c1-49ec-8eb1-f4b78b1e8c80)

As Overall increases Potential also increases...

### Scatter Plot of Best_Position vs Value(in_Euro).

![Best Position vs Value](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/09b7ef2b-a342-493d-b362-e193025d8db7)

Suprisingly, ST viz. Stopper is actually the most Valued Position...

### Scatter Plot of Best_Position vs Overall.

![Best Position vs Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/84075713-1385-4f63-b14f-09304007b849)

Again, All Positions are Rated in the range of 40-91 and only C.F viz. Center Forward Position is least Rated around more than 50...

### Correlation Plot.

![Corrplot](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/79cee62f-a031-4d55-841a-f1ccc3ce2e8d)

Wage(in_Euro), Overall and Potential have the major Corelation with Value(in_Euro)...

# Model Building
Builded 2 models using Decision Tree Regressor keeping n_features_to_select as 6 and changing max_depth: This determines the maximum depth of the tree.
1. max_depth = 8 we get r2score of testing data = 0.9649860643071263 and of training data  = 0.9886439514028638
2. max_depth = 6 we get r2score of testing data = 0.9665456486322586 and of training data = 0.9703911779702108

# Conclusion
1. There is no significant difference between the training as well as testing accuracy which shows that there is no sign of Overfitting or Underfitting...
2. Even after changing depth of the Decision Tree we get the r2score almost same.
3. Value(in_Euro) is majorly correlated with Overall, Potential, Age, Height, Weight and Wage(in_Euro).
4. On_Loan can be 1 of the features to affect in change in Value(in_Euro) of a Player but with the least concern and given a Real Time Situation.

# Lastly
![RegPlot](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regressor/assets/135433418/aca09471-e0a0-484e-a7c7-3984ae12cc0b)

The RegPlot shows the distribution of y_pred vs y_test around the Regression Model Fit Line initially and then scattering as the values increases in a Pattern.

