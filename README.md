Here's the full README with the modification:

# The AirBnB Clone Project

![AirBnB Logo](https://www.pngitem.com/pimgs/m/132-1322125_transparent-background-airbnb-logo-hd-png-download.png)

## Project Description
This is the first part of the AirBnB clone project where we worked on the backend while interfacing it with a console application using the cmd module in Python.

Data (Python objects) generated are stored in a JSON file and can be accessed with the help of the json module in Python.


## Description of the Command Interpreter:
The interface of the application resembles the Bash shell but with a limited number of accepted commands designed specifically for the AirBnB website.

This command-line interpreter serves as the frontend of the web app, allowing users to interact with the backend developed with Python OOP programming.

Some available commands include:
- show
- create
- update
- destroy

The command line interpreter, coupled with the backend and file storage system, enables the following actions:
- Creating new objects (e.g., User or Place)
- Retrieving an object from a file or database
- Performing operations on objects (e.g., counting, computing stats)
- Updating attributes of an object
- Destroying an object

## How to Start It
These instructions will help you set up a copy of the project on your local machine (Linux distro) for development and testing purposes.

## Installing

Clone the repository of the project from GitHub. This will include the simple shell program and all its dependencies.

```
git clone https://github.com/Lincoln-Madaraka/AirBnB_clone.git
```

After cloning the repository, you'll find a folder named AirBnB_clone containing several files necessary for the program to work.

- **console.py**: The main executable of the project, the command interpreter.
- **models/engine/file_storage.py**: Class that serializes instances to a JSON file and deserializes JSON files to instances.
- **models/__ init __.py**: A unique `FileStorage` instance for the application.
- **models/base_model.py**: Class that defines all common attributes/methods for other classes.
- **models/user.py**: User class that inherits from BaseModel.
- **models/state.py**: State class that inherits from BaseModel.
- **models/city.py**: City class that inherits from BaseModel.
- **models/amenity.py**: Amenity class that inherits from BaseModel.
- **models/place.py**: Place class that inherits from BaseModel.
- **models/review.py**: Review class that inherits from BaseModel.

## How to Use It
The program can operate in two different modes: **Interactive** and **Non-interactive**.

In **Interactive mode**, the console will display a prompt (hbnb) indicating that the user can write and execute a command. After the command is executed, the prompt will reappear, waiting for a new command. This cycle can continue indefinitely until the user exits the program.

```
$ ./console.py
(hbnb) help

Documented commands (type help <topic>):
========================================
EOF  help  quit

(hbnb) 
(hbnb) 
(hbnb) quit
$
```

In **Non-interactive mode**, the shell needs to be run with a command input piped into its execution so that the command is executed as soon as the shell starts. In this mode, no prompt will appear, and no further input will be expected from the user.

```
$ echo "help" | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
$ cat test_help
help
$
$ cat test_help | ./console.py
(hbnb)

Documented commands (type help <topic>):
========================================
EOF  help  quit
(hbnb) 
$
```

## Format of Command Input

To give commands to the console, they need to be piped through an echo in **Non-interactive mode**.

In **Interactive Mode**, the commands need to be typed with a keyboard when the prompt appears and will be recognized when the Enter key is pressed. After pressing Enter, the console will attempt to execute the command, or it will show an error message if the command fails. In this mode, the console can be exited using the **CTRL + D** combination, **CTRL + C**, or the command **quit** or **EOF**.

## Arguments

Most commands have several options or arguments that can be used when executing the program. To recognize these parameters, the user must separate everything with spaces.

Example:

```
user@linux:~/AirBnB$ ./console.py
(hbnb) create BaseModel
49faff9a-6318-451f-87b6-910505c55907
user@linux:~/AirBnB$ ./console.py
```
or
```
user@linux:~/AirBnB$ ./console.py $ echo "create BaseModel" | ./console.py
(hbnb)
e37ebcd3-f8e1-4c1f-8095-7a019070b1fa
(hbnb)
user@linux:~/AirBnB$ ./console.py
```

## Authors
- Lincoln <madarakalincoln48@gmail.com>
- Noni
