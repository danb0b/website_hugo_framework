---
types: [tutorial,] 
title: Solidworks Export Tutorial
---

Solidworks is an attractive way to model popup devices because you can interact with the three-dimensional kinematics of your popup device.  However, Solidworks is not good at everything.  First, it cannot create your cut-files for you automatically.  Solidworks knows nothing about *how* you're going to make your device, out of how many layers, and with what manufacturing processes. Second, Solidworks is such an expansive tool, and can be used in so many different ways that the most straightforward way to design a popup device is not very obvious.  

So, to help users with these issues, we have outlined a workflow which can be used to rapidly create a popup device whose kinematics you can visualise and interact with quickly.  Second, we also outline the steps to export those basic multilayer kinematics to a popupCAD file so that the manufacturing specifics can be done in an environment with built-in manufacturing knowledge.

Download [example.zip](../../figures/solidworks-export-tutorial/example.zip) to see this example project.

<!--

Tutorial Video
----------------

Please follow [this link](https://www.youtube.com/embed/fqtUoCcbiJk?rel=0&amp;showinfo=0)^[[https://www.youtube.com/embed/fqtUoCcbiJk?rel=0&amp;showinfo=0](https://www.youtube.com/embed/fqtUoCcbiJk?rel=0&amp;showinfo=0)] to watch the tutorial video:
-->
Step-by-step Instructions
----------------

1. Create a new part file

    ![01](../../figures/solidworks-export-tutorial/images/01.png){height=2in}
    
    ![02](../../figures/solidworks-export-tutorial/images/02.png){height=2in}

1. Select a reference plane(top, for example) and then create a new sketch (or create a new sketch and select any reference plane)

    ![03](../../figures/solidworks-export-tutorial/images/03.png){height=2in}
  
1. Sketch the lines which define your robot.  The outline of your robot should be a drawn out of solid lines.  Any internal hinges should be drawn as construction lines, or made into construction lines once drawn.  If you are making a robot which consists of multiple sub-laminates, you should create one of these sketches per sublaminate.

    ![04](../../figures/solidworks-export-tutorial/images/04.png){height=2in}
  
1. Next, for each sub-laminate sketch that you have created, you can should create a planar surface.  Go to  insert->surfaces->planar surface.  Select each sketch.  This should create a surface whose outline matches the closed shape of solid lines you drew in your sketch.

    ![05](../../figures/solidworks-export-tutorial/images/05.png){height=2in}
    
    ![06](../../figures/solidworks-export-tutorial/images/06.png){height=2in}
    
    ![07](../../figures/solidworks-export-tutorial/images/07.png){height=2in}

1. For each surface you just created, you want to split that surface along all the lines representing joints from your original sketch.  First, unhide the original sketch by clicking on the eyglasses icon under the surface->sketch in the left project pane.  This will allow you to view, select, and reference lines drawn in that sketch.

    ![09](../../figures/solidworks-export-tutorial/images/09.png){height=2in}
    
    ![10](../../figures/solidworks-export-tutorial/images/10.png){height=2in}

1. Next, create a new sketch on the same reference plane(such as the top plane), select one or more joint lines, and in the sketch tools, select "convert entities".  Only select sets of lines which do not cross each other, as the next step will fail.  Make sure that the lines you do select completely cross the surface, or create a loop.

    ![11](../../figures/solidworks-export-tutorial/images/11.png){height=2in}
    
    ![12](../../figures/solidworks-export-tutorial/images/12.png){height=2in}
    
    ![13](../../figures/solidworks-export-tutorial/images/13.png){height=2in}

1. Repeat the last two steps for the remaining joint lines, making sure not to select sets of lines which cross each other or more than two lines at any point.
  
    ![14](../../figures/solidworks-export-tutorial/images/14.png){height=2in}
    
    ![15](../../figures/solidworks-export-tutorial/images/15.png){height=2in}
    
    ![16](../../figures/solidworks-export-tutorial/images/16.png){height=2in}
    
    ![17](../../figures/solidworks-export-tutorial/images/17.png){height=2in}
    
    ![18](../../figures/solidworks-export-tutorial/images/18.png){height=2in}
    
    ![19](../../figures/solidworks-export-tutorial/images/19.png){height=2in}

1. Use insert->curve->split line to separate faces.  You will need to do this for each sketch you just created. When you do this, remember to select all the surface faces to ensure they get split by the sketch.

    ![20](../../figures/solidworks-export-tutorial/images/20.png){height=2in}
    
    
    ![21](../../figures/solidworks-export-tutorial/images/21.png){height=2in}
    
    ![22](../../figures/solidworks-export-tutorial/images/22.png){height=2in}
    
    ![23](../../figures/solidworks-export-tutorial/images/23.png){height=2in}
    
    ![24](../../figures/solidworks-export-tutorial/images/24.png){height=2in}
    
    ![25](../../figures/solidworks-export-tutorial/images/25.png){height=2in}
    
    ![26](../../figures/solidworks-export-tutorial/images/26.png){height=2in}
    
    ![27](../../figures/solidworks-export-tutorial/images/27.png){height=2in}
    
    ![28](../../figures/solidworks-export-tutorial/images/28.png){height=2in}
    
    ![29](../../figures/solidworks-export-tutorial/images/29.png){height=2in}
  
1. Use the insert->surface->offset function to create independent surfaces from faces of original body.  Hint: to repeat creating the same feature over and over, hit enter after creating one offset surface feature and solidworks will begin a new one.

    ![30](../../figures/solidworks-export-tutorial/images/30.png){height=2in}
    
    
    ![31](../../figures/solidworks-export-tutorial/images/31.png){height=2in}
    
    ![32](../../figures/solidworks-export-tutorial/images/32.png){height=2in}
    
    ![33](../../figures/solidworks-export-tutorial/images/33.png){height=2in}
    
    ![34](../../figures/solidworks-export-tutorial/images/34.png){height=2in}

1. Use insert->boss/base->thicken feature to thicken each feature.  Hint: deselect the merge body option after creating the first thickened part, otherwise the bodies will merge back together.

    ![35](../../figures/solidworks-export-tutorial/images/35.png){height=2in}
    
    ![36](../../figures/solidworks-export-tutorial/images/36.png){height=2in}
    
    ![37](../../figures/solidworks-export-tutorial/images/37.png){height=2in}
    
    ![38](../../figures/solidworks-export-tutorial/images/38.png){height=2in}
    
    ![39](../../figures/solidworks-export-tutorial/images/39.png){height=2in}
    
    ![40](../../figures/solidworks-export-tutorial/images/40.png){height=2in}
    
    ![41](../../figures/solidworks-export-tutorial/images/41.png){height=2in}

1. Save your file!!

    ![42](../../figures/solidworks-export-tutorial/images/42.png){height=2in}

1. Look at the project menu on the left.  You should have a number of solid bodies in your part file.

    ![43](../../figures/solidworks-export-tutorial/images/43.png){height=2in}

1. Right click on the solid bodies folder and select "save bodies"

    ![44](../../figures/solidworks-export-tutorial/images/44.png){height=2in}

1. In the save bodies menu, auto-assign names and select an assembly name.  This will automatically put all the saved bodies into an assembly file.  Click the green check box.  Select "rebuild" if a notification box pops up.  This should begin the save process and open up your new assembly file in the background

    ![45](../../figures/solidworks-export-tutorial/images/45.png){height=2in}
    
    ![46](../../figures/solidworks-export-tutorial/images/46.png){height=2in}
    
    ![47](../../figures/solidworks-export-tutorial/images/47.png){height=2in}
    
    ![48](../../figures/solidworks-export-tutorial/images/48.png){height=2in}

1. Save and close your part file.  Now the newly-created assembly file should be visible.

    ![49](../../figures/solidworks-export-tutorial/images/49.png){height=2in}
    
    ![51](../../figures/solidworks-export-tutorial/images/51.png){height=2in}

1. All the parts in your assembly are fixed in space relative to each other.  To visualize how they will move, you must float all the parts except for one.  To do this, select all the parts  you wish to be able to move, right click on them in the project manager on the left, and select "float".  These parts should now be able to be moved by dragging them.

    ![52](../../figures/solidworks-export-tutorial/images/52.png){height=2in}
    
    ![53](../../figures/solidworks-export-tutorial/images/53.png){height=2in}
    
    ![54](../../figures/solidworks-export-tutorial/images/54.png){height=2in}
    
    ![55](../../figures/solidworks-export-tutorial/images/55.png){height=2in}

1. Next, you must create mating conditions to define the joint kinematics of your devie.  Since these thickened flat sheets represent several layers laminated together, they will most likely rotate around their midplane.  However, to assemble the device faster, it is easier to select edges and points on the top or bottom surface, with the knowledge that it may not move exactly the same in real life. Select one mating line on two parts you would like to joint with a joint and then select the "mate" button in the assembly tab.  This will bring the two lines together.  Hit enter to accept

    ![57](../../figures/solidworks-export-tutorial/images/57.png){height=2in}
    
    ![58](../../figures/solidworks-export-tutorial/images/58.png){height=2in}

1. Next select two points at the end of the mating edge you just joined, one for each part.  This should join those two points and constrain the parts as if they are joined by a hinge.  You can now move those two parts relative to each other.

    
    ![59](../../figures/solidworks-export-tutorial/images/59.png){height=2in}
    
    ![60](../../figures/solidworks-export-tutorial/images/60.png){height=2in}
    
    ![61](../../figures/solidworks-export-tutorial/images/61.png){height=2in}
    
1. Repeat this process for each joint you wish to create.  This should fully define the motion of the device.  You can move the device around as it will work once created, as in this [video](example.mp4)

    ![62](../../figures/solidworks-export-tutorial/images/62.png){height=2in}
    
    ![63](../../figures/solidworks-export-tutorial/images/63.png){height=2in}
    
    ![64](../../figures/solidworks-export-tutorial/images/64.png){height=2in}

1. Once you have defined the kinematics of the device, you must now re-flatten the assembly so that you can export it to popupCAD.  Add additional mating constraints to neighboring faces of your device, making them "coincident" to each other.  This will flatten it.

    ![65](../../figures/solidworks-export-tutorial/images/65.png){height=2in}

1. Save your Assembly
1. Make a new drawing by selecting file->"create drawing from assembly"

    ![66](../../figures/solidworks-export-tutorial/images/66.png){height=2in}

1. Deselect the sheet format option

    ![67](../../figures/solidworks-export-tutorial/images/67.png){height=2in}

1. Drag in the top view of the assembly and hit enter. (I'm assuming you used the top view to create your original sketches)

    ![68](../../figures/solidworks-export-tutorial/images/68.png){height=2in}
    
    ![69](../../figures/solidworks-export-tutorial/images/69.png){height=2in}

1. download the macro found at <https://github.com/popupcad/popupcad_solidworks_exporter/raw/master/swp/ExportDrawingFaces.swp>. 

1. Select the top view

    ![71](../../figures/solidworks-export-tutorial/images/71.png){height=2in}

1. Export the top view.  Go to tools->macro->edit, and select "ExportDrawingFaces.swp", found in the /swp directory of the downloaded macro project.  Note: this will only work with Solidworks 2014, 64-bit.  Otherwise you will have to re-create the macro project from the included source files.  That will have to be the subject of a different tutorial

    ![72](../../figures/solidworks-export-tutorial/images/72.png){height=2in}
    
    ![73](../../figures/solidworks-export-tutorial/images/73.png){height=2in}
    
1. A code window should open.  Select the run icon, and select run on the dialog that opens.

    ![74](../../figures/solidworks-export-tutorial/images/74.png){height=2in}

1. Select "Export Generic" and hit run to export the view to a .yaml file that your code can interpret.

    ![75](../../figures/solidworks-export-tutorial/images/75.png){height=2in}