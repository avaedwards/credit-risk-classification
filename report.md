# Module 12 Report Template

## Overview of the Analysis

In this section, describe the analysis you completed for the machine learning models used in this Challenge. This might include:

* Explain the purpose of the analysis.
* Explain what financial information the data was on, and what you needed to predict.
* Provide basic information about the variables you were trying to predict (e.g., `value_counts`).
* Describe the stages of the machine learning process you went through as part of this analysis.
* Briefly touch on any methods you used (e.g., `LogisticRegression`, or any resampling method).


## Overview of the Analysis

The purpose of this analysis is to look at how accurate the machine learning models used are for this dataset, and how good it is at predicting who should be given loans, ie giving loans out to low risk applicants rather than high risk ones. By comparing the machine learning models, we can see which one will be better to use for this situation, overall a financial institution wants to only give out loans to low risk applicants, so they will be able to get their money back. If their model lets a lot of high risk applicants slip through, the bank may end up losing a lot of money to people who may not be able to pay the money back. The logistic regression model alone has a hard time predicting the people that are high risk loan applicants corrently, and this is due to the much smaller sample size of high risk loan applicants. By using the logistic regression model in conjunction with the randomoversampler module, we are able to inflate the dataset of high risk loan applicants, and have two equal datasets for the model to look at, which brought the accuracy up significantly. 

For this analysis, we needed to predict whether or not someone would be a high risk or a low risk option for a bank loan, this was done by taking a dataset of individuals that did or did not get loans from the bank, and then their financial details, including the size of the loan, their finances, their debt to income ratio, etc. The machine learning model, which was a logistic regression model, was then able to use this data to train and then test the dataset, to see if it was able to predict individuals that were bad or good choices for granting loans from a bank. Initially, the precision of detecting bad loan choices as bad loans was only 90%, which means that 10 in 100 people could get bank loans and not be in a position to pay the bank back, which is a bad position for a financial institution. By inflating the number of indivials that are high risk loan applicants to be the same number as the number of individuals that were low risk applicants, the model was able to train and become more accurate. By doing this, we were able to get the model's accurance up to 99%, a big increase over the original 90%.


## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * Accuracy 0.99
  * Precision 0 (Low Risk): 1.00
  * Precision 1 (High Risk): 0.84
  * Recall 0 (Low Risk): 0.99
  * Recall 1 (High Risk): 0.90

* Machine Learning Model 2:
  * Accuracy 0.99
  * Precision 0 (Low Risk): 1.00
  * Precision 1 (High Risk): 0.84
  * Recall 0 (Low Risk): 0.99
  * Recall 1 (High Risk): 0.99

## Summary

In this instance, the second machine learning model performed better, since it was able to detect 99% of the high risk applicants as high risk (recall for 1), in comparison, the first machine learning model was only able to detect 90% of the high risk applicants as high risk. The other values were all the same, so there was no negatives to using model 2 for this particular instance. 

For this specific situation, it is more important to detect the 1's (the high risk applicants), however this is not a blanket statement for all problems of this nature, it depends on what the specific question being asked (if '0' precision over '1' is desired), how the question is being asked, and the larger context of the question. 

For this situation, a bank denying a loan to a low risk applicant does not harm the bank, and neither does giving a loan to a low risk applicant. However, giving a loan to a high risk applicant can be risky. In comparison, denying a loan to a high risk applicant would also not harm the bank. So for the bank, being the most precise about detecting the high risk applicants makes the most sense, the model can detect them and then the bankteller can make an informed decision on whether or not to give that person the loan. 


