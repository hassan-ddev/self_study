# Day 1 --- Navigation
We have some command for navigation purpose:
1. pwd : pwd stands for print working directory it shows where we are in terminal.
2. whoami : if i use this command so it prints my username which i gave during installation.
## ls command
1. ls : ls stands for lists it simply prints all files and folder that are in your current directory.
2. ls -l : we know ls but -l is used to see permissions, size and folder name.
3. ls -a : similarly we know what ls is but now -a means show all files including hidden also.
4. ls -lh : so ls -l prints permissions , size (in bytes) and folder name and other. but adding h give us size in human readable like 4096B --> 4.0KB.
## cd command 
1. cd folder : cd stands for change directory and after cd we can see 'folder' that the name of folder/directory where we want to go.
2. cd .. : we know cd but what is .. let's see when you write ls -a you will see . and .. file or something like file so simple .. works like going backward one directory.
3. cd ../.. : we now cd .. but /.. means one more step similarly you can go two or more steps backward by chaining this /..
4. cd - : - sign change to the previous directory.
5. cd ~ and cd : these both are used for moving directly home directory.
## mkdir
1. mkdir folder_name : mkdir stands for make directory with folder name when we apply this it simply make a folder for us.
2. mkdir -p a/b/c : we know mkdir now -p is used when the parent folder (a is parent folder) is not exist if it exist we simply write a/b/c (b is the child of a and c is the child of b).
## help
1. man command_name : man stands for manual and is used for reading complete manual of any command example man ls
2. whatis command_name : it gives one line of defination about command.
3. command_name --help : it gives information about command pattern and arguments.
## Case sensetive
Guys linux is case sensetive if you have two file like user.log or User.log so these are two different files not same.
## Short cut keys for linux terminal
1. Tab : Auto-complete a command or filename
2. Ctrl + c : it will kill the running process means something is processing in your terminal you press these so it stops at the right time.
3. Ctrl + l : clear the Screen ( same as clear command ) you can write clear also.
4. Ctrl + R : Search through command history.
5. Ctrl + A : Jump to start of line in file if these are opened in terminal.
6. Ctrl + E : Jump to end of line works same as Ctrl + E works.
## The Linux File System:
1. / : that is the space/memory where everything is.
2. home/ : which is really your personal space you can store whatever you want to.
3. etc/ : it contains System config files like wifi config and others.
4. usr/ : all installed programs goes in this folder like python3, pip3 and git also.
5. tmp/ : it contains tmperary files which are removed when system reboots.
6. bin/ : it contains all command we write in terminal.
