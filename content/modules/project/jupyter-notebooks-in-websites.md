---
title: Working with Jupyter Notebooks in your website
types: [tutorial,] 
---

## Introduction

The point of this tutorial is to show you how to add a compiled jupyter notebook to your website in a way that it can be viewed.  There are two possible ways

1. Save the compiled notebook (.ipynb) directly to your website and use a third party site to view content
1. Export the compiled notebook to html or markdown and post to your website

Both methods are relatively easy to do and neither is more preferable than the other.

### Option 1: Save the complied notebook directly

1. Start Jupyter notebook by opening up a command terminal and typing ```jupyter notebook```
1. In Jupyter notebook, load the notebook and select the "kernel" --> "restart and run all" menu item.

    [![](../../figures/notebooks-in-website/15.png){width=25%}](../../figures/notebooks-in-website/15.png){target="_blank"}

1. Save the notebook, then select "file" --> "close and halt"

    [![](../../figures/notebooks-in-website/14.png){width=25%}](../../figures/notebooks-in-website/14.png){target="_blank"}

1. Navigate to your github repository and select the "files" --> "upload files" menu item.

    [![](../../figures/notebooks-in-website/16.png){width=25%}](../../figures/notebooks-in-website/16.png){target="_blank"}

1. Select the .ipynb file, upload, and commit.

    [![](../../figures/notebooks-in-website/17.png){width=25%}](../../figures/notebooks-in-website/17.png){target="_blank"}

1. Create a special link to your file
    1. Open up index.md or whatever file you would like to point to the new notebook from.  Select edit 

        [![](../../figures/notebooks-in-website/18.png){width=25%}](../../figures/notebooks-in-website/18.png){target="_blank"}

    1. Add a new link.  Remember, that links look like ```[link text](http://www.mycustomurl.com/path/to/file)```.  In our case, the link will start with ```https://nbviewer.jupyter.org/url/``` and end with the path to your file, ```danaukestest01.github.io/vectors.ipynb```.  The link text can be whatever you want it to be.  So, for a full example, the whole link to an example file would look like this

        ```
        [link to vectors notebook](https://nbviewer.jupyter.org/url/danaukestest01.github.io/vectors.ipynb)
        ```
1. Save and commit your changes to index.md
1. Navigate to your website (myusername.github.io)

    [![](../../figures/notebooks-in-website/19.png){width=25%}](../../figures/notebooks-in-website/19.png){target="_blank"}

1. Try out the new link.

    [![](../../figures/notebooks-in-website/20.png){width=25%}](../../figures/notebooks-in-website/20.png){target="_blank"}


### Option 2: 

1. Start Jupyter notebook by opening up a command terminal and typing ```jupyter notebook```
1. Make sure your notebook starts with a markdown header that looks like the following:

    ```
    ---
    title: this is a simple juptyer notebook
    ---
    ```

1. In Jupyter notebook, load the notebook and select the "kernel" --> "restart and run all" menu item.

    [![](../../figures/notebooks-in-website/15.png){width=25%}](../../figures/notebooks-in-website/15.png){target="_blank"}

1. Select "file" --> "download as" --> "markdown".  Save the file to disk when the option pops up.

    [![](../../figures/notebooks-in-website/02.png){width=25%}](../../figures/notebooks-in-website/02.png){target="_blank"}

1. Save the notebook, then select "file" --> "close and halt"

    [![](../../figures/notebooks-in-website/14.png){width=25%}](../../figures/notebooks-in-website/14.png){target="_blank"}

1. Unzip the file that was downloaded (if necessary).
1. Navigate to your github repository and select the "files" --> "upload files" menu item.

    [![](../../figures/notebooks-in-website/16.png){width=25%}](../../figures/notebooks-in-website/16.png){target="_blank"}

1. Select the .md file as well as any other unzipped files (if applicable), upload, and commit.

    [![](../../figures/notebooks-in-website/17.png){width=25%}](../../figures/notebooks-in-website/17.png){target="_blank"}

1. Create a link to your file
    1. Open up index.md or whatever file you would like to point to the new notebook from.  Select edit 

        [![](../../figures/notebooks-in-website/18.png){width=25%}](../../figures/notebooks-in-website/18.png){target="_blank"}

    1. Add a new link.  Remember, that markdown files get compiled for you to html files.  Thus, if you name it "simple.md", github will convert that to a folder titled "/simple".  The link text can be whatever you want it to be.  So, for a full example, the whole link to an example file would look like this

        ```
        [link to simple markdown](/simple)
        ```

        [![](../../figures/notebooks-in-website/03.png){width=25%}](../../figures/notebooks-in-website/03.png){target="_blank"}

1. Save and commit your changes to index.md
1. Navigate to your website (myusername.github.io)

    [![](../../figures/notebooks-in-website/21.png){width=25%}](../../figures/notebooks-in-website/21.png){target="_blank"}

1. Try out the new link.

    [![](../../figures/notebooks-in-website/22.png){width=25%}](../../figures/notebooks-in-website/22.png){target="_blank"}
