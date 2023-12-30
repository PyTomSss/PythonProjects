# PythonProjects
## Tom Rossa, Jean-Lou Valeau, Anthonin Izoret


Bienvenue sur le github présentant notre projet de python pour la data science réalisé dans le cadre de notre année de M1 à l'ENSAE. 

Notre objectif est le suivant : nous souhaitons identifier les caractéristiques d'un jeu vidéo qui impactent son succès pour ensuite prédire le succès du jeu en fonction de ses caractéristiques.  

Voici la structure de notre projet : 

I/ Récupération des données 
    I/A Webscrapping des titres des jeux sur Wikipédia 
    I/B Webscrapping des notes des jeux sur metacritic 
    I/C Webscrapping des autres données 

II/ Nettoyage des données extraites
    II/A Premier nettoyage des données 
    II/B Reformatage et standardisation des données dans le dataframe 

III/Représentatation et analyse descriptive  
    III/A Description de la base et visualisation 
        III/A/1 Répartition des différents types de jeux vidéos 
        III/A/2 Répartition des notes des jeux vidéos
    III/B Corrélations entre les variables 
        III/B/1 Matrice des corrélations 
        III/B/2 Régressions simples

IV/ Modélisation
    IV/A/ Régressions multiples
    IV/B/ Analyse en Composantes Principales

V/ Conclusion 

Pour exécuter l'intégralité du notebook principal (main.ipynb) il est nécessaire d'installer au préalable les packages suivants: 

Pour le webscrapping :

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


Pour la visualisation et l'analyse descriptive: 

!pip install plotly
!pip install fancyimpute

from collections import Counter
import numpy as np
import pandas as pd
import ast
import matplotlib.pyplot as plt
from matplotlib.colors import LinearSegmentedColormap
import plotly.express as px


Pour la modélisation: 

from sklearn.linear_model import LinearRegression
from sklearn.model_selection import train_test_split
import sklearn.metrics
import seaborn as sns
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import RobustScaler
from fancyimpute import KNN
from sklearn.cluster import KMeans
import statsmodels.api as sm
import statsmodels.formula.api as smf
from sklearn.linear_model import LassoCV
from sklearn.linear_model import RidgeCV
from sklearn.metrics import mean_squared_error, mean_absolute_error

# PythonProjects
## Tom Rossa, Jean-Lou Valeau, Anthonin Izoret

Bienvenue sur le GitHub présentant notre projet Python pour la data science réalisé dans le cadre de notre année de M1 à l'ENSAE.

Notre objectif est le suivant : nous souhaitons identifier les caractéristiques d'un jeu vidéo qui impactent son succès pour ensuite prédire le succès du jeu en fonction de ses caractéristiques.

## Structure du Projet

### I/ Récupération des données
   #### I/A Webscrapping des titres des jeux sur Wikipédia
   #### I/B Webscrapping des notes des jeux sur Metacritic
   #### I/C Webscrapping des autres données

### II/ Nettoyage des données extraites
   #### II/A Premier nettoyage des données
   #### II/B Reformatage et standardisation des données dans le dataframe

### III/ Représentation et analyse descriptive
   #### III/A Description de la base et visualisation
       #### III/A/1 Répartition des différents types de jeux vidéo
       #### III/A/2 Répartition des notes des jeux vidéo
   #### III/B Corrélations entre les variables
       #### III/B/1 Matrice des corrélations
       #### III/B/2 Régressions simples

### IV/ Modélisation
   #### IV/A Régressions multiples
   #### IV/B Analyse en Composantes Principales

### V/ Conclusion

## Installation des Packages

Pour exécuter l'intégralité du notebook principal (main.ipynb), il est nécessaire d'installer au préalable les packages suivants:

### Webscrapping
```bash
!pip install unicode
!pip install unidecode
!pip install requests_html
!pip install igdb-api-v4
!pip install requests
```

### Visualisation et Analyse Descriptive
```bash
!pip install plotly
!pip install fancyimpute
```

### Modélisation
```bash
!pip install scikit-learn
!pip install seaborn
!pip install fancyimpute
!pip install statsmodels
```

## Importation des Packages

```python
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
```


    

