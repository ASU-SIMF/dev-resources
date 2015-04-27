# Python Windows Setup Instructions 

We will be using Python 2.7.9 to develop our applications using a distirbution provided by Continuum Analytics. You will need to perform the following steps in order to setup your system:

1.  Install Anaconda from Continuum Analytic's website
2.  Create a virtual environment for SIM Fund projects
3.  Install a standard set of Python packages
4.  Test installation

## Installing Anaconda 

We will first need to install [Anaconda](https://store.continuum.io/cshop/anaconda/) onto our Windows system.  Anaconda is a free, enterprise-ready Python distribution for scientific computing.   It simplifies installing Python scientific libraries such as NumPy, SciPy, Pandas, and others which require a compiler to install succesfully.  Download Anaconda (Python 2 Version) [here](http://continuum.io/downloads).  Verify that the program installed correctly by running `python --version` in the command line.  

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/version.PNG)

## Creating a Virtual Enviroment 

Next, we will setup a virtual environment to run all our project code.  A virtual environment is a tool to keep the dependencies required by different projects in separate places. It solves the “Project X depends on version 1.x but, Project Y needs 4.x” dilemma, and keeps your global site-packages directory clean and manageable ([source](http://docs.python-guide.org/en/latest/dev/virtualenvs/)).

Create a virtual environment using conda (Anaconda's built-in package manager) by running the commands:

`conda create -n simfenv python=2.7.9`

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/env.PNG)

Activate your virutal environment by running:

`activate simfenv`

You can check all of your environments by running `conda info -e`.  Notice, that your environment appears in brackets on the left side of the command line `[simfenv]`.

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/activate.PNG)

## Install Packages

Our last step is to install all the required Python packages.  Again, we will be using conda to accomplish this goal.  Run the command:

`conda install --file "C:\Users\USERNAME\...\GitHub\dev-resources\setup\win-package-list.txt"` 

You will need to replace the directory path with the loaction of the `win-package-list.txt` file on your computer.  

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/install.PNG)

## Verifying Installation

To verify that the installation was successful, open a Python prompt on the command line.  Attempt to import pandas, numpy, and scipy.  If you do not receive an error message your installation was successful!

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/check%20install.PNG)
