# Python Windows Setup Instructions 

We will be using Python 2.7.9 to develop our applications using a Python distirbution provided by Continuum Analytics. You will need to perform the following steps in order to setup your system:

1.  Install Anaconda from Continuum Analytic's website
2.  Create a virtual enviroment for SIM Fund projects
3.  Install a standard set of Python packages
4.  Test installation

## Installing Anaconda 

We will first need to install [Anaconda](https://store.continuum.io/cshop/anaconda/) onto our Windows system.  Anaconda is a free enterprise-ready Python distribution for scientific computing.   It greatly simplifies installing Python scientific libraries such as NumPy, SciPy, Pandas, and others which require a compiler in order to install succesfully.  Download Anaconda (Python 2 Version) [here](http://continuum.io/downloads).  Verify that the program installed correclty by running `python --version` in the command line.  

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/version.PNG)

## Creating a Virtual Enviroment 

Next we will setup a virutal enviorment to run all our project code.  A Virtual Environment is a tool to keep the dependencies required by different projects in separate places, by creating virtual Python environments for them. It solves the “Project X depends on version 1.x but, Project Y needs 4.x” dilemma, and keeps your global site-packages directory clean and manageable ([source](http://docs.python-guide.org/en/latest/dev/virtualenvs/)).

Create a virtual enviroment using conda (Anaconda's built-in package manager) by running the commands:

`conda create -n simfenv python=2.7.9`

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/env.PNG)

Activate your virutal enivorment by running:

`activate simfenv`

You can check all of you enviorments by running `conda info -e`.  Notice, that your enviroment appears in brackets on the left side of the command line `[simfenv]`.

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/activate.PNG)

## Install Packages

Our last step is to install all the required Python packages.  Again, we will be using conda to accompish this goal.  Run the command:

`conda install --file "C:\Users\USERNAME\...\GitHub\devresources\setup\win-package-list.txt"` 

You will need to replace the directory path with the loaction of the `win-package-list.txt` file on your computer.  

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/install.PNG)

## Verifying Installation

To verify that the installation was sucessfull open a Python promprt on the command line.  Attempt to import pandas, numpy, and scipy.  If you do not receive an error message your installation was sucesfull!

![alt text](https://github.com/ASU-SIMF/devresources/blob/master/setup/img/check%20install.PNG)
