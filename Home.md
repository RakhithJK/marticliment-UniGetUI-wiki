# WingetUI

**First of all... What is WingetUI?** WingetUI is an application whose main goal is to create an intuitive UI to manage the most common CLI package managers for Windows, such as [Winget](https://learn.microsoft.com/en-us/windows/package-manager/) and [Scoop](https://scoop.sh/). 

With this app, you'll be able to download, install, update and uninstall any software that's published on the supported package managers — and so much more.

AppGet was supported in release 0.3, but since that project has been discontinued, the support has been removed.

**Disclaimer:** This project has no connection with the official [Winget project](https://github.com/microsoft/winget-cli) — it's completely unofficial.

## Table of contents

 1. [WingetUI](#wingetui)</b><br>
 2. [How does it work?](#how-does-it-work)</b><br>
 3. [Is WingetUI safe?](#Is-WingetUI-safe)</b><br>
 4. [Installation](#wingetui-installation)<br>
 5. [Common Problems](#common-problems)
 6. [Running and building the source code](#running-and-building-the-source-code)
    - [Cloning the source code](#cloning-the-source-code)
    - [Installing dependencies](#installing-dependencies)
    - [Running the source code](#running-the-source-code)
    - [Building WingetUI from source](#building-wingetui-from-source)

# How does it work?

To understand how WingetUI works, first it's necessary to understand what is a package manager. Basically, it's a software that allows the users to download, install, upgrade and uninstall computer programs with ease. 

While most Windows users aren't familiar with the concept, various package managers have existed on Linux for several years, such as APT on Debian/Ubuntu and Pacman on Arch Linux.

There are a few unofficial package managers for Windows, such as Chocolatey, Scoop and Ninite. On 2020, Microsoft finally decided to develop an official package manager, called Winget-CLI (inspired by the now defunct AppGet). 

However, there's no official graphical user interface (GUI) for Winget and Scoop. It's necessary a CLI (PowerShell or cmd) to be able to use it. 

Therefore, WingetUI provides a GUI for Winget-CLI and Scoop, making it easy for users to enjoy their capabilities without having to deal with a command-line interface (CLI).
<br><br><br>
Learn more about Winget: https://learn.microsoft.com/en-us/windows/package-manager/

Learn more about Scoop: https://scoop.sh/

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>

# Is WingetUI safe?

WingetUI, Winget-CLI and Scoop are open-source applications, which makes it possible for anyone to verify that there's no malware in their source-code.

However, WingetUI, Microsoft and Scoop aren't responsible for the packages available for download, which are provided by third parties and can theoretically be compromised.

To mitigate the risks of downloading malware, Microsoft has implemented a few checks for the software available on Winget-CLI:

>We are automatically checking each manifest. We leverage SmartScreen, static analysis, SHA256 hash validation and a few other processes to reduce the likelihood of malicious software making its way into the repository and onto your machine

Even so, it's recommended to only download software from publishers that you trust.
<br><br><br>
Source: https://devblogs.microsoft.com/commandline/windows-package-manager-preview/

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>

# WingetUI Installation

<br><p align="center"><b>Check out the <a href="https://github.com/martinet101/WingetUI#installation">installation instructions</a> for more information!</b></p>

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>

# Common Problems

<br><p align="center"><b>Check out the <a href="https://github.com/martinet101/WingetUI#faq">FAQ</a> for more information!</b></p>

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>

# Running and building the source code
Cloning the source code is useful to be able to test WingetUI's source code, to debug it, to modify it, and even to build your custom WingetUI version with your custom features or fixes. Though this steps are really intuitive and are the same that most software use, here are the detailed steps required to achieve that.

If you want to clone a specific version, you can download the source code in a zip file from [GitHub Releases](https://github.com/martinet101/WingetUI/releases)

## Cloning the source code

### Clone using git
1. Open a **Command Prompt** on a folder
2. Run the following command to clone the repository and access it:
```cmd
git clone https://github.com/martinet101/WingetUI && cd wingetui
```
**NOTE:** If you _want_ to use **PowerShell**, the command would be the following:
```powershell
git clone https://github.com/martinet101/WingetUI; cd wingetui
```
![image](https://user-images.githubusercontent.com/53119851/147467203-a23485ff-35e4-45df-bbad-63fba8395c5a.png)
<br><br>

### Clone manually
1. Open a browser and download the [source code](https://github.com/martinet101/WingetUI/archive/refs/heads/main.zip).
2. Extract the files into a new folder. To do this, you can use any zip extractor, such as 7-zip, Winzip, etc...
<br><br>

## Installing dependencies
Python 3.10 is required to run WingetUI. Other versions of python are **NOT** supported. You can download python from [here](https://www.python.org/downloads/windows/)

**NOTE:** The Microsoft Store Python _should_ work, but you **won't** be able to build WingetUI.

When Python 3.10 is installed:
1. Open the folder where the WingetUI source is located. Open the **ROOT** folder of the repo, **NOT** the folder where __init__.py is placed
2. Make sure you have `pip` installed. You can see how to install pip here: https://pip.pypa.io/en/stable/installation/
2. Open a Command Prompt or PowerShell window and run:
```powershell
pip install -r ./requirements.txt
```
3. Wait for it to finish
<br><br>

## Running the source code
1. Open the local repository folder and navigate to a subfolder named wingetui
2. Open a Command Prompt or PowerShell Window on that folder
3. Run the following command:
```powershell
python __init__.py
```
## Building WingetUI from source
1. Open the WingetUI local folder and navigate to the root folder of the repository
2. Run `build.bat` to build a standalone executable file. If the process finishes successfully, a file named `WingetUI.exe` will be generated on the same folder.
2. Run `build_debugging.bat` to build a debuggable executable. If the process finishes successfully, a folder named `__init__` will be generated on the same folder. Access this folder and run the file named `__init__.exe`. A console will appear and WingetUI will run in debugging mode


<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>