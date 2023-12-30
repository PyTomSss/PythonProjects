# PythonProject
## Tom Rossa, Jean-Lou Valeau, Anthonin Izoret

Bienvenue sur le GitHub présentant notre projet Python pour la data science réalisé dans le cadre de notre année de M1 à l'ENSAE.

L'objectif est le suivant : nous souhaitons identifier les caractéristiques d'un jeu vidéo qui impactent son succès auprès des joueurs. Succès qui est mesuré par la note moyenne attribuée au jeu par des sites spécialisés (les notes sont extraites du site Métacritic -> https://www.metacritic.com). 
Il suffit d'exécuter le notebook principal (main.ipynb) pour voir nos travaux.


## Méthodologie 

### 1) Collecte des données :

Pour constituer notre base de données, nous avons choisi d'extraire les jeux vidéos répertoriés sur Wikipédia comme étant sortis après 2016. Nous avons donc scrappé la liste de leurs titres sur Wikipédia puis, pour chacun d'entre eux, nous avons récupéré la note qui leur a été attribuée dans leur review sur le site Métacritic. Cette note est un aggrégat des critiques faites par des sites spécialisés dans les jeux vidéos : le Métascore. 

Nous sommes partis du postulat que cette note était un des meilleurs indicateurs que nous pouvions trouver pour rendre compte du succès des jeux auprès des joueurs. 

Puis nous nous sommes appuyés sur une API (https://api-docs.igdb.com/#getting-started) qui permet d'obtenir de nombreuses informations sur un jeu vidéo à partir de son titre (developer, graphismes...) afin de constituer la base de données avec laquelle nous allons tenter de créer un modèle prédictif des Métascores à partir de certaines caractéristiques des jeux vidéos. 

### 2) Nettoyage des données :

Le but de cette partie a été d'obtenir un dataframe plus propre afin de faciliter son analyse. Nous avons donc transformé des variables catégorielles (comme le genre du jeu vidéo) en de nouvelle variables binaires et créer des variables composites qui nous semblaient à partir des informations du dataframe (comme la varible "Moyenne des jeux similaires". 

### 3) Analyse Descriptive :

Cette partie a consisté en l'analyse descriptive de notre dataframe afin d'avoir une idée des grandes tendances et de l'importance de chacune des variables : graphiques descriptifs, matrice de corrélation des variables, régressions simples...

### 4) Modélisation :

Enfin, le but de cette partie a été de comparer les résultats de différents modèles prédictifs afin de voir lequel est le plus efficace pour prédire la note d'un jeu à partir de ses caractéristiques. Nous avons aussi tenté une ACP afin de résumer au mieux l'information contenue dans notre dataframe et voir quelles implications cela pouvait avoir sur la qualité prédictive des différents modèles. 



## Structure du Projet

### I/ Récupération des données 
####    I/A Webscrapping des titres des jeux sur Wikipédia 
####    I/B Webscrapping des notes des jeux sur Métacritic 
####    I/C Récupération des données via l'API 


### II/ Nettoyage des données 
####    II/A Première visualisation 
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

### Webscrapping et API
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

