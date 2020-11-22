# Creditcard_fraud_detection
Separating the fraudulent transactions from normal transactions for Credit Cards.
The Dataset contains only 492 (0.17%) fraudlent transactions as compared to 2,83,000 normal trasnactions, thus the dataset is heavily skewed.

Three Different models were created for separating the fradulent transactions from the normal ones.

## Using Autoencoders in association with LogisticRegression.
The Autoencoders were trained only using 2000 normal transcations and the latent representation was obtained from the encoder part.
Since it is trained only for the normal transactions, a fradulent transaction will have a different latent representation which can easily be classified by any classifier.
The model was trained only on 2000 normal records, as a result the training completed in mere few seconds as compared to hours for other methods.

## Using XGBClassifier after upsampling using SMOTE.
The dataset was up sampled using SMOTE and then XGBClassifier was trained on it.
GridSearchCV and RandomizedSearchCV was used to find the best hyper parameters for the XGB model.

## Using RandomForestClassifier, LogisticRegression after upsampling using SMOTE.
The dataset was up sampled using SMOTE and then RandomForestClassifier and LogisticRegression was trained on it.
GridSearchCV and RandomizedSearchCV was used to find the best hyper parameters for RandomForest model.

