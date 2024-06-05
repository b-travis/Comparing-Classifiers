# Comparing-Classifiers
 Berkeley_MLAI_PA3

## Practical Application 3: Comparing Classifiers
### Dataset: Bank Marketing

## Summary of Findings:

Our stated goal was to develop an accurate model that is also easy to fit and interpret. Lets go through all the models from worst to best in thinking about these criteria:

(5) SVM with linear kernel -- decent model with respect to accuracy and F1, but the fit time was orders of magnitude larger than other models. It was the least accurate but the F1 was third best.

(4) and (3). Decision Trees and KNN. Both of these methods were similarly accurate and with similar F1. Their fit times were extremely low, however their quality with respect to accuracy and F1 wasn't quite to the level of the next two models.

(2) SVM with rbf kernel: Tied for best accuracy (90.0% and second best F1 (32.3%). Fit time was considerably longer than decision tree and K-Nearest Neighbor methods but worth the accuracy tradeoff.

(1) Logistic Regression: outperformed all over models with the best accuracy and F1 and a very fast fit time.

Additional note on model interpretability: Logistic Regression has an advantage over SVM of being much less "black box", and actually being able to provide quantitative probabilities of "Yes" or "No" for each data point. That helps its case as the best model for this use case.

When time allows, here are some next steps to improve this analysis:
- Improve the Grid Search for the best hyperparameters and models. Figure out why the SVM models (other than rbf) take so long to fit and whether there is a way to speed that up. Perhaps with feature selection so that there are fewer features.
- Feature Selection as a way to (1) Identify the most important feature predictors of "churn", and (2) create a simplified version of the model with only the most important features. The below code shows the most important 10 features identified by the best Logistic Regression model.

See full analysis here: https://github.com/b-travis/Comparing-Classifiers/blob/main/Comparing_Classifiers_in_Banking_Marketing.ipynb
