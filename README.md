# Titanic_dataset_cleaning
Cleaning and preprocessing Titanic Dataset
# I imported the data in Jupyter notebook as csv file.
# I used Python libraries like Numpy, Pandas, Skicit-learn(for plotting graphs and labelling in a neat manner), Matplotlib(for visualizing data),Seaborn.
# 1)Handle missing values using mean/median/imputation:
      # Using Pandas, the missing data from the dataset was found.
      # The missing data:
              # PassengerId      0
              # Survived         0
              # Pclass           0
              # Name             0
              # Sex              0
              # Age            177
              # SibSp            0
              # Parch            0
              # Ticket           0
              # Fare             0
              # Cabin          687
              # Embarked         2
              # dtype: int64
      - For **Age**, median was taken to avoid outliers and the filled the missing data with the median,
      - As **Embarked** is categorical data mode was found and replaced in the places where data was missing.
      - The "Cabin" data has huge missing values, it is safe and the results would be accurate if the colums is removed.
# 2)Convert categorical features into numerical using encoding.
      - Categorical data like "Embarked" was converted into numerical data by one-hot decoding.
      - "sex" was converted to 0/1 using label encoding technique.
# 3)Normalize/standardize the numerical features
      - StandardScaler() is imported from Skicit-learn and the columns like "Age" and "Fare" are normalized so that the values are in smale factor.
# 4)Visualize outliers using boxplots and remove them.
      - Using Seaborn and matplotlib library, the boxplots for age and fare are visualized. the points which do not lie in the box are called outliers and they are removed for the better accuracy of the model.
      - Q1(25% point) and Q3(75% point) are calculated 
      - IQR(InterQuartile Range) = Q3-Q1
      - the values between Q1 - 1.5*IQR and Q3 + 1.5*IQR should be considered and the points(outliers) out of this range should be removed.
### Now, the data is cleaned and preprocessed.
      

