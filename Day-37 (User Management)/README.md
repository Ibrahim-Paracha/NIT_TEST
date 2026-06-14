# Day 37 (Module 04)

Module 04
IAM = Identity and Access Management (User Management is a part of IAM)

To change the value of the minimum or max amount of UIDs or GIDs or manage users, you have to go to /etc/login.defs

 to delete users without deleting their files, just type userdel username, but if you want to remove their files as well, add the -r flag, so userdel -r username

To get the id context, type id -Z

In DAC (Discretionary Access Control), the owner can control who can access or edit the files
In MAC (Mandatory Access Control), the system can control who gets access
RBAC (Role Based Access Control)

To check if a user is created, go to /etc/passwd, to see password encryptions, go to /etc/shadow

Use usermod username -g groupname to change a users primary group, and -G to change the secondary group (primary group is always their username) and -Ga to add them to more secondary groups, and the command groups username to check the groups of a user

You can unlock and lock a user by using usermod -L username to lock and -U to unlock, if there is a ! after their name in /etc/shadow, that means its locked, otherwise its not
Locking a user prevents the user loging in

chage command to change the min and max amount of time to change passwords (RHEL)

# (For more detail, go to the 100 Day linux repo,to day 37, module 4)