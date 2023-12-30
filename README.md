# PythonProjects
## Tom Rossa, Jean-Lou Valeau, Anthonin Izoret

Bienvenue sur le GitHub présentant notre projet Python pour la data science réalisé dans le cadre de notre année de M1 à l'ENSAE.

Notre objectif est le suivant : nous souhaitons identifier les caractéristiques d'un jeu vidéo qui impactent son succès pour ensuite prédire le succès du jeu en fonction de ses caractéristiques. Il suffit d'exécuter le notebook principal

## Structure du Projet

### I/ Récupération des données 
####    I/A Webscrapping des titres des jeux sur Wikipédia 
####    I/B Webscrapping des notes des jeux sur metacritic 
####    I/C Webscrapping des autres données 

### II/ Nettoyage des données extraites
####    II/A Premier nettoyage des données 
####    II/B Reformatage et standardisation des données dans le dataframe 

### III/Représentatation et analyse descriptive  
####    III/A Description de la base et visualisation 
#####        III/A/1 Répartition des différents types de jeux vidéos 
#####        III/A/2 Répartition des notes des jeux vidéos
####    III/B Corrélations entre les variables 
#####        III/B/1 Matrice des corrélations 
#####        III/B/2 Régressions simples

### IV/ Modélisation
####    IV/A/ Régressions multiples
####    IV/B/ Analyse en Composantes Principales

### V/ Conclusion 


## Installation des Packages

Pour exécuter l'intégralité du notebook principal, il est nécessaire d'installer au préalable les packages et modules suivants:

### Webscrapping
```bash
!pip install unicode
!pip install unidecode
!pip install requests_html
!pip install igdb-api-v4
!pip install requests

import requests 
import urllib
import bs4
from requests_html import HTMLSession
from tqdm import tqdm
from unidecode import unidecode
import datetime
import time

from igdb.wrapper import IGDBWrapper
from igdb.igdbapi_pb2 import GenreResult
from igdb.igdbapi_pb2 import ThemeResult
from igdb.igdbapi_pb2 import GameResult
from igdb.igdbapi_pb2 import InvolvedCompanyResult
from igdb.igdbapi_pb2 import PlayerPerspectiveResult
from igdb.igdbapi_pb2 import MultiplayerModeResult
from igdb.igdbapi_pb2 import ArtworkResult
from igdb.igdbapi_pb2 import AgeRatingResult
from igdb.igdbapi_pb2 import CompanyResult
from igdb.igdbapi_pb2 import CollectionResult
from igdb.igdbapi_pb2 import GameEngineResult
from igdb.igdbapi_pb2 import FranchiseResult
```

### Visualisation et Analyse Descriptive
```bash
!pip install plotly
!pip install fancyimpute

from collections import Counter
import numpy as np
import pandas as pd
import ast
import matplotlib.pyplot as plt
from matplotlib.colors import LinearSegmentedColormap
import plotly.express as px
```

### Modélisation
```bash
from fancyimpute import KNN
import seaborn as sns
import statsmodels.api as sm
import statsmodels.formula.api as smf
import sklearn.metrics

from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import RobustScaler
from sklearn.cluster import KMeans

from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.linear_model import LassoCV
from sklearn.linear_model import RidgeCV
from sklearn.metrics import mean_squared_error, mean_absolute_error
from sklearn.linear_model import BayesianRidge
from sklearn.svm import SVR
```

