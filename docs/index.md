![forum](logos/bandeau.jpg)
<img src="logos/cea.png" width="100" height="100">
<img src="logos/cnrs.png" width="100" height="100">


# Atelier "Python pour l’analyse des données haute pression"

__[14e Forum de technologie des hautes pressions](https://forumhp2024.sciencesconf.org/)__

__Nouvelles frontières en haute pression : de l'instrumentation à l'analyse de données__

__3-7 juin 2024 - Argelès-sur-Mer__

Cet atelier propose une initiation à l'analyse de données en utilisant le langage de programmation Python, adapté au contexte des expériences haute pression. L’objectif est de montrer un aperçu des vastes possibilités et de fournir des informations utiles à la fois pour les débutants et les utilisateurs confirmés, sans se focaliser sur la syntaxe du langage. Python bénéficie d’une grande popularité et est très utilisé dans la gestion et l'analyse de données, ainsi que pour le pilotage des expériences sur grands instruments (ESRF, Soleil...). Il figure désormais parmi les langages les plus enseignés aux étudiants en sciences.

# Ressources 

* [Slides de présentation](Slides_AtelierPython.pdf). 
* [Tutoriel : installation de python, de packages additionnels, et utilisation des environnements virtuels](installation.md)
* Fit d'un spectre de luminescence du rubis. [Visualiser](https://github.com/alexisforestier/Atelier-Python-HP/blob/main/Rubis_demo_fit/Rubis_demo.ipynb) [Télécharger](https://github.com/alexisforestier/Atelier-Python-HP/raw/main/zips/Rubis_demo_fit.zip)
* Analyse d'un spectre de rayonnement de corps noir. [Visualiser](https://github.com/alexisforestier/Atelier-Python-HP/blob/main/Corps_Noir_demo_fit/Corps_Noir_demo.ipynb) [Télécharger](https://github.com/alexisforestier/Atelier-Python-HP/raw/main/zips/Corps_Noir_demo_fit.zip)
* Ouverture et intégration azimuthale d'une plaque image de diffraction des rayons X au format HDF5 (.h5) [Visualiser](https://github.com/alexisforestier/Atelier-Python-HP/blob/main/Plaque_image_XRD_demo/Plaque_image_h5.ipynb) [Télécharger](https://github.com/alexisforestier/Atelier-Python-HP/raw/main/zips/Plaque_image_XRD_demo.zip)

# Autres ressources utiles

### Bases

* [Un très bon notebook pour apprendre les bases de python de manière interactive](https://github.com/jupyter/mozfest15-training/blob/master/00-python-intro.ipynb)
* Les bases de python : boucles for/while, tests if else, fonctions et opérateurs, types natifs, listes, tuples et dictionnaires etc. : [sur courspython.com](https://courspython.com/bases-python.html)
* Manipulation de tableaux numpy : [doc. de numpy](https://numpy.org/doc/stable/user/absolute_beginners.html)
* Indexation des tableaux numpy : [dans la documentation de numpy](https://numpy.org/doc/stable/user/basics.indexing.html), voir aussi : [le slicing en python](https://anislerouge.com/tutorial-python-slicing/)
* La librairie pandas, utilisation du type DataFrame : [documentation de pandas](https://pandas.pydata.org/docs/user_guide/index.html)
* Indexation des DataFrame de pandas : [dans la documentation de pandas](https://pandas.pydata.org/docs/user_guide/indexing.html)
* [Les compréhension de listes](https://www.docstring.fr/glossaire/comprehension-de-liste/)
* [Types mutables, non-mutables](https://bouquinpython.readthedocs.io/fr/latest/mutabilite.html)
* Gestion des exceptions, try...except : [sur docs.python.org](https://docs.python.org/fr/3/tutorial/errors.html)
* Quelques bases de programmation orientée objet : [sur courspython.com](https://courspython.com/classes-et-objets.html)
* Documentation officielle de Python [sur docs.python.org](https://docs.python.org/fr/3/index.html).
* Documentation officielle de la distribution Conda, utilisée par Anaconda/Miniconda : [sur docs.conda.io](https://docs.conda.io/en/latest/#)
* Documentation officielle de l'éditeur/IDE Spyder : [sur docs.spyder-ide.org](https://docs.spyder-ide.org/5/index.html)

### Quelques programmes orientés haute-pression basés sur Python

* [__Dioptas__](https://www.clemensprescher.com/programs/dioptas), programme graphique très complet (écrit en python + Qt) pour l'analyse des données de diffraction des rayons X sous haute pression
* [__Amorpheus__](https://github.com/CelluleProjet/Amorpheus), un programme python pour l'analyse des données de diffraction des rayons X sur les liquides et solides amorphes, voir la publication associée : [Boccato et al. High Pressure Research 2022, vol. 42, No. 1, 69–93](https://www.tandfonline.com/doi/full/10.1080/08957959.2022.2032032)
* [__myPGM__](https://github.com/AHilberer/myPGM), un outil avec interface graphique écrit en python avec Qt pour le post-traitement (fit...) des mesures spectroscopiques de jauges de pression (rubis, samarium, Raman du nitrure de bore cubique, edge Raman du diamant, vibron H2)
* [__RubyCond__](https://github.com/CelluleProjet/Rubycond), un outil graphique pour la mesure de pression avec la luminescence du rubis, avec pilotage en direct du spectromètre OceanOptics (écrit en python + tkinter)
* [__Smile__](https://github.com/CelluleProjet/Smile), un outil pour la visualisation via caméra USB de microscope
* [__h5temperature__](https://github.com/alexisforestier/h5temperature), un outil graphique (écrit en python + Qt) pour l'analyse des mesures de température par pyrométrie optique de l'ESRF au format h5

### Tracé de graphiques

* [Guide de l'utilisateur matplotlib](https://matplotlib.org/stable/users/index.html)
* [Galerie d'exemples de graphiques matplotlib](https://matplotlib.org/stable/gallery/index.html)
* [Liste des noms de couleurs de matplotlib](https://matplotlib.org/stable/gallery/color/named_colors.html#css-colors)
* [Liste des types de symboles de matplotlib](https://matplotlib.org/stable/api/markers_api.html)
* Une autre bilbiothèque qui permet de réaliser des graphiques interactifs dans un notebook jupyter : [plotly](https://plotly.com/python/)
* D'autres bibliothèques pour le tracé graphique, Seaborn et Bokeh : [galerie d'exemples de Seaborn](https://seaborn.pydata.org/examples/index.html), [galerie d'exemples de Bokeh](https://docs.bokeh.org/en/latest/docs/gallery.html)

### Interfaces graphiques 

* La bibliothèque Qt, qui permet le plus de possibilités (bibliothèque issue du C++ et utilisée pour de nombreux logiciels) : [documentation](https://doc.qt.io/qtforpython-5/index.html), [une introduction sur courspython.com](https://courspython.com/interfaces.html), un très bon site avec de nombreux exemples pour les figures, les tableaux etc... : [pythonguis.com](https://www.pythonguis.com/tutorials/creating-your-first-pyqt-window/)
* La bibliothèque tkinter : [documentation](https://docs.python.org/fr/3/library/tkinter.html)

### Fichiers au format HDF5

* Un outil avec interface graphique pour visualiser l'arborescence de fichiers h5 : [ViTables](https://vitables.org/)
* Un autre outil avec de nombreuses fonctionnalités pour l'analyse des données : [PyMca](http://www.silx.org/doc/PyMca/dev/index.html)
* Accéder au contenu d'un fichier h5 avec la librairie h5py : [documentation de h5py](https://docs.h5py.org/en/stable/quick.html)

### Accélerer Python : optimisation des temps d'exécution

* [Cython](https://cython.org/) est une extension de Python qui permet d'appeler des fonctions C et de déclarer des types statiques C. Cython convertit le code en C/C++ puis le compile afin d'obtimiser les performances, [informations et exemple simple sur Wikipedia](https://fr.wikipedia.org/wiki/Cython).
* [Numba](https://numba.pydata.org/) permet de compiler du code python (en particulier employant numpy) afin de se rapprocher des performances du C ou du FORTRAN.

### Générer des executables
* Le package PyInstaller permet de créer des executables à partir de codes python (utilisé notamment par Dioptas) : [documentation](https://pyinstaller.org/en/stable/) 

### Contacts

* **Alexis FORESTIER**,  alexis.forestier@cea.fr
* **Antoine HILBERER**,  antoine.hilberer@cea.fr
* **Yiuri GARINO**,      yiuri.garino@cnrs.fr
* **Silvia BOCCATO**,    silvia.boccato@cnrs.fr

