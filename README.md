We use fetch_california_housing() from sklearn.datasets, which retrieves a dataset containing information about housing prices in California. The dataset includes features like:

MedInc: Median income in block
HouseAge: Median house age in block
AveRooms: Average number of rooms per household
AveBedrms: Average number of bedrooms per household
Population: Block population
AveOccup: Average household occupancy
Latitude: Block latitude
Longitude: Block longitude
The target variable (MedHouseVal) represents the median house value.

To handle data more easily, we convert the dataset into a pandas.DataFrame

The California Housing dataset does not have missing values.
We separate the independent variables (X) from the dependent variable (y)
We split our dataset into training and testing sets using train_test_split()
Machine learning models work better when features are on a similar scale. Since our dataset has variables like income (MedInc) in thousands and latitude in single digits, we standardize features using StandardScaler
We implement five different regression models and explain why each might work well
 Linear Regression (from sklearn.linear_model import LinearRegression)
📌 Used for: Predicting house prices using a linear relationship.

LinearRegression().fit(X_train, y_train) – Trains the model.
.predict(X_test) – Makes predictions.
🔹 Decision Tree Regressor (from sklearn.tree import DecisionTreeRegressor)
📌 Used for: Making non-linear predictions using a decision tree structure.

DecisionTreeRegressor().fit(X_train, y_train)
🔹 Random Forest Regressor (from sklearn.ensemble import RandomForestRegressor)
📌 Used for: Improving predictions using multiple decision trees (ensemble learning).

RandomForestRegressor(n_estimators=100).fit(X_train, y_train)
🔹 Gradient Boosting Regressor (from sklearn.ensemble import GradientBoostingRegressor)
📌 Used for: Boosting model accuracy by sequentially improving weak learners.

GradientBoostingRegressor().fit(X_train, y_train)
🔹 Support Vector Regressor (SVR) (from sklearn.svm import SVR)
📌 Used for: Predicting house prices using a hyperplane in higher-dimensional space.

SVR(kernel='rbf').fit(X_train, y_train)
