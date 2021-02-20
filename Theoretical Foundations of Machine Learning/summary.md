



# Parametric methods

# Bayesian Decision Theory

## Naïve Bayes

![Image result for naive bayes](https://uc-r.github.io/public/images/analytics/naive_bayes/naive_bayes_icon.png)

## Discriminant Functions

### Gaussian

#### Univariate Gaussian

![image-20210220091728018](Theoretical Foundations of Machine Learning/screenshots/image-20210220091728018.png/image-20210220091728018.png)

#### Multivariate Gaussian



![image-20210220092715299](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220092715299.png)

#### Squared *Mahalanobis distance* 

****

$$
R^2 = (x − µ)^T Σ^{-1} (x − µ)
$$

### Discriminant Functions for the Gaussian Density

![image-20210220100638780](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220100638780.png)

## Bayesian classifier for Gaussian density

**(optimal) Bayesian classifier is a linear classifier when** 

- Gaussian PDFs

- Sigmas are the same in all classes

- Linear classifier is orthogonal to line joining class means if sigmas are diagonal

- Linear classifier is not orthogonal to class means if sigmas are not diagonal

**(optimal) Bayesian classifier is a non-linear classifier when sigmas are different**

### CASE 1

**If both classes have the same variance (*meaning that the covariance is both equal*) and the covariance matrix is diagonal matrix (*a matrix in which the entries outside the main diagonal are all zero*).**

![image-20210220112412601](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220112412601.png)

![image-20210220112433148](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220112433148.png)

#### **EXAMPLE**

![image-20210220112509996](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220112509996.png)

![image-20210220112521462](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220112521462.png)

**The separation line will be orthogonal to the line between the two means. it will be either exactly in the middle if the two class prior probability are equal, or close to class 2 if class 1 prior probability is higher, or close to class 1 otherwise.**

![image-20210220113338431](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220113338431.png)

### CASE 2

**If both classes have the same covariance matrix but not a diagonal matrix.**

![image-20210220113846534](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220113846534.png)

![image-20210220113914916](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220113914916.png)

**The separation line will not be necessarily orthogonal to the line between the two means.**  **it will be either exactly in the middle if the two class prior probability are equal, or close to class 2 if class 1 prior probability is higher, or close to class 1 otherwise**.

![image-20210220113932364](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220113932364.png)

### CASE 3

**If the covariance matrices are not equal.**

![image-20210220115014245](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220115014245.png)

**The decision boundary will be hyperquadric**

![image-20210220115100758](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220115100758.png) E

#### **EXAMPLE**

![image-20210220115223861](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220115223861.png)

![image-20210220115250986](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220115250986.png)

![image-20210220115307398](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220115307398.png)

![image-20210220115319802](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220115319802.png)

![image-20210220115328228](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220115328228.png)

# Confusion Matrix

![Image result for confusion matrix](https://miro.medium.com/max/1854/1*uR09zTlPgIj5PvMYJZScVg.png)

![image-20210220122115212](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220122115212.png)

![image-20210220122255770](C:\Users\Zoey\AppData\Roaming\Typora\typora-user-images\image-20210220122255770.png)



## **ACCURACY**

Accuracy is a metric that generally describes how the model performs across all classes. It is useful when all classes are of equal importance. It is calculated as the ratio between the number of correct predictions to the total number of predictions.

When should we avoid accuracy?

- in case of class imbalance.

$$
Accuracy = \frac{TP + TN}{total}
$$


$$
Accuracy = \frac{184 + 1543}{184 + 1543 + 223 + 50} = 0.8635
$$

## **RECALL**

The recall is calculated as the ratio between the number of *Positive* samples correctly classified as *Positive* to the total number of *Positive* samples. The recall measures the model's ability to detect *Positive* samples. The higher the recall, the more positive samples detected.
$$
Recall = \frac{TP}{TP + FN}
$$

$$
Recall = \frac{184}{184 + 223} = 0.4520
$$

## **PRECISION**

The precision is calculated as the ratio between the number of *Positive* samples correctly classified to the total number of samples classified as *Positive* (either correctly or incorrectly). The precision measures the model's accuracy in classifying a sample as positive.
$$
Precision = \frac{TP}{TP + FP}
$$

$$
Precision = \frac{184}{184 + 50} = 0.7863

$$
