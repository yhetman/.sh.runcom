# .sh.runcom

## .bashrc

The shell program /bin/bash (hereafter referred to as just "the shell") uses a collection of startup 
files to help create an environment. Each file has a specific use and may affect login and interactive 
environments differently. The files in the /etc directory generally provide global settings. 
If an equivalent file exists in your home directory it may override the global settings.

An interactive login shell is started after a successful login, using /bin/login, 
by reading the /etc/passwd file. This shell invocation normally reads /etc/profile and its private 
equivalent ~/.bash_profile (or ~/.profile if called as /bin/sh) upon startup.

An interactive non-login shell is normally started at the command-line using a shell program 
(e.g., [prompt]$/bin/bash) or by the /bin/su command. An interactive non-login shell is also started 
with a terminal program such as xterm or konsole from within a graphical environment. This type of 
shell invocation normally copies the parent environment and then reads the user's ~/.bashrc file 
for additional startup configuration instructions.

A non-interactive shell is usually present when a shell script is running. It is non-interactive 
because it is processing a script and not waiting for user input between commands. For these shell 
invocations, only the environment inherited from the parent shell is used.

The file ~/.bash_logout is not used for an invocation of the shell. It is read and executed when a user 
exits from an interactive login shell.

Many distributions use /etc/bashrc for system wide initialization of non-login shells. 
This file is usually called from the user's ~/.bashrc file and is not built directly into bash itself.
