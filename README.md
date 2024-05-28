# Parallelization of search queies to web server using Rust language
## Free Software (free software)

The application is free software.

## Functions
- Application of regular expressions to search by pattern
- Lemmatization and sorting of text in a text file and search bar
- Converting letters in a text file and search string to lowercase
- Create independent threads to find matches in each text file
- Presentation of information in the browser

 
## Requirements:
- [Rust](https://www.rust-lang.org) - to create applications 
- [Actix Web](https://actix.rs) -  Web framework for Rust
- [JavaScript](https://www.ecma-international.org/publications-and-standards/standards/ecma-262) - to send the search string to the server
 - [Python](https://www.python.org) - for lemmatization and text sorting

 The application is also open source with code on Github

## Installation
Installation on Linux (Fedora) is performed with administrator rights.
To run the project you need to install Rust.
Installing Rust:

\# dnf install rust cargo

To install dependencies correctly, the Cargo.toml file must contain:

[dependencies]

actix-web = "4"

serde = { version = "1.0.201", features = ["derive"] }

regex = "1.10.4"

Installing Python:

\# dnf install python

Installing pip:

\# dnf install python3-pip

Installing package for text lemmatization:

\# pip install pymystem3


The text of the Rust program is contained in the file **src/main.rs**.
The project directory contains subdirectory **public**.
The subdirectory **public** contains the subdirectory **html** in it. 
The **html** subdirectory contains the files **index.html** and two text files in which the search is performed **file1.txt** and **file2.txt**.
In the file **python_lemma/a.py** there is a variable **text**.
The text to be lemmatized is assigned to variable **text**.

Lemmatize text by running the command

\$ python a.py

The console output will contain the lemmatized, sorted, and lowercase text.
The resulting text should be entered into a text file(s) that will be used for searching.


## Usage
Rust is started from the project directory using the command

\$ cargo run

Open localhost:8080 in the browser.
A text input area will appear on the screen. 
The lemmatized and sorted text for the search should be entered in the text input area.
The text is converted to lower case in the **src/main.rs** file.
The result will be displayed on the screen.


## License
MIT
