# Fifa-2023-Research-Decision-Tree-Regression
Builded a Regression Model on a Dataset 'Fifa 2023 Research' which can be downloaded from the given link.
https://www.kaggle.com/datasets/babatundezenith/fifa-archive?select=Fifa_23_Players_Data.csv

Used Regressive Feature Elimination(RFE) feature selection method to get the features that are majorly correlated with the Label Feature i.e. Value(in Euro).
Engineered the Model to show the Relationship between Value(in Euro) and the Multiple Features using Decision Tree Regressor.

# Data
The Data contains 17529 records and 89 features that ultimately lead in deciding a Player's  Value(in Euro).
No NULL Values.
Dropped the irrelevant Features.
Data Cleaning has been referred by the a code available on Kaggle by EMIR T. and you can access it through the link.
https://www.kaggle.com/code/emirtatlc/fifa-23-players-eda-data-cleaning

# EDA

### CountPlot of Overall.

![CounPlot Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/b8d857ae-484f-4d7b-9984-7e0dc6a99b18)

Players with Overall Rating are Maximum in the range of 62-70 out of 100 being 47 as min and 91 as max...


   
### Distribution of Overall.

![DistPlot Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/378f2401-655c-4c6d-921a-c6e8ec81d67a)

The DistPlot shows the Distribution of Overall.

### Scatter Plot of Overall vs Value(in_Euro).

![Overall vs Value](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/e16e0706-c007-4fc3-99a2-cde4741e7abc)

Here's an exponential growth in Value(in Euro) of a Player as Overall i.e. Overall Rating of a player increases...

### Countplot of Number of Players from Each Country.

![Countries countplot](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/a0f1f85d-c1da-4cc0-ae01-c8bee5b5893a)

And says that England has most Players in Fifa 2k23 following by Germany and then Spain...
India has almost 200 players...

### Distribution of Age.

![Dist plot of Age](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/192aa8ba-5267-47f6-b67b-fa58f865da90)

Shows a idea of Distribution of Age where Age need not to show or follow Normal Distribution.

### Scatter Plot of Potential vs Overall.

![Potential vs Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/8dd9c749-8026-4b04-83a9-ff65d1f229a0)

As Overall increases Potential also increases...

### Scatter Plot of Best_Position vs Value(in_Euro).

![Best Position vs Value](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/c644ca48-f32d-4637-8229-36089a5f484c)

Suprisingly, ST viz. Stopper is actually the most Valued Position...

### Scatter Plot of Best_Position vs Overall.

![Best Position vs Overall](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/da80b268-9704-4d25-850a-c55145335703)

Again, All Positions are Rated in the range of 40-91 and only C.F viz. Center Forward Position is least Rated around more than 50...

### Correlation Plot.

![Corrplot](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/e09ceea0-bf5f-4b28-9ee0-39fc4d43b491)

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
![RegPlot](https://github.com/001-Shubham/Fifa-2023-Research-Decision-Tree-Regression/assets/135433418/067ca09c-567b-4f7f-8e2b-502be7e27dd1)

The RegPlot shows the distribution of y_pred vs y_test around the Regression Model Fit Line initially and then scattering as the values increases in a Pattern.

