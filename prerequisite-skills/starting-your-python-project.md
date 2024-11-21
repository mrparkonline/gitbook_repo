# Starting Your Python Project

**0. Set Up Your Visual Studio Code**

```
Open Visual Studio Code
File >> New Window

(In your new window)
File >> Open Folder >> Right Click on an Empty Space and Create a New Folder
     >> Select the newly created folder

```

1. **Learn the Terminal**

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

[TerminalTutor](https://www.terminaltutor.com/) is a fanatastic tool to learn how to use the terminal.

2. **Create a Github Repository and Clone it onto your drive**

Git + Github is a good way to do version control so that you can go back to your previous states of your program without worrying about `CTRL+Z`.&#x20;

## DO NOT CLONE A REPOSITORY INSIDE ANOTHER REPOSITORY

{% hint style="info" %}
#### Creating a Public/Private GitHub Repository

1. **Log in to GitHub**:
   * Go to GitHub and log in with your credentials.
2. **Create a New Repository**:
   * Click on the **+** icon in the top right corner and select **New repository**.
3. **Repository Details**:
   * Enter a **repository name**.
   * Optionally, add a **description**.
   * Select **Private** under the repository visibility options.
   * Optionally, you can initialize the repository with a README, .gitignore, or a license.
4. **Create Repository**:
   * Click on the **Create repository** button.

#### Cloning the Repository to Your Local Machine

1. **Copy Repository URL**:
   * On your repository page, click on the **Code** button.
   * Copy the URL provided (either HTTPS or SSH).
2. **Open Terminal/Command Prompt**:
   * Open your terminal (Mac/Linux) or Command Prompt (Windows).
3. **Navigate to Desired Directory**:
   *   Use the `cd` command to navigate to the directory where you want to clone the repository.

       ```bash
       cd path/to/your/directory
       ```
4. **Clone the Repository**:
   *   Use the `git clone` command followed by the repository URL you copied.

       ```bash
       git clone https://github.com/your-username/your-repository.git
       ```
5. **Navigate into the Cloned Repository**:
   *   Change into the repository directory:

       ```bash
       cd your-repository
       ```
{% endhint %}

3. **(Windows Only) Enable your computer to run scripts**

{% hint style="info" %}
1. **Open PowerShell as Administrator**:
   * Press `Win + X` and select **Windows PowerShell (Admin)** or **Windows Terminal (Admin)** if you're using Windows Terminal.
2.  **Check Current Execution Policy**:

    * In the PowerShell window, type the following command and press Enter:

    ```powershell
    Get-ExecutionPolicy
    ```

    * This will show you the current execution policy. By default, it might be set to `Restricted`.
3.  **Set Execution Policy**:

    * To allow scripts to run, you can set the execution policy to `RemoteSigned`

    ```powershell
    Set-ExecutionPolicy RemoteSigned
    ```
{% endhint %}

4. **Set up a Python Virtual Environment in your repository**

The reason we want to have a Python Virtual Environment is to isolate our project for the following benefits:

* **Isolated Projects will have their own modules and libraries installed**
  * Example: If your project is using an earlier version of Streamlit and your computer has a newer version of Streamlit, your project will not be affected by the local machine's version differences
* Easier to create a list of libraries and modules your project is dependent on

{% hint style="info" %}
**Create a Virtual Environment**:

```bash
// Windows
python -m venv myenv

// macOS
python3 -m venv myenv
```



This command creates a directory named `myenv` containing a new Python environment.

**Activate the Virtual Environment**:

On **Windows**:

```bash
myenv\Scripts\activate
```



On **macOS/Linux**:

```bash
source myenv/bin/activate
```



To Deactivate to `venv` you can simply run `deactivate` on your terminal
{% endhint %}

5. With your virtual environment activated, **Install your libraries/dependencies/modules**

**Windows:**

```bash
python -m pip install PACKAGENAME

// Example: python -m pip install pygame
```

**macOS:**

```bash
python3 -m pip install PACKAGENAME

// Example: python3 -m pip install pygame
```

Now your project should have all it requires.

6. Upload any changes to your GitHub

```bash
// On changes
git add FILENAME
git commit -m "What changes you have made"
git push
```
