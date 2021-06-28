---
title: Download and Link to Python Packages
types: [tutorial,] 
---

# Download and Link to Python Packages

Say you want to run a python package from source using a git repository.  Here is a quick set of steps, using the pynamics repository as an example:

1. Install and set up git extensions.
1. clone the pynamics repository on your local computer
    1. go here: https://github.com/idealabasu/code_pynamics
    1. click on clone and copy the path:
    1. right click in a destination directory and select the clone menu item
1. add the path to your new repository to your system variables
    1. open up explorer, navigate to and right click on"this pc-->properties-->advanced system settings-->environment variables"
    1. add a new PYTHONPATH key in your user variables if it does not exist
    1. add a path to the list of packages inside the repository folder, ie "C:\Users\username\(wherever you've placed the repo)\code_pynamics\python".  The subfolders of this folder are all python packages that can be searched for now.
1. test the install by importing one of the packages (subfolders of "python") in a blank python script.