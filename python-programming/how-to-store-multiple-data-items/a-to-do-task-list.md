# A To-Do Task List

## Goal

Create a simple to-do task list that prioritizes task with earlier due dates.

_For example:_

```
Our Tasks
- Vacuum, 21 July 2024
- Laundry, 19 July 2024
- Marshall to Vet, 1 August 2024

Priority Order:
1. Laundry, 19 July 2024
2. Vacuum, 21 July 2024
3. Marshall to Vet, 1 August 2024
```

## Program Requirements

* Insert tasks
  * A task should have a string data explaining the task
  * A task should have a date attached explaining the due date
* Remove tasks
  * Either a task was completed or want to be removed
* Task Sorting
  * Tasks are to be sorted based on date (early ones first)
* View the Tasks
  * Display the tasks in order
* Save the Tasks to an external file
  * The program will generate a file after tasks have been inserted
  * The program will remember previous/unfinished tasks by reading the previous task file
  * The program will update with changes and save the changes to the same file

### Python Translation

```python
# Tasker.py
# A to-do task list terminal application

# Internal Imports
import os
from datetime import datetime

# Custom Functions
def task_file_exists():
    ''' This function returns True if we made tasks.txt before '''
    return os.path.isfile("tasks.txt")
# end of task_file_exists()

# Get tasks if tasks.txt has tasks written
def get_tasks(tasks_table):
    data = None
    with open("tasks.txt", "r") as task_file:
        data = task_file.readlines()
        header = data[0]
        data = data[1:]
    # end of reading task_file

    # Iterate the data list and insert it to the tasks_table
    for line in data:
        current_line = line.replace("\n", "")
        current_line = current_line.split(", ")
        task_name = current_line[0]
        task_due = datetime.strptime(current_line[1], '%Y-%m-%d %H:%M:%S')
        tasks_table[task_name] = task_due
# end of get_tasks()

# Option 1: Insert a Task
def insert(tasks_table):
    """ This function inserts a task in the dictionary argument provided """

    task_name = input("Enter the task's name: ")
    print("Enter the task due date:")
    print(" -- Format: (Day Month Year)")
    print(" -- Example: 7 July 2024")
    task_due = input("Input Due date: ")

    # task_due String variable will be turned into a date object via datetime module
    tasks_table[task_name] = datetime.strptime(task_due, "%d %B %Y")
# end of insert()

# Option 2: remove/complete a task
def remove(tasks_table):
    """ This function removes a task in the dictionary argument provided """
    if not tasks_table:
        # There are no tasks!
        print("No tasks to be deleted")
        return None

    print("Which task should be deleted?")
    task_list = list(tasks_table.keys())

    for i, task in enumerate(task_list):
        print(f" -- {i}. {task}")
    
    choice = int(input("Enter the task number to delete: "))
    target = task_list[choice]

    del tasks_table[target]
# end of remove()

# Option 3: Display unfinished tasks
def view(tasks_table):
    """ This function displays the task dictionary table """
    if not tasks_table:
        print("There are no tasks!")

    task_list = list(tasks_table.items())
    task_list = sorted(task_list, key=lambda x : x[1])

    print("Here are your list of tasks:")
    for task, due_date in task_list:
        print(f" - {task} | Due: {due_date}")
# end of view()

# Option 4: Write tasks.txt to save current session info
def export(tasks_table):
    """ This table creates/recreates task.txt with current session's task data"""
    with open("tasks.txt", "w") as task_file:
        task_file.write("List of tasks:\n")

        for task, due_date in tasks_table.items():
            task_file.write(f"{task}, {due_date}\n")
# end of export()

# Initial Setups
options = """
1. Insert a Task
2. Remove/Complete a Task
3. View Unfinished Tasks
4. Export the current list of tasks and end the program.
"""

tasks = {} # Initializing an empty dictionary

# If the tasks.txt file exists, we update tasks dictionary
if task_file_exists():
    get_tasks(tasks)

# End of Setup

# Start the application
while True:
    print(options)
    choice = int(input(" - Select one of the options: "))

    if choice == 1:
        insert(tasks)
    elif choice == 2:
        remove(tasks)
    elif choice == 3:
        view(tasks)
    elif choice == 4:
        export(tasks)
        print("The current session's tasks have been written to tasks.txt")
        break
# end of while loop
```

### Code Explanation



## Connected Readings

* Title (Link)
