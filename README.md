[![PyPi Version](https://img.shields.io/pypi/v/ml-python.svg)](https://pypi.python.org/pypi/ml-python)
[![Python Compatibility](https://img.shields.io/pypi/pyversions/ml-python.svg)](https://pypi.python.org/pypi/fastai)
[![License](https://img.shields.io/pypi/l/ml-python.svg)](https://pypi.python.org/pypi/ml-python)
# ML

This module provides for the easiest way to implement Machine Learning algoritms without the need to know about them.

Use this module if
- You are a complete beginner to Machine Learning.
- You find other modules too complicated.

This module is not meant for high level tasks, but only for simple use and learning.

I would not recommend using this module for big projects.

This module uses a tensorflow backend.

### Pip installation
```bash
pip install ml-python
```
### Python installation
```bash
git clone https://github.com/vivek3141/ml
cd ml
python setup.py install
```
### Bash Installation
```bash
git clone https://github.com/vivek3141/ml
cd ml
./install.sh
```
This module has support for ANNs, CNNs, linear regression, logistic regression, k-means.

## Examples
Examples for all implemented structures can be found in `/examples`. <br>
In this example, we will see how to learn a linear regression example.
<br><br>
First, import the required modules.
```python
import numpy as np
from ml.linear_regression import LinearRegression
```
Then make the required object
```python
l = LinearRegression()
```
This code below randomly generates 50 data points from 0 to 10 for us to run linear regression on.
```python
# Randomly generating the data
x = np.array(list(map(int, 10*np.random.random(50))))
y = np.array(list(map(int, 10*np.random.random(50))))
```
Lastly, train it. Set `graph=True` to visualize the dataset and the model.

```python
l.fit(data=x, labels=y, graph=True)
```
![Linear Regression](https://github.com/vivek3141/ml/blob/master/images/linear_regression.png)<br><br>
The full code can be found in `/examples/linear_regression.py`