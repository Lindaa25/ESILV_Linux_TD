# TD1
## Exercice 1 : Move around

### 1. Go to the root directory
```
$ cd /
```
the “/$” sign indicates that you’re in the root directory now.

### 2. Display the content of the current (root) directory
```
$ cd
```
### 3. Check your current location
```
$ pwd
```
### 4. Try to create a directory named test
```
$ mkdir test
```
### 5. Go to the general home directory (should contain folders named after each user)
```
$ cd ..
```
quand il y a d'autres utilisateurs il y a un 'general home' entre root et home (mais pas le cas pour nous)
### 6. Go to your home directory
```
$ ~
```
### 7. Go back to the general home directory (located "just above")
```
$ cd ..
```
### 8. Go again "just above", you should be back to the root directory
```
$ cd 
$ pwd
```

## Exercise 2 : Create, Rename, copy, delete

### 1. Go to your home directory (should be named after you, you might be there by default)
```
$ pwd
```

### 2. Check your current location
```
$ pwd
```

### 3. Create a folder linux_l
```
$ mkdir linux_l
```

### 4. Go to this folder
```
$ cd linux_l
```

### 5. Create an empty file named (first name/last name)
```
$ touch linda_he.txt
```

### 6. Create a folder notes
```
$ mkdir notes
```

### 7. Move your text into this folder
```
$ mv linda_he.txt notes/
```

### 8. Rename the text file by appending the current year (first name] last name] [current year]
```
$ mv notes/linda_he.txt notes/linda_he_2023.txt
$ ls notes
```

### 9. Make a copy of this folder, name it notes 2022
```
$ cp -r notes notes2023
$ ls
```

### 10. Delete the first folder (notes) using the verbose option
```
$ rm -rv notes
```

##  Exercise 3 : Create and run a script

### 1. Create a script script_1.sh in the folder linux_ex_1
```
$ touch script_1.sh
$ ls
```

### 2. In the script, write the commands that would output the following : Script running please wait...Done.
```
$ nano script_1.sh
#echo script ok
```

### 3. Quit editing and save the script
```
# crtl x/y/enter
```

### 4. Display the content of the script (using a command, not from editor)
```
cat script_1.sh
$ ./script_1.sh
```

### 5. Run the script
```
$ source script_1.sh
#ou
$ ./script_1.sh
```
## Exercise 4 :  Accessing or modifying a file : permissions and
root privilege
## 4.1  Change the rights for accessing or modifying a file
### 1. Create a file credentials in the folder linux_ex_1
```
cd linux_ex_1
touch credentials
```
### (a) Write any kind of (fake) personal information within the file
```
blabla...
```
### (b) Display the file content
```
cat credentials
```
### (c) Display the current permissions
```
ls -l credentials
```

### 2. Change the current permissions to : read only for all users
```
chmod u=r credentials
```
### (a) Display the new permissions
```
ls -l credentials
```
### (b) Modify and save the file
```
nano credentials
#Crtl+X+Y+ENT
```
### (c) Display the file content
```
cat credentials
```
### 3. Change the permissions back to read and write for all users
```
chmod ugo+rw credentials
```
### (a) Display the new permissions
```
ls -l credentials
```
### (b) Modify and save the file
```
nano credentials
#Crtl+X+Y+ENT
```
### (c) Display the file content
```
cat credentials
```
## On the same file :
### 1. Add the execute permission to the owner
```
chmod u+x credentials
```
### (a) Display the new permissions
```
ls -l credentials
```
### 2. Remove the read permission to other users
```
chmod o-r credentials
```
### (a) Display the new permissions
```
ls -l creddentials
```
### 3. Change the permissions to read, write and execute for all users
```
chmod u+rwx credentials
```
### (a) Display the new permissions
```
ls -l creddentials
```
## Exercise 4.2 Access root files
### 1. Go to the root folder
```
cd /
```
### 2. Create a file in root user mode named .private_file
```
sudo touch /.private_file
```
### (a) Write some information in the file
```
sudo vi /.private_file
```
--> on presse i, on écrit et":wq" 
### (b) Display the file content
```
sudo cat /.private_file
```
### (c) Display all the files in the folder including hidden files
```
sudo ls -a /
```
### 3. Modify the file in normal user mode
```
sudo chown linda /.private_file
sudo chmod u+rwx /.private_file
```
### (a) Write some new information in the file
```
#idem 
```
### (b) Display the file content
```
sudo cat /.private_file
```
### 4. Modify the file in root user mode
```
sudo vi /.private_file
```
### (a) Write some new information in the file
```
#idem
```
### (b) Display the file content
```
sudo cat /.private_file
```
### 5. Change permissions to read, write and execute for all users
```
sudo chmod a+rwx /.private_file
```
### (a) Modify the file content in normal user mode
```
#idem
```
### (b) Display the file content
```
sudo cat /.private_file
```
## Exercise 4.3 Change a file owner

### 1. Change permissions of .private_file to read and write for all users, in normal user mode
```
sudo chown linda .private_file
sudo chmod a+rw .private_file
```
### 2. Set the new file owner as the current user
```
sudo chown $USER .private_file
```
### 3. Change permissions of .private_file to read and write for all users, in normal user mode
```
chmod a+rw .private_file
```
## Exercise 4:.4 Manage Packages (tools / functions)
### 1. Update your main package manager named apt
```
apt update
```
### 2. Upgrade apt
```
apt upgrade
```
### 3. Install the package cmatrix
```
apt install cmatrix
```
### 4. Launch cmatrix
```
cmatrix
```
### 5. Quit cmatrix
Press "Ctrl+c"
### 6. Install the package tmux
```
apt install tmux
```
### 7. Launch tmux
```
tmux
```

















