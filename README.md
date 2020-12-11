# MOOSE Framework Information

The [MOOSE](https://mooseframework.org) framework is an open-source, parallel finite element method framework.
Here we collect information for installation of MOOSE on typical systems of members of the UML Linux Club.

## Updating Moose and Conda

Updating Conda
1. `conda activate moose`
1. `conda update --all`

Make sure to update both conda and moose at the same time. You should update it weekly

Updating Moose
1. `cd ~/projects/moose`
1. `git fetch origin`
1. `git rebase origin/master`

Then return to your application, re-compile, and test
1. `cd ~/projects/YourAppName`
1. `make clobberall`
1. `make -j4`
1. `./run_tests -j4`

## Install Notes on a Windows 10 Virtualbox Host with a Ubuntu Gest

This options has not been sucessfull to anyone in our club who tried. The reason is...

## Install Notes on Windows 10 WSL using Ubuntu

1. 
1.
1. `Peacock` is not working on `Ubuntu/WSL` nor is `Paraview`. 
1. The alternative for visualization of `MOOSE` files is to install `Paraview` in the Windows 10 side (see below).
## Some Important Installation Commands in 'Order'for successfull installation and compilation of Moose on Windows 10 WSL using Ubuntu (after Ubuntu is installed)
1.    sudo apt-get update
1.    sudo apt-get upgrade
1.    sudo apt-get install x11-apps libglu1-mesa
1.    sudo apt-get install build-essenisals
1.    echo "export DISPLAY=localhost:0" >> ~/.bashrc
1.    echo "export DISPLAY=localhost:0" >> ~/.bashrc
1.    exit
1.    ls
1.    curl -L -O https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
1.    bash Miniconda3-latest-Linux-x86_64.sh -b -p ~/miniconda3
1.    export PATH=$HOME/miniconda3/bin:$PATH
1.    conda config --add channels conda-forge
1.    conda config --add channels idaholab
1.    conda create --name moose moose-libmesh moose-tools
1.    exit
1.    conda activate moose
1.    ls
1.    export PATH=~/miniconda3/bin:$PATH
1.    conda activate moose
1.    conda init bash
1.    exit
1.    conda activate moose
1.    mkdir ~/projects
1.    cd ~/projects
1.    git clone https://github.com/idaholab/moose.git
1.    cd moose
1.    git checkout master
1.    cd ~/projects/moose/test
1.    make -j 4
1.    sudo apt install make
1.    make -j 4

## Install Notes of `Paraview` for `Windows 10 WSL`
 1. Go to the [Paraview site](https://www.paraview.org/download)
 1. Install `ParaView-5.8.0-Windows-Python3.7-msvc2015-64bit.exe`
 1. Completely install and run
 1. Type `paraview` in my `PC` search bar
 1. Locate the `paraview` application and create a shortcut to desktop
 1. In `Ubuntu 20.0.4` type:   
     `explorer.exe .`
 1. Go to the projects folder in the `MOOSE` installation
 1. Go to results you'd like to see *i.e* `ex01_out`
 1. Open with `paraview` application; recall you defined the application as a shortcut to your desktop
 1. Go to desktop and open `ex01_out` with the `paraview` application. 
 1. When it is up, go to the upper left corner, you should see gradient icons, and click the `chain` gradient icon
 1. Next to this icon is a drop down tap called `vtxblockcolors`
 1. Change this to the variable of interest. 

## Install Notes on Gentoo Linux (from source code)

## Install Notes for Mac
- go to https://mooseframework.inl.gov/getting_started/installation/conda.html
- install Miniconda3 for Macintosh Users
- proceed with install as listed

## Installing Peacock for Mac
- go to https://mooseframework.inl.gov/application_usage/peacock.html
- follow steps listed under "Environment"
- in order to open your bash profile to add the path, type touch ~/.bash_profile; open ~/.bash_profile
- add the path as specified
