# PythonProjects
## Tom Rossa, Jean-Lou Valeau, Anthonin Izoret

Bienvenue sur le GitHub présentant notre projet Python pour la data science réalisé dans le cadre de notre année de M1 à l'ENSAE.

Notre objectif est le suivant : nous souhaitons identifier les caractéristiques d'un jeu vidéo qui impactent son succès pour ensuite prédire le succès du jeu en fonction de ses caractéristiques.

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

Pour exécuter l'intégralité du notebook principal (main.ipynb), il est nécessaire d'installer au préalable les packages suivants:

### Webscrapping
```bash

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

Vous pouvez copier-coller ces instructions dans votre fichier README.md pour une meilleure lisibilité sur GitHub. N'hésitez pas à ajuster la mise en forme selon vos préférences.

