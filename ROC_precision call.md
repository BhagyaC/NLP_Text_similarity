# How to Use ROC Curves and Precision-Recall Curves for Classification in Python
- It can be more flexible to predict probabilities of an observation belonging to each class in a classification problem rather than predicting classes
- This flexibility comes from the way that probabilities may be interpreted using different thresholds that allows the operator of the model to trade off concern in the errors made by the model, such as the number of false positive compared to the number of false negetives.
- This is required when using model where the cost of the one error outweight the cost of other types of errors
- The two diagnostic tools that helps in the interpretation of the probabilistic forecast for binary classificatio predictive modeling problems are ROC curves and precision recall curves
- ROC curve summarize the trade - off between the true positive rate and false positive rate for a predictive model using different probability thresholds
- Precision -recall curves summarize the trade off between the true positive rate and positive predictive value for a predictive model using different probability threshold
- ROC curves are appopriate when the observation are balanced between each classes and whereas precision call curves are appropriate for imbalanced dataset

## ROC
- The useful tool when predicting the probability of a binary outcome is the Reciever Operating Charecteristc curve or ROC
- It is a plot of false positive rate on the x axis versus the true positive rate on the y axis for a number of different candidate threshold value is between 0 to 1 in another words it is a plot again the false alarm rate to the hit alarm rate
- `True Positive Rate = True Positives / (True Positives + False Negatives)` also reffered to sensitivity
- `False Positive Rate = False Positives / (False Positives + True Negatives)` also reffered to specificity
- ROC is useful because - the curves of different models can be compared directly in general or for different thresholds
- The area under the curve (AUC) can be used as a summary of model skill
- A model is assign a higher probability to a randomly chosen  real positive values occurance than a negative occurance on average
- Generally skill ful model are represented by curves that bow up to the top left of the plot
- The model with no skill will plot a line at a point 0.5, 0.5- a diagonal line bottom left to top right
