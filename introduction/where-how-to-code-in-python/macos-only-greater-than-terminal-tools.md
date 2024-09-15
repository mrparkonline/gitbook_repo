# macOS Only -> Terminal Tools

<figure><img src="https://brew.sh/assets/img/homebrew-social-card.png" alt=""><figcaption></figcaption></figure>

## Homebrew

Homebrew is a free, open-source package manager for macOS and Linux. It simplifies the process of installing, managing, and updating software on your system. Instead of manually downloading and configuring various tools and libraries, Homebrew allows you to install them with a single command.

Homebrew works by downloading the source code of the requested software, compiling it (if necessary), and installing it in a designated location. It also manages dependencies, ensuring that all required libraries are installed automatically.

To use Homebrew, you typically run commands like:

* `brew install <package>` – to install a package.
* `brew update` – to update Homebrew itself.
* `brew upgrade` – to upgrade installed packages.

It's widely used by developers to install programming languages, tools, and libraries efficiently.

### Homebrew Installation Guide

1. Search for `terminal` on spotlight (The maginifcation icon on the top right of all macs)
2. Insert the following code on terminal:

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

3. Let the Installation complete, then close and quit your terminal.

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
