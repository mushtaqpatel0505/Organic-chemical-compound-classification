# Organic-chemical-compound-classification

Data Source: https://drive.google.com/file/d/1pZhzZnaPi74aKCQImSPrzrTxWzVeE0qv/view?usp=sharing

The dataset is available in .csv forms

### Data Information
The given dataset contains details about organic chemical compounds including their chemical features, isomeric conformation,  names and the classes in which they are classified. The compounds are classified as either ‘Musk’ or ‘Non-Musk’ compounds. 

 Number of records : 6598
 
 Number of Attributes/Columns in data: 170

### Attribute Information:

1. ID               : unique id
2. molecule_name    : name of the molecule
3. conformation_name: unique name 
4. class  and etc.  : binary class(0 or 1)

### Objective:

Given a record, determine whether the record is Musk (1) or Non-Musk (0).

### Action Plan

#### 1. Undersatnd the data
- Datatypes of features

   - 166 features have 'int64' and 2 have 'object'
   
- Description of data(unique, max, min, mean, count and etc)
   
   - 102 types of molecules
   
   - NON-MUSK-j146 comes 1044 times
   
- Checking the data (Balanced or Imbalanced)

   - Imbalanced
   
   - class '1' is minority(1017)
   
- Describe the features

   - scatter plot, pdf, box-plot

#### 2.Pre-processing
- Null Value :  No Null values

- Duplicate rows  : No duplicate rows

- Duplicate features/columns  : No duplicate features

- Single value in columns across all rows : No single value

- Converting categorical features into one hot encoding(molecule_name)

- Standardized the data

#### 3. Train- Test split
- 80:20 ratio train-test split

- 5278 records in Train and 1320 in Test set

#### 4. Model

-  Uses Xgboost 
  - The test log loss is: 0.05
  - The Test accuracy of the xgbdt classifier is 98.33%
  - F1 Score:  0.9458
  
- 2 layer Neural network with 32 neurons in each layer
  - Test Loss: 1.7620610411871562e-05
  - Test Accuracy: 0.999
  - F1 Score:  1.0
