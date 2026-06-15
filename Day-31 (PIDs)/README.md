# Day 31

When a new user is created with `` useradd `` ,it picks the files up from /etc/skel and adds them to the new users home
ping a users ip to see if its active or not by typing `` ping ipaddress `` , and to connect to it you can type `` ssh root(or username)@ipaddress ``
First the PID1 gets set up, which is systemd, then sshd, then bash, then bash initialieses it to see which prompt to give, as in which user to give a prompt for, either root or one of the users, it loads up the 2 global files (/etc/profile and /etc/) then the 3 local files (bashrc, bash_profile etc)
``md5sum`` command gives a code on the contents of a file so you could see if there is a difference between 2 files
The `diff` command can also tell if there is any difference between 2 commands, if after entering both filenames after the diff command and there is no output then that means that both files are the same
`echo $PATH` shows the path that the initialization files have set to look for the commands that it executes, if the command is not found in these files, it gives an error that command not found


