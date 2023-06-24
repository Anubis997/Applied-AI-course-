# "Classification of Cancer Genetic Mutations using General Linear Models with Text-Based Clinical Literature"

The dataset provided by Memorial Sloan Kettering Center consists of 3,321 data points and 5 features. The task is to classify mutations based on these features into eight different strains.

Data Preprocessing:
The text data in the 'TEXT' column was preprocessed using various techniques such as removing special characters, converting to lowercase, removing stopwords, etc. This was done to clean the text data and make it suitable for analysis.

Exploratory Data Analysis:
The distribution of class labels in the dataset was visualized using a bar plot.

Model Evaluation:
A dummy classifier was trained and evaluated using log loss as the performance metric. The log loss of the dummy classifier was calculated to establish a baseline for comparison with other models.

Genetic Variation Feature Encoding:
Genetic variation feature ('Gene' and 'Variation') response coding was implemented to convert the categorical features into numerical representations based on the target variable.

Text Feature Encoding:
Text feature encoding was performed using TF-IDF vectorization. The 'Variation' feature was transformed using TF-IDF vectorizer to represent it as a numerical feature.

Feature Stacking:
The response-coded features and TF-IDF encoded features were stacked together to create the final feature sets for training, validation, and testing.
Classification with Optimized Hyperparameters:

Stochastic Gradient Descent (SGD) classifier with logistic loss was used for classification. The hyperparameters (alpha) were optimized using cross-validation to minimize the log loss.

Evaluation and Results:
The trained classifier was used to make predictions on the training, validation, and test sets. The log loss was calculated for each set to evaluate the model's performance.

Additional Analysis:
Stability analysis was performed to determine the coverage of features in the test and cross-validation data.
The variation distribution was visualized to analyze the distribution of gene variations.

Gene Feature:
Logistic regression with only the Gene feature resulted in overfitting, with a train log loss of 0.6701, cross-validation log loss of 1.7426, and test log loss of 1.6515. Despite overfitting, the model performed better than the dummy classifier, indicating the significance of the Gene feature.

Variation Feature:
When including the Variation feature along with Gene, the model still suffered from overfitting, especially when using TF-IDF encoding. However, the model performed better than the dummy classifier. This suggests the significance of the Variation feature in improving the classification performance.

Text Feature:
Logistic regression with the Text feature, either using TF-IDF or response coding, resulted in overfitting. However, the model showed better performance compared to the dummy classifier. This indicates the significance of the Text feature in improving classification accuracy.
