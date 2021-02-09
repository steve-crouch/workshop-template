---
layout: page
title: Software Prerequisites
---

[[Home]](index.html)

**By 5.00pm on FIXME-DATE, you must install the required software on your laptop. Instructions are provided below.**

There is no time during the workshop to deal with installation problems, so you must arrive with your software already installed.

<!------------- Installation Day --------------------------------------------->

## Installation Day: FIXME:DATE

We've set aside the above date to provide help with installing software. Our Research Software Engineers will be online
from 9.00am - 5.00pm to help with your installation.

The installation is fairly straightforward, but if you have any problems, let us know via FIXME:ADD-TEAMS-CHANNEL-LINK.
or by [emailing us](mailto:rsg-info@soton.ac.uk). We'll arrange a Teams call with you to talk you through the process.


<!------------- Spreadsheets ------------------------------------------------->

## Spreadsheets

If you have access to **Microsoft Excel**, as a standalone application, please use this.  (Unfortunately Office 365 Online is not suitable for this workshop).
If you have no access to Microsoft Excel, please download and install **LibreOffice** Calc.

#### Windows

Download the and run the [LibreOffice 6.4 installer for Windows](https://downloadarchive.documentfoundation.org/libreoffice/old/6.4.6.1/win/x86_64/LibreOffice_6.4.6.1_Win_x64_helppack_en-GB.msi).
FIXME: test download link, the site has changed the file locations

#### Mac OS (10.15 / Catalina)

Download the [LibreOffice 6.4 installer for Mac](https://downloadarchive.documentfoundation.org/libreoffice/old/6.4.6.1/mac/x86_64/LibreOffice_6.4.6.1_MacOS_x86-64_langpack_en-GB.dmg).
FIXME: test download link, the site has changed the file locations

- If prompted, choose to allow downloads from libreoffice.org.
- Open the downloaded dmg archive from the Downloads folder.
- Drag the LibreOffice icon into the Applications folder.

#### Linux

FIXME: add download instructions for Linux.


<!------------- OpenRefine --------------------------------------------------->

## OpenRefine

**OpenRefine** is a powerful tool for working with messy data: cleaning it, transforming it and extending it with external data.
It works by running a small server on your computer.  You use your web browser to interact with it.

#### Windows

Download the [OpenRefine 3.4.1 Windows kit (with embedded Java)](https://github.com/OpenRefine/OpenRefine/releases/download/3.4.1/openrefine-win-with-java-3.4.1.zip).

- Open the downloaded zip archive from where you saved it.  It's safe to ignore any Windows Security warnings.
- Opening the archive will reveal a single folder `openrefine-3.4.1` - drag this folder to your Desktop.
- OpenRefine can be started by clicking `openrefine.exe` (blue diamond icon).
- If you see a **"Windows protected your PC"** warning, click **More info**, and choose **Run anyway**.

#### Mac OS 

Download the [OpenRefine 3.4.1 Mac kit](https://github.com/OpenRefine/OpenRefine/releases/download/3.4.1/openrefine-mac-3.4.1.dmg).

- If prompted, choose to allow downloads from openrefine.org.
- Open the downloaded dmg archive from the Downloads folder.
- If you receive a warning that the archive cannot be opened because it is from an unidentified developer:
    - Open System Preferences -> Security & Privacy -> General
    - Near the bottom of the pane you should see a message that openrefine was blocked.  Choose **Open Anyway**.
    - Accept the warning and **Open** the archive.
    - Drag the OpenRefine icon to your Desktop.
    - To run OpenRefine you must **Right Click** the icon and choose Open.
    - You can then ignore the subsequent warning and choose to Open the application.


<!------------- Bash --------------------------------------------------------->

## Bash

Among many other things, Bash allows you to automate repetitive tasks.

#### Windows

Bash is provided as part of the Git for Windows installation as described below.

#### Mac OS X

The Bash shell is accessed by opening the "Terminal" application. The Terminal application can be found in the "Utilities" folder which is in your "Applications" folder.


<!------------- R and RStudio ------------------------------------------------>

## R and RStudio

R is a programming language and software environment for statistical computing and graphics. The RStudio Integrated Development Environment (IDE) is a set of tools designed to help you be more productive with R.

#### Windows

Download and run the [R 4.0.3 for Windows Installer](https://cran.rstudio.com/bin/windows/base/R-4.0.3-win.exe).

Download and run the [RStudio Desktop 1.3 Installer for Windows](https://download1.rstudio.org/desktop/windows/RStudio-1.3.1093.exe).

#### Mac OS

Download the [R 4.0.3 Package for Mac OS](https://cran.rstudio.com/bin/macosx/R-4.0.3.pkg).

- If prompted, choose to allow downloads from cran.rstudio.com.
- Open the downloaded pkg file from the Downloads folder to install.

Download the [RStudio Desktop 1.3 Installer for Mac OS](https://download1.rstudio.org/desktop/macos/RStudio-1.3.1093.dmg).

- If prompted, choose to allow downloads from rstudio.com.
- Open the downloaded dmg archive from the Downloads folder.
- Drag the RStudio icon to the Applications folder to install.


<!------------- Text Editor -------------------------------------------------->

## Text Editor

A text editor is the piece of software you use to view and write code. If you have a preferred text editor, please use it.  
Otherwise we recommend using the terminal-based **Nano** editor.

#### Windows

Nano is provided as part of the Git for Windows installation as described below.

#### Mac OS X

Nano is already installed as part of the Mac OS X base install.

#### Linux

Nano is already installed as part of the Linux base install.


<!------------- Python ------------------------------------------------------->

## Python

We use Python 3, because it is generally the most widely used version of Python.  The "Anaconda3" package provides everything Python-related you will need for the workshop. To install Anaconda, follow the instructions below.

**<span style="color:red">IMPORTANT</span>: When asked "Add Anaconda to my PATH environment variable", answer "yes".
After it's finished, close and reopen any open terminals to reload the updated PATH and allow the installed Python to be found.**

If you want to use Microsoft Visual Studio Code (VSCode) as your text editor, install it when prompted. **Note** This requires administrator rights.

#### Windows

Download the [Python 3.7 Anaconda Windows installer](https://repo.anaconda.com/archive/Anaconda3-2018.12-Windows-x86_64.exe). Double click the installer and follow the instructions.

#### Mac OS X

Download the [Python 3.7 Anaconda Mac OS X installer](https://repo.anaconda.com/archive/Anaconda3-2018.12-MacOSX-x86_64.pkg). Double click the `.pkg` file and follow the instructions.

#### Linux

Download the [Python 3.7 Anaconda Linux Installer](https://repo.anaconda.com/archive/Anaconda3-2018.12-Linux-x86_64.sh). Install via the terminal like this

~~~{.code}
bash Anaconda3-2018.12-Linux-x86_64.sh
~~~

Answer 'yes' to allow the installer to initialize Anaconda3 in your .bashrc


<!------------- Git ---------------------------------------------------------->

## Git

Git is the version control software we will use. It allows you to keep track of your code, details of the edits that are made to it, and by whom.

   <!------------- GitHub Account -------------------------------------------->

#### Create a Github account

**You must create a Github account before attending the workshop!**

To create an account, [go to the Github website](https://github.com/join) and provide your details. It's quick and it's free. Once you have your account, you need to install the Git software as described below.

   <!------------------------------------------------------------------------->

#### Windows

Download and install [Git for Windows](https://github.com/git-for-windows/git/releases/download/v2.28.0.windows.1/Git-2.28.0-64-bit.exe).

- When prompted to choose the default editor used by Git, select your preference, or Nano (at the top of the list) if you have none.
- When prompted to Adjust your PATH environment, accept the default choice to use Git from the command line and 3rd-party software.
- Accept the default values for the remaining installation options. dio

#### Mac OS X

To use Git you must install the Apple Command Line Tools.  You can obtain these [from Apple](https://developer.apple.com/download/more/?name=command%20line%20tools%20for%20xcode%2012) (requires your Apple ID)

- Select **Command Line Tools for Xcode 12** and click the link to download the dmg archive.
- If prompted, choose to allow downloads from developer.apple.com
- Open the downloaded dmg archive from the Downloads folder
- Double click the Command Line Tools.pkg icon to install

#### Linux

Install via a terminal like this:

Ubuntu and derivatives:

~~~ {.code}
sudo apt-get install git
~~~

Fedora:

~~~ {.code}
su -
dnf install git
~~~

<!------------- Troubleshooting ---------------------------------------------->

## Troubleshooting

If anything fails, please [contact us](mailto:rsg-info@soton.ac.uk) before the workshop.
