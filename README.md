  MINISHELL 
-------------
A simple Unix shell written in C, reproducing basic behaviors of bash. 

The goal of this project is to understand how a Unix shell works by implementing a command-line interpreter from scratch.  

The shell parses user input, executes commands, manages processes, and handles signals.


## Features 
- Prompt display and user input handling
- Command execution with absolute and relative paths
- Environment variable management
- Built-in commands:
  - `echo` (with `-n`)
  - `cd`
  - `pwd`
  - `export`
  - `unset`
  - `env`
  - `exit`
- Input/output redirections (`<`, `>`, `>>`)
- Pipes (`|`)
- Signal handling (`Ctrl-C`, `Ctrl-D`, `Ctrl-\`)
- Exit status management (`$?`)


## Challenges & learnings
- Parsing and tokenizing complex user input
- Managing processes using `fork`, `execve`, and `wait`
- Handling pipes and file descriptors correctly
- Implementing redirections without memory leaks
- Signal handling to mimic bash behavior
- Designing a clean and modular architecture


## Build & Run 
Git clone https://github.com/parisseux/42-MINISHELL.git minishell

cd minishell

make 

./minishell


## Usage Exemples
$ echo hello | cat -e
hello$

$ export TEST=42
$ echo $TEST
42

$ ls > files.txt
$ cat < files.txt


## Project Structure 
├── src/
│   ├── command/
│   ├── execution/
│   ├── parsing/
│   ├── signals/
│   └── main.c
├── inc/
├── libft
├── Makefile
└── README.md


👥 Project developed in collaboration with avarrett
