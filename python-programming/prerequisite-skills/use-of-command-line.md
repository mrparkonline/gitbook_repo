# Use of Command Line

<figure><img src="https://images.unsplash.com/photo-1629654297299-c8506221ca97?crop=entropy&#x26;cs=srgb&#x26;fm=jpg&#x26;ixid=M3wxOTcwMjR8MHwxfHNlYXJjaHwyfHxjb21wdXRlciUyMHRlcm1pbmFsfGVufDB8fHx8MTY5MzI1ODQ1Nnww&#x26;ixlib=rb-4.0.3&#x26;q=85" alt="" width="375"><figcaption><p>An ubuntu command-line interface</p></figcaption></figure>

Command line proficiency empowers programmers with efficiency, flexibility, automation capabilities, remote access, and deeper system-level understanding, making it an essential skill for software development and system administration.

{% embed url="https://www.youtube.com/watch?v=FpRGRLI8Fy8" %}
How to use Window's Terminal
{% endembed %}

## Windows: Command Prompt & PowerShell

Command Prompt and PowerShell are both command-line interfaces found in Windows operating systems, but they serve different purposes and offer varying capabilities.

{% tabs %}
{% tab title="Command Prompt" %}
Command Prompt is a basic command-line interpreter in Windows. It provides a way to interact with the operating system using text-based commands. Users can execute various commands to perform tasks like navigating the file system, running programs, managing files and directories, and more. Command Prompt commands are often simple and use commands like "dir" to list files and "cd" to change directories. While it's been a core part of Windows for a long time, it has limitations in terms of scripting and automation.
{% endtab %}

{% tab title="PowerShell" %}
PowerShell is a more advanced and versatile command-line shell and scripting language developed by Microsoft. It offers a more comprehensive set of tools and capabilities compared to the traditional Command Prompt. PowerShell enables automation, task scripting, and system administration tasks through its object-oriented scripting approach. It's built on the .NET framework and allows users to manipulate various data sources (such as files, registry, and services) as if they were objects. This makes it particularly powerful for managing and automating complex tasks in Windows environments.
{% endtab %}
{% endtabs %}

{% embed url="https://www.youtube.com/watch?v=5XgBd6rjuDQ" %}
How to use the macOS terminal.
{% endembed %}

## macOS: Terminal

In macOS, the "Terminal" is an application that provides a command-line interface (CLI) to interact with the operating system. It allows users to enter text-based commands to perform various tasks, navigate the file system, run programs, manage files and directories, and more. The Terminal is similar to the Command Prompt in Windows and the shell in Unix-like systems.

## Important Commands for both PowerShell & Terminal

```
Example:

cd C:\User\Park\Documents

will navigate the command line interface to the Documents directory.
```

1. **Listing Files and Directories:**
   * List files and directories: `ls` (macOS) or `dir` (PowerShell)
   * List all files (including hidden): `ls -a` (macOS) or `dir -Force` (PowerShell)
2. **Changing Directories:**
   * Change directory: `cd [directory]`
3. **Working with Files and Directories:**
   * Create a new directory: `mkdir [directory]`
   * Create a new file: `touch [filename]`
   * Copy a file: `cp [source] [destination]`
   * Move or rename a file: `mv [source] [destination]`
   * Delete a file: `rm [filename]` (use with caution)
   * Delete a directory: `rmdir [directory]` (empty directory) or [`rm -r [directory]` (non-empty directory)](#user-content-fn-1)[^1]
4. **Displaying Text:**
   * Display text: `echo [text]` (PowerShell) or `echo [text]` or `echo "[text]"` (macOS)
5. **Getting Help:**
   * Get help for a command: `man [command]` (macOS) or `Get-Help [command]` (PowerShell)
6. **Viewing File Contents:**
   * View file contents: `cat [filename]` (macOS) or `Get-Content [filename]` (PowerShell)
7. **Running Programs:**
   * Run a program or script: `[program]` or `./[script.sh]` (macOS) or `.\[script.ps1]` (PowerShell)
8. **Getting Current Location:**
   * Print current working directory: `pwd` (macOS) or `Get-Location` (PowerShell)
9. **Exiting the Terminal/PowerShell:**
   * Exit the Terminal/PowerShell: `exit`

[^1]: Don't delete system32
