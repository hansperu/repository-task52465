# Assignment
# Programming for Data Analysis

## By Hans Perez Rubin de Celis

## 1. Random numbers in NumPy
### What is a random number?
In this notebook I will respond and discuss the following points:

### Explain the general purpose of the package.
It is a Python package, specialized for building and manipulating large and multidimensional arrays. NumPy has built-in functions for linear algebra and random number generation. It is an important library because many of the other Python packages such as SciPy, Matplotlib rely on Numpy to work (to a reasonable degree).

The numpy.random module supplements Python's built-in random with functions to efficiently generate complete arrays of sample values from many types of probability distributions. Python source for data analysis by Wes McKinney.

### Import libraries

`import numpy as np`

`import matplotlib.pyplot as plt`

`import pandas as pd`

`import seaborn as sns`

`from matplotlib.ticker import FuncFormatter`

To begin with, we’ll first import the NumPy module by running import `numpy` as `np`, allowing us to access all relevant functions in the module.

`import numpy as np`

### 1. rand(d0, d1, ..., dn)
This method generates random numbers in a given shape. Some common examples are given below. Note that the numbers specified in the rand() function correspond to the number of dimensions of the array that is to be generated. A special case is that when no numbers are specified in the function, a random value will be generated.

`np.random.rand()`

`0.5242129213883749`

`np.random.rand(4)`

`array([[0.27452013, 0.4426765 , 0.23433773, 0.86329531],`

       `[0.02179784, 0.23914946, 0.24846379, 0.41607698],`

       `[0.3212738 , 0.37238859, 0.43868957, 0.30780613]])`

### 2. randn(d0, d1, …, dn) and standard_normal([size])
Both methods are used to generate random numbers from the standard normal distribution, the curves of which are shown in the figure below. The red curve shows you the standard normal distribution with a mean of 0 and standard deviation of 1.

![Imagent](https://miro.medium.com/max/640/1*PfODI74UmIlRfDj0q-I3Kw.png)
              *Standard Normal Distribution Shown By Read Curve (Source: Wikipedia)*
Both methods are to draw numbers randomly from the distribution to generate arrays of the defined shape. Their usages are about the same, except that for the `standard_normal()` method, we need to use a tuple to set the shape size. Some common examples are given below.
`np.random.randn(4)`




In the file **1. Random numbers in NumPy.ipynb** we develop and explain in detail the Numpy random numbers.

## 2. What is Simple Random data fuction?
In this section we will develop the Simple Random Data function and generate random numbers of different types, such as matrices of various shapes, normally distributed matrices, ranges of floats of different parameters such as the range, dimensions and probabilities of the returned values.

The following lines of code demonstrate the usefulness of the random.rand function to generate random numbers between 0 and 1 and how this data can then be manipulated, plotted and visualised.

```#numpy.random.rand(d0, d1, ..., dn) function example
#returns array of random floats between 0 and 1 of shape (d0 to dn)
import numpy as np #import numpy package
import matplotlib.pyplot as plt
import scipy as sc
from scipy import stats
import math as mt
import pandas as pd
%matplotlib inline
R1 = np.random.rand(100,1) #return 100 x 1 random array of floats between 0 and (not including) 1
x = np.arange(100) #create a list 0f 1 to 100 in order to plot the random no's created against in a scatter plot
plt.scatter(x,R1)
plt.title("plot of 100 random floats ")
```

`Text(0.5, 1.0, 'plot of 100 random floats ')`

![Imagent](data:image/png;base64,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%0A)

The file **2.Simple random data and Permutations.ipynb** demonstrates the utility of the random.rand function to generate random numbers between 0 and 1 and how this data can be manipulated, plotted, and displayed.

## 3. What is data distribution?
The data distribution is a list of all possible values and the frequency with which each value occurs. These lists are important when working with statistics and data science.

The random module offers methods that return randomly generated data distributions.

Normal distributions are often used in the natural and social sciences to represent real-valued random variables whose distributions are not known. The normal distribution is a continuous theoretical probability distribution.

The **3.Distributions funtions.ipynb** file explains the use and purpose of at least five "Distributions" functions.

## 4. Generate Random Numbers in Python

The use of randomness is an important part of configuring and evaluating machine learning algorithms.

From randomly initializing weights in an artificial neural network to dividing data into test sets and random trains, shuffling a set of stochastic gradient descent training data, generating random numbers, and taking advantage of randomness is a skill. necessary.

File **4. Using seeds to generate pseudorandom numbers.ipynb** explains the use of seeds to generate pseudorandom numbers.

# References
## Books

![Imagent](http://rps2images.ebscohost.com/rpsweb/othumb?id=NL$1084592$PDF&s=d)

### Learning IPython for Interactive Computing and Data Visualization - Second Edition
**Series:Community Experience Distilled**
**Authors:** Rossant, Cyrille
**Publication Information:** Ed.: Second edition. Birmingham, UK : Packt Publishing. 2015
**Resource Type:** eBook

![Imagent](http://rps2images.ebscohost.com/rpsweb/othumb?id=NL$1703793$PDF&s=d)

### IPython Interactive Computing and Visualization Cookbook : Over 100 Hands-on Recipes to Sharpen Your Skills in High-performance Numerical Computing and Data Science in the Jupyter Notebook, 2nd Edition
**Series:Community Experience Distilled**
**Authors:** Rossant, Cyrille
**Publication Information:** Ed.: Second edition. Birmingham : Packt Publishing. 2018
**Resource Type:** eBook


![Imagent](http://rps2images.ebscohost.com/rpsweb/othumb?id=NL$1841870$PDF&s=d)

### Hands-On Data Analysis con NumPy y pandas: Implementar Python Paquetes De Datos manipulación para procesamiento
**Authors:** Miller, Curtis
**Publication Information:** Birmingham: Packt Publishing. 2018
**Resource Type:** eBook

![Imagent](http://rps2images.ebscohost.com/rpsweb/othumb?id=NL$880858$PDF&s=d)

### Python Data Analysis
**Series:Community Experience Distilled**
**Authors:** Idris, Ivan
**Publication Information:** Birmingham, U.K. : Packt Publishing. 2014
**Resource Type:** eBook


![Imagent](http://rps2images.ebscohost.com/rpsweb/othumb?id=NL$1495814$PDF&s=d)

### Python Data Analysis - Second Edition
**Authors:** Fandango, Armando
**Publication Information:** Ed.: Second edition. Birmingham : Packt Publishing. 2017
**Resource Type:** eBook


