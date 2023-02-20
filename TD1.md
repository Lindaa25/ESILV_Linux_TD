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
$ chmod 777 script_1.sh
$ ./script_1.sh
```








