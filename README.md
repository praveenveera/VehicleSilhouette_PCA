# VehicleSilhouette_PCA
------------------------
The purpose of the case study is to classify a given silhouette as one of four different types of vehicle, using a set of features extracted from the silhouette. The vehicle may be viewed from one of many different angles.

Four "Corgie" model vehicles were used for the experiment: a double decker bus, Cheverolet van, Saab 9000 and an Opel Manta 400 cars. This particular combination of vehicles was chosen with the expectation that the bus, van and either one of the cars would be readily distinguishable, but it would be more difficult to distinguish between the cars.

The purpose is to classify a given silhouette as one of three types of vehicle, using a set of features extracted from the silhouette. The vehicle may be viewed from one of many different angles.
------------------------------

# Project Summary:

- The vehicle.csv data was processed for Null Values, duplicate values and Outliers.
- Outliers are neutalized with median of the respective columns
- Correlation amoung the various features are observed.
- The data was scaled using zscore and made ready to use for modelling.
- From Elbow Curve we observed the characteristics of the data shared along the explained variance and Priciple components. Finallised to go with 9 Components which is covered almost 95% more data.
- Applied SVM, Gaussian and GridSearch with SVM model to the reduced features.
- The best test data prediction accuracy from PCA is 95.7% was scored from GridSearch classifier (SVM: {'C': 10, 'gamma': 'auto', 'kernel': 'rbf'})
- We also applied SVM, Gaussian and GridSearch with SVM model to the data without reducing features to understand the data and model behaviour.
- Below are comparision amount the models with PCA and without PCA.
		Acc -          PCA , without PCA 
		SVM -          93.2% , 94.4%
		Gaussian -     85.2  , 69.3%
		GridSearch -   95.7% , 98.1%
- From the above we could see that the best PCA score from GridSearch - classifier was actualy 3 units less compared to the score given by dataset with all features.

## Conclusion:
Overall from the above analysis we can say that PCA has done a very good job with proven accuracy. Accuracy with PCA is approx near to the accuracy of the all features data. The PCA given accuracy 94% is only 8 dimension where as actual data has 18 dimension with accurary 98%
