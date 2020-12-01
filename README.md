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

!(Imagent)[home/hans/Escritorio/52465/random1.png]



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


