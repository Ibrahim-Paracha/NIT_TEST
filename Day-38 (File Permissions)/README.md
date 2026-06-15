# Day 38

To see history size, run `$HISTSIZE

After running the history command, each command has a number, to run a command with its number just type the number with a exclamation mark (!) before it (eg !205 to run command 205)

Difference between su - user and su user is that with the -, it logs in as the user completely, loads the initialization files, and loads the users path and usually asks for the password, while without the - it logs in as the user through root rather than as the user completely, and doesn't load the init files and keeps the root/prev users environment.

`STOUT = 1`, `STERR = 2`, `STIN = 0`

To add both STOUT and STERR to a file, eg `cat /etc/passwd /etc/shadow > file.txt 2>&1`, which means that just put the error along with the output, so you should get both the output from the /passwd file, and the error from the /shadow file in the file.txt.

If you wish to add the output and error in separate files, you can run `cat /etc/passwd /etc/shadow > output.txt 2> error.txt`.

           ==========================================================

# FILE PERMISSIONS

x=1, w=2, r=4

The kernel gives full permission ie for files 666 and for directories 777, but the umask by default changes the values, and subtracts 022 from each of them. So 644 and 755.

chmod to change file permissions
chown to change file owner
chgrp to change file group
(chown can change both owner and group together as well, by running chown username:groupname filename, and if you just run this command without the username {:groupname} this will change just the groupname)

