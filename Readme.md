#   CodeAnalyzer
## About::
CodeAnalyzer is a `GO` based program that helps in analyzing a code base.
User will have to enter the path and command to run test for a code base.

CodeAnalyzer will trace the calls of function and display it on terminal.
A web based UI will also be developed for the same.
The facility will be independent of the coding language used in the code.

##  Usage::
OpenSource contribution is getting popular day-by-day and the same should be encouraged.
To get introduction to the code base for a neive developer is a troublesome process in which,
he/she ends up most of his/her time spending on.
To aid the understanding and analyzing the codebase CodeAnalyzer will be used.
Unlike traditional debugging tools CodeAnalyzer will also be able to work on a Codebase with 
multiple coding languages used.

##  Working::
### Input::
- `path` for the codebase. 
- `path` for the temperory directory.
- `command` to run the tests.
- build `commands`.
- `debugging level` 
  - 0: Only displays the functions that are called.
  - 1: Displays the functions used along with the variables used while calling the function.

### Workflow::
- The engine will take the commands.
- A unique id will be given and will be registed in the database.
- Throughout the codebase, functions will be identified as per the coding language.
- Each of these functions will be given an unique id and will be registed in the database.
- These functions will be modified as per the debugging level to print the debugging statements in the logs along with the function id.
- The codebase will be build and a test files will be called.
- Logs will be collected, parsing out the function id and the input variables.
- This will be saved in the database.
- Whenever the user intends to analyze the function calls, the data will be taken from the database and displayed on the screen/ terminal.


## Development workflow::
|Steps|Details|Status|
|-|-|-|
|CodeAnalyzer Engine|The main engine which will be responsible to handle the API calls| |
|Go Plugin|Plugin to add the debuggin statements in a Go codebase| | 
|Database Connection feature for Postgres| Saving the metadata in a database| | 
|CodeAnalyzerTerminal|A terminal based UI for analyzing the codebase| | 
|Generalize the Database feature|Allow the addition of plugins for other database| |
|Python Plugin|Plugin to add the debuggin statements in a Python codebase| |
|Elixir Plugin|Plugin to add the debuggin statements in a Elixir codebase| | 

