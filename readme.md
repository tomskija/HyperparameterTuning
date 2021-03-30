
## Tree-based Methods with an Emphasizes in Hyperparameter Tuning

#### Project Description:

This project demonstrates the application of hyperparameter tuning for Decision Trees and several Ensemble Methods (i.e., Gradient Boost, Tree Bagging, and Random Forest). Once each method has tuned hyperparameter in regard to predicting production, 2D spatial prediction is performed on the training and testing datasets given latitude and longitude coordinates. This project aims to help geoscientists in understanding how to tune hyperparameters effectively, and then visualize the predicted production results spatially.

#### Project Requirements:

This project requires the following Python libraries to be installed in order to work:

* Numpy
* Pandas
* Os
* Matplotlib
* Seaborn
* Warnings (optional)
* Sklearn (model_selection, metrics, tree, and ensemble packages)

Unfortunately, the project data cannot be supplied, but the workflow can be slightly altered based on any other data you choose to use to have this workflow run on your machine.

#### Project Results:

* Each method did relatively well in predicting production, but it was clear that the decision tree had trouble with overfitting, and as a result, I implemented three ensemble methods: gradient tree boosting, tree bagging, and random forest.
* The gradient tree boosting method gave better results than that of the tree bagging, but appeared sensitive to the choice of parameters when performing the spatial production predictions. That said, this may be more of an issue to how the spatial production prediction function was coded up.
* Furthermore, tree bagging and random forest (which is a more advanced version of tree bagging) showed less sensitivity to the choice in parameters in regard to the spatially predicting production, where the trees in these methods can be grown to be very complicated and prune back in order to avoid overfitting.
* However, tree bagging can suffer from trees growing in a similar manner due to having a feature with a variance that dominates over the overs. Whereas random forest splits the trees based on the square root of the number of predictive features to ensure that each tree grows in a different way.
* As a result, the spatial production prediction results of the random forest method were more conservative and represented a wider range of values overall than the tree bagging method, which could be a result of how each tree grew.