# JB1_2401FTDS
JB1_2401FTDS UNSUPERVISED LEARNING PROJECT

# Anime Recommender System Dataset


![](https://img.shields.io/badge/Python-3776AB.svg?style=for-the-badge&logo=Python&logoColor=white) [![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](URL_TO_YOUR_APP)

<div id="main image" align="center">
  <img src="https://github.com/MoteneJan/JB1_2401FTDS/blob/main/pic.png" width="550" height="300" alt=""/>
</div>

## Table of contents
* [1. Project Overview](#project-description)
* [2. Dataset](#dataset)
* [3. Packages](#packages)
* [4. Environment](#environment)
* [5. MLFlow](#mlflow)
* [6. Streamlit](#streamlit)
* [7. Team Members](#team-members)

## 1. Project Overview <a class="anchor" id="project-description"></a>

In today’s technology-driven world, recommender systems are socially and economically critical for ensuring that individuals can make appropriate choices surrounding the content they engage with on a daily basis. One application where this is especially true surrounds movie content recommendations; where intelligent algorithms can help viewers find great titles from tens of thousands of options.

What We Did:
- Data Loading: We began by sourcing and loading the news articles dataset.
- Preprocessing: This involved cleaning and preparing the data to ensure optimal performance of the machine learning models.
- Model Training: We developed various machine learning models to classify the news articles into specific categories.
- Evaluation: We evaluated the performance of these models to ensure they accurately categorize news articles.
- Deployment: Finally, we deployed the best-performing model as an interactive web application using Streamlit.

Streamlit is a powerful and easy-to-use framework for building web applications in Python. It allows for the rapid development and deployment of data-driven applications with interactive features, making it ideal for showcasing machine learning models and their results in a user-friendly manner.

By automating the classification process, we aim to improve content organization, boost operational efficiency, and enhance the overall user experience for readers.


## 2. Dataset <a class="anchor" id="dataset"></a>
### Amime Dataset
+ anime_id - myanimelist.net's unique id identifying an anime.
+ name - full name of anime.
+ genre - comma-separated list of genres for this anime.
+ type - movie, TV, OVA, etc.
+ episodes - the number of episodes in the series. (1 if movie).
+ rating - average rating out of 10 for this anime.
+ members - number of community members that are in this anime's "group".
### Train Dataset
+ user_id - non-identifiable randomly generated user id.
+ anime_id - the anime that this user has rated.
+ rating - rating out of 10 this user has assigned (-1 if the user watched it but didn't assign a rating).
+ You can find both the `anime.csv` and `train.csv` datasets
[here](https://www.kaggle.com/competitions/anime-recommender-system-project-2024/data?select=anime.csv).


## 3. Packages <a class="anchor" id="packages"></a>

To carry out all the objectives for this repo, the following necessary dependencies were loaded:
+ `Pandas 2.2.2` and `Numpy 1.26`
+ `Matplotlib 3.8.4` and `Seaborn 0.12.2`
+ `Nltk 3.8.1` and `ML Flow 2.14.1`
+ `IPython 8.20.0` and `IPython Sql 0.3.9`
+ `Python 3.11.8` and `'Pymysql 1.0.2`
 

## 4. Environment <a class="anchor" id="environment"></a>
### Below we are going to guide you through creating an environment

Use the Anaconda programme to create the environment. Click on the plus icon at the bottom of the Anaconda environments pane. Select All on the drop down menu to select the packages needed to run this report.Select the following packages one by one from the drop down menu: numpy version 1.20.4, pandas version 2.2.2, seaborn version 0.13.2 & matplotlib version 3.8.4,nltk version 3.8.1,ipython version 8.20.0,ipython sql version 0.3.9, python version 3.11.8,pymysql version 1.0.2 & ML Flow version 2.14.1. After selecting the tick boxes - click on apply. Then right click on the play button and scroll down to open in Jupyter notebook to install this report.

### Create the new evironment - you only need to do this once

```bash
# create the conda environment
conda create --name <env>
```

### This is how you activate the virtual environment in a terminal and install the project dependencies

```bash
# activate the virtual environment
conda activate <env>
# install the pip package
conda install pip
# install the requirements for this project
pip install -r requirements.txt
```
## 5. MLFlow<a class="anchor" id="mlflow"></a>

MLOps, which stands for Machine Learning Operations, is a practice focused on managing and streamlining the lifecycle of machine learning models. The modern MLOps tool, MLflow is designed to facilitate collaboration on data projects, enabling teams to track experiments, manage models, and streamline deployment processes. For experimentation, testing, and reproducibility of the machine learning models in this project, you will use MLflow. MLflow will help track hyperparameter tuning by logging and comparing different model configurations. This allows you to easily identify and select the best-performing model based on the logged metrics.

- Please have a look here and follow the instructions: https://www.mlflow.org/docs/2.7.1/quickstart.html#quickstart

## 6. Streamlit<a class="anchor" id="streamlit"></a>

### What is Streamlit?

[Streamlit](https://www.streamlit.io/)  is a framework that acts as a web server with dynamic visuals, multiple responsive pages, and robust deployment of your models.

In its own words:
> Streamlit ... is the easiest way for data scientists and machine learning engineers to create beautiful, performant apps in only a few hours!  All in pure Python. All for free.

> It’s a simple and powerful app model that lets you build rich UIs incredibly quickly.

[Streamlit](https://www.streamlit.io/)  takes away much of the background work needed in order to get a platform which can deploy your models to clients and end users. Meaning that you get to focus on the important stuff (related to the data), and can largely ignore the rest. This will allow you to become a lot more productive.  

#### 6.1 Running the Streamlit web app on your local machine

As a first step to becoming familiar with our web app's functioning, we recommend setting up a running instance on your own local machine. To do this, follow the steps below by running the given commands within a Git bash (Windows), or terminal (Mac/Linux):

- Ensure that you have the prerequisite Python libraries installed on your local machine:

 ```bash
 pip install -U streamlit numpy pandas scikit-learn
 ```

- Navigate to the base of your repo where your base_app.py is stored, and start the Streamlit app.

 ```bash
 cd JB1_2401FTDS/Streamlit/
 streamlit run base_app.py
 ```

 If the web server was able to initialise successfully, the following message should be displayed within your bash/terminal session:

```
  You can now view your Streamlit app in your browser.

    Local URL: http://localhost:8501
    Network URL: http://192.168.43.41:8501
```
You should also be automatically directed to the base page of your web app. This should look something like:

<div id="s_image" align="center">
  <img src="https://github.com/MoteneJan/JB1_2401FTDS/blob/main/streamlit.jpg" width="850" height="400" alt=""/>
</div>

Congratulations! You've now officially deployed your first web application!

#### 6.2 Deploying your Streamlit web app

- To deploy your app for all to see, click on `deploy`.
  
- Please note: If it's your first time deploying it will redirect you to set up an account first. Please follow the instructions.

## 7. Team Members<a class="anchor" id="team-members"></a>

## Team Members<a class="anchor" id="team-members"></a>

| Names                                                                                     | Emails              
|-------------------------------------------------------------------------------------------------------------------------|----------             
| [Sihle Kalolo](https://github.Toni8)                                                      | kalolohlesi@gmail.com
| [Dimpho Lebea](https://github.DimphoLebea28)                                              | dimpholebea28@gmail.com
| [Disney Malete ](https://github.Disney17)                                                 | kgomotsodisneymalete@gmail.com
| [Lindokuhle Mhlongo ](https://github.link)                                                | lindokuhlemakhedama@gmail.com
| [Jan Motene](https://github.com/MoneteJan)                                                | motenejo@gmail.com
| [Josephina Foloko](https://github.DJFoloko)                                               | missfolokodj@gmail.com

