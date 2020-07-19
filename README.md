# Evaluating Credit Risk
To properly assess risk, I have done a few different ML Models using different sampling techniques.  After training each model, it was assessed for accuracy.

The data set used was loan application details assessed for risk.  By nature of this data set, the data is heavily unbalanced,  There will be very few high risk applications compared to low risk.  As such, the model's training data needs to be balanced to account for this.  To to this, I evaluated three different strategies

##Evaluating Accuracy
To ensure these models are truly accurate, we take the known data and divide it into 2 sets.  One to train the model, and one to test.  Once we have that, we use some evaluative metrics
### Precision which evaluates predicted positives against all positives
### Recall or sensivity measures how many people who are high risk was correctly identified
### Balanced Accuracy to evalues the Recall value in each class (low risk, high risk)



## Oversampling Sampling
instances of the minority class are randomly selected and added to the training set until the majority and minority classes are balanced.

While it identified 61 or the 92 high risk applicants with an accuracy score of 63.5%, it also incorrectly predicted 6712 low risk applicants, so precision was very low at less than .01.  Recall was .66.

## SMOTE Sampling
SMOTE analysis is a less random approach than the previous.  The synthetic minority oversampling technique (SMOTE) is another oversampling approach to deal with unbalanced datasets. In SMOTE, like random oversampling, the size of the minority is increased.  

SMOTE was less accurate at 62.9%, and betwcause of the high number of False Positives, it was virtually the same in precision at less than .01.  Recall was lower at .61

## Under Sampling
Undersampling involves using fewer low risk training data while keeping the same amount of high risk data.  Undersampling produced a balanced accuracy of 62.3%, a precission of .01, and recall of .62, the same as SMOTE.

## Combination Sampling
We can combine the techniques to see if either improved.  In this example, we achieved an accuracy of 64.4%.  Once again, given the high false positive rate, precision was .01  Recall was .7, the highest of the approaches.

## Recommendation
No model was truly accurate on its own.  While for risk testing, a False Positive may be acceptable, none of the models were very precise.  This could lead to additional effort in properly assessing a loan's risk.  However, the basis for any future model should use Combination Sampling.  It showed the highest degree of sensitivity.  Next steps could be to evaluate additional model approaches, increase the training data, or find additional data to include in the model

