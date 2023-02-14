README.md

Welcome to the 0x00. AirBnB clone - The console project!

This project is about writing command interpreter that will manage the AirBnB leading to building of full web application.

The following are required concept for the project: 

First step: Write a command interpreter to manage your AirBnB objects.
This is the first step towards building your first full web application: the AirBnB clone. This first step is very important because you will use what you build during this project with all other following projects: HTML/CSS templating, database storage, API, front-end integration…

Each task is linked and will help you to:

put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances
create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file
create all classes used for AirBnB (User, State, City, Place…) that inherit from BaseModel
create the first abstracted storage engine of the project: File storage.
create all unittests to validate all our classes and storage engine
What’s a command interpreter?
Do you remember the Shell? It’s exactly the same but limited to a specific use-case. In our case, we want to be able to manage the objects of our project:

Create a new object (ex: a new User or a new Place)
Retrieve an object from a file, a database etc…
Do operations on objects (count, compute stats, etc…)
Update attributes of an object
Destroy an object

Resources

Read:

cmd module
cmd module in depth
packages concept page
uuid module
datetime
unittest module
args/kwargs
Python test cheatsheet
cmd module wiki page
python unittest

Learning Objective: 

At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

General:

How to create a Python package
How to create a command interpreter in Python using the cmd module
What is Unit testing and how to implement it in a large project
How to serialize and deserialize a Class
How to write and read a JSON file
How to manage datetime
What is an UUID
What is *args and how to use it
What is **kwargs and how to use it
How to handle named arguments in a function

AirBnB_clone AirBnB clone is an ALX project to build an application similar tothe popular Airbnb. This application will be completed in milestones (steps) and each step will link to a concept:

Description 🏠

AirBnB is a complete web application, integrating database storage, a back-end API, and front-end interfacing in a clone of AirBnB.

The project currently only implements the back-end console.

Storage 🛄

The above classes are handled by the abstracted storage engine defined in the FileStorage class.

Every time the backend is initialized, HBnB instantiates an instance of FileStorage called storage. The storage object is loaded/re-loaded from any class instances stored in the JSON file file.json. As class instances are created, updated, or deleted, the storage object is used to register corresponding changes in the file.json.

Console 💻

The console is a command line interpreter that permits management of the backend of cloneBnB. It can be used to handle and manipulate all classes utilized by the application (achieved by calls on the storage object defined above).

Using the Console

The AirBnB console can be run both interactively and non-interactively. To run the console in non-interactive mode, pipe any command(s) into an execution of the file console.py at the command line.

Files and Directories

models: This directory contains all classes used for the entire project. A class, called "model" in a OOP project is the representation of an object/instance.

tests: This directory contains all unit tests.

console.py: console.py file is the entry point of our command interpreter

models/base_model.py: This file is the base class of all our models. It contains common elements:

attributes: id, created_at and updated_at methods: save() and to_json() models/engine: This directory contains all storage classes (using the same prototype). For the moment, it contains onlt the file_storage.py file.

Authors ✒️

Adeoye Victor Olufemi <Oluviktor>
George Olotu <Tommy_geo>
