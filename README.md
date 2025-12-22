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
The Random Forest works in such way - it creates many indepedent decision trees and every one of them is trained with the randomly selected subsample of data. Then the so-called feature randomness comes to work - with every tree node division all features are taken randomly so the trees are less corealted with each other. When it comes to classification every tree "votes" so the final decision is a majority voting result. This approach of course has some drawback for example it can consume large amounts of RAM and the training process might be a little bit slower when it comes to large models but still this model is considered as one of the best espeically for this problem.  

### Second approach

### Third approach

## Description of the Chosen Concept

### Required data

### Algorithm's output

### Applied method

### Real world implementation

### Testing procedure

## Summary
