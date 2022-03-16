
Conversational AI Data Science UCS663 

Kaggle-based Lab Evaluation - I






About Data:
To analyse gender by voice and speech, a training database was required. A database was built using thousands of samples of male and female voices, each labeled by their gender of male or female.
Data Loading & Preprocessing
Initially the dataset is loaded into the notebook using the cudf library. The data set is analyzed thoroughly using different functions to check for null values and to check description of all the columns.
The data is preprocessed to deal with the inconsistencies within the data. The data available on Kaggle didn’t have any inconsistencies. The categorical values are converted into numerical for computation
Let us fetch and explore the data before getting into training.




Now let us perform some sanity check on the data to make sure there are no empty fields which we might need to impute further.





DATA EXPLORATION
Done in order to understand the data visually. Built pairplot of each and every column



Preprocessing Data
There are multiple steps we will take in this section to transform the original data into format we need
Converting String Value To int Type for Labels
Encode label category
Male -> 1
Female -> 0





Normalize data
Normalization = (x - min (x))/ (max(x) - min(x))
Each feature can have different type of measures . So we must normalize them into same scalar.
Splitting Dataset into Training Set and Testing Set
APPLYING DIFFERENT MODELS
Logistic regression 
KNN classifier 
Decision tree
Support Vector machine
I inferred that the best output was given by the logistic regressor and KNN Classifier









Where we use Logistic Regression?
To predict whether a voice/face man (1) or woman (0)

Logistic regression is generally used where the dependent variable is Binary or Dichotomous. That means the dependent variable can take only two possible values such as “Yes or No”, “Default or No Default”, “Living or Dead”, "Man or Woman", “Responder or Non Responder”, “Yes or No” etc. Independent factors or variables can be categorical or numerical variables.

















According to our confusion matrix the model predict 6 and 11 wrong sample.6 represent it is 1 but model predict 0 instead of it, 1 also represent it is 0 but model predict 1 instead of it





CREATING DATAFRAME TO COMPARE THE ACCURACY AND R2 SCORE OF KNN AND LOGISTIC REGRESSION ALGORITHM. AND PLOTING GRAPH FOR THE SAME

















