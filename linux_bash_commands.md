# Linux and Bash

- Everything in Linux is a file
- Linux is extensionless (it does not consider the file extension when running files)
- Linux is case sensitive (must enter exact file name, case matters)

[Linux/Bash command line interface Tutorial](https://ryanstutorials.net/linuxtutorial/)

To zoom in/out Ctrl + scroll or Ctrl + + or Ctrl + -.

'*' = wild card to include all of whatever follows directly after.

#! = shebang

### Permissions

Permissions are divided into 3 sections: owner of file (u), group (g), everyone else (o).

Permissions include:

r = read

w = write

x = execute/run file

[Linux Permissions Calculator - for short hand](https://chmod-calculator.com/)

## Linux/Bash commands

`cd` = change directory

`cd ..` = changes directory to one directory back

`init` =  initialize

`sudo` = "super user do", gives admin rights for specific command that follows

`apt` = Advanced Packaging Tool, a powerful command-line utility tool in Linux that manages packages (installing, updating, removing) (`apt-get` = instructions for package manager)

`update` = gets updates, but doesn't put them into effect

`upgrade` = puts updates into effect (all latest versions)

`-y` = flag for permission to say 'yes', so it doesn't ask later (automation of permission)

`install` = installs something that is listed after the command

`q` = quit, after executing an installation/upgrade returns to part of VM terminal where you can type further

`pwd` = print working directory in Bash

`ls` = list files, gives all files/folders in current directory (excludes hidden)

`ls -a` = list files all, gives all files/folders in current directory including hidden ones

`touch example.txt` = creates .txt file called example.txt

`file example.txt` = gives type of file (example: empty)

`head example.txt` = first 10 lines of file; `head -2 example.txt` = first 2 lines

`tail example.txt` = last 10 lines of file; `tail -4 example.txt` = last 4 lines

`sort example.txt` = gives alphabetical/numberical order depending on the first character in line (can use flags with this) (numbers take precedence if no further instructions given)

`nl example.txt` = numbers/enumerates lines (can use flags with this)

`wc example.txt` = gives word count; `wc -l example.txt` =  gives number of lines, (other flags available)

`grep` = search (Error: `grep example.txt` = cannot complete, here is where you would use Ctrl + Z)

`grep hello example.txt` = finds and returns each line with hello in example.txt

`top` = real time processes running + details (q to exit)

`ps` = processes being used by user

`ps aux` = displays snapshot of the most amount of information a user usually needs to understand the current state of their system’s running processes

[More on the ps aux command](https://www.linode.com/docs/guides/use-the-ps-aux-command-in-linux/)

Ctrl + Z = kills command to get back to terminal (like task manager)

`touch puppy.jpeg` = creates .jpeg file

`mv puppy.jpeg puppy.txt` = moves and/ renames files/directories (puppy.jpeg is now puppy.txt)

`cat example.txt` = concatenate, reads and shows contents of file without having to open it

`sudo nano new_file.txt` = creates (if file does not exist) and opens file that allows you to write to it. Ctrl + X = exit file gives option to save or not.

`rm puppy.txt` = removes/deletes file (cannot be recovered on Linux)

`mkdir my_folder` = makes directory named my_folder (Note: If you want a name with spaces parse it with "".)

`rm -rf` = removes all files and folders in VM

`rm -rf my_folder` = removes specified directory

`mkdir .hidden_directory` = makes a hidden directory

`touch .hidden_file.txt` = makes a hidden file

`ls *.txt` = lists all .txt files

`ls -l` = gives list of permissions for files

`clear` = clears the terminal from text

`exit` = logs out of VM and returns you to the terminal. Alternatively Ctrl + C does the same.

### Piping: |

Used for chaining commands together & to send data to/from files.

`ls | head -3` = shows the first 3 files/directories

`ls | tail -2` = shows last 3 files/directories

`ls | head -3 | tail -1` = gives the 3rd file name only

`cat example.txt | grep hello` = prints out lines that have hello in it

### Processes:

`sleep 120 &` = creates process called sleep running in background for 120 seconds (currently sleep does nothing)

PID (program ID is a number usually 4 long) = ps to get

`kill <PID>` = ends program (can use without sudo if owner of process, otherwise use sudo)

`kill -9 PID` = forcefully ends program

`sleep 5` = takes away control while running as a foreground process (moves to bg by ctrl + z, but this doesn't kill it)

`fg` = brings background process to foreground

### Long-hand Changing Permissions:

`chmod u+x example.txt` = change permissions on a file to give execute permissions to owner

`chmod g-x example.txt` = change group permissions to remove execute permissions on a file

`sudo chmod +x` = give all permissions to all users

### Short-hand Changing Permissions: 

`sudo chmod 777 example.txt` = give all permissions to all users

[More on Permissions Commands](https://www.pluralsight.com/blog/it-ops/linux-file-permissions)
