
### Shell Program

This custom shell provides enhanced functionality, including commands such as `alias`, `unalias`, `listdir`, `getuser`, `setcore`, `getfiletype`, and more. It supports built-in commands, background and foreground execution, and redirection. This shell is designed to work similarly to the Bash shell but with added custom features.

### Features

- **Alias Management**: Set custom command aliases for easier command usage.
- **Directory Listing**: `listdir` command lists files, directories, and links with filtering options.
- **User Information**: `getuser` command retrieves the username and group for a given process ID.
- **Core Affinity**: Set the CPU core for processes using the `setcore` command.
- **File Type Identification**: Quickly identify file types with `getfiletype`.
- **Customizable Prompt**: Change the shell prompt with `chprompt`.
- **Job Control**: Run jobs in the background, bring them to the foreground, and manage their states.

### How to Compile and Run

#### Prerequisites
- **Linux**: The shell is designed for Linux environments, utilizing Linux-specific commands and libraries.
- **G++ Compiler**: Install G++ if not already available:  
  ```bash
  sudo apt update && sudo apt install g++
  ```

#### Compilation

To compile the shell, open a terminal and run the following command:

```bash
g++ -o custom_shell shell_program.cpp -std=c++11
```

Replace `shell_program.cpp` with the name of your file containing the code.

#### Running the Shell

1. **On Linux**:
   Run the shell directly from the terminal:
   ```bash
   ./custom_shell
   ```

2. **On a Virtual Machine**:
   If you’re on another operating system, you can use a virtual machine running Linux (e.g., Ubuntu on VirtualBox).
   - Start your Linux VM, transfer the `custom_shell` binary or the source code.
   - Run it with the command above.

#### Example Commands

- **Set an Alias**:
  ```bash
  alias lsdir='listdir'
  ```

- **List Files**:
  ```bash
  listdir /path/to/directory
  ```

- **Get User Information**:
  ```bash
  getuser 1234
  ```

