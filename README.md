# Minishell

A UNIX shell that emulates BASH behavior. Made in cooperation with Kirkram.

# Scope

The minishell handles basic functionalities in the same way as BASH. Including pipes, working directory, enviromental variables,
POSIX signals, redirections including here_doc (<, <<, >, >>).
Readline library is included for portability. The original project uses a installed version on MAC/LINUX.

# Project

My main focus was the parsin/lexing of the project, whie Kirkram was in charge of executing.
We also implemented some of the builtins ourselves: CD, PWD, EXPORT, UNSET, ENV, ECHO and EXIT.
