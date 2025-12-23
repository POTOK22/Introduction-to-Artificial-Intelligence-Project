# Introduction-to-Artificial-Intelligence-Project

## Introduction
With increasing life expentency worldwide the problem of heart diseases has become a major and progressive challange to deal with. Since the likelihood of developing heart diseases can be estimated from various health parameters the question is how to do it precisely and accurately. The goal of this project is to create a simple but effective program that can predict and identify patients risk of developing a heart diesese in the future.

The project belongs to the subfield of machine learning called specifically "supervised learning", which relies on the principle that every training example is accompanied by a label with the correct answer. The model uses these labaled examples to learn underlying patterns, enabling it to subsequently predict and recoginze outcomes for new unseen data - in this case whether a patient is at risk of developing heart disease. Moreover the task is to achieve binary classification. In simple terms model must predict one of two classes based on medical examination features - class 1 (likely to develop heart disease) or class 0 (not likely to develop heart disease). 

## Description of the Real-World Problem

### Goal
The primary objective of developing this program is to accrately predict the patients likelihood of developing a heart disease based on the various health-related factors and paramteres. In simple terms, the program should accept specific amount of patient records, process the provided data and give the the reliable prediction as an outcome.

### Motivation
Improving health outcomes and extending human longevity represent fundamental goals in medice and must be recognized as highly valuable and important endevaours. Additionally this project may contribute to a better understanding of the key factors that are the most influential and strongly correlate with human health and cardiovascular system.

### Input data
The data for this program will be provided in a .csv file containing several key health parameters that may influence the likelihood of developing the hearth disease in the future. It includes general attributes e.g. age and sex and specialized medical indicators such as serum choresterol level, resting blood pressure or fasting blood sugar.  

## State of the Art
There are several different ways to achieve the same goal and the choice depends on various factors. In this project six methods were initialy tested in order to determine which offered the best prognosis. It was easy to see the dominance of so-called scale-insensitive methods generaly performed better. These scale-insensitive methods differ from scale-sensitive ones in that they do not require the training and testing data to be properly standarized (i.e. scaled to values between 0 to 1). Therefore the further analysis was primarily focused on the scale-insensitive methods due to their siglthy superior performance.   

### First approach
The first approach considered was a Random Forest model, widely regarded as one of the best and most popular machine learning algorithms due to its high precision and accuracy as well as its rboustness to typical medical datasheet issues, such as small sample sizes and correlated features. Moreover, Random Forest offers further benefits including resistance to overfitting and build-in feature importnce metrics, which allow identification of the health parameters most strongly correlated with the likelihood of developing a heart disease.

The Random Forest operates by constructing numerous indepedent decision trees and each one of them is trained on randomly selected subsample of data. The so-called feature randomness is also introduced - at each tree node split only a random subset of features is considered so the correlation between trees is reduced improving overall diversity. For classification tasks each tree "votes" so the final prediction is determined by majority voting result.

Despite all of these strengths this approach of course has some drawback - for example it can consume significant amounts of RAM and the training time might require longer time for large models. Nevertheless, Random Forest remains one of the top choices for this problem.  

### Second approach
The second approach considered was a Gaussian Naive Bayes (GaussianNB) model - a popular variant of the Naive Bayes classifier. This algorithm assumes that all features are indepedent of one another - a condition known as conditional independence which is rarely fully satified in real-world datasets. Despite this unrealistic assumption, this model frequently performs good enough and serves as a popular baseline i.e. a simple, interpretable reference point for initial evaluations and comparisions in futher analysis.

GaussianNB offers several significant adventages, including very fast training and prediciton times, the ability to work effectively with small sample dataset sizes and high stability with strong resistance to overfitting. However, these benefits comes at a cost - it generaly achieves poor accuracy and precision in comparision to more sophisticated models mainly due to the oversimplyfying assumptions that features are uncorrelated.

### Third approach
The final approach considered was the GradientBoostingClassifier (also known as Gradient Boosting Machine, or GBM) a highly powerful algorithm built on the principle of sequential ensemble learning. In this method each new decision tree is trained to correct the errors made by the previous ones. GBM performs exceptionally well on small to medium-sized datasheets and in this project achieved results were almost as good as those of Random Forest.

The key difference from Random Forest lies in the tree structure, while Random Forest builds independent trees in parallel Gradient Boosting is focused on dependecy between trees sequentially reducing residual errors. Among its strongest advantages there are very high accuracy and precision, built-in feature importance metrics (similar to Random Forest) and superior handling of complex interactions and nonlinear relationships in the data.

However there are also noticable weakneasses like vulnerability for overfitting as well as lower stability across different runs and even longer training times than those required by Random forest and its very high sensivity for hyperparameters settings.  

## Description of the Chosen Concept
The selected concept was straightforward to choose as Random Forest clearly outperformed other models. In further analysis this method was optimized in order to achieve the best possible outcome while also focusing on interpretation of predictions and feature importance.

### Required data
The dataset used for training and testing the models was a popular, publicly available heart disease dataset from [Kaggle](https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset "Kaggle dataset link"), stored in CSV format. It contains key health parameters from various patients along with a target column indicating the presence or absence of heart disease, enabling supervised learning.
One of the dataset's major advantages is its high quality and readiness for use: no preprocessing was required, as all features were already encoded as numerical values (e.g., chest pain type represented on a scale from 0 to 3, rather than categorical labels). This clean, well-prepared structure allowed direct application of the models without additional data cleaning or feature engineering.

### Algorithm's output
In the first part of the project all algoritms were compared based on their performance metrics in predicting heart disease. The key evaluation metric - the score - included accuracy, precision and recall in order to allow a direct assessment of each model's predictive capability.

The second part focused primarily on optimizing the Random Forest model. As a result there were generated a correlation heatmap to visualize relationships between the individual features and the feature importance scores were extracted to indentify which health parameters had the strongest influence on the probability of developing heart disease. 

### Applied method
Method applied to achieve the best possible performance were the hyperparameters tuning - specifically Grid Search. This exhaustive method systematically tests all possible combinations of hyperparameters from a predefined grid, ensuring the identification of the optimal configuration that gets highest model performance.

Although Grid Search can be time-consuming for larger datasets or more extensive grids this is not a significant issue in this project because the given datasets are relatively small in size.

### Real world implementation
This type of machine learning project has strong potential for real-world applications, as cardiovascular diseases remain one of the leading causes of death worldwide. Although this project represents only a small step of what a significant benefits the machine learning can bring to healthcare. In future such models could become powerful tools for predicting and preventing the development of heart disease.

### Testing procedure
Model evaluation in this project was conducted multiple times by using various techniques to ensure robust and reliable results. Each algorithm was assessed based on standard classification metrics such as accuracy, precission and recall which measure overall predictive performance.

Additionally, the Receiver Operating Characteristic (ROC) curve was plotted for the models, along with the corresponding Area Under the Curve (AUC) score. The ROC curve illustrates the trade-off between true positive rate and false positive rate across different classification thresholds, providing a comprehensive view of the model's ability to distinguish between positive and negative classes. A higher AUC value (closer to 1) indicates superior discriminative performance, with Random Forest achieving the best results in this regard.
