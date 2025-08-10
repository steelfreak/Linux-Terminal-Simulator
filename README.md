# Linux Terminal Simulator - Advanced Web Edition

## Overview
This project is a web-based Linux terminal simulator built using HTML, CSS, and JavaScript. It aims to replicate many common Linux shell features, providing an interactive and educational environment directly in the browser with no backend required.

## Features

### Basic Terminal Simulation
- Simulates a Linux-style command line interface with prompt and input line.
- Supports basic commands: `help`, `ls`, `pwd`, `echo`, `date`, `clear`, `cat`, `whoami`, `history`, `uname`.

### Extended Command Set
- Directory and file management:  
  - `cd` to navigate directories  
  - `mkdir` to create directories  
  - `touch` to create files  
  - `rm` to remove files and empty directories  
- File viewing: `cat filename` to display file contents.
- Command aliases: `alias name='command'` and `unalias name` to create and remove custom command shortcuts.
- Command history with navigation using Up/Down arrow keys.

### Command Autocompletion
- Press `Tab` key to autocomplete commands and filenames.
- Supports autocompletion for commands, aliases, directories, and files in the current path.

### Persistent File System & Session
- Simulated file system stored in-browser using `localStorage`.
- User-created files and directories, history, aliases, current directory, and terminal output persist across page reloads.

### Prompt Customization
- The command prompt dynamically reflects the current working directory.
- Uses `~` as a shorthand for `/home/user` directory.

### Syntax Highlighting
- Terminal output highlights different elements: command names, parameters, directories, errors, and prompts are styled with distinct colors for clarity.

### Mouse Support
- Users can click on terminal tabs to switch between terminal sessions.
- Input field supports default browser text selection and cursor placement.

### Basic File Editor (`nano`)
- Supports a simplified `nano filename` command that opens a modal editor with the file content.
- Allows editing and saving of text files within the simulated file system.

### Multiple Terminal Tabs
- Users can open multiple independent terminal sessions as tabs.
- Each tab maintains separate terminal output, current working directory, file system snapshot, command history, and aliases.
- Tabs can be switched via mouse clicks.

### User Interface
- Clean, monochrome terminal design with green text on black background.
- Blinking cursor effect on command input for realistic feel.
- Responsive layout using flexible containers for terminal and input areas.

## Commands Summary

| Command  | Description                                           | Usage                          |
|----------|-------------------------------------------------------|-------------------------------|
| `help`     | Show list of available commands                      | `help`                        |
| `ls`       | List directory contents                              | `ls [directory]`              |
| `pwd`      | Print working directory                              | `pwd`                        |
| `echo`     | Display text                                         | `echo [text]`                 |
| `date`     | Display current date and time                        | `date`                       |
| `clear`    | Clear terminal output                                | `clear`                      |
| `cat`      | Show contents of a file                              | `cat filename`                |
| `whoami`   | Show current logged-in user                          | `whoami`                     |
| `history`  | Show command history                                 | `history`                    |
| `uname`    | Show system information                             | `uname`                      |
| `cd`       | Change directory                                    | `cd [directory]`             |
| `mkdir`    | Create a directory                                  | `mkdir dirname`              |
| `touch`    | Create a file                                       | `touch filename`             |
| `rm`       | Remove a file or (empty) directory                   | `rm name`                    |
| `alias`    | Create or list command aliases                       | `alias name='command'`       |
| `unalias`  | Remove command alias                                 | `unalias name`               |
| `nano`     | Open basic text editor for file                      | `nano filename`              |

## How to Use

1. Open the HTML file in any modern web browser (Chrome, Firefox, Edge, Safari).
2. Type commands at the prompt and press Enter to execute.
3. Use Up/Down arrow keys to navigate command history.
4. Use Tab key for autocompletion of commands and file/directory names.
5. Use mouse clicks on tabs to switch between multiple terminal sessions.
6. Launch the text editor by running `nano filename` to view or edit file contents.
7. Create files or directories, navigate the file system, and experiment with aliases for a realistic terminal experience.
8. Your changes (files, directories, history, aliases, etc.) persist across reloads.

## Technical Details

- **Frontend only:** No backend or server communication.
- **Persistent state:** Utilizes `localStorage` for saving file system, history, aliases, and terminal content.
- **Modular design:** Supports multiple independent terminal tabs, each with its own isolated environment.
- **Accessible:** Keyboard focused input, ARIA roles for modal dialogs.

## Limitations & Future Improvements

- Limited shell scripting or complex command parsing.
- No real Linux kernel or process simulation.
- Basic `nano` editor without advanced text editing features.
- Does not support mouse terminal escape codes for full mouse interaction.
- Plans for improvements such as better syntax highlighting, mouse-based text selection, and session export/import.

## License

This project is open-source and free to use for educational and personal purposes.

---

Feel free to ask if you want the README tailored or extended further!
