

# Atelier "Python pour l’analyse des données haute pression"
Cet atelier propose une initiation à l'analyse de données en utilisant le langage de programmation Python, adapté au contexte des expériences haute pression. L’objectif est de montrer un aperçu des vastes possibilités et de fournir des informations utiles à la fois pour les débutants et les utilisateurs confirmés, sans se focaliser sur la syntaxe du langage. Python bénéficie d’une grande popularité et est très utilisé dans la gestion et l'analyse de données, ainsi que pour le pilotage des expériences sur grands instruments (ESRF, Soleil...). Il figure désormais parmi les langages les plus enseignés aux étudiants en sciences.

Des tutoriels et exemples seront fournis, permettant de prendre en main le langage. Les aspects suivant seront abordés :

- Installation de Python, stratégies d'utilisation (Spyder, notebook, etc.).

- Démonstration des possibilités : programmes d'analyse de données simples, programmes avancés avec interfaces graphiques.

- Ouverture de fichiers de données aux formats ASCII et HDF5, manipulation, visualisation des données (bibliothèques numpy, matplotlib...).

- Les bibliothèques les plus utile pour diverses applications.

- Mise en pratique : ajustements non linéaire (bibliothèque LMFIT), application aux spectres de luminescence du rubis utilisé comme jauge de pression.

# Where ? 14e Forum de technologie des hautes pressions
Nouvelles frontières en haute pression : de l'instrumentation à l'analyse de données  
3-7 juin 2024 - Argelès-sur-Mer  
  
[14e Forum de technologie des hautes pressions](https://forumhp2024.sciencesconf.org/)  

# Atelier Table of contents: 
> [!NOTE]
> Silvia WIP

1. Introduction
2. Python as analytical tool and/or Instrument Control Software
3. Graphical interfaces face to face
Command based interface (Amorpheus) – Tkinter (rubycond) – Qt5(myPRL, Dioptas)
4. How to python: Spyder vs. Notebook
5. Useful libraries: matplotlib, lmfit, h5py (fabio?, vitables in Qt5?)
6. Hands on: fit a ruby signal, fit a temperature with two colors analysis

# Additional info:
> [!NOTE]
> This page Table of contents

1. Install Conda (Yiuri)
2. Spyder tips and tricks (Yiuri)
3. Jupyter Notebook (Alexis/Antoine)
4. lmfit examples (Yiuri)
5. h5py (???)
6. fit a ruby signal (???)
7. fit a temperature with two colors analysis (???)
8. Shortcuts to filename.py in my_env (Yiuri)
9. Shortcuts to app in my_env (Yiuri)


## 1. Install Conda
> [!NOTE]
> Yiuri WIP

1) Download and install Miniconda **OR** Anaconda (NOT both)

   - Miniconda  
   https://docs.anaconda.com/free/miniconda/miniconda-install/
  
   - Anaconda  
   https://docs.anaconda.com/anaconda/install/
  
> [!CAUTION]
> Do not install Miniconda/Anaconda in the default directory (C:\Users\username\anaconda3) if **username** contains spaces  
> if **username** contains spaces change the installation directory to "C:\Anaconda"

2) From anaconda prompt (windows) or terminal (Ubuntu & MAC) add conda-forge repository (required only 1 time)

```bash
conda config --add channels conda-forge
conda config --set channel_priority strict
```

3) Create a new virtual environment with name "my_env":

```bash
conda create -n my_env
```
to save time, you can directly create the environment with some installed packages, or install later (point5)

```bash
conda create -n my_env spyder lmfit matplotlib pathlib configparser
```

4) activate the virtual environment
```bash
conda activate my_env 
```
the name at the beginning of the line will change from "base" to "my_env" indicating that now you are working in the "my_env" environment
<!-- single line warning style = :warning: Never Install software in the "base" environment -->

> [!WARNING]
> Never Install software in the "base" environment
  
5) install the programs **if** you have not installed them before on point 3
```bash
conda install spyder
```

6) launch spyder

```bash
spyder
```

7) list all the virtual environments
```bash
conda env list
```
The output will show the environmet names and installation folders 

8) delete my_env
```bash
conda remove -n my_env
```

9) changing Env folder
'''bash
conda create --prefix D:\folder\my_env python=3.10 spyder lmfit matplotlib pathlib configparser 
conda activate D:\folder\my_env
conda env remove --prefix D:\folder\my_env
'''

## 2. Spyder tips and tricks
> [!NOTE]
> Yiuri WIP  

  https://docs.spyder-ide.org/3/editor.html
  
figure 1 2 3

inline plot

report
Save as HTML (Ctrl+S)

working directory
Tools => Preferences => Run
On the Panel on the right change "Working directory settings" to "The current working directory"
**Apply** 

On the Top right drop down menu change directory

> [!WARNING]
> new directory accepted if the check mark ✔ is gray (pink = NOT accepted)
  
kernel

scripts debug



## 3 Shortcuts to filename.py in my_env
right click on the link, Properties

![Shortcut_figure](https://github.com/CelluleProjet/ReadMeTest/assets/83216683/c173225f-ef17-41a2-8a44-24e50abc67e3)


**Target** : 
%windir%\System32\cmd.exe "/K" C:\Users\username\anaconda3\Scripts\activate.bat C:\Users\username\anaconda3\envs\my_env & python "D:\path_to_script\filename.py"

**Start in:**
%HOMEPATH

**Where:**

1) Anaconda or Miniconda installation folder 
C:\Users\yiuri\anaconda3\Scripts\activate.bat

2) Env folder (from command "conda env list: in conda prompt)
my_env                C:\Users\username\anaconda3\envs\my_env

3) Python script to be launched in Env, use it inside "" to account space in folder name (if any)
D:\path_to_script\filename.py

## 4 Shortcuts to app in my_env
right click on the link, Properties

![Shortcut_figure](https://github.com/CelluleProjet/ReadMeTest/assets/83216683/c173225f-ef17-41a2-8a44-24e50abc67e3)


**Target** : 
%windir%\System32\cmd.exe "/K" C:\Users\username\anaconda3\Scripts\activate.bat C:\Users\username\anaconda3\envs\my_env & app_name
  
**Start in:**
%HOMEPATH

**Where:**

1) Anaconda or Miniconda installation folder 
C:\Users\yiuri\anaconda3\Scripts\activate.bat

2) Env folder (from command "conda env list: in conda prompt)
my_env                C:\Users\username\anaconda3\envs\my_env

3) app_name installed in Env (like i.e. spyder)
spyder

# Contacts

**Alexis FORESTIER**
- mail or not email ... ???

**Antoine HILBERER**
- antoine.hilberer@cea.fr

CEA or Lab or ... ???

**Yiuri GARINO**  
- yiuri.garino@cnrs.fr
   
**Silvia BOCCATO**
- silvia.boccato@cnrs.fr

<img src="https://github.com/CelluleProjet/Rubycond/assets/83216683/b728fe64-2752-4ecd-843b-09d335cf4f93" width="100" height="100">
<img src="https://github.com/CelluleProjet/Rubycond/assets/83216683/0a81ce1f-089f-49d8-ae65-d19af8078492" width="100" height="100">

[Cellule Projet](http://impmc.sorbonne-universite.fr/fr/plateformes-et-equipements/cellule-projet.html) @ [IMPMC](http://impmc.sorbonne-universite.fr/en/index.html)

## License ???
there are no scripts here, so license or copyright or copyleft of nothing ...
this is a c&p what I use usually

**Main Title**

Copyright (c) 2022-2023 ???

**Main Title** is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.
This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see <https://www.gnu.org/licenses/>.

# Usefuls Links for this page

[Basic writing and formatting syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)  
[Rubycond](https://github.com/CelluleProjet/Rubycond)  
[Amorpheus](https://github.com/CelluleProjet/Amorpheus)  
[Smile](https://github.com/CelluleProjet/Smile)  

