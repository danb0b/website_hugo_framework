---
type: tutorial
title: Add Folder to System Path
class_name: EGR557
---

# Add Folder to System Path

These are the Windows 10 instructions.  Different operating systems, including older versions of Windows act slightly differently.  Please find OS specific instructions

1. Open file explorer
1. Right click on "This PC"-->"properties"
1. On the left menu select "advanced system settings"
1. Click on "Environment Variables..."
1. A dialog box will pop up with two windows.  The top window is the user-level settings, while the lower box controls globals settings.  **In the lower window**, find the ```PATH``` variable, and click "Edit..."
1. To add a new directory, navigate to the *end* of the list (lowest priority in the ```PATH``` search to minimize the impact of a conflict)
    1. Select "New" to add a new line.
    1. Either browse or paste in a path in the format ```C:\path\to\folder``` 

## External Resources

* [External Tutorial](https://www.howtogeek.com/118594/how-to-edit-your-system-path-for-easy-command-line-access/)