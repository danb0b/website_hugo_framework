---
title: Installing Anaconda
subtitle: for foldable robotics topics
types: [tutorial,] 
class_name: EGR557:Foldable Robotics
---

# Installing Anaconda

## Introduction

Anaconda is a distribution of Python that includes the ability to manage packages using the conda package manager as well as the ability to create and manage _environments_, or collections of packages that work together.  Anaconda ships as a ~500 Mb installer.  This tutorial gets you started with miniconda, a slimmed down installer that allows you to install just the packages you need.  Below are the steps to gettting a working installation of Python with all the packages you need for _Foldable Robotics_.

<!--
## Optional Prerequisites
1. Install Virtualbox
1. Download Windows from [MyApps](https://myapps.asu.edu)
1. [Miktex](https://miktex.org/download).  This is required to save jupyter files directly to pdf.
-->
## Required Steps

1. Download and install [Miniconda](https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe)
    * install for all users (if possible).
    * install in the c:/Anaconda3/ directory rather than the supplied default.
    * check the box to add to system path
    * keep all other defaults.
1. _(optional)_ If you were not able to check the box to add anaconda to your system path,  
    1. go to file explorer
    1. right click on my computer
    1. on the left menu sele advanced system settings
    1. click on environment variables
    1. in the lower window, find the path variable, and click edit
    1. (in windows 10), click edit text.
    1. Go to the *end* of the string, and paste in the following, _ensuring consistency with the actual install location_.  **Important:** Make sure there are semicolons between each path.  Do not replace any other items in the path. 
     
        ```
        C:\Anaconda3;C:\Anaconda3\Scripts;C:\Anaconda3\Library\bin;
        ```

1. **Install standard packages.** open up powershell *in administrator mode*, and paste the following code(line by line):

    ```
    Set-ExecutionPolicy remotesigned
    conda init powershell
    conda install -y anaconda
    conda install -y django paramiko pyqtgraph pyopengl gitpython pycairo shapely pycrypto
    python -m pip install --upgrade pip
    pip install meshio pygmsh ezdxf pandoc-fignos pandoc-eqnos pypdf4 service_identity ftd2xx pygithub twine paho-mqtt
    pip install ntplib pygame pysftp pyserial
    conda update -y --all
    ```

1. Install foldable-robotics-specific packages.

    ```
    pip install pypoly2tri idealab_tools foldable_robotics pynamics
    ```


<!--
### Ubuntu Installation

#### Install Anaconda
1. Open a terminal window(ctrl+alt+T)
1. Paste the following code(line by line)

```bash
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh;
bash miniconda.sh -b -p $HOME/miniconda
export PATH="$HOME/miniconda/bin:$PATH"
echo "export PATH="$HOME/miniconda/bin:$PATH"" >> ~/.bashrc
conda update conda
conda install python=3.6 setuptools cython pyyaml numpy scipy spyder sympy
conda install pyopengl pyqt pyqtgraph matplotlib jupyter pillow lxml pandoc
conda install -c conda-forge shapely
pip install ezdxf imageio meshio 
pip install pypoly2tri idealab_tools foldable_robotics pynamics
```
-->

<!--
## Advanced: Creating a custom environment

An environment is a nice way to sandbox your install from perhaps other python projects which need different, conflicting packages.  If you want more control over your installation, do this instead of the default way of installing packages in your root installation.  [Learn More](http://conda.pydata.org/docs/using/envs.html).

### Windows

1. Open up cmd *in administrator mode*, and paste the following code(line by line):

```cmd
conda create -n myenvironmentname
activate myenvironmentname
conda update conda
conda install python=3.6 setuptools cython pyyaml numpy scipy spyder sympy
conda install pyopengl pyqt pyqtgraph matplotlib jupyter pillow lxml pandoc
conda install -c conda-forge shapely
pip install ezdxf imageio meshio 
pip install pypoly2tri idealab_tools foldable_robotics pynamics
```

### Ubuntu

```cmd
wget https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh -O miniconda.sh;
bash miniconda.sh -b -p $HOME/miniconda
export PATH="$HOME/miniconda/bin:$PATH"
echo "export PATH="$HOME/miniconda/bin:$PATH"" >> ~/.bashrc
conda update conda
conda install python=3.6 setuptools cython pyyaml numpy scipy spyder sympy
conda install pyopengl pyqt pyqtgraph matplotlib jupyter pillow lxml pandoc
conda install -c conda-forge shapely
pip install ezdxf imageio meshio 
pip install pypoly2tri idealab_tools foldable_robotics pynamics
```

### Using your custom environment

To activate your environment you have to type

```cmd
activate myenvironmentname
```

or, in Ubuntu,

```bash
source activate myenvironmentname
```

to use this environment.
-->
Now you are Ready to open either spyder or jupyter, two good environments, to start coding!

## References
* [Managing Conda Environments](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)
