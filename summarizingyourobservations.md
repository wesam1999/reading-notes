# summarizing your observations
## 1. The Command Line
A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text.<br />
## 2. Navigation
The first command we are going to learn is pwd which stands for Print Working Directory. (this command tell you about your place in terminal).<br />
It's one thing to know where we are. Next we'll want to know what is there. The command for this task is ls. It's short for list. Let's give it a go.(this Current where we are)<br />
we can used Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / ).<br />
In order to move around in the system we use a command called cd which stands for change directory.(it used for enter of the file and Exit from it)<br />
## 3. More About Files
### Quotes
The first approach involves using quotes around the entire item. You may use either single or double quotes (later on we will see that there is a subtle difference between the two but for now that difference is not a problem).<br />
### Escape Characters
which is a backslash ( \ ). What the backslash does is escape (or nullify) the special meaning of the next character.<br />
The command ls which we have seen in the previous section will not list hidden files and directories by default. We may modify it by including the command line option -a so that it does show hidden files and directories.<br />
## 4. Manual Pages
### Searching
It is possible to do a keyword search on the Manual pages. This can be helpful if you're not quite sure of what command you may want to use but you know what you want to achieve.<br />
example:<br />
man -k <search term>  <br />
### More on the Running of Commands
-a or --all  and can uesd both of them like -alh useing ls command
## 5. File Manipulation
### Creating a directory
Creating a directory is pretty easy. The command we are after is mkdir which is short for Make Directory.<br />
example: <br />
mkdir [options] <Directory>  <br />
can we used with it to command like  -p and -v
### Removing a Directory
The command to remove a directory is rmdir. <br />
example:<br />
rmdir [options] <Directory>  <br />
### Creating a Blank File
 In fact we can make use of this very characteristic to create blank files using the command touch.  <br />
example: <br />
touch [options] <filename> <br />
 ###  Copying a File or Directory
The command we use for this is cp which stands for copy. <br />
example: <br />
cp [options] <source> <destination>
### Moving a File or Directory
To move a file we use the command mv which is short for move. <br />
### Removing a File (and non empty Directories)
The command to remove or delete a file is rm which stands for remove.
