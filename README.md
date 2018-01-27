# Iris Flowers Species #

## Domain ##

The problem is drawn from the analysis of data when studying specific structural features of three related variations of Iris flowers.

![Iris](/data/iris.png)

### References ###

Fisher,R.A. "The use of multiple measurements in taxonomic problems" Annual Eugenics, 7, Part II, 179-188 (1936); also in "Contributions to Mathematical Statistics" (John Wiley, NY, 1950).

Duda,R.O., & Hart,P.E. (1973) Pattern Classification and Scene Analysis. (Q327.D83) John Wiley & Sons. ISBN 0-471-22361-1. See page 218.

Dasarathy, B.V. (1980) "Nosing Around the Neighborhood: A New System Structure and Classification Rule for Recognition in Partially Exposed Environments". IEEE Transactions on Pattern Analysis and Machine Intelligence, Vol. PAMI-2, No. 1, 67-71.

Gates, G.W. (1972) "The Reduced Nearest Neighbor Rule". IEEE Transactions on Information Theory, May 1972, 431-433.

## Problem Statement ##

Given the four measurements of sepal length, sepal width, petal length, and petal width, we will use supervised learning to develop a classification model which will predict the class of a new Iris flower, that we may come across. This model will help distinguish the species from one other.


## Dataset ##

The Iris dataset contains measurements for 150 Iris flowers from 3 different species (50 in each of three classes).

As each element will be stored in an R, the size of the dataframe will be approximately 5400 bytes (150 rows * 4 columns * 8 bytes + 150 rows * 1 column * 4 bytes) plus any overhead associated with the dataframe. With an overhead of 30% for this small dataset, the total in-memory size of this dataframe is about 7200 bytes.

Number of Attributes: 4 numeric, predictive attributes and the class

The 3 Classes in Iris dataset are:
 * Iris Setosa
 * Iris Versicolor
 * Iris Virginica

The four features include:
* sepal length in cm
* sepal width in cm
* petal length in cm
* petal width in cm
    
Missing Attribute Values: None

Summary Statistics:

|   SepalLength |    SepalWidth |   PetalLength |    PetalWidth|
|---------------|---------------|---------------|--------------|
| Min.   :4.300 | Min.   :2.000 | Min.   :1.000 | Min.   :0.100|
| 1st Qu.:5.100 | 1st Qu.:2.800 | 1st Qu.:1.600 | 1st Qu.:0.300|
| Median :5.800 | Median :3.000 | Median :4.350 | Median :1.300|
| Mean   :5.843 | Mean   :3.054 | Mean   :3.759 | Mean   :1.199|
| 3rd Qu.:6.400 | 3rd Qu.:3.300 | 3rd Qu.:5.100 | 3rd Qu.:1.800|
| Max.   :7.900 | Max.   :4.400 | Max.   :6.900 | Max.   :2.500|
|          IrisSpecies|
| Iris-setosa    :50|
| Iris-versicolor:50| 
| Iris-virginica :50|

Class Distribution: 33.3% for each of 3 classes.
    
## Solution Statement ##

We will create three different models, as possible solutions to our classification problem, using three different algorithms. These include: Discriminant Analysis (LDA), K Nearest Neighbor (KNN), and Classification and Regression Trees (CART). We will break up our measurement data, and use part of it for creating the models, while we use the other part of our dataset for validation of our models. From the results of the validation step, we can determine the most accurate model of the three, that is suited for this problem.

## Benchmark Model ##

A good benchmark would be to predict the class of a newly discovered Iris flower, given its four features of sepal length, sepal width, petal length, and petal width. Because we are using supervised learning, we can divide our data into two sets, one consisting of 80% of the measurements, to be used for training and developing the model, and the other 20% for validation of our models.


## Evaluation Metric ##

We will be using the metric of 'Accuracy' to evaluate our models. This is a ratio of the number of correctly predicted instances divided by the total number of instances in the dataset multiplied by 100 to give a percentage (e.g. 98% accurate).
