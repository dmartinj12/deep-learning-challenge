# deep-learning-challenge


Analysis of Neural Network Performance for Predicting Fundraising Success
Introduction
The goal of this analysis is to predict the success of fundraising campaigns for nonprofit organizations based on their characteristics. By leveraging a neural network, we aim to build a classification model that determines whether a campaign is likely to achieve its target based on features such as organization type, application details, income amount, and more.

The dataset contains details about nonprofit fundraising campaigns, including information such as application type, classification, use case, status, and special considerations. We preprocess the data, build a neural network model, and evaluate its performance to assess its accuracy and loss.

Data Overview
The dataset consists of the following features:

APPLICATION_TYPE: The type of application submitted.
AFFILIATION: The organization's affiliation.
CLASSIFICATION: Tax classification.
USE_CASE: The primary area for which the funds will be used.
ORGANIZATION: Type of organization.
STATUS: Current status of the organization (active/inactive).
INCOME_AMT: Income range of the organization.
SPECIAL_CONSIDERATIONS: Indicates special factors like priority status.
ASK_AMT: Amount requested by the campaign.
IS_SUCCESSFUL: Target variable indicating campaign success.

Model Details
Neural Network Architecture
Input Layer: Features derived from preprocessing the dataset (e.g., encoded categorical variables, normalized numeric variables). The number of input features was determined by X.shape[1].
Hidden Layer 1: 12 neurons with ReLU activation.
Hidden Layer 2: 8 neurons with Tanh activation.
Output Layer: 1 neuron with Sigmoid activation to predict a binary outcome (success or failure).
Training Results
Accuracy: 72.76%
Loss: 0.5547
Results
1. What are the key trends in the data?
The dataset highlights several trends:

The majority of organizations are classified under specific categories (e.g., C1000, C2000).
A large number of applications are grouped under specific types such as T3, T4, and T10.
Special considerations (SPECIAL_CONSIDERATIONS) and income levels (INCOME_AMT) vary widely but may be influential in predicting success.
2. What features most influence campaign success?
From initial preprocessing and feature selection:

ASK_AMT: Smaller requested amounts tend to be more successful.
USE_CASE: Categories like "Healthcare" and "Preservation" show higher success rates.
APPLICATION_TYPE: Certain types like T3 and T5 are associated with higher success.
3. How well does the model perform?
The model achieves:

An accuracy of 72.79%, indicating that it correctly predicts campaign success approximately 73% of the time.
A loss of 0.5556, suggesting room for improvement in prediction precision.

4. Could a different model be used?
Yes, an alternative model such as Random Forest could be employed. Random Forest aggregates predictions from multiple decision trees, reducing variance and improving the overall accuracy of the model.
It is particularly effective for datasets with complex patterns or non-linear relationships.