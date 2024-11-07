# titanic-dataset
Train and Test Data:

Train csv was split into 80/20 split using statified shuffle split . 

Data cleaning:
- null values in Age were replaced with mean using SimpleImputer
- irrelevant features were dropped i.e. Name, Embarked,Ticket Number etc
- Created custom transformers to one hot Encode Gender and Embarked
- Created a pipeline with the AgeImputer, OneHotEncoder and the Feature Dropper.

Pipeline:
- strat _train
- strat_test
- original df (train.csv)
- titanic_test_data was passed into the pipeline

Scaling
- used standard scaler on all the X inputs.
- converted all the Y inputs into arrays.

Training the Algorithm
- used RandomForests
- obtained the best hyperparameters using GridSearch
- using the best_estimators. predicted the survived labels on the testing data and got 0.79 accuracy on kaggle.
