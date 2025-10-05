# 0x03. Shell, init files, variables and expansions

This project covers shell scripting fundamentals including variables, expansions, aliases, and shell arithmetic.

## Project Information

- **Project**: 0x03-shell_variables_expansions
- **Language**: Bash
- **Topic**: DevOps, Shell
- **Weight**: 1

## Learning Objectives

By the end of this project, you should understand:

- Shell initialization files (`/etc/profile`, `~/.bashrc`)
- Difference between local and global variables
- Reserved variables (HOME, PATH, PS1)
- Special parameters (`$?`)
- Shell expansions and command substitution
- Shell arithmetic operations
- Creating and managing aliases
- Difference between single and double quotes

## Requirements

- Ubuntu 20.04 LTS
- All scripts exactly 2 lines long
- First line: `#!/bin/bash`
- All files must be executable
- No use of `&&`, `||`, `;`, `bc`, `sed`, or `awk`

## File Descriptions

### 0-alias
Creates an alias `ls` that executes `rm *` (dangerous - removes all files)

### 1-hello_you
Prints "hello user" where user is the current Linux user using `$USER` variable

### 2-path
Appends `/action` directory to the PATH environment variable

### 3-paths
Counts and displays the number of directories in the PATH using `tr` and `wc`

### 4-global_variables
Lists all environment variables using `printenv` command

### 5-local_variables
Lists all local variables, environment variables, and functions using `set` command

### 6-create_local_variable
Creates a local variable `BEST` with value "School" (not exported)

### 7-create_global_variable
Creates and exports a global variable `BEST` with value "School"

### 8-true_knowledge
Performs arithmetic: adds 128 to the value of `TRUEKNOWLEDGE` environment variable

### 9-divide_and_rule
Divides `POWER` by `DIVIDE` environment variables using shell arithmetic

### 10-love_exponent_breath
Calculates `BREATH` to the power of `LOVE` using exponentiation operator `**`

### 11-binary_to_decimal
Converts binary number (stored in `BINARY` variable) to decimal using base notation `2#`

### 12-combinations
Prints all two-letter combinations from aa to zz, excluding "oo", using brace expansion

### 13-print_float
Formats and prints a number with exactly 2 decimal places using `printf`

## Usage Examples

```bash
# Make scripts executable
chmod +x *

# Run scripts that modify environment (use source or .)
source ./0-alias
. ./2-path

# Run regular scripts
./1-hello_you

# Test arithmetic scripts with environment variables
export TRUEKNOWLEDGE=1209
./8-true_knowledge

export POWER=42784
export DIVIDE=32
./9-divide_and_rule

export BINARY=10100111001
./11-binary_to_decimal

export NUM=3.14159265359
./13-print_float
```

## Key Concepts

### Variables
- **Local**: `VARIABLE="value"` - available only in current shell
- **Global**: `export VARIABLE="value"` - available to child processes

### Shell Arithmetic
```bash
$((expression))  # Arithmetic expansion
$((a + b))       # Addition
$((a / b))       # Division
$((a ** b))      # Exponentiation
$((2#binary))    # Base conversion
```

### Special Variables
- `$USER` - Current username
- `$PATH` - Executable search path
- `$?` - Exit status of last command
- `$HOME` - User's home directory

### Command Substitution
- Modern: `$(command)`
- Legacy: `` `command` ``

## Resources

- [Bash Variables](https://www.gnu.org/software/bash/manual/html_node/Shell-Variables.html)
- [Shell Expansions](https://www.gnu.org/software/bash/manual/html_node/Shell-Expansions.html)
- [Shell Arithmetic](https://www.gnu.org/software/bash/manual/html_node/Shell-Arithmetic.html)

## Author

ALX Software Engineering Program

## Repository

- **GitHub**: alx-system_engineering-devops
- **Directory**: 0x03-shell_variables_expansions