# Covid-Hospitalizations-Predictor
A project that uses the Google search trends of various symptoms in different states to predict the number of weekly new hospitalization cases using both decision trees and KNN regressors. The models achieved R^2 errors of 0.53 and 0.58 respectively and both reached an RMSE of 17 (for reference, the TA's were getting 40 on that front, so we did a pretty good job!).

The project done as part of the COMP 551: Applied Machine Learning class. My teammates were the honorable [Preyansh Kaushik](https://github.com/preyansh98) and Wenhao Geng.

### A few notes
1. The data collected from Google has a number of invalid cells, so data cleaning, normalization & scaling were used to alleviate this issue for model training purposes.
2. For privacy reasons, Google does not provide the exact search volume of each symptom for every state; the data is instead normalized by region making comparisons between regions complex. To address this, we scaled the normalized data with the population estimates of each state. This alone improved our models' accuracy by 40%.
3. Obviously, not all symptoms are related to COVID. We kept the top 4% of symptoms (which amounts to 22 symptoms) that showed the best correlation with new hospitalization cases.
4. We used grid search to optimize hyperparameters efficiently.

