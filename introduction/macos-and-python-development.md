# macOS & Python Development

### Setting up Python for macOS

1. Install Python 3.11 or later from the Python Organization's website ([Link](https://www.python.org/downloads/))
   1. You can install either the Gzipped source or XZ compressed file
2. Install Visual Studio Code from their [**website**](https://code.visualstudio.com/download).
3. Run Visual Studio Code for initial setup
4. You do not need to download any extensions, and you are more than welcome to ignore such pop-ups



<figure><img src="https://brew.sh/assets/img/homebrew-social-card.png" alt=""><figcaption></figcaption></figure>

## Set up Homebrew

[_Instructions here_](https://mac.install.guide/commandlinetools/3)

Homebrew is a free, open-source package manager for macOS and Linux. It simplifies the process of installing, managing, and updating software on your system. Instead of manually downloading and configuring various tools and libraries, Homebrew allows you to install them with a single command.

Homebrew works by downloading the source code of the requested software, compiling it (if necessary), and installing it in a designated location. It also manages dependencies, ensuring that all required libraries are installed automatically.

To use Homebrew, you typically run commands like:

* `brew install <package>` – to install a package.
* `brew update` – to update Homebrew itself.
* `brew upgrade` – to upgrade installed packages.

It's widely used by developers to install programming languages, tools, and libraries efficiently.

{% hint style="danger" %}
Make sure that during installation of Homebrew, you are getting `XCode Command Line Tools`

A message will pop up on your terminal during the installation of homebrew
{% endhint %}

### Homebrew Installation Guide

1. Search for `terminal` on spotlight (The magnification icon on the top right of all macs)
2. Insert the following code on terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

3. Let the Installation complete, then close and quit your terminal.
4. _**MAKE SURE TO RUN THE COMMANDS IT TELLS YOU TO AFTER A SUCCESSFUL INSTALLATION**_

<figure><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdd25hyNQOMs4Xx1Cv_A_oaT0zagfSWlXMBA&#x26;s" alt=""><figcaption></figcaption></figure>

## Git

Git is a distributed version control system that tracks changes to files and coordinates work among multiple people on a project. It allows developers to manage different versions of their code, collaborate efficiently, and revert to previous versions if needed.

### Git Installation Guide

1. Search for `terminal` on spotlight (The maginifcation icon on the top right of all macs)
2. Insert the following code on terminal:

```
brew install git
```

3. This will install `git` using `homebrew` which installed in the prior section

## Add $HOME to your sidebar in Finder

<figure><img src="https://i.ytimg.com/vi/j4rzCTi3dqc/maxresdefault.jpg" alt=""><figcaption></figcaption></figure>

Finder is the file manager for macOS.

Our final step to setup our coding environment on a macOS is to make a shortcut to your home folder.

1. On the top bar of your mac when you have `finder` open, is to go to `settings`
2. Click the Sidebar tab, then select the boxes for the folders you want visible in the Sidebar, which can include Home — it can named like your user account or Home.

<figure><img src="https://cdn3-imgix.macpaw.com/images/content/Make%20Home%20visible%20via%20Finder%20settings_1716382412.png?auto=format&#x26;dpr=1&#x26;fm=png&#x26;ixlib=php-3.3.1&#x26;q=60&#x26;w=608" alt=""><figcaption></figcaption></figure>

3. This will place important directories that we need for coding on the sidebar!
