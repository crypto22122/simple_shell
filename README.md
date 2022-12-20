Simple Shell
Simple Shell is a project for students at Alx School. The project test everything we have learned about the C programming language and our skills for work as a team and planning for a long term project.

Description
The Simple Shell is a simple UNIX command interpreter written in C. The program runs based on bash commands obtained from the input stream by the user, the respective command typed by the user in executed as if in a UNIX shell.

Requirements
Allowed editors: vi, vim, emacs
All your files will be compiled on Ubuntu 14.04 LTS
Your C programs and functions will be compiled with gcc 4.8.4 using the flags -Wall -Werror -Wextra and -pedantic
All your files should end with a new line
A README.md file, at the root of the folder of the project is mandatory
Your code should use the Betty style. It will be checked using betty-style.pl and betty-doc.pl
Your shell should not have any memory leaks
No more than 5 functions per file
All your header files should be include guarded
Use system calls only when you need to (why?)
Compilation
All of the .c files along with a main.c file are to be compiled with gcc 4.8.4 on Ubuntu 14.04 LTS with the flags -Wall Werror -Wextra and -pedantic. The files will be compiled this way:

gcc -Wall -Werror -Wextra -pedantic *.c -o hsh
Execute
$ ./hsh
Usage
The shell works like this in interactive mode:

($) ls -l
total 72
-rw-rw-r-- 1 vagrant vagrant   343 Apr 12 01:02 built_in.c
-rw-rw-r-- 1 vagrant vagrant   850 Apr 12 01:02 error.c
-rw-rw-r-- 1 vagrant vagrant   555 Apr 12 14:27 execute_line.c
-rw-rw-r-- 1 vagrant vagrant   305 Apr 10 00:46 _getenv.c
-rwxrwxr-x 1 vagrant vagrant 14563 Apr 12 12:57 hsh
($)
($) pwd
/home/vagrant/simple_shell
($)
($) exit
$
The shell works like this in non-interactive mode:

$ echo "/bin/ls" | ./hsh
built_in.c      _getenv.c    man_1_simple_shell  shell.c         split_line.c
error.c         hsh          mini_shell          shell.h         useful_func.c
execute_line.c  list_path.c  README.md           special_case.c  _which.c
$
$ echo "///////bin/////ls" | ./hsh
built_in.c      _getenv.c    man_1_simple_shell  shell.c         split_line.c
error.c         hsh          mini_shell          shell.h         useful_func.c
execute_line.c  list_path.c  README.md           special_case.c  _which.c
$
$ echo "non-interactive" | ./hsh
./hsh: 1: non-interactive: not found
$
Built-ins
The simple shell has support for the following built-in commands:

Command	Definition
env	Prints the 
