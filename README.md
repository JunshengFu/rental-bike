# **Rental bike prediction**

## Objective

Bike-sharing systems are popular choice among young generations to solve their last mile problem.
As we know, bike-sharing rental process is highly correlated to the environmental and seasonal conditions, e.g. weather conditions,
precipitation, day of week, season, hour of the day, etc.

This project uses machine learning to learn the bike-sharing rental patterns
and predicts the number of bikes should be placed in a spot based on the environmental conditions. The data is based
on real two-year historical logs from [here](http://capitalbikeshare.com/system-data), and the dataset is organized and provided by [1].


#### **Prediction example**
![][image2]

#### **Training data example**
![][image1]

---

### Code & Files

#### 1. My project includes the following files
* [simplenetwork.py](simplenetwork.py) is a designed network for rental bike prediction.
* [main.ipynb](main.ipynb) is the main file that executes the code and presents related data.
* [dataset/hour.csv](dataset/hour.csv) bike sharing counts aggregated on hourly basis for 17379 hours
* [dataset/day.csv](dataset/day.csv) bike sharing counts aggregated on daily basis for 731 days
* [assets](assets) a folder contains plotted figures.

#### 2. Dependencies & my environment

* python3, numpy, pandas, matplotlib, jupyter notebook
* OS: Ubuntu 20.04

#### 3. How to run the code

* Start juyter notebook.

	```sh
	jupyter notebook
	```

* Run `main.ipynb` file.

#### 4. Reference

[1] Fanaee-T, Hadi, and Gama, Joao, "Event labeling combining ensemble detectors and background knowledge", Progress in Artificial Intelligence (2013): pp. 1-15, Springer Berlin Heidelberg, doi:10.1007/s13748-013-0040-3.


[//]: # (Image References)
[image1]: ./assets/data.png
[image2]: ./assets/prediction.png
[forward]: ./assets/forward.jpg
[error_MSE]: ./assets/error_MSE.jpg
[gradient_descent]: ./assets/gradient_descent.JPG
[cross_entropy]: ./assets/cross_entropy.JPG
[mult_class_cross_entropy]: ./assets/m_class.JPG

----

#### 5. Key Concepts

In `simplenetwork.py`, there is a simple 3-layer network. In this network, we aim to go through and understand the detailed
math for each of these concepts (e.g. forward pass, backward pass, error function, gradient descents), instead of looking into more advance networks to achieve the best performance.

##### (1) Forward pass

In forward pass, the input data are fed into the network and traversed
through all neurons from the first layer to the last layer of the network.
![][forward]

##### (2) Backward pass (or back-propagation)

In backward pass, it uses the gradient descent algorithm to update the
weights/bias in the network, and it runs from last layer backward to the first layer.

Gradient descent

![][gradient_descent]

##### (3) Error function

There are a lot of different error functions has been developed, and three commonly used error functions are listed. In this project, **mean square error** is used, since the prediction of the bike numbers is a regression problem.

* **Mean Squared Error function** is usually used for regression problems, where the output is usually real-valued number, such as
the number of bikes in this project, or weight/salary/etc.

![][error_MSE]

* **Binary Cross-Entropy function** is usually used for the binary classification problem, where the output is usually true or false,
e.g. university student admission (accept or not).

![][cross_entropy]

* **Multi-Class Cross-Entropy function** is usually used for the multi-class classification problem, where the network should be able to classify
multiple classes, such as traffic-sign recognition.

![][mult_class_cross_entropy]
