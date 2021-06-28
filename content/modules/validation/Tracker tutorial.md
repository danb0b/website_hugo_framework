---
title: Tracker Tutorial
types: [tutorial,] 
---
# Basic Tracker Tutorial

_Thanks to Chien-Wen Pan for his screenshots and assistance._


## External Resources

[Tracker Software](https://physlets.org/tracker/)


## Procedure

1. Set up your Experiment

    * Create your experiment so that captured motion is _planar_ to the lens's radial axis.
    * Ensure markers are not occluded as your system moves.  This will result in lost data.
    * Ensure your "ground link" is rigidly attached to ground.  Any unmeasured flexibility will add error to your system
    * Eliminate the effects of contact and friction if possible.  Rigidly attach your system in a given configuration rather than assuming it is unmoving due to friction.
    
1. Place Markers.

    * Utilize a high-contrast color scheme in the materials you use.  If your device is dark or light-colored, create colored markers that are the inverse color scheme.
    * Add markers to your (fixed) base reference frame.  This will be useful in case your camera moves during capture.
    * When sizing your markers, consider that the larger your marker, the larger the search window needs to be in tracker, which will slow tracking down.  The smaller your marker, the higher 
  
1. Light your Experiment

    * Light your scene well so that your camera may use a smaller aperture.  This will help reduce blurring and improve tracking performance.  
    * Avoid shadows, changing lighting conditions, or other dark/light spots in your scene.  Sunlight is good as long as it does not go behind a cloud.
  
1. Measure your experiment.  Take key measurements of your system, including:

    * Distance between each marker
    * Mass of rigid links
    * Distance between camera lens and plane of experiment. (useful for expert-level calibration)

1. Take video.  Suggestions: 
    
    * If possible to manually adjust camera settings, increase shutter rate
        * Set your shutter speed to at least 1/500th of a second or faster.
        * Use a lens that has a long focus length so that you can reach the action (200mm or higher)
    * Use "slow motion" mode if available.  This will increase the frame-rate.
    * Set the camera far enough back that it captures the whole scene as your device moves throughout its workspace.  Utilize the center of the frame as much as possible to minimize lens distortion effects
    * Measure the angle of "ground" by including 
    * Use a tripod to ensure your camera does not move.
    
1. Open Tracker, then load a new video.
    
    ![](./Tracker tutorial_media/media/image3.jpg){width="5.734375546806649in" height="4.291591207349081in"}

    1. Adjust the markers on the left and right of the timeline to select a portion of the video

2.  Create a "coordinate system".
    
    ![](./Tracker tutorial_media/media/image4.jpg){width="5.756537620297463in" height="4.199010279965004in"}
    
    ![](./Tracker tutorial_media/media/image1.jpg){width="5.765625546806649in" height="4.358421916010498in"}

1. Create a Calibration Stick.  Use shift+left click to place two points, then enter the length

    ![](./Tracker tutorial_media/media/image8.jpg){width="5.6312817147856515in" height="4.244792213473316in"}

3.  Track points.  

    1. Create a new point mass

        ![](./Tracker tutorial_media/media/image2.jpg){width="5.6175688976377955in" height="4.157001312335958in"}
    
    1. Using ctrl+shift+left click, select an identifiable object in the scene to create a keyframe
    
        ![](./Tracker tutorial_media/media/image5.jpg){width="5.734375546806649in" height="4.309970472440945in"}

        ![](./Tracker tutorial_media/media/image6.jpg){width="5.7516163604549435in" height="4.311064085739282in"}
        
        * you can also adjust the size of the search box
        
    1. If problems occur, you can adjust points or reselect a keyfram using the tools in the autotracker window.
        
        * if you select a point in the plot, you can delete all points after and reselect the marker, or redefine the keyframe.
        
        ![](./Tracker tutorial_media/media/image7.jpg){width="5.755208880139983in" height="4.362521872265967in"}
    
    Repeat if you have multiple markers to track.

4. Export data table to a .csv file. Note: it seems that tracker's export function truncates floats to 2 values of precision.  Copy and paste the table directly into a text editor and save as a .csv file to get full precision.

5. Use the following code to extract your data and interpolate it: 

    ```python
    # -*- coding: utf-8 -*-
    """
    Created on Wed Mar  3 13:54:15 2021

    @author: danaukes
    """

    import pandas as pd
    import numpy
    import matplotlib.pyplot as plt
    import scipy.interpolate as si

    df=pd.read_csv(r'C:\Users\danaukes\Documents\Tracker\mydata.csv', sep=',')

    #x = df.x.astype('float64').to_numpy()
    x = df.x.to_numpy()
    y = df.y.to_numpy()
    t = df.t.to_numpy()


    xy = numpy.array([x,y]).T
    f = si.interp1d(t,xy.T,fill_value='extrapolate',kind='quadratic')
    new_t = numpy.r_[0:t[-1]:.1]

    plt.figure()
    plt.plot(t,x)
    plt.plot(new_t,f(new_t)[0])

    plt.figure()
    plt.plot(t,y)
    plt.plot(new_t,f(new_t)[1])
    plt.figure()
    plt.plot(x,y)
```