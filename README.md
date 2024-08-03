
# Minishell

## Overview

**Minishell** is a project that involves creating a simple shell similar to Bash. This project provides a deep understanding of processes, file descriptors, and shell command execution.

## Summary

The goal of the project is to build a shell that can execute commands, handle pipes, redirections, and support built-in shell commands. It also involves handling special characters, environment variables, and signal management.

## Mandatory Part

### Features

- **Prompt Display**: The shell displays a prompt and waits for user input.
- **Command Execution**: 
  - Executes the right executable based on the `PATH` variable or using a relative or absolute path.
- **History**: Maintains a history of commands.
- **Quotes Handling**:
  - **Single Quotes ('')**: Prevents the shell from interpreting meta-characters within the quoted sequence.
  - **Double Quotes ("")**: Similar to single quotes, but allows expansion of `$` (dollar sign) for environment variables.
- **Redirections**:
  - `<` : Redirect input.
  - `>` : Redirect output.
  - `<<` : Here document; reads input until a line containing the delimiter.
  - `>>` : Redirect output in append mode.
- **Pipes (`|`)**: Connects the output of one command to the input of the next.
- **Environment Variables**: `$` followed by characters expands to their values.
- **Exit Status (`$?`)**: Expands to the exit status of the most recent foreground pipeline.
- **Signal Handling**:
  - **Ctrl-C**: Displays a new prompt.
  - **Ctrl-D**: Exits the shell.
  - **Ctrl-\**: Does nothing in interactive mode.

### Built-in Commands

- `echo` with option `-n`
- `cd` with relative or absolute paths
- `pwd` with no options
- `export` with no options
- `unset` with no options
- `env` with no options or arguments
- `exit` with no options

### Program Requirements

- **Program Name**: `minishell`
- **Turn-in Files**: `Makefile`, `*.h`, `*.c`
- **Makefile Targets**: `NAME`, `all`, `clean`, `fclean`, `re`
- **External Functions**: Various C library functions, including `readline`, `fork`, `execve`, `pipe`, `dup2`, and many others.

## Bonus Part

The following additional features are implemented in the bonus part:

- **Logical Operators**: Support for `&&` and `||` with parenthesis for managing command priorities.
- **Wildcards (`*`)**: Wildcards should function for the current working directory, expanding to match file names.

## Installation and Usage

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/aabderrafie/minishell_42.git
   cd minishell
   ```

2. **Compile the Program**:
   ```sh
   make
   ```

3. **Run the Shell**:
   ```sh
   ./minishell
   ```

4. **Use Built-in Commands**:
   - Use `echo`, `cd`, `pwd`, `export`, `unset`, `env`, `exit`, etc.

5. **Handle Redirections and Pipes**:
   - Use `|` to pipe commands, `<` and `>` for redirections.

6. **Exit the Shell**:
   - Press `Ctrl-D` or type `exit`.

7. **Clean Up**:
   ```sh
   make clean
   ```

8. **Clean Up All Files**:
   ```sh
   make fclean
   ```

9. **Recompile**:
   ```sh
   make re
   ```

## Contributing

Contributions are welcome! Fork the repository, make your changes, and submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

Special thanks to the 42 Network and the community for their guidance and support.
