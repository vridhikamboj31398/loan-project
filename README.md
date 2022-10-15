
# loan_prediction_project

# objective: Attempted to build a machine learning model that is capable of predicting whether a person should be given loan or not

# exploratory data analysis

exploring the data feature by

keeping these three questions in mind:

i) What does the distribution of each feature look like?

ii) If the variables are categorical, how much does each category impact the Loan status?

iii) If there are missing values, what should be the best strategy to impute them?

# Feature Engineering

The data set has 8 categorical features and 3 continuous features.

Binary features like Married, Education, Self-employed, Credit-History, Loan status were all One Hot encoded.

Applicant Income had outliers. So, discretization of Applicant Income, based on their sample quantiles, into 5 categories was a valid solution.

Loan Amount was almost Normally distributed but it had few outliers which we had to deal
with. Therefore, after filling the null spaces with the median of the distribution as median is not sensitive
towards the outliers, the feature Loan Amount was also, based on the sample quantiles, discretized into 5 categories.

Loan Amount term had only 10 unique values in the form of the number of years. Therefore, it
was label encoded.

EDA of Property Area showed that individuals living in semi-urban areas were more likely to get
their loans approved. Therefore, most weight was given to the applicants coming from semi urban areas.

# Algorithms

The algorithms used in this project are the following:

i) Random Forests

ii) Logistic Regression

iii) Support Vector Classifier

iv) Gaussian Naïve Bayes


The number of observations in the training set were pretty small so it made more sense to choose
algorithms with a high bias and low variance 

• Initially, all 11 features were used to evaluate the performance of the algorithms.

• Once, we got the top 2 performing models from the first iteration, their feature importance
values were used to create a second feature set

• Finally, a third feature set was created based on the correlation analysis of all 11 features. The
features that were least corelated with Loan status were dropped and the ones that were
highly corelated among themselves were also taken care of.

# Result
I aimed for high recall value so as to reduce the false negative
therefore logistic regression with 7 features gave me a recall value (0.723)

# conclusion:

Such a model will help in the speeding up of the loan approval process
