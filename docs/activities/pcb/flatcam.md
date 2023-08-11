# Install FlatCam

FlatCam is open source software available on [bitbucket](https://bitbucket.org/jpcgt/flatcam/downloads/){: target=_blank}.

!!!Info
    This page is a point in time with the state of the project at August 2023

## Broken instructions

### Master Branch
This is the branch used when following the instructions.

The primary (master) branch hasn't been updated since July 2019 and is quite out of date.  I could not get this version running.

### Beta Branch
This branch was last updated February 2022

This version can be made to work (I tested on Ubuntu Linux and Mac OS Ventura 13.4.1).  However, there are many issues with this branch, making it quite difficult and frustrating to work with:

- Some fields not displaying, making certain functions unabilible (Calculator tool for v-bit)
- Running system in dark mode results in some black text on dark gray background, irrespective if FlatCam is running in light or dark mode
- Many crashes occur in many different places, suggesting a fundamental mismatch in dependencies
- Some key functionality, such as board cutout not available due to application crash

To make it work, with the above mentioned issues, do the following:

1. Checkout the git repo and switch to the beta branch:

    ```shell
    git clone https://bitbucket.org/jpcgt/flatcam.git
    cd flatcam
    git checkout -b Beta origin/Beta
    ```

2. modify the requirements.txt file, change / add the following:
    - pyopengl==3.1.6
    - vispy==0.7.0
    - shapely==1.8.4
    - networkx>=3.1
3. install dependencies with command `pip install -r requirements.txt`
4. run FlatCam with command `python FlatCAM.py`

## Working version

Whilst searching through the issues I cam across comments from the current active developer about their active development branch.  Using this development branch results in a working application.  The version has gone through some modernisation and UI redesign, which is greatly improved.

To use the active development version do the following:

!!!Todo
    detail system packages that need to be installed, such as `brew install pyqt`

1. clone the repo with command `git clone https://bitbucket.org/marius_stanciu/flatcam_beta.git`
2. cd flatcam_beta
3. checkout the Beta_8.995 branch `git checkout -b Beta_8.995 origin/Beta_8.995`
4. install dependencies with command `pip install -r requirements.txt`
5. run FlatCam with command `python flatcam.py`
