

[![LinkedIn][linkedin-shield]][linkedin-url]

# SVM-Hyperparameter-Tuning

<!-- TABLE OF CONTENTS -->
<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-repository">About The Repository</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Repository

In this, we see how to tune hyperparameters of Support Vector Machine (SVM). We use the Wine dataset to perfrom task. We tune the hyperparameters using GridSearchCV.




<p align="center">
<img src="https://miro.medium.com/max/1204/1*eF2b1QgLHtZKIK63gyeaDQ.png"
 alt="Logo" width="500" height="200">
</p>


### Built With

To perform this task we have pre-defined libraries, by using them we can easily achieve our task.
* [Pandas](https://www.w3schools.com/python/pandas/default.asp)
* [Numpy](https://numpy.org/)
* [Sklearn](https://scikit-learn.org/stable/)
* [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)
* [SVM](https://aniketyadavv.medium.com/svm-and-hyper-parameter-tuning-9a5cfed42e74)
* [Matplotlib](https://matplotlib.org/)
* [Seaborn](https://seaborn.pydata.org/)


<!-- GETTING STARTED -->
## Getting Started

### Prerequisites
* Any python Compiler

### Installation

1. Install packages
   ```sh
   pip install seaborn
   pip install scikit-learn
   pip install pandas
   pip install numpy
   pip install matplotlib
   ```



<!-- USAGE EXAMPLES -->
## Usage

The reason to do this is simple: sometimes it is not showing good results/accuracy due to the unsignficant parameters, so we change parameters using GridSearchCV to get better results and good accuracy.



<!-- ROADMAP -->
## Roadmap

First we understand about SVM
* SVM stands for Support Vector Machine. It is a Supervised Machine Learning algorithm. It is used for both classification and regression problem. It uses a process called kernel strategy to modify your data and based on these changes finds the perfect boundary between the possible results.
* Most of the times we get linear data but usually things are not that simple. Let’s take an example of classification with non-linear data :
<p align="center">
<img src="https://miro.medium.com/max/418/1*bMSkq3BtmiWKc7jFDjnN8g.png"
 alt="Logo" width="250" height="200">
</p>
* Now, to classify this type of data we add a third dimension to this two-dimension plot. We rule that it be calculated a certain way that is convenient for us: z = x² + y² (you’ll notice that’s the equation for a circle). It give us a three dimension space. Since we are in three dimensions now, the hyperplane is a plane parallel to the x axis at a certain z (let’s say z = 1). Now, we convert it again in two dimensions.
* It looks like this :
<p align="center">
<img src="https://miro.medium.com/max/444/1*tZF_OKBk5c10ITkw7730OA.png"
 alt="Logo" width="250" height="200">
</p>

* And here we go! Our decision boundary is a circumference of radius 1, which separates both tags using SVM.

**Let's Start to understand tha code:**

1. We take the Wine dataset to perform Support Vector Classifier. We import Wine data using sklearn in-built datasets.

2. In this repository I use necessary libraries like:
* Pandas
* Matplotlib
* Numpy
* Seaborn
* Sklearn

3. Now, the main part that every data scientist is Data Pre-processing. In this we first see our dataset information using DESCR method means describe. It shows our attribute information and target column.
4. To understand the dependency of every feature on the output we use seaborn and matplotlib library for visualization. First we use boxplot to know the relation between features and output.
<p align="center">
<img src="https://miro.medium.com/max/676/1*tiIicd2_XJ9t2cj90L367g.png"
 alt="Logo" width="300" height="200">
</p>
In this boxplot we easily see there is a linear relation between alcalinity_of_ash and class of wine.

5. So, our SVM model might assign more importance to those features which are varying linearly in relation with output.
6. To see how our data is distributed we use matplotlib python library. We use histogram here, let’s see an example of it :
<p align="center">
<img src="https://miro.medium.com/max/510/1*ahtOckKu39MAezqk7nmMvA.png"
 alt="Logo" width="300" height="200">
</p>
Feature malic_acid follows left-skewed distribution.

7. Now, we train our machine learning model. We import Support Vector Classifier (SVC) from sklearn’s SVM package because it is a classification problem.
8. We split the data into two parts training dataset and testing dataset using train_test_split module of sklearn’s model_selection package in 70% — 30% respectively. Because we first train our model using training dataset and then test our model accuracy using testing dataset.
9. Now the main part comes Hyper-parameter Tuning. First we understand about hyper-paramter — it is a parameter whose value is used to control the learning process and hyper-parameter tuning means to choose a optimal parameters. To accomplish this task we use GridSearchCV, it is a library function that is member of sklearn’s model_selection package. It helps to loop through predefined hyper-parameters and fit your estimator (like-SVC) on our training set.
10. The final output we get with 90% accuracy and by using SVC model and GridSearchCV.


You can develop your own model and improve accuracy by using others algorithms and tuning Hyperparameteres. Good Luck 😎



## Contact

Aniket Yadav - [Medium](https://aniketyadavv.medium.com/) - [Gmail](https://yadavaniket0820gmail.com/)
<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/aniket-yadav-2008/
