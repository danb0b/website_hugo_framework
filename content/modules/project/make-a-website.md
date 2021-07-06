---
title: Make a Project Repository and Website
type: tutorial
---

# Make a Project Repository and Website

## Introduction

The purpose of this post is to help you create a website to share your work.  Sharing your work with the class and the broader community is important, as you should generate a persistent portfolio of class work to demonstrate your abilities when you apply for a job or academic career.

We will be using github to host and share websites this year.  This is for a couple reasons:

* Hosting websites on github is free.
* Git is iterative.  As your project evolves we can see how it has changed
* Editing content is easy, using either the web interface or windows-based clients.


## Procedure

1. Go to Github.com
1. Create an account under the free plan 
1. Verify your email
1. Create a new **public** repository

    [![01](../../figures/create-a-project-repository-and-website/01.png){width=25%}](../../figures/create-a-project-repository-and-website/01.png){target="_blank"}

    1. name it your-user-name.github.io (ex: *danaukestest01.github.io*) 
    1. keep other options blank for now. 

        [![02](../../figures/create-a-project-repository-and-website/02.png){width=25%}](../../figures/create-a-project-repository-and-website/02.png){target="_blank"}

1. Select the link to create a new file.  

    [![03](../../figures/create-a-project-repository-and-website/03.png){width=25%}](../../figures/create-a-project-repository-and-website/03.png){target="_blank"}

    1. Name it index.md

        [![04](../../figures/create-a-project-repository-and-website/04.png){width=25%}](../../figures/create-a-project-repository-and-website/04.png){target="_blank"}

    1. Paste in the following code and hit commit

        ```markdown
        ---
        title: Home
        ---

        # Home

        ```

        [![05](../../figures/create-a-project-repository-and-website/05.png){width=25%}](../../figures/create-a-project-repository-and-website/05.png){target="_blank"}

1. In the main repository, go to settings and scroll down the main settings page.  

    [![07](../../figures/create-a-project-repository-and-website/07.png){width=25%}](../../figures/create-a-project-repository-and-website/07.png){target="_blank"}

    1. Ensure that your site is published.   

        [![08](../../figures/create-a-project-repository-and-website/09.png){width=25%}](../../figures/create-a-project-repository-and-website/09.png){target="_blank"}

    1. Navigate to the linked page (your-user-name.github.io) and check out the results

    1. Now navigate back to the main repository 

        [![10](../../figures/create-a-project-repository-and-website/10.png){width=25%}](../../figures/create-a-project-repository-and-website/10.png){target="_blank"}

1. Replace the text in index.md with the following code and hit save:

    ```markdown
    ---
    title: Home
    ---

    # Home

    ## Introduction

    **Bold Text**
    _Italic Text_
    **_Bold and Italic Text_**

    ## Research Question

    * Bullet Point 1
    * Bullet Point 2
    * Bullet Point 3

    ## Background

    ![image caption](https://idealab.asu.edu/assets/images/research/jumper1.png)

    [link to background](/background)

    ## Results

    1. Numbered Point 1
    1. Numbered Point 2
    1. Numbered Point 3

    ## Conclusions and Future Work

    ## External Links

    [example link to idealab](https://idealab.asu.edu)


    ## References
    ```

    [![11](../../figures/create-a-project-repository-and-website/11.png){width=25%}](../../figures/create-a-project-repository-and-website/11.png){target="_blank"}

    [![13](../../figures/create-a-project-repository-and-website/13.png){width=25%}](../../figures/create-a-project-repository-and-website/13.png){target="_blank"}

    [![14](../../figures/create-a-project-repository-and-website/14.png){width=25%}](../../figures/create-a-project-repository-and-website/14.png){target="_blank"}

1. Navigate back to the repository

    [![15](../../figures/create-a-project-repository-and-website/15.png){width=25%}](../../figures/create-a-project-repository-and-website/15.png){target="_blank"}

1. Create a new file named "background.md"

    [![16](../../figures/create-a-project-repository-and-website/16.png){width=25%}](../../figures/create-a-project-repository-and-website/16.png){target="_blank"}

    [![17](../../figures/create-a-project-repository-and-website/17.png){width=25%}](../../figures/create-a-project-repository-and-website/17.png){target="_blank"}

1. Paste in the following code:

    ```markdown
    ---
    title: Background
    ---

    # Background

    ## Introduction

    ## Conclusions

    ## References

    ```

    [![18](../../figures/create-a-project-repository-and-website/18.png){width=25%}](../../figures/create-a-project-repository-and-website/18.png){target="_blank"}

1. Refresh the page at your-user-name.github.io and check out the results

    [![19](../../figures/create-a-project-repository-and-website/19.png){width=25%}](../../figures/create-a-project-repository-and-website/19.png){target="_blank"}

