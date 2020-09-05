# Eye Feature Clustering For Emotion Recognition
 Experimenting with Feature Clustering in the Eye Region, for Emotion Recognition.
 
> **Note**: Not able to view the `ipynb`s? Please follow [these instructions](https://github.com/iurisegtovich/PyTherm-applied-thermodynamics/issues/11#issue-184473171). 

## Prereqs:
- Python3
- Jupyter Notebook/Google Colab/Anything you like to render Python notebooks on

## Dataset:
[Extended Cohn Kanade (CK+)](https://ieeexplore.ieee.org/document/5543262) emotion and [FACS](https://en.wikipedia.org/wiki/Facial_Action_Coding_System) action unit labelled dataset (327 emotion labelled images).  

The data required (Action units of the Eye region) have been extracted and available in `data/` in this repo. The files in this directory were imported into the notebooks.

## Clustering:
The features were clustered into 2 and 3 clusters using K-means Clustering. New features after clustering were used to train and test 7 classifiers.
- Ada Boost classifier
- Decision Tree Classifier
- Gradient Boost classifier
- K-nearest Neighbors
- Multinomial Naive Bayes
- Random Forest Classifier
- Support Vector Machine

## Results:
|classifier |	k2score	| k3score |  
|-----------|---------|---------|  
|ABC	| 43.90 | 47.56 |  
|DTC	| 65.85	| 68.29 |  
|GBC	| 62.20	| 62.20 |  
|KNN	| 60.98	| 63.41 |  
|MNB	| 25.61	| 25.61 |  
|RFC	| 67.07	| 67.07 |  
|SVC	| 41.46	| 56.10 |  

The highest accuracy was by DTC at 68.29%, followed by the RFc at 67.07%.  
Thus, clustering is probably **not the best** way to classify eye images based on emotions.
