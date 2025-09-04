# HW0: Environment setup for COS597

In this initial assignment, the goals are:

1. to set up a working programming environment using either conda environments.
2. to get acclimated with Jupyter Lab, which is required for all assignments in this course.

**Please read through readme.md carefully**

**After setting up the assignment environment, please look into the Jupyter notebook (*.ipynb)**

## Anaconda/Miniconda Environment Setup (Python Environment)

### Installation
This course uses **Python 3**. Python 2 will not work for these assignments, and all assignments will be graded with Python 3 on our end. Python 2 is [leaving the data science programming stack](https://pythonclock.org/) on Jan 1, 2020.

The easiest way to get set up is to use [**miniconda**](https://docs.conda.io/en/latest/miniconda.html). However, the full version of Anaconda is totally fine as well [**Anaconda**](https://docs.anaconda.com/anaconda/install/). I personally use Anaconda since it comes with a lot of functionality. Still, miniconda is the right environment for you if you have limited disk space.

Install the appropriate version of anaconda/miniconda for your operating system (select the Python 3 version). After miniconda is installed, you should be able to run `conda`. If you get an error (e.g. `-bash: conda: command not found`), make sure to source your bash file afterward (`source ~/.bash_profile` worked for Prem) or if on Windows, restart your terminal. For Windows you might need to use the "Anaconda prompt" to navigate with conda. 
It is not unheard of that people are experiencing problems installing conda on your platform. In that case, you might want to look in the system paths and replace the standard Python version with the anaconda path. Google (and stackoverflow) is also a great resource to get these problems sorted out.

### cos597 Environment
Now let's create a virtual environment. Virtual environments are a simple way to isolate all the dependencies for a particular project. They make it easy to work on multiple projects without them interfering with each other (e.g., conflicting versions of libraries between tasks). 

If you are new to CONDA please read through this article. It should really help you get started and understand better what this is all about
https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html

Now, let's get started setting everything up. Here's the command:

``conda create -n COS597 python``

`COS597` is the name for the environment, and it can be used for all assignments. Its name can be whatever you want, just make sure to remember it! You can even use your *base* environment. However, we recommend using separate environments for different classes, projects, etc. 

Once the environment is created, you should activate it with:

``conda activate COS597``

Your shell/cmd/bash might look something like `(COS597) your folder/name`. The environment name is in parenthesis, indicating that it is active. If this is not the case, something likely went wrong. 

Now let's install a few packages that might come in useful throughout the course. Note that you might need to install more packages during the class. This is just a selection of packages we consider essential. You are free to install whatever package you might consider useful.

Do this by navigating to this folder's top root on the terminal and running, with your activated COS597 conda environment:

``pip install -r requirements.txt``

Note that we are installing many packages. This can take a while since all of those packages need to be downloaded first. If a package cannot be installed, you google to figure out what went wrong and install it manually.

Great! Your environment is all set up. You can check if those environments are correctly installed, by simply open an "ipython"-console and trying to import several of the packages in requirements.txt


## Jupyter Lab

We installed our required libraries from the requirements.txt for our environment 'COS597'.

Make sure that you have activated the conda environment of `COS597`; otherwise the packages might not be visible to you:

`conda activate COS597`

We will be using Jupyter Lab throughout the quarter.
Note that you can also use Jupyter Notebook and a different IDE for completing the python files.
However, we highly recommend sticking with Jupyter Lab since it provides the complete IDE experience since we have designed this course this way.

To start Jupyter Lab, the easiest way is to `cd` into the specific homework assignment (here it will be in the directory where assignment0.ipynb is present) and simply enter:

`jupyter lab`

If some problem persists after this command, the jupyter libraries might not have been installed correctly.
In that case, just run these commands and any missing components will be installed:

```
pip install ipykernel
pip install jupyter
pip install jupyterlab
```

Once you can open jupyter lab, try a simple import and see if there is no compilation issue once you execute it (using ctrl + Enter). Example:

`import numpy as np`

To use all the packages and libraries we installed in our COS597 conda environment, we need to create a corresponding Jupyter "environment".
(Make sure that you have activated the conda environment of `COS597`):

`python -m ipykernel install --name=COS597 --user`

To check if this was successful:
Go to Jupyter Lab (or notebook) -> Go To "Change Kernel" option -> you should now see "COS597" as an option. Select that and you are good to start your assignment!

Each assignment will consist of a coding and writing task. In the initial homework, the coding and writing tasks are straightforward. They should help you get started with everything.


# Coding Task

1. Open the Jupyter Notebook (*.ipynb)
2. Implement the missing functions ( that show a `NotImplementedError` when running) in the `src` folder as indicated inside the jupyter notebook. You are welcome to use the numpy implementations.
3. Test the implemented functions in the jupyter notebook.

After completing the task, submit the zipped code with the Jupyter to Canvas. No need to write a report.  
