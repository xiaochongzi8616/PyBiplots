# PyBiplots 

## Overview
PyBiplots is a python package that performs the classic biplots methods. This methods are GH-Biplot, JK-Biplot and HJ-Biplot. 

## Dependences 
PyBiplots supports Python 3.6+ and no longer supports Python 2.

Installation requires [numpy](https://numpy.org/), [scipy](https://www.scipy.org/), [pandas](https://pandas.pydata.org/), [matplotlib](https://matplotlib.org/), [seaborn](https://seaborn.pydata.org/), [sklearn](https://scikit-learn.org/stable/) and [adjustText](https://github.com/Phlya/adjustText)

## Example
```python
## 1. Packages needed
import pybiplots.classic.HJ_Biplot as hj
import pandas as pd
import matplotlib
from sklearn.datasets import load_iris

## 2. Load iris data
iris = pd.DataFrame(data=load_iris().data, columns=load_iris().feature_names)

## 3. Fit Biplot
HJ = hj.fit(iris, Transform='Standardize columns')

## 4. Draw Biplot
matplotlib.style.use("seaborn")
HJ.plot(groups=load_iris().target, ind_name=False)
```