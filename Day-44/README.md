# Day - 44

## -The find command-
The find command, you can use it with `-type f (file), d (directory), l (sym link), b (block) or s (socket)` and also `-name` to search for a specific files name, or `-size +20(K/M/G)` to search for a file above 20, or `-user username` to search for files of a user, or `-empty`, or `-mmin -20` to search for files that were modified in the last 20 mins, or `-mtime -1` (this applies for files that are a day old)

Example command `find /home -type d -name "dev"`

`find / -type f -size +20M -exec ls -ld {}\;`

`find / -type f -mtime -1 -exec rm -rf {}\;` (the exec tells the system to run the rm command on all the results from the find command, and the {} means on all the files from the find command, and the \; tells the shell that this is where the command ends)

## -The stat command-
this command tells us multiple things about a file, including its size, blocks, file type, inode, links, context etc.

## Here document
`cat << EOF > file.txt`
this tells the shell to keep adding the text i type to the file until i type "EOF" (which can be replaced with almost any word)

# /dev/null
This is the abyss of linux, if you dont need the output of a command or file, you can send it to this file.

## grep flags
### -i (ignore case)
While using grep or searching for something, using the `-i` flag will allow it to ignore case.

### -v (invert match)
To hide the word you search for, it shows all lines that dont have the word you search for (eg grep -v "^#" /filename) (the ^ means starts with).

### -r (Recursive directory search)
This tells grep to look inside the specified folder and look thru every single sub directory. (`grep -r "ibrahimsfiles" /etc`)

### -c (Counting matches)
Instead of printing out every single line, this just outputs a single line telling how many times that string appeared.


