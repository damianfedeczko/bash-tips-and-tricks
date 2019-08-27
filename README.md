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

### Debugging Bash Scripts ###

When things don't go according to plan, you need to determine what exactly causes the script to fail. Bash provides extensive debugging features. The most common is to start up the subshell with the -x option, which will run the entire script in debug mode. Traces of each command plus its arguments are printed to standard output after the commands have been expanded but before they are executed.

This is the script.sh script ran in debug mode.
$ bash -x script.sh

Using the set Bash built-in you can run in normal mode those portions of the script of which you are sure they are without fault, and display debugging information only for troublesome zones.

$ set -x	# activate debugging from here
$ set +x	# stop debugging from here

### Pattern maching ###

$ "*" - matches any given character
$ "$" - matches a single character
$ "[zbc]" - matches any of the characters inside the square brackets. If the first character within the brackets is either an exclamation point "!" or a carat "^", then the pattern means anything other than the remaining characters in the brackets. Basically, [^zbc] means, that your capturing group will match everything besides the "z", "b" or "c".

Similar to ranges, you can specify character classes within braces.

Character class | Description
-------------------------------------------------------------------
[:alnum:] 	| Alphanumeric
[:alpha:] 	| Alphabetic
[:ascii:] 	| ASCII
[:blank:] 	| Space and tab
[:ctrl:] 	| Control characters
[:digit:] 	| Number
[:graph:] 	| Anything other than control characters and space
[:lower:] 	| Lowercase
[:print:] 	| Anything other than control characters
[:punct:] 	| Punctuation
[:space:] 	| Whitespace including line breaks
[:upper:] 	| Uppercase
[:word:] 	| Letters, numbers, and underscore
[:xdigit:] 	| Hexadecimal
