---
title: Pendulum Model Fitting
type: tutorial
---

1. Find a bright round spherical object like a tennis ball, orange, etc.
1. Weigh it
1. Measure its diameter
1. Find a piece of string and attach it to the ball
1. Tape the other end of the string to a door frame. Make sure that the background is relatively neutral and free of color.
1. Set up a video camera to capture the ball as it swings.  Ensure the following to make sure your data is free from error:
    * That the camera is attached to a tripod or otherwise resting firmly on the ground.  
    * That the radial axis of the camera's lens is perpendicular to the plane of the ball's motion
    * That the center of the camera's lens is approximately in the middle of the scene.
    * That the camera can see the attachment point of the string as well as the ball as it swings
1. Measure the length of the string between the ball and the attachment point
1. Measure the distance between the camera lens and the plane of the ball's motion
1. start recording
1. while watching through the video camera, pull back the ball until it reaches the edge of the camera frame and release.  if it swings out of plane too badly, stop and restart.
1. Capture at least 15 seconds of video.
1. Open tracker and import the video
1. Create a tracking marker for the attachment point and the center of the ball
1. extract the motion data.
1. Scale the motion data based on the measurement you took of the string.
1. Open this pendulum code
1. enter the constants that you know
1. adapt the optimization function to include parameters you do not know or found it difficult to measure.
1. Run the optimization using either cmaes or scipy.optimize.minimize
1. Identify the unknown parameters
