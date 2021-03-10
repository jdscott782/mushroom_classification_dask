# mushroom_classification_dask

## Big Data Challenge

In this challenge, you'll replicate one of the supervised learning projects that you did before in the program. This time, you'll use Dask instead of pandas and NumPy. Follow the instructions below:

The aim of this challenge is to get your hands dirty on writing code using Dask. This is why there is no minimum or maximum limit on the size of the dataset that you can use.

Use Dask counterparts to replicate all the data-cleaning and machine-learning parts of your supervised learning project. In other words, do the following:

Instead of pandas DataFrames, use Dask DataFrames whenever possible.
Instead of NumPy arrays, use Dask arrays whenever possible.
Use Dask to parallelize your model trainings.

## Capstone 2: Supervised learning
### Mushroom classification model
Dataset: Mushroom records drawn from The Audubon Society Field Guide to North American Mushrooms (1981).

## Dataset & research question

This dataset includes descriptions of hypothetical samples corresponding to 23 species of gilled mushrooms in the Agaricus and Lepiota Family. Each species is identified as definitely edible, definitely poisonous, or of unknown edibility and not recommended. This latter class was combined with the poisonous one. The Guide clearly states that there is no simple rule for determining the edibility of a mushroom; no rule like "leaflets three, let it be'' for Poisonous Oak and Ivy.

From this dataset we aim to determine the following:
Can mushroom samples be correctly identified as edible or poisonous based on a set of physical attributes?


## Model specification & results

For this analysis, five classification models were fit to the data. AUC ROC scores were used to assess the accuracy of each model. For the random forest and KNN classifiers, hyperparameter tuning was done to determine the optimal number of estimators and neighbors, respectively.


## Practical uses & considerations

For our purposes, the best model was the KNN classifier with a processing time of 0.062 s. Ultimately the top factor in selecting the best model was processing time, since all 5 of the models achieved 100% accuracy.

* This model could be used by mushroom collectors to determine whether the mushrooms they encounter in the field are edible or poisonous. 
* This can mean the difference between survival and death in certain instances, so it is important that the model has the highest possible accuracy. 
* Since the model would likely not be usable out in the field, it would be less useful to survivalists and more useful for individuals collecting the mushrooms and later determining whether or not they are edible. That is, unless a portable application of the model could be created to test samples in the field.
