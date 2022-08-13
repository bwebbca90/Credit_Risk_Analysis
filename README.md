# Credit_Risk_Analysis

## Summary
Determining the risk associated with loan approval can be difficult as there is a lot more information about successful loans than unsuccessful ones. Lack of data on dangerous loan decisions makes it challenging to teach a machine learning model the characteristics that most frequently indicate a risky loan decision. Using resampling may help develop a model that forecasts problematic loans more precisely. 

## Machine Model Testing
* The first model made use of a straightforward oversampling strategy. The model's balanced accuracy rating was 66%, and 71% of the high risk loans were in fact projected to be high risk. Given that a model is required to detect high risk loans in order to prevent loans from being granted in those circumstances, this sounds quite amazing. The accuracy of predicting high risk loans is about 1%, though. Loans are likely to be forecasted as high risk when they are not, despite the strong recall of this model. This can result in more loan denials than necessary.
* The second model included fresh data with previously collected data using the SMOTE method. Instead of being randomly selected, these data points are sampled based on their closeness to already existing data points. Despite this, the predictive power of this model was comparable to that of the prior model with 66% for balanced accuracy.
* Undersampling was the third model employed in this investigation. The balanced accuracy score in this instance dropped to 52%. In comparison to earlier models, the precision ratings for high and low risk predictions remained unchanged. The SMOTEENN resampling procedure was used to accomplish a combination of under and oversampling.
* The fourth model's recall in this instance was extremely high (72%), and its balanced accuracy rating was 64%. Although the recall scores for high risk loans have increased, the accuracy for high risk loan predictions has remained at 1% across all of these models. To estimate credit risk, having a balance between precision and accuracy may be preferable.
* In the fifth model, Random Forest Classification, only some characteristics were sampled at random using bootstrap sampling. The decision tree that eventually produces the prediction values is fitted with these samples. Prediction accuracy for high-risk loans rose to 23% in this initial model. A balanced accuracy score of 100% did exist as well.
* Bootstrap samples are also utilized in the sixth model, Easy Ensemble for Imbalanced Classification. But rather than oversampling, this model arbitrarily undersamples the data. Similar to the prior algorithm, these results were produced. The balanced accuracy score was 99%, whereas the precision for high risk loans was 11%.  

## Results
Although the accuracy scores from the first four models employed in this analysis were generally acceptable, the precision for forecasts of high risk loans was rather poor. This may initially appear to be acceptable because it indicates that the majority of the high risk loans in the sample were correctly projected to be high risk. This is crucial in the financial industry since persistently lending to high-risk clients runs the danger of forcing an institution out of business. Nevertheless, despite modifications to the sampling approach, precision remained at or around 1%. A low precision score may indicate a high number of false positive predictions, which could cause loan applications to be identified as high risk even though they are not. The accuracy ratings of the last two models grew to nearly 100% in both, but the precision scores only slightly improved. This can be a sign that the dataset has been overfit, resulting in insufficient models all around. 
