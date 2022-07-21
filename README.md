# Daily Min Temperature in Melbourne, Australia #

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/jofaval/melbourne-temperature-timeseries/blob/master/notebook.ipynb)

## Table of contents

1. [📁 Data](#-data)
1. [📓 Description](#-description)
1. [✔️ Objective](#-objective)
1. [🧱 Tech stack](#-tech-stack)
1. [💹 Algorithms](#-algorithms)
1. [📊 Visualization](#-visualization)
1. [🤓 Conclusions](#-conclusions)
1. [©️ Credits](#-credits)

## 📁 Data
[↑ Back to the table](#table-of-contents)

The data is available at the following link (not the official one, nor that I could find one):\
[https://raw.githubusercontent.com/jbrownlee/Datasets/master/daily-min-temperatures.csv](https://raw.githubusercontent.com/jbrownlee/Datasets/master/daily-min-temperatures.csv)

## 📓 Description
[↑ Back to the table](#table-of-contents)

An optional exercise about timeseries that we were assigned in the Artificial Intelligence and Big Data degree. Melbourne, Australia. The source of the data was created by Australian Bureau of meteorology over a ten year span (1981 - 1990).

Not many info is out there about this specific dataset, not that I could find without going too deep, I did not find a paper, maybe there's only the dataset to it, which, for this (small) project, is more than enough.

## ✔️ Objectives
[↑ Back to the table](#table-of-contents)

1. Single step model, where from the temperature of the last seven days we are able to estimate the temperature of the next day.
1. Multi step model, where from the temperature of the last 28 days, we estimate the temperature of the next seven days.
1. Use a Recurrent Neural Network that uses Long Short-Term Memory.
1. Convert the date to a unique pair of attributes (it's sine and cosine).

## 🧱 Tech stack
[↑ Back to the table](#table-of-contents)

Python, that's it! R is a programming language that, as for the moment being, I have no experience with, even though it's powerful and broadly used, but I'd dare to say that no more than Python.

And one of the strongest points, if not the most, about Python, are it's libraries, so... the libraries I've used are:

- Pandas, data manipulation with an ease of use and exploration data analysis.
- Numpy, a really strong linear algebra library, used in the project for it's statistics utilities, SciPy may be an alternative, but I have no experience at all with it.
- Matplotlib and Seaborn, both fantastic libraries for data visualization, and they complement each other.
- Scikit-Learn, the library used for Machine Learning and statistics models: Linear Regression, SVR, Lasso, Ridge, etc.
- Tensorflow and Keras, the industry standard for Deep Learning, the way to go, not really, it's just that for now I don't have that many experience with PyTorch

## 💹 Algorithms
[↑ Back to the table](#table-of-contents)

This was solved by using deep learning neural networks based on Tensorflow and keras. I did try it out with Facebook's prophet (as per recomendation of trying it out of our professor Sergio Vivo), I may upload it as a different project, or maybe on this one, who knows.

- **Dense Neural Network**, it's one of the most "basic" neural networks, it's a sequential neural network that using two hidden layers to predict the outcome.
- **Single-shot Neural Network**, it's the most simple architecture, there's no hidden layers, as soon as data is inputted it tries to solve it.
- **RNN LSTM**, this is a more advanced type of neural networks that "feeds" on itself, it's based on the concept of short-term memory, but prolonged to the whole fitting process, so that previous outcomes influence the present.

## 📊 Visualization
[↑ Back to the table](#table-of-contents)

Lineplots and scatterplots, my main focus for the visualizations (there's not that many) was to try and detect any sort of cyclic pattern (as we were told to do so in timeseries projects) and to evaluate that the operations were done correctly.

There's also the date visualization to check that the cycles are complete and there's no gap to fill in (which could be hotfixed but would be a problem, or render the whole project nearly impossible, luckily, it didn't).

## 🤓 Conclusions
[↑ Back to the table](#table-of-contents)

Having a consistent dataset (daily without a miss) for 10 straight years is a great starting point, but it's just that, a starting point, without any other feature that could contribute to the temperature prediction it becomes really hard to actually get accurate predictions, even more for a whole straight week.

I'd guess that if we had hour, or even minute detail, it may be more precise, but I can't tell for certain.

And timeseries are really hard as a starting point, not because of the theory, but to actually apply it properly, and get decent results at it.

## ©️ Credits
[↑ Back to the table](#table-of-contents)

First of all, to [Australian Bureau of meteorology](http://www.bom.gov.au/) for the actual dataset.

Then to [Jason Brownlee](https://github.com/jbrownlee/) the author of the incredible [Machine Learning Mastery](https://machinelearningmastery.com/).

And finally, to Sergio Vivo for the exercise and comprehensive explanation of timeseries and neural networks in Tensorflow.