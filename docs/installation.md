# Python Installation with conda distribution
*Conda* is the most common package manager for the Python programming language, allowing installation of a distribution of Python together with addon modules.

It can be installed alone (light weight if using [miniconda](https://docs.anaconda.com/free/miniconda/miniconda-install/) for instance, but requires some work to reach a usable configuration), or wrapped in a larger distribution for data-science called *Anaconda*.

**Table of content:**
 - [Easiest installation](#Anaconda)
   - [Get started](#startup)
   - [How to install new packages](#packages)
 - [Use virtual environments](#venv)
 - [Create Windows shortcuts](#shortcuts)

<a id="Anaconda"></a>
## Easiest installation

<a id="startup"></a>
### Get started

1) Download the __Anaconda__ installer from the official website: [https://www.anaconda.com/download/success](https://www.anaconda.com/download/success).

![](tuto_screenshots/download_installer.PNG)


2) Run the installer and follow the steps without changing any options, unless: if your **username** on Windows contains spaces, do not install in the default directory (C:\Users\username\anaconda3). If your **username** contains spaces, change the installation directory to "C:\Anaconda".


3) You now have a new software called __Anaconda Navigator__ in the startup menu. Launch it. You will see a number of different applications that you can use:

![](tuto_screenshots/navigator.PNG)


We are mainly interested in __Spyder__ and __Jupyter Notebook__ in this workshop.


4) Run __anaconda prompt__ from __Anaconda Navigator__ (Windows) or run any terminal (GNU/Linux, Mac).  

![](tuto_screenshots/navigator_prompt.PNG)


We will add conda-forge repository (__this is required only one time at installation__). This will allow you to install all the packages you may need from the *conda-forge* repository later. 
Run the following two commands one after the other as shown:

```bash
conda config --add channels conda-forge
conda config --set channel_priority strict
```

![](tuto_screenshots/condachannels1.PNG)
![](tuto_screenshots/condachannels2.PNG)

__You have python installed and set up.__ 

*Instead of installing the full Anaconda distribution you may be interested by [the more lightweight Miniconda distribution](https://docs.anaconda.com/free/miniconda/miniconda-install/), but do not install both!*

<a id="packages"></a>
### How to install new packages

To install any new package, run the __anaconda prompt__ (see above). Then run the following command (example here to install `lmfit`) :

```
conda install lmfit
```

![](tuto_screenshots/install_lmfit.PNG)

When asked to proceed, type `y` and `enter`. 

The new package is installing.


__To install several packages, you can use a single command line :__
```
conda install numpy matplotlib scipy lmfit h5py hdf5plugin fabio pyFAI tifffile
```

<a id="venv"></a>
## Use virtual environments
  
Create a new virtual environment with name "my_env":

```
conda create -n my_env
```
to save time, you can directly create the environment with some installed packages, or install later (see below)

```
conda create -n my_env spyder lmfit matplotlib pathlib configparser
```

Activate the virtual environment:

```
conda activate my_env 
```
The name at the beginning of the line will change from "base" to "my_env" indicating that now you are working in the "my_env" environment
__Warning:__ Never Install software in the "base" environment

Install the programs you want, if not already installed at creation of the virtual environment, e.g.:
```
conda install spyder
```

You can now launch spyder in my_env:
```
spyder
```

List all the virtual environments:
```
conda env list
```
The output will show the environment names and installation folders 

Delete my_env:
```
conda remove -n my_env
```

Changing Env folder:
```
conda create --prefix D:\folder\my_env python=3.10 spyder lmfit matplotlib pathlib configparser
conda activate D:\folder\my_env
conda env remove --prefix D:\folder\my_env
```

<a id="shortcuts"></a>
## Create Windows shortcuts to execute your .py file with one click
To create a shortcut to execute `filename.py` within its associated virtual environment `my_env`, start by right-clicking the file and click 'Create a shortcut'.

Right click on the created link, go to 'Properties'.

![Shortcut_figure](https://github.com/CelluleProjet/ReadMeTest/assets/83216683/c173225f-ef17-41a2-8a44-24e50abc67e3)

Change the **Target** to: 
```
%windir%\System32\cmd.exe "/K" C:\Users\username\anaconda3\Scripts\activate.bat C:\Users\username\anaconda3\envs\my_env & python "D:\path_to_script\filename.py"
```

**Start in:**
```
%HOMEPATH
```

**Where:**

Anaconda or Miniconda installation folder 
```
C:\Users\username\anaconda3\Scripts\activate.bat
```

Env folder (from command "conda env list: in conda prompt)
my_env                C:\Users\username\anaconda3\envs\my_env

Python script to be launched in Env, use it inside "" to account for space in folder name (if any)
```
D:\path_to_script\filename.py
```
## Shortcuts to an app in my_env (e.g. spyder)

Right click on the link, Properties

![Shortcut_figure](https://github.com/CelluleProjet/ReadMeTest/assets/83216683/c173225f-ef17-41a2-8a44-24e50abc67e3)


**Target** : 
```
%windir%\System32\cmd.exe "/K" C:\Users\username\anaconda3\Scripts\activate.bat C:\Users\username\anaconda3\envs\my_env & app_name
  ```

**Start in:**
```
%HOMEPATH
```
**Where:**

Anaconda or Miniconda installation folder 
C:\Users\username\anaconda3\Scripts\activate.bat

Env folder (from command "conda env list: in conda prompt)
my_env                C:\Users\username\anaconda3\envs\my_env

app_name installed in Env (like i.e. spyder)
spyder
