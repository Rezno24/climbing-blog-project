# Climbing Route Ratings Analysis

This project explores climber preferences and trends in bouldering grades and route ratings across three iconic U.S. areas — Hueco Tanks, Joe’s Valley, and Joshua Tree — using data from MountainProject.com. The analysis includes visual exploration of user ratings, route difficulty, and popularity, and finishes with a regression model predicting route ratings based on difficulty and location.

To Replicate:

Requirements
Make sure you have Python 3.7+ and the following packages installed:

pip install pandas matplotlib seaborn numpy statsmodels scikit-learn

Here’s a full list of libraries used in the notebook (written as python installation code):

import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import statsmodels.formula.api as smf
import re
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.preprocessing import OneHotEncoder
from sklearn.compose import ColumnTransformer
from sklearn.pipeline import Pipeline
from sklearn.metrics import mean_squared_error, r2_score

Obtaining and Replicating the Data:

All data was downloaded from MountainProject.com. The website allows users to export CSVs for specific climbing areas. The three areas used in this project were:

Joe's Valley:
https://www.mountainproject.com/route-finder?diffMaxaid=75260&diffMaxboulder=21250&diffMaxice=38500&diffMaxmixed=65050&diffMaxrock=5500&diffMinaid=70000&diffMinboulder=20000&diffMinice=30000&diffMinmixed=50000&diffMinrock=1800&is_sport_climb=1&pitches=0&selectedIds=105880382&sort1=area&sort2=rating&stars=0&type=boulder


Joshua Tree National Park:
https://www.mountainproject.com/route-finder?diffMaxaid=75260&diffMaxboulder=21250&diffMaxice=38500&diffMaxmixed=65050&diffMaxrock=5500&diffMinaid=70000&diffMinboulder=20000&diffMinice=30000&diffMinmixed=50000&diffMinrock=1800&is_sport_climb=1&is_top_rope=1&is_trad_climb=1&pitches=0&selectedIds=105720495&sort1=popularity%20desc&sort2=rating&stars=0&type=boulder

Heuco Tanks:
https://www.mountainproject.com/route-finder?diffMaxaid=75260&diffMaxboulder=21250&diffMaxice=38500&diffMaxmixed=65050&diffMaxrock=5500&diffMinaid=70000&diffMinboulder=20000&diffMinice=30000&diffMinmixed=50000&diffMinrock=1800&is_sport_climb=1&pitches=0&selectedIds=105810691&sort1=area&sort2=rating&stars=0&type=boulder

Use the filters at the bottom of each page to show only bouldering routes between V-Easy and V12–13, with at least 0 stars. Then export the data by clicking Export CSV.
Once downloaded, rename the files appropriately (joes_valley.csv, joshua_tree.csv, hueco_tanks.csv) and place them in the working directory.

2. Run the Analysis
Open the Jupyter Notebook file included in this folder and run all cells. This will:

Import and clean the datasets
Generate the visualisations
Fit and evaluate the regression model

All cleaning and preprocessing steps are fully documented within the notebooks.


# File Structure
/climbing-project
    README.md
    blog.txt
    /project-files
        /data
            - joes_valley.csv
            - joshua_tree.csv
            - hueco_tanks.csv
        /jupyter_notebooks
            - climbing_blog.html
            - climbing_blog.ipynb
            - climbing_code_only.html
            - climbing_code_only.ipynb
        /graph_output_images
            - boxplot_of_ratings.png
            - distrubution_of_grades.png
            - predictive_model.png
            - scatter_of_ratings.png
            - total_climbs.png


