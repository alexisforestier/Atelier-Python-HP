# Python Installation with conda distribution
## The easiest way  

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

# How to install new packages 

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


## Using virtual environments
  
Create a new virtual environment with name "my_env":

```
conda create -n my_env
```
to save time, you can directly create the environment with some installed packages, or install later (point5)

```
conda create -n my_env spyder lmfit matplotlib pathlib configparser
```

Activate the virtual environment:

```
conda activate my_env 
```
the name at the beginning of the line will change from "base" to "my_env" indicating that now you are working in the "my_env" environment
__Warning__ Never Install software in the "base" environment

install the programs you want, if you have not installed them already at creation of the virtual environment:
```
conda install spyder
```

You can now launch spyder
```
spyder
```

List all the virtual environments:
```
conda env list
```
The output will show the environment names and installation folders 

8) delete my_env:
```
conda remove -n my_env
```

9) changing Env folder
'''
conda create --prefix D:\folder\my_env python=3.10 spyder lmfit matplotlib pathlib configparser 
conda activate D:\folder\my_env
conda env remove --prefix D:\folder\my_env
'''
