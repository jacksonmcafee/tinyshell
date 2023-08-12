
# tinyshell

tinyshell is a simple shell program written in C that reads and executes commands from either an interactive prompt or a batch file. 



## Installation

Clone this repository and make the executable:

```bash
git clone https://github.com/jacksonmcafee/tinyshell.git
make
```

Run the tinyshell!

`./tinysh [batch.in]` 
## Documentation

The project implements a basic shell program that emulates the behavior of a command-line interface. It allows users to execute commands interactively or from a batch file. Key features of the shell include:

- **Command Execution:** The program utilizes the `fork` system call to create a child process, which is then replaced by the command execution using `execvp`. This enables the execution of various system commands with their specified arguments.

- **Interactive and Batch Modes:** The shell supports both interactive and batch modes of operation. In interactive mode, users can enter commands directly into the shell prompt. In batch mode, the shell reads and executes commands from a batch file provided as an argument.

- **Graceful Quit Command:** The shell program detects the "quit" command, allowing users to gracefully exit the shell. When the "quit" command is encountered, the program sets a flag to exit gracefully after the current iteration of command processing is complete.

### Main Function

The `main` function serves as the control center of the shell program:

- **Mode Determination:** Based on the number of command-line arguments provided, the `main` function determines whether to operate in interactive or batch mode. In interactive mode (no arguments), the program repeatedly prompts the user for commands. In batch mode (one argument), the program reads and executes commands from the specified batch file.

- **Command Processing Loop:** Within each mode, the program reads input lines, parses them using the `parse_args` function, and then processes each command. For each command, the `parse_commands` function is used to split the command and its arguments. The "quit" command is detected, and a flag is set to gracefully exit the program.

This extremely simple shell program aims to provide a simple and functional command-line environment, capable of executing commands interactively or from a batch file.
## Authors

- [@jacksonmcafee](https://www.github.com/jacksonmcafee)

