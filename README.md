#  HBnN   - AirBnB clone

##  Contents:

- Project Description
- General Objectives
- Command Interpreter Description
    * How to start it
    * Commands and their usage
    * How to use it
    * examples

## Project Description

HBnB is a 4-month-long project which has as its main goal to deploy a clone of
the AirBnB website on our server.
The final version needs to include the following:A command interpreter to manipulate data without a visual interface, like in a Shell (perfect for development and debugging).
A website (the front-end) that shows the final product to everybody: static and dynamic database or files that store data (data = objects).
An API that provides a communication interface between the front-end and your data (retrieve, create, delete, update them).


##  Learning Objectives

Learn:
* How to create a Python package
* How to create a command interpreter in Python using the cmd module
* What is Unit testing and how to implement it in a large project
* How to serialize and deserialize a Class
* How to write and read a JSON file
* How to manage datetime
* What is an UUID
* What is *args and how to use it
* What is **kwargs and how to use it
* How to handle named arguments in a function

## Command Interpreter Description

It is a console capable of performing the following tasks:

Create a new object (ex: a new User or a new Place)
Retrieve an object from a file, a database etc…
Do operations on objects (count, compute stats, etc…)
Update attributes of an object
Destroy an object
* How to start it

In interactive mode:
```
$ ./console.py
(hbnb) help

Documented commands (type help <topics>):
========================================

EOF  help  quit

(hbnb)
(hbnb)
(hbnb) quit
$
```
In non-interactive mode:
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


* Commands and their usage


quit and EOF to exit the program
help to print the list of commands with help documentation (see example above).

Usage:
help <command_name>
help

Example:
```
$ help
$ help quit
```

create: Creates a new instance of a class, saves it (to the JSON file) and prints its id

Usage:
create <class name>

Example:
```
$ create BaseModel
```

show: Prints the string representation of an instance based on the class name and id

Usage:
show <class name> <instance id>
<class name>.show(<id>)

Example:
```
$ show BaseModel 1234-1234-1234
$ BaseModel.show(“1234-1234-1234”)
```

destroy: Deletes an instance based on the class name and id (save the change into the JSON file). 

Usage:
destroy <class name> <instance id>
<class name>.destroy(<id>)

Example:
```
$ destroy BaseModel 1234-1234-1234.
```


all: Prints all string representations of all instances based or not on the class name. 

Usage:
all <class name>
<class name>.all()

Example:
```
$ all BaseModel
$ all
$ User.all()
```

update: Updates an instance based on the class name and id by adding or updating attribute (save the change into the JSON file). 

Usage:
update <class name> <id> <attribute name> "<attribute value>"

Example:
```
$ update BaseModel 1234-1234-1234 email "aibnb@holbertonschool.com"
```


count: Retrieves the number of instances of a class.

Usage:
<class name>.count().

Example:
```
User.count()
```


##  Prerequisites

This program needs to be run using Ubuntu 14.04 LTS preferably.

##  Installation.

- Clone the following repository.
> `https://github.com/ikki2530/AirBnB_clone.git`
- Run the program
> `./console.py`

##  Built with...

- Visual Studio Code and emacs - Coding and structuring.
- vagrant (Ubuntu 14.04 LTS)
- Virtual Box – virtual machine
- python 3.4.3

## Classes

###  [BaseModel](./models/base_model.py)

* class BaseModel that defines all common attributes/methods for other classes

###  [File storage](./models/engine/file_storage.py)

* class FileStorage that serializes instances to a JSON file and deserializes JSON file to instances

###  [User](./models/user.py)
* class User that inherits from BaseModel

###  More classes
* Classes that inherit from BaseModel:
    - [State](./models/state.py)
    - [City](./models/city.py)
    - [Amenity](./models/amenity.py)
    - [Place](./models/place.py)
    - [Review](./models/review.py)

###  [Console](./console.py)

* program called console.py that contains the entry point of the command interpreter and executes the following commands: create, show, all, count, destroy, update