## Comparing the performance of ML algorithms trained on the [UCI Parkinson's Data Set](https://archive.ics.uci.edu/ml/datasets/parkinsons) before and after feature scaling and dimensionality reduction.

The training featuers are scaled using sklearn's RobustScaler. PCA is then applied to the scaled training features and the top 4 PCs are selected as they account for approximately 90% of the variance in the data. The models are then trained and tested using the raw and conditioned data.

### sklearn ML Algorithms Trained:
* LogisticRegression
* LinearSVC
* GaussianProcessClassifier
* DecisionTreeClassifier
* KNeighborsClassifier

### Results:
* All models except for LogisticRegression perform better on the testing data when trained and tested with the PCs
* The performance of LogisticRegression is the same when trained and tested using the PCs and the original 22 features
* LinearSVC exhibits the largest gain in performance when using the PCs versus the raw features

### Additional Notes/Future Experiments/etc.:
* Test performance of models with different combinations of 1st and other PCs
* Attempt optimizing best performing models with GridSearchCV
* Experiment with other methods of dimensionality reduction
