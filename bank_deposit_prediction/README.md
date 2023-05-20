## Problem Description
**Overview**: In this exercise, my goal is to predict the outcome of a Marketing bank products over telephone using different classifiers. Goal is to compare the performance of different popular classifiers, namely K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines their hyper parameters and additional techniaues we could use to optimize for certin desired outcomes.

## Summary
Based on the f1 scores Decision Tree produced the best model.

I looked at recall score as well since I wanted to minimize the impact of false negatives while maintaining the right balance between not missing out any potential customer who will subscribe for a long term deposit while not calling/following up on every single potential customer.

The predict proba threshold can be a way to find the right trade off that business wants to choose from the best model while choosing between true positive rate and false positive rate.

If we are targetting a certain number of customers for the campaign and there is a significant amount fo cost for each campaign, I recommend looking at the lift curves and identifying a threasholds that have better lift to achieve desired outcomes.

Below you can find the ROC curves for the best decision tree model which resuted in a AUC of 0.75

<figure>
  <img src="images/ROC Curve for DTree.png" width="70%" height="60%">
  <figcaption>
  ROC curve for the best Decision Tree model which resulted in an AUC of 0.75.
  </figcaption>
</figure>
