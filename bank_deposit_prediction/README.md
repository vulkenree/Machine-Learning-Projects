## Problem Description
**Overview**: In this exercise, my goal is to predict the outcome of a Marketing bank products over telephone using different classifiers. Goal is to compare the performance of different popular classifiers, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines their hyper parameters and additional techniaues we could use to optimize for certin desired outcomes.

## Summary
Based on the f1 scores Decision Tree produced the best model.

I looked at recall score as well since I wanted to minimize the impact of false negatives while maintaining the right balance between not missing out any potential customer who will subscribe for a long term deposit while not calling/following up on every single potential customer.

The predict proba threshold can be a way to find the right trade off that business wants to choose from the best model while choosing between true positive rate and false positive rate.

If we are targetting a certain number of customers for the campaign and there is a significant amount fo cost for each campaign, I recommend looking at the lift curves and identifying a threasholds that have better lift to achieve desired outcomes.


### Visual plots for ROC and Lift curves for the best model

**ROC**
Below you can find the ROC curves for the best decision tree model which resuted in a AUC of 0.75
<br>
<figure>
  <img src="images/ROC Curve for DTree.png" width="50%" height="40%">
  <figcaption>
  ROC curve for the best Decision Tree model which resulted in an AUC of 0.75.
  </figcaption>
</figure>
<br>
<br>
**Lift Curves**
I ended up generating a lift curves as well that shows the lift in true positives the model will prodcuce for each deciles ordered by their height probability of being classified as candidates to accept the bank marketing campaign.

<figure>
  <img src="images/Lift and Cumulative Gains Curve for DTree.png">
  <figcaption>
  Lift Curve for the Decision Tree model
  </figcaption>
</figure>


** I used a python library to create the lift curves, I think the 'wizard' legends are for showing the performance of a best case hypothetical model or a model with some god mode predicitons :).
