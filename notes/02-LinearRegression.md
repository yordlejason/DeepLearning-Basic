# Linear Regression

By using the given dataset, train the model and find the optimal linear model.

$H(x) = Wx + b$

### Cost Function (Loss Function)
Check the distnace between the given data points and the linear model.

$(H(x) - y)^2$

* By squaring the loss, we can amplify the outliers and ignore the negative loss.

$cost(W,b) = \frac{1}{m}\sum_{i=1}^m (H(x^i) - y^i)^2$

* $m$ is the number of data
* $H(x^i)$ is the predicted value
* $y^i$ is the true value

And by minimizing the cost, we can get the optimal linear model.
