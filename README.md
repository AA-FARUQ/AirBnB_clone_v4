# AirBnB Clone - The Console

The console is the first phase of the AirBnB project at Holberton School, aimed at covering essential higher-level programming concepts. The ultimate goal is to deploy a simple clone of the AirBnB website (HBnB). This phase includes creating a command interpreter to manage objects for the AirBnB website.

### Features:
* Create new objects (e.g., User, Place)
* Retrieve objects from storage
* Perform operations on objects (count, stats, etc.)
* Update object attributes
* Delete objects

## Table of Contents
* [Environment](#environment)
* [Installation](#installation)
* [File Descriptions](#file-descriptions)
* [Usage](#usage)
* [Examples](#examples)
* [Bugs](#bugs)
* [Authors](#authors)
* [License](#license)

## Environment
This project is tested on Ubuntu 14.04 LTS using Python 3.4.3.

## Installation
* Clone the repository: `git clone "https://github.com/alexaorrico/AirBnB_clone.git"`
* Navigate to the directory: `cd AirBnB_clone`
* Run the console interactively: `./console.py`
* Run the console non-interactively: `echo "<command>" | ./console.py`

## File Descriptions
[console.py](console.py) - Entry point for the command interpreter. Commands include:
* `EOF`, `quit` - Exit the console
* `<emptyline>` - Do nothing
* `create` - Create a new instance of `BaseModel`
* `destroy` - Delete an instance
* `show` - Show an instance
* `all` - Show all instances
* `update` - Update an instance

### `models/` directory
[base_model.py](/models/base_model.py) - BaseModel class:
* `__init__`, `__str__`, `save`, `to_dict`

Derived classes:
* [amenity.py](/models/amenity.py)
* [city.py](/models/city.py)
* [place.py](/models/place.py)
* [review.py](/models/review.py)
* [state.py](/models/state.py)
* [user.py](/models/user.py)

### `/models/engine` directory
[file_storage.py](/models/engine/file_storage.py) - Handles JSON serialization and deserialization:
* `all`, `new`, `save`, `reload`

### `/tests` directory
Unit tests for the project, covering various modules and classes, ensuring PEP8 compliance and functionality.

## Examples
```sh
$ ./console.py
(hbnb) help
EOF  all  create  destroy  help  quit  show  update

(hbnb) create BaseModel
1234-1234-1234
(hbnb) all BaseModel
[BaseModel] (1234-1234-1234) {'id': '1234-1234-1234', 'created_at': '...', 'updated_at': '...'}
(hbnb) show BaseModel 1234-1234-1234
[BaseModel] (1234-1234-1234) {'id': '1234-1234-1234', 'created_at': '...', 'updated_at': '...'}
(hbnb) destroy BaseModel 1234-1234-1234
(hbnb) quit
```

## Bugs
No known bugs at this time.

## Authors
* Faruq Akande - [GitHub](https://github.com/AA-FARUQ) / [Twitter](https://twitter.com/FaruqAdewumi)
* Laurenchia Mugwiria

## License
Public Domain. No copyright protection.
