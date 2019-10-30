
### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.
Used Libraries:

* numpy
* pandas
* matplotlib.pyplot
* seaborn
* progressbar
* sklearn.preprocessing.StandardScaler
* sklearn.cluster.KMeans
* sklearn.model_selection.GridSearchCV
* sklearn.model_selection.KFold
* sklearn.preprocessing.MinMaxScaler
* sklearn.metrics.roc_auc_score
* sklearn.ensemble.RandomForestClassifier
* sklearn.ensemble.AdaBoostClassifier
* sklearn.ensemble.GradientBoostingClassifier
* IPython.display.clear_output

## Project Motivation<a name="motivation"></a>

For this project, I was interested in using the Bertelsmann data for the Udacity Data Scientst Nanodegree Capstone Project. In this Project I will look at the followung points:

1. How is the data structured and what are the different stastistics of the datas content
2. Whats the best Customer segmentation
3. Building a model to find future customers for a mail-order company
4. Taking part in a Kaggle competition

Furthermore a [report](https://medium.com/p/5a76e7d725b9/edit) was written on Medium


## File Descriptions <a name="files"></a>


* README.md: This readme file
* Arvato Project Workbook_own.ipynb: The main project file
* nan_list_altered.tsv: Tab seperated list with descriptions of missing data
* LICENSE: licence file
* resources/*: folder with all graphics used for the blog


## Results<a name="results"></a>

Findings:
While following the predefined structure this project went through different steps and reveled much information which was hidden in the data.

* In the pre-processing phase which is for many Data Science projects the most time consuming part, the project had to overcome the lack of description to many features and the sheer overload of different features. Non the less it was possible to define, unify and mend the missing data problem. Some compressed information was re-coded and some unnecessary data was dropped.
* With the pre-processed data the project went through the unsupervised learning / clustering phase. In order to shrink down the complexity of the data 1000 components werde selected via a PCA analysis taking care of 70% of explained variance. The Clustering then reveled that the main customer of the mail order company can be described as the average mainstream online buyer who never orders offline.
* Then the problems started appear and the cleaning / coding step had to be redesigned and redone. With the new design the model choice could be made resulting in the GradientBoosting model.
* The model was then fine tuned by doing a grid search cross validation with different parameters. To prepare the last step the tuned model was trained on the whole data set to be able to predict the response of the Kaggle Challenge.


Score = 0.47020
## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to Udacity, Bertelsmann Arvato Analytics and Kaggle for the data. Otherwise, feel free to use the code here as you would like! 