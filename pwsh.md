# Powershell CLI Cheat Sheet

- [Powershell CLI Cheat Sheet](#powershell-cli-cheat-sheet)
  - [General](#general)
    - [Terminology](#terminology)
      - [Paths](#paths)
        - [Anatomy of a Path](#anatomy-of-a-path)
        - [Path Example](#path-example)
  - [Common Commands](#common-commands)
    - [Interacting with Items](#interacting-with-items)
    - [Navigating your Device](#navigating-your-device)
    - [Getting Information](#getting-information)

## General

### Terminology

- **Directory** - A directory is a collection of files, and or subdirectories.
- [**Path**](#paths) - A path is the directions for how to get to an item on the device.
- **Current Working Directory** - The current working directory (cwd) is the directory that you are currently in within the terminal.

#### Paths

A path is essentially the directions, that tell the computer where to find an item.

There are two types of paths. Relative and absolute.<br>
A relative path is relative to your cwd.
An absolute path starts at the root folder. When working on your own device this is often the drive.
Hence on Windows, an absolute path will often start with `C:`, `E:`, or `D:`.

##### Anatomy of a Path

A path is made up of names of directories separated by either a `\` (on Windows) or a `/` (on Mac and Linux).
I use a Windows device so these cheat sheets will use `\`.
The final part of the path can be either a directory or a file, but anything in between two separator characters must be a directory.

- `.\` or `.` denotes the cwd.
- `..\` denotes one folder up from the cwd. These can be chained so `..\..\` goes two folders up in the tree.

##### Path Example

Take the following example directory tree:

```bash
E:
└── Coding
    └── C
        └── Tutorials
            └── CS50
                ├── hello_world.c
                ├── hello_world.exe
                ├── hello_you.c
                └── hello_you.exe
        └── Projects
            └── Personal
                ├── calculator.c
                └── calculator.exe
```

Let's say I am in the "Coding" directory, and I would like to access the `hello_world.c` file.

The required relative path would be as such `.\C\Tutorials\CS50\hello_world.c`.<br>
While the absolute path would look like `E:\Coding\C\Tutorials\CS50\hello_world.c`.

Now what if we were in the Personal folder. How would we then access the `hello_world.c` file?

We could do it as such:

- Using a relative path: `..\..\Tutorials\CS50\hello_world.c`
- Using an absolute path: `E:\Coding\C\Tutorials\CS50\hello_world.c`

As you can see the absolute path to a file remains unchanged regardless of the cwd,
while this is not the same for the relative path.

## Common Commands

Add `-?` or `--help` after any command to get the documentation for that command.

### Interacting with Items

- `mv` - Move item
  - `mv [path] [destination]`
- `cp` - Copy item
  - `cp [path] [destination]`
- `rni` - Rename item
  - `rni [path] [destination]`
- `mk` - Make item
  - `mk [path]`
- `rm` - Remove item
  - `rm [path]`
- `mkdir` - Make directory
  - `mkdir [path]`
- `rmdir` - Remove directory
  - `rmdir [path]`

### Navigating your Device

- `cd` - Change the cwd (Change directory)
  - `cd [destination]`

### Getting Information

- `ls` - List items
  - `ls [directory]`
  - `ls`
