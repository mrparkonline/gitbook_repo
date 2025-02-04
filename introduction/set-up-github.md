# Set up Github

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

[**GitHub**](https://github.com/) is a web-based platform used for version control and collaborative software development, allowing multiple people to work on projects simultaneously. It provides a repository hosting service that includes features like bug tracking, task management, and continuous integration.

{% hint style="danger" %}
On your personal machine, you must have Git installed
{% endhint %}

## Create a GitHub Account

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
It is highly recommended to use your personal email account for GitHub
{% endhint %}

## Setting Git with your Github Account

1. Open Terminal on VS Code
2. _Enter the following code_

```sh
git config --global user.name “YOUR GITHUB USER NAME”
git config --global user.email “YOUR GITHUB EMAIL USED”
```

## Fork the Exercises Repository

{% hint style="info" %}
A repository is a central location where code, files, and documentation for a project are stored and managed, often used for version control and collaboration.
{% endhint %}

1. While logged into your GitHub account, on the same browser: Go to the following repository [**(LINK)**](https://github.com/mrparkonline/marshall-py)

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

2. Fork the Repository to your account
3. Navigate to your forked repository that now exists in **your account**
4. Click the **Code** button. Copy the URL for the repository.
5. On your visual studio code's terminal, go to your home directory

```sh
cd $HOME
```

6. Clone the repository to your own machine

```sh
git clone https://github.com/YOUR-USERNAME/YOUR-FORKED-REPO.git
```

_Make sure to replace_ `YOUR-USERNAME/YOUR-FORKED-REPO` with your repository's information

## How to use this repository

This repository currently contains the following:

1. A directory per exercise problems with solutions on YouTube
2. An empty Python file that a potential programmer can code on.

_It is expected that the user understands/knows how to navigate to different directories and execute a Python file from the terminal._

You should be coding the exercises within these directories then pushing your changes to GitHub.

After any meaningful changes, on your terminal:

```sh
git add FILENAME.py
git commit -m “explanation of changes”
git push
```
