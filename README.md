# Basic-Linux-Commands
## This project Demonstrates Baslic Linux Commands

### Linux commands are utilities of the Linux OS. All tasks in Linux can be accomplished by executing commands through the Linux terminal. Let's connect to the EC2 instance.

* Navigate to the host directory of the .pem file and connect through ssh

`ssh -l "linux-mini-project.pem" username@<ip address>.zone.compute.amazonaws.com`

![connect](./img/connect-ssh.png)

## Make a directory in the root.

### To create a directory use _mkdir_ command to create a dir name example in the root directory

* `mkdir /root/example`

![mkdir](./img/mkdir-denied.png)

### The *_mkdir_* command returned permision denied. This is because the operation is to carried out on the root folder and requires a super user. Super user do *'sudo'* has to prefix the command. This elevates the current user account to have root privileges.

* Run `sudo mkdir /root/example`

![sudo-mkdir](./img/sudo-mkdir.png)

### To verify that the folder has the created,we use the **_ls_** to view folder content

* Run `sudo ls /root`

![](./img/sudo-ls.png)

### Example folder was created as desired as shown above.

### Print Working Directory *'pwd'* command. This  writes the full pathname of the current working directory to the standard output.

* On the terminal run `pwd` switch to /home/ubuntu `cd /home/ubuntu` run `pwd` again to see that you have moved from root to home/ubuntu which is your username.

![pwd](./img/home-ubuntu.png)

### The root *("/")* directory is the first or top-most directory in a hierarchy

### /bin contains user command binaries for all users both the sysadmin and other users and has no sub directories. Binaries contained in /bin include commands like ls, cp, mv, mkdir, rm etc. 

### /etc directory is a special folder in Linux that holds system-wide configuration files. These files tell your system how to behave, from setting up your network to managing user accounts. 

### /home directory is a directory that is assigned to each user account on a Linux system. It is the directory where a user's personal files and settings are stored.

### /var is a standard directory that stands for "variable files". As the name suggests, this directory contains data that changes frequently while the system is running.

### /usr file system contains executable files that can be shared among machines and user utilities.

* Run `tree -L1` to view some of the root directory contents we talked about. The _L1_ flag means show level 1

![tree](./img/tree-l1.png)

* Run `sudo cd /` to switch to root dir. Them run `pwd` to you are in the root directory.

![pwd-root](./img/pwd-root.png)

* Runs `ls -l` to long list the contects of the root directory.

### `ls -l` is a long listing format that dispalys detailed information about files and directories(permissions, owner, group, size, modification time etc.)

![ls-l](./img/main-ls-l-root.png)

### Notice the total number of items in the root (total 76)

* Run `ls -la` and compare the output.

![kop](./img/ls-la-root2.png)

### The difference is that _ls -la_ is flaged with a _-l_  (detailed listing) and _-a_ (show all files, including hidden ones). This is the reason why total is now 84 as compaired to total 76 from the previous command.

### Let us explore some other commands and directories.



* Run `sudo cd /usr` to change working directory to usr.

![usr](./img/cd-usr.png)

### Make a child directory named photos inside usr

* Run `mkdir photos`

### Permission denied because we ommited the super user do prefix

* Run `sudo mkdir photos`
* Run `cd photos`
* Run `sudo mkdir photo1 photo2 photo3`

![mkdir](./img/usr-photos.png)

* Run `ls` to verify the folders created in the last command

![](./img/show-photos.png)

### Navifgate to first sub-directory in photos directory

* Run `cd photo1` and `pwd` to verify the working directory

![photo1pwd](./img/show-photo1.png)

### Navifgate to second sub-directory in photos directory

* Run `cd ..` to back one step into photos directory then run `cd photo2` and `pwd` to verify the working directory.

![](./img/show-photo2.png)

### Navifgate to third sub-directory in photos directory

* Run `cd ..` to back one step into photos directory then run `cd photo3` and `pwd` to verify the working directory.

![](./img/show-photo3.png)

### _ls_ command.
### The ls command is used to display the files and directories or path in the terminal. The _ls_ command has options that allow users to customize the output.

* Run `ls /home/ubuntu/Documents` to list all files and folders in the Documents directory.

![list-doc](./img/ls-documents.png)

### Some options or flags for _ls_ command includes:
* Run `ls -R` to list all files in the sub folder.

![](./img/ls-R.png)

### ls -R lists all the files in the subdirectories.
* Run `ls -R` to show all files, hidden files inclusive.

![](./img/ls-a.png)

### ls -lh shows the file sizes in easily readable formats, such as MB, GB, and TB.

* Run `ls -lh` to show file sizes in human readable format.

![](./img/ls-lh.png)


### Cat Command

### The cat command in Linux is more than just a simple tool, it’s a versatile companion for various file-related operations, allowing users to view, concatenate, create, copy, merge, and manipulate file contents.

* Run `sudo cat /etc/os-release` to view the OS details

![](./img/cat-os-release.png)

### Add content to a file using `echo` command so we can `cat` to see the contents

* Run `echo 'coping my files' > text1.txt` This will write the sentence in single quote into a file named text1.txt. If this file does not exist, it will be created.


![](./img/copy1file-to-another-.png)


### cp Command
### The `cp` command is an essential tool which is used for copying files or groups of files and directories.



* Run `cp file2.txt /home/ubuntu/Documents` to copy the file.

* Run `ls /home/ubuntu/Documents` to verify the _cp_ command.

![](./img/copy-list-file.png)

### To copy multiple files at once.

* Run `cp text1.txt text2.txt text3.txt /home/ubuntu/Documents` Then list the directory to confirm.

![](./img/multiplt-copy-list-file.png)


### Copy contents of one file to another

* Run `cp text1.txt text4.txt` to copy the contents of text1.txt to text4.txt. Run `cat text4.txt` to verify the cp command.

![](./img/copy1-to-another.png)

### To copy entire directory, run the _cp_ command with a _-R_ flag

* Run `cp -R /home/ubuntu/Documents /home/ubuntu/Documents_backup`

![](./img/cp-R.png)
