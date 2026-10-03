# Day 34

Understanding aliases

To create a temporary alias, just type `alias shortcut 'command'`, and you can remove it by typing `unalias shortcut`.

To create a permanent alias, go to ~/.bashrc, and enter the command in the same format. To remove this alias, go to the file and remove the alias. After entering or removing a new alias, you must run `source ~/.bashrc` for the alias to run.

To view available aliases, simply type `alias`.

## Some useful aliases for a Linux Admin:
- alias mylogs='ls -l /var/log'
- alias mynet='ip addr'
- alias mydisk='df -h'
- alias mymem='free -h'
- alias myproc='ps -ef'