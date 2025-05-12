# Basic-Linux-Commands
## This project Demonstrates Baslic Linux Commands

### Linux Commands are typed in terminal. Let's connect to the EC2 instance.

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

### Example folder was created as desired as seen above.



