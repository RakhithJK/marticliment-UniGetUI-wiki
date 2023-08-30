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
 6. [Running and building the source code](https://marticliment.com/wingetui/help/build-overview/)
    - [Cloning the source code](https://marticliment.com/wingetui/help/build-overview/#download-source)
    - [Installing dependencies](https://marticliment.com/wingetui/help/build-overview/#download-dependencies)
    - [Running the source code](https://marticliment.com/wingetui/help/build-overview/#run-source)
    - [Building WingetUI from source](https://marticliment.com/wingetui/help/build-overview/#build-source)
 7. [Translating WingetUI](#translating-wingetui)
    - [How does it work (Nerd section)](#how-does-it-work-nerd-section)
    - [Contributing](#contributing)
    - [Rules](#rules)
    - [Supported languages](#supported-languages)
 8. [The icon and screenshots database](#The-icon-and-screenshots-database)

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

<br><p align="center"><b>Check out the <a href="https://marticliment.com/wingetui/help/install/#install">installation instructions</a> for more information!</b></p>

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

See our new documentatiojn here: https://marticliment.com/wingetui/help/build-overview/

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>


# Translating WingetUI
Since WingetUI is an app that wants to reach every single person in the world running Windows 11, on issue [#67](https://github.com/martinet101/WingetUI/issues/67) it was requested to add this feature. And here we are. On this page you will find useful information about how does the WingetUI translation program works and how to participate on it, because anyone can contribute here!

You can check the supported languages [here](#supported-languages). If you want to add a new language, drop an e-mail at [marticlilop@gmail.com](mailto:marticlilop@gmail.com)

⚠️ Please, do not create a pull request — follow the instructions below, it's quite easy to translate using Tolgee!

## How does it work (Nerd section)

The method WingetUI uses to translate the UI is based on JSONs, containing a reference sentence and a translated sentence. Every language file codes for a different language, and every language is stored on one single file. If a translation is missing, the program will fallback to English, providing always a readable UI for everyone. Those language files need to be registered to be used, and this is done in [languages.py](https://github.com/martinet101/WingetUI/blob/main/wingetui/languages.py).

## Contributing

Either if you want to update an already existing language or you want to create a new one, the steps are the same:
1. Log in or create an account in [Tolgee](https://app.tolgee.io/projects/). You can log in with GitHub, if you prefer.

![image](https://user-images.githubusercontent.com/53119851/172662695-2842c827-6a03-482a-9264-c17c31382251.png)

2. E-mail me to [marticlilop@gmail.com](mailto:marticlilop@gmail.com) with the following information: the mail you used for registration and the languages where you are willing to contribute.

3. I'll accept you (or not hehe) and you'll find the WingetUI project in your [Tolgee Dashboard](https://app.tolgee.io/projects/)
![image](https://user-images.githubusercontent.com/53119851/172662758-a5b766d2-81cc-454b-90fb-f3abf6def65e.png)

4. Now select the language you want to translate
![image](https://user-images.githubusercontent.com/53119851/172663274-614b8363-ba0f-4841-ab7c-6320aa496853.png)

5. To make things easier, you can filter the untranslated strings
![image](https://user-images.githubusercontent.com/53119851/172664131-a79ed8a5-4c2f-4b2d-823c-bdfb142ec48c.png)

6. You can then start translating. The changes will be included with the next WingetUI release.
![image](https://user-images.githubusercontent.com/53119851/172664301-1935d61f-ed16-47e9-98e4-860eab4e13a8.png)

## Rules

 - Make sure **not to modify the original strings**. If this happened the translation wouldn't work at all.
 - Make sure to add any final stop/colon/semicolon/hyphen/etc.
 - Make sure to add the {0} symbols, since they code for variable values

## Supported languages  

[List of supported languages here](https://github.com/martinet101/WingetUI#currently-supported-languages)
 

<br><br>
_You have arrived at the end of the section. [Return to top](#wingetui)_
***
<br><br>

# The icon and screenshots database
The icon and screenshot list is supported by users like you.

In order to contribute, you need to:
1. open this [Google Spreadsheet](https://docs.google.com/spreadsheets/d/1Zxgzs1BiTZipC7EiwNEb9cIchistIdr5/edit#gid=342425283) and request for write access, telling which packages you wish to update (no need to list all of them, just a few.)
3. You'll be accepted (or not hehe). Paste then the icon andf screenshots URL in a PNG format there. 

NOTE: This guide will be improved soon ;)