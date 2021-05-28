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
* [assets](assets) a folder contains ploted figures.

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


