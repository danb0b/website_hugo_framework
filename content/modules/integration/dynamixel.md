---
type: tutorial
title: Running Dynamixel X-Series 
subtitle: Using Arduino IDE for OpenCM9.04
class_name: EGR557
---


# Running Dynamixel X-Series Using Arduino IDE for OpenCM9.04

## Install Arduino IDE and OpenCM9.04 Software

<!-- -->

1.  Install OpenCM9.04 USB CDC driver - [Driver Download]
2.  Install Arduino IDE - [Arduino IDE]
3.  After Arduino IDE is run, click File --> Preferences in top menu of IDE
4.  Copy and paste the following link to the Additional Boards Manager URLs textbox

    <https://raw.githubusercontent.com/ROBOTIS-GIT/OpenCM9.04/master/arduino/opencm_release/package_opencm9.04_index.json>

5.  Click Tools --> Board --> Boards Manager
6.  Type OpenCM9.04 into the textbox to find the OpenCM9.04 by ROBOTIS package. Click Install. After Installation, "INSTALLED" will appear

    ![][1]

7.  Check if OpenCM9.04 Board is now on the list of Tools --> Board. Click this to import the OpenCM9.04 Board source.
<!-- -->
II. **[Run Dynamixel X-Series Servo Using OpenCM9.04 Board]{.underline}**
<!-- -->
8.  Click File --> Examples --> OpenCM9.04 --> 07\_DynamixelSDK --> Protocol 2.0 --> read\_write

    ![][2]
    
9.  If these are not the values on your table then change what is on your screen so it looks like this
10. Click Tools Serial Monitor
11. Press any key and hit enter to run the Dynamixel X-Series Motor.

  [Driver Download]: https://www.st.com/en/development-tools/stsw-stm32102.html
  [Arduino IDE]: https://www.arduino.cc/en/Main/Software
  [1]: ../figures/image1.png {width="6.5in" height="3.704861111111111in"}
  [2]: ../figures/image2.png {width="4.895833333333333in" height="5.46875in"}
