# 🚢 Titanic Dataset Project: Predicting Passenger Survival

## 📝 Introduction  
The Titanic dataset is well-known in data science and machine learning competitions. This project aims to predict the survival of passengers aboard the Titanic based on features such as age, gender, passenger class, and more. This project follows a systematic data exploration, preprocessing, modeling, and evaluation approach.

---

## ⚙️ Methodology  

### Step 1: 🔍 Data Exploration and Preprocessing  
1. **Loading the Data**:  
   - Loaded the training (`train.csv`) and test (`test.csv`) datasets into Pandas DataFrames:  
     ```python
     train_data = pd.read_csv('/content/drive/My Drive/titanic/train.csv') 
     test_data = pd.read_csv('/content/drive/My Drive/titanic/test.csv')
     ```  

2. **Understanding the Data**:  
   - Used `.info()`, `.describe()`, and `.isnull().sum()` to explore data types, distributions, and missing values.  

3. **Handling Missing Values**:  
   - Filled missing values in the `Age` column with the median age.  
   - Filled missing values in the `Embarked` column with the mode.  
   - Filled missing values in the `Fare` column with the median fare.  

4. **Feature Engineering**:  
   - Created a new feature `FamilySize` by combining `SibSp` (siblings/spouses) and `Parch` (parents/children).  

5. **Converting Categorical Variables**:  
   - Converted categorical variables (`Sex`, `Embarked`) into numerical formats using one-hot encoding and mapping.  

---

### Step 2: 📊 Data Visualization  
1. **Age Distribution**:  
   - Plotted a histogram to visualize the age distribution of passengers.  

2. **Survival Rates by Gender**:  
   - Used a count plot to visualize survival counts based on gender.  

3. **Survival Rates by Passenger Class**:  
   - Visualized survival counts by passenger class using a count plot.  

4. **Age vs. Gender vs. Survival**:  
   - Created a violin plot to analyze how age interacts with gender and survival status.  

5. **Correlation Heatmap**:  
   - Generated a heatmap to understand correlations between numerical features.  

---

### Step 3: 🤖 Model Selection  
1. **Preparing Data for Modeling**:  
   - Separated features (`X`) from the target variable (`y`) and split the data into training and validation sets (80% train, 20% validation).  

2. **Training Models**:  
   - Trained three models:  
     - Logistic Regression  
     - Decision Tree Classifier  
     - Random Forest Classifier  
   - Evaluated each model using accuracy scores and classification reports.  

---

### Step 4: 🔧 Hyperparameter Tuning  
1. **Grid Search for Random Forest**:  
   - Defined a parameter grid for Random Forest hyperparameters.  
   - Used `GridSearchCV` to find the best parameters through cross-validation.  

2. **Grid Search for Decision Tree**:  
   - Similarly tuned hyperparameters for the Decision Tree model.  

3. **Evaluating Best Models**:  
   - Evaluated the best-performing models on the validation set using accuracy scores.  

---

### Step 5: ✅ Final Model Evaluation  
1. **Preparing Test Data**:  
   - Preprocessed the test dataset similarly to the training dataset (handling missing values, feature engineering).  

2. **Making Predictions**:  
   - Used the best Random Forest model to predict survival outcomes on the test dataset.  

---

## 🏆 Results  
- Models were evaluated based on accuracy scores obtained from validation data.  
- The best-performing model was identified through hyperparameter tuning using Grid Search.  

---

## 📖 Conclusion  
This project provided valuable insights into:  
- Data preprocessing  
- Exploratory data analysis  
- Model selection  
- Hyperparameter tuning  
- Final evaluation using machine learning techniques  

The systematic approach not only improved understanding of machine learning workflows but also highlighted the importance of data visualization in uncovering patterns that inform modeling decisions.  

---
