\slides{### Classification

- In classification we take in a *feature matrix* and make predictions of *class labels* given the features. 
- Our features are $\inputVector_i$ for the $i$th data point
- Our labels are $\dataScalar_i$ which is either -1 (negative) or +1 (positive).}

\slides{### Classification

- predict the class label, $\dataScalar_i$, given the features associated with that data point, $\inputVector_i$, using the *prediction function*: 

    $$\mappingFunction(\inputScalar_i) = \text{sign}\left(\mappingVector^\top \inputVector_i + b\right)$$

- Decision boundary for the classification is given by a *hyperplane*. 
- Vector $\mappingVector$ is the [normal vector](http://en.wikipedia.org/wiki/Normal_(geometry) to the hyperplane.
- Hyperplane is described by the formula $\mappingVector^\top \inputVector = -b$}


\slides{### Toy Data

- Need to draw a decision boundary that separates red crosses from green circles.}

\setupcode{import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline}

\code{np.random.seed(seed=1000001)
x_plus = np.random.normal(loc=1.3, size=(30, 2))
x_minus = np.random.normal(loc=-1.3, size=(30, 2))

# plot data
plt.plot(x_plus[:, 0], x_plus[:, 1], 'rx')
plt.plot(x_minus[:, 0], x_minus[:, 1], 'go')}