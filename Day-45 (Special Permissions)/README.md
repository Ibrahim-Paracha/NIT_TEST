

`chown user:group file` (to change both owner and group of a file)
`chown user: file` (to change just the user)
`chown :group file` (to change just the group)

`usermod -aG group user` (to add a user to a group)
`groupadd groupname` (to create a new group)


## ACLs (Access Control List)
---------------------------
`getfacl file` (to check the acl of a file)

`setfacl -m u:user:rwx file` (you can see when acl is applied if there is a + after the permissions)

`namei -l file`

`setfacl -b file` (to remove ALL acls)

`setfacl -x u:user file` (to remove the permissions given through acl to a user)

------------------------------------------------------
## Sticky bit (represented with a 1)

Can be set with either `chmod 1755 folder` or `chmod +t folder`
(in a directory with sticky bit, only users or root can delete their own files, even if others have write permission they cant delete the files, this is mostly common in the /tmp folder)(showed with a t at the end of the permissions)(there should be a 1 if the stat command is run on the file in the access section) 
If at the end of the permissions the t is small, that means that others have execute permissions, if the T is captial, that means that other do not have execute permissions.


## SUID (special permission for user)(represented with a 4)

Can be set with either `chmod 4755 file` or `chmod u+s file`
like in the passwd command (run the whereis passwd command, you should see a s in the permissions of the user), this means that users also have the permission to run this command along with root
To check which commands have this SUID, run `find /usr/bin/ -perm -4000`
This means that these commands run with any user like they do with root.
if the stat command is run on the file, there should be 4 in the access section that means that the file has this

## SGID (s in the group permissions in the file)(represented with a 2)

Can be set with either `chmod 2755 folder` or `chmod g+s folder`
This means that if a directory has this setting, then all files created inside this will have the group settings of that directory, so all files will have the primary group of the directory.
