# Bash tips and tricks
This repository will consist of a number of commands and shortcuts I found useful or interesting when working with the Linux Command Line Interface, called later on simply the CLI. Feel free to contribute and share your favourite tips and tricks! 

## What is the Command Line Interface, and why do I focus on bash?

Before we even start, let's anwser those two simple questions from above. The CLI is a tool which gives an intimate connection with the underlying operating system (OS). Within the operating system lives an astounding amount of functionality that has been cherished and improved over decades of use and development. Unfortunetly, the ability to interact with the OS by using the command line is quickly becoming a lost art. It has been replaced instead by graphical user interfaces (GUIs), which often increase ease of use at the expense of speed and flexibility, and distance the user from the underlying capabilities.

As for the bash shell, it has been around for decades, it's available in nearly every version of Linux, and has even permeated the Windows operating system.

### Files, Scripts, Built-ins, and Keywords

The commands that you can run within your CLI are either files, built-ins, or keywords.
- Files are executable programs.
- Scripts are human-readable text files possible to interpret and execute by your system.
- Built-ins are part of the shell.
- Keywords are also just parts of the language of the shell.

To check if a word is a keyword, built-in or a file, you can use the type command:

$ type -t if
keyword

$ type -t pwd
builtin

$ type -t ls
file
