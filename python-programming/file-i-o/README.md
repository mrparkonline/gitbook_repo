# 💾 File I/O

File Input / Output (I/O) is a fundamental concept in programming that involves reading data from and writing data to external files.&#x20;

It is recommended that you read the following article from [**realpython**](https://realpython.com/read-write-files-python/).

## Benefits

1. **Data Persistence**: File I/O allows programs to store data persistently on disk, ensuring information is retained across program runs.
2. **Data Sharing**: It provides a means for different programs and platforms to exchange data efficiently.
3. **Configuration and Logging**: File I/O is essential for storing program configurations and logging events and errors.
4. **Data Import/Export**: Files enable data import/export in various formats, making it valuable for data analysis and interactivity.
5. **Resource Management and Security**: Properly managing file resources is essential, and file permissions ensure data security from unauthorized access.

In Python, the `open()` function can read plain text files without the need to import additional modules. You can read files with the following extensions using `open()` without importing any additional modules:

1. `.txt`: Plain text files.
2. `.log`: Log files.
3. `.ini`: INI configuration files.
4. `.cfg`, `.conf`: Configuration files.
5. `.dat`: Generic data files.

For these file types, you can use `open()` to read the content line by line or as a whole, depending on your needs.&#x20;

### Example: Reading a `.txt` file

```python
# Open and read a plain text file
with open('example.txt', 'r') as file:
    content = file.read()
    print(content)
```

## How to do File I/O in Python

```python
# Formatting

with open('path/filename.extension', 'mode') as file_object_label:
    
    # Some code here dealing with the file object

# end of open() ... the file is now closed.
```

### Note

* `open()` creates a file object in Python that links an external file to your python script
* `with open() as label:` creates a new code block where you can interact with the file object created by `open()`.&#x20;
  * We use this nomenclature to let the with statement close our files if we exit the code block.
  * Closing a file object in Python is important because it releases system resources (such as file handles) associated with the file, ensuring that other programs can access it. Failing to close a file properly may lead to resource leaks and potential data corruption, especially when writing to a file, as data may not be flushed from memory to disk until the file is closed.

### `open()` different modes

```python
# Reading Data
with open("example1.txt" , "r") as file_obj:
```

In this situation, we set our mode as `"r"` for _reading._ Our intended purpose with the file is to obtain data from the file.

```python
# Writing Data
with open("example2.txt" , "w") as file_obj:
```

In this situation, we set our mode as `"w"` for _reading._ Our intended purpose with the file is to overwrite an existing data from the file.

If the `"example2.txt"` file did not exist in the same directory as the python script, it will create a new file entitled `"example2.txt".`

```python
# Appending Data
with open("example.txt" , "a") as file_obj:
```

In this situation, we set our mode as `"a"` for _appending._ Our intended purpose with the file is to add data starting from the end of the file. If the file does not exist, it will be created.

{% hint style="info" %}
#### Other Notable Modes:

**'x' (Exclusive Creation)**:

* Opens the file for exclusive creation.
* Raises an error if the file already exists.

**'+' (Read/Write)**:

* Appends '+' to any mode ('r+', 'w+', 'a+', etc.) to allow both reading and writing.
* The file is opened in both read and write modes.
{% endhint %}

### How to read data from a file.

1.  **`.read()`**:

    * This method reads the entire content of the file as a single string.
    * You can specify the number of characters to read as an optional argument, but if omitted, it reads the entire file.

    ```python
    with open('example.txt', 'r') as file:
        content = file.read()  # Read the entire content
        print(content)
    ```
2.  **`.readline()`**:

    * This method reads a single line from the file each time it's called.
    * It returns an empty string when it reaches the end of the file.

    ```python
    with open('example.txt', 'r') as file:
        line1 = file.readline()  # Read the first line
        line2 = file.readline()  # Read the second line
        print(line1)
        print(line2)
    ```
3.  **`.readlines()`**:

    * This method reads all lines of the file and returns them as a list of strings.
    * Each element in the list represents a line from the file.

    ```python
    with open('example.txt', 'r') as file:
        lines = file.readlines()  # Read all lines
        for line in lines:
            print(line)
    ```

It's important to note that these methods maintain a position in the file, so consecutive calls to `.readline()` will read successive lines, and calling `.read()` or `.readlines()` again will continue from where the file pointer is located. To reset the file pointer, you can use `.seek()` to change the file's position.

### How to write new data onto a file.

1.  **Open the File in Write Mode**: First, you need to open the file in write mode ('w'). If the file doesn't exist, it will be created. If it does exist, its contents will be truncated (deleted).

    ```python
    with open('example.txt', 'w') as file:
        # Use 'w' mode to open the file for writing
        # This will create a new file or overwrite an existing one
    ```
2.  **Use `.write()` to Write Data**: You can use the `.write()` method to write data to the file. It takes a single string argument that represents the data you want to write.

    ```python
    with open('example.txt', 'w') as file:
        file.write("Hello, world!\n")
        file.write("This is a new line of text.")
    ```
3.  **Close the File**: After writing data, it's a good practice to close the file using the `with` statement or the `.close()` method to ensure that changes are flushed to the file and resources are released.

    ```python
    with open('example.txt', 'w') as file:
        file.write("Hello, world!\n")
        file.write("This is a new line of text.")
    # File is automatically closed when the 'with' block exits
    ```

This code will create or overwrite the file "example.txt" with the specified text. If the file already exists, the content will be replaced, so be cautious when using 'w' mode to avoid unintentional data loss.

{% hint style="info" %}
To avoid deleting the contents of a file and add on data instead, the mode should be set to `"a"` for your `open()` mode.
{% endhint %}
