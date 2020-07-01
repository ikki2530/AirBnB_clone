#  AirBnB clone - The console

For further information, click on the previous link.


##  Contents:

- Project Description
- General Objectives
- Command Interpreter Description
	* (How to start it)
	* Commands and their usage
	* How to use it
    * examples

## Project Description

Airbnb project is 

##  General Objetives

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

* How to start it
* Commands and their usage
* How to use it
* examples

##  Prerequisites

For further installation is necessary to set this program on Ubuntu 14.04 LTS using Vagrant in VirtualBox.

You need to install this software
```
1. VirtualBox - Virtual Machine
2. Vagrant
3. Emacs
4. Vim/Vi
5. VSCode
6. Usage: ./console.py
```
##  Instalation.

Follow the following instructions to get a copy of the program and run in your local machine.

- Clone the following repository.
> `https://github.com/ikki2530/AirBnB_clone.git`
- Run the program
> `./console.py`

##  Built with...

- Visual Studio Code - Coding and structuring.

- python 3.4.3

###  [BaseModel](./models/base_model.py)

* Write a class BaseModel that defines all common attributes/methods for other classes

###  [File storage](./models/engine/file_storage.py)

* Write a class FileStorage that serializes instances to a JSON file and deserializes JSON file to instances

###  [Console](./console.py)

* Write a program called console.py that contains the entry point of the command interpreter:

  create
- show
- destroy
- all
- update

###  [First User](./models/user.py)
* Write a class User that inherits from BaseModel

###  More classes
* Classes that inherit from BaseModel:
	- [State](./models/state.py)
	- [City](./models/city.py)
	- [Amenity](./models/amenity.py)
	- [Place](./models/place.py)
	- [Review](./models/review.py)
