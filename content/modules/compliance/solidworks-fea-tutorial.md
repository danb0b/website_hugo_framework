---
title: Solidworks FEA Tutorial
types: [tutorial,] 
---

## Solidworks FEA Tutorial

1. Create a new part

    [![png](../../figures/solidworks-fea/01.png){width=50%}](../../figures/solidworks-fea/01.png){target="_blank"}

1. Select the Top Plane

    [![png](../../figures/solidworks-fea/02.png){width=50%}](../../figures/solidworks-fea/02.png){target="_blank"}

1. Create a new Sketch
1. Select the rectangle tool
1. Draw a rectangle (hint: click on the origin to constrain the rectangle to that point)

    [![png](../../figures/solidworks-fea/03.png){width=50%}](../../figures/solidworks-fea/03.png){target="_blank"}

1. Select the dimensioning tool

    [![png](../../figures/solidworks-fea/04.png){width=50%}](../../figures/solidworks-fea/04.png){target="_blank"}

1. Click on the top edge of the rectangle. A dimension will appear.  Enter the desired dimension
1. Repeat for the side of the rectangle
1. Select the features tab and then select extruded boss/base
    
    [![png](../../figures/solidworks-fea/05.png){width=50%}](../../figures/solidworks-fea/05.png){target="_blank"}

1. Enter the thickness of your laminate

    [![png](../../figures/solidworks-fea/06.png){width=50%}](../../figures/solidworks-fea/06.png){target="_blank"}

1. Save your part into a new folder

    [![png](../../figures/solidworks-fea/07.png){width=50%}](../../figures/solidworks-fea/07.png){target="_blank"}

1. Turn on the Solidworks Simulaton Add in.  Go to tools-->add ins

    [![png](../../figures/solidworks-fea/08.png){width=50%}](../../figures/solidworks-fea/08.png){target="_blank"}

1. Click on the check box to the left of the "solidworks simulation item"

    [![png](../../figures/solidworks-fea/09.png){width=50%}](../../figures/solidworks-fea/09.png){target="_blank"}

1. Now select the Simulation tab.

    [![png](../../figures/solidworks-fea/10.png){width=50%}](../../figures/solidworks-fea/10.png){target="_blank"}

1. Create a new study

    [![png](../../figures/solidworks-fea/11.png){width=50%}](../../figures/solidworks-fea/11.png){target="_blank"}

1. Next, define your fixtures.  Go to the menu on the left and select fixtures-->Fixed Geometry...

    [![png](../../figures/solidworks-fea/12.png){width=50%}](../../figures/solidworks-fea/12.png){target="_blank"}

1. Define the fixed end of the cantilever beam by rotating the part and selecting the left cross-sectional face of the beam.

    [![png](../../figures/solidworks-fea/13.png){width=50%}](../../figures/solidworks-fea/13.png){target="_blank"}

1. Define an axis along which you will align a force.  Select The Front plane and the top plane, then select insert-->reference geometry-->axis from the top menu

    [![png](../../figures/solidworks-fea/14.png){width=50%}](../../figures/solidworks-fea/14.png){target="_blank"}

1. The two-planes method should be automatically selected for you.  Select the green check mark to accept the new axis

    [![png](../../figures/solidworks-fea/15.png){width=50%}](../../figures/solidworks-fea/15.png){target="_blank"}

1. Define your forces. In the left menu select External forces/torques-->force...

    [![png](../../figures/solidworks-fea/16.png){width=50%}](../../figures/solidworks-fea/16.png){target="_blank"}

1. Select the right cross-sectional face of the beam, then ensure the force option is selected on the left.  Check the "sekected direction option", and the new axis you just created (axis 1).  Then select the axial load option and define the magnitued of the force.

    [![png](../../figures/solidworks-fea/17.png){width=50%}](../../figures/solidworks-fea/17.png){target="_blank"}

1. Next, define your material.  You can select from a list of favorite materials, or go into the material selector to create a custom material.
    [![png](../../figures/solidworks-fea/18.png){width=50%}](../../figures/solidworks-fea/18.png){target="_blank"}
    [![png](../../figures/solidworks-fea/19.png){width=50%}](../../figures/solidworks-fea/19.png){target="_blank"}

1. In the left menu, select mesh-->mesh and run to run your simulation

    [![png](../../figures/solidworks-fea/20.png){width=50%}](../../figures/solidworks-fea/20.png){target="_blank"}

1. If you get a message that the solver failed, with an option to restart, select "yes"
1. If you get a message to turn on large displacement solving, select yes.

    [![png](../../figures/solidworks-fea/21.png){width=50%}](../../figures/solidworks-fea/21.png){target="_blank"}

1. If it succeeds, you may now view the results of the solver    

    [![png](../../figures/solidworks-fea/22.png){width=50%}](../../figures/solidworks-fea/22.png){target="_blank"}
    [![png](../../figures/solidworks-fea/23.png){width=50%}](../../figures/solidworks-fea/23.png){target="_blank"}


## Notes

Common sources of failure include:

* Too high of a force or too soft of a material for the given dimensions.  Try selecting a stiffer material

