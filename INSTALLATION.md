# Installation Guide

This is a full guide on how to install Kubuntu for my set up. Feel free to use or copy the whole thing, or just an individual section (see the [license](./LICENSE) for the full legal disclamer)). Things may not work perfectly on your machine, so feel free to create an issue or, even better, a pull request with a solution, to make it work for you.

# Contents

1. [Installing Kubuntu](#Installing-Kubuntu)

2. [Installing ]

# Installing Kubuntu

Do this before anything else. These instructions will install Kubuntu on your device, which is the operating system that all the configurations I've made run on. Most of my config files should work fine on other Linux distributions, and some of them on other operating systems, including Windows, MacOS and BSD variants, but they might require some tweaks.

## Preparing a USB to boot Kubuntu

This section assumes you are on a Windows 10 machine before you install Kubuntu. To install from other machines, follow the [Kubuntu installation guide](https://userbase.kde.org/Kubuntu/Installation). If you are using Windows 10, follow these instructions:

1.    Insert an empty USB drive at least 4GB in size

2.    Download and run[UNetbootin](https://unetbootin.github.io/)

3.    Ensure the ```Distribution``` checkbox in the top left of the window is selected

4.    Select ```Kubuntu``` from the first drop down list

5.    Ensure the current LTS release (20.04 at the time of writing) is selected in the second drop down list

6.    Select ```USB drive``` from the drop down list in the bottom left

7.    Ensure the correct USB drive is selected in the next drop down list

8.    Press install and wait for the .iso to be downloaded and written to the USB drive

## Installing Kubuntu

If you want acsess to anything you currently have on the computer you are going to install Kubuntu onto, **EXTERNALLY BACKUP THE COMPUTER**, there is a risk you will remove all data on this computer. For the remainder of these instructions, I will be showing how to install Kubuntu to be the sole OS on a new computer, so if you want to dual boot or keep acsess to files on your hard drive, follow the [Kubuntu installation guide](https://userbase.kde.org/Kubuntu/Installation#Install_Process), and ignore the instructions here.

1.    Turn off your computer

2.    Connect your computer to the internet via an Ethernet cable

3.    Insert the USB drive you prepared in the last step

4.    Turn on your computer, and press the key set by your computer to boot from installation media. This is probably one of ```Esc```, ```F2```, ```F10```, ```F12``` or ```Del```

5.    A lodaing screen, and then an installation menu, should appear

6.    Ensure the installation language is set to your langauage and select ```Install Kubuntu```

7.    Select the correct keyboard layout and press ```Continue```

8.    Ensure ```Normal installation``` is selected, then tick the boxes marked ```Install this third-party software``` and ```Download updates whilst installing```, and then press ```Continue```

9.    On the next screen, select ```Guided - use entire disk``` and press ```Install Now```

10.    On the pop-up window that appears, press ```Continue```

11.    Ensure the correct time zone is selected, and press ```Continue```

12.    Pick a name, username, password (ensure this is both memorable and hard to guess) and name for your computer

13.    Ensure ````Require my password to log in```` is selected, and press ```Continue```

14.    Wait for the installation to complete. Upon completion, a prompt will appear, asking you to restart. Press ```Restart Now```

## First time Kubuntu setup

Congratulations, you have installed Kubunutu! Now to update it.

1.    Enter your password you set earlier into the box on the login screen

2.    Press ```Alt + Space``` and begin typing ```Konsole```, a menu should appear from the top of the screen

3.    Select ```Konsole``` either with a mouse, or with the arrow keys and Enter

4.    A window will open up - called a terminal

5.    In this window, type the following:
```
sudo apt update
```
6.    You will be prompted to enter your password. Do this

7.    Note the password will not appear, not even starred out like this ```******```, but this is not a bug. Press enter when you have finished typing your password

8.    Some text will appear in the terminal, you can read it if you wish

9.    Run the following by typing it and then pressing Enter:
```
sudo apt upgrade
```
10.    This time, you will not be asked for your password, as you have already entered it this session

11.    A lot of text will appear on screen. At the end of this will be an choice written like ```[Y,n]```. Pressing Enter will select the capitalised option, which is what you want to do here. If you wanted to say no to this, type ```n``` and hit enter

12.    Wait for the updates to finish, then reboot by running:
```
sudo reboot
```

# Basic Setup

These steps will make the rest of the installation easier. From now on, "running a command" means opening the terminal (by default, this is Konsole), typing in the command and pressing enter. Where prompted, type in your password. When multiple commands are in the same code block, run each one by one.

## Git

Git is a version control system, and git and github will be required to install my configuration files on your machine. 

### [Installing Git](https://git-scm.com/)

1.    Run:
```
sudo apt install git
```
2.    Next, install LazyGit using Launchpad by running
```
sudo add-apt-repository ppa:lazygit-team/release
```
3.    When prompted, press Enter, then finish the installation by running:
```
sudo apt update
sudo apt install lazygit
```
### [Gihub cli](https://github.com/cli/cli)

Github is the website you are on now, where this configuration is stored. If you haven't already, create a github account [here](https://github.com/join?). Then follow the steps below:

1.    Install github cli using these commands:
```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0
sudo apt-add-repository https://cli.github.com/packages
sudo apt update
sudo apt install gh
```
2.    Connect your github account by running and following the instructions on screen, choosing the deafault whenever given an option:
```
gh auth login
```
## [Curl](https://curl.se)

Curl, or cURL is an application that can transfer data with URLs. Installing this will make installing further configurations and proframs easier. To install, run:
```
sudo apt install curl
```
## Install my Configuration Files

### Install all configuration files

My configuration files can be downloaded individually. However, you can simply install all my configuration files as follows:

XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

### Download all configuration files

Alternatively, you can download all configuration files and then choose which ones to use:

XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

# KDE Configuration

# Installing and Configuring Other Software

## General software

### Kitty

Kitty is an alternative to Konsole. You can type the same commands as you do on Konsole or any other terminal, but it looks a little different and runs quite quickly. Install and configure it like this:

1.    In Konsole, run:
```
sudo apt install kitty
```
2.    -INSERT GIT INSTRUCTIONS HERE-
