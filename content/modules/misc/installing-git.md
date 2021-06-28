---
types: [tutorial,] 
title: Installing Git Extensions for Windows
class_logo: "../graphics/ClassLogo.pdf"
university_logo: "../graphics/UniversityLogo.pdf"
---

# In Windows
1. Download and install [Git](https://git-scm.com/download/win)
    1. keep default install location
    1. I prefer to disable shell integration
    1. I prefer to use notepad++ as a text editor, but you must install it separately.
    1. keep "git from the command line and also from 3rd-party software"
    1. use openssh
    1. use openssl
    1. checkout windows-style, commit unix-style
    1. use mintty
    1. on the next page, check
        * enable file system caching
        * enable git credential manager
    1. Install
1. Download and install [Kdiff](https://sourceforge.net/projects/kdiff3/files/).  Keep all options default.
1. Download and install [git extensions](https://github.com/gitextensions/gitextensions/releases/latest).
    1. install for all users
    1. keep default install location
    1. Keep all options default
    1. keep putty as default.
    1. select a language(english)
    1. set your username and password in the git extensions settings window that pops up

# In Ubuntu

1. Open up a terminal window (ctrl+alt+t)
1. Paste the following code(substituting in your name and email) to install git.

```sudo apt-get update
sudo apt-get install -y git
git config --global user.name "LastName, Firstname"
git config --global user.email "email@address.com"
```
