# TD2 Fundamental Linux functionalities
## Exercise 1: Access general computer informations
### 1. Put system up to date
```
sudo apt-get update
```
### 2. Put system up to date
```
cat /etc/os-release
ps -ef
top
scpu|grep cache
df -h
du -h
cat /proc/mounts
dmesg | grep usbhostname

```
## Exercise 2 : Shell - Variables and scripts scope 

### 1. Create a variable x and assign it the short text piri pimpin 
```
x="piri pimpim"
```
### 2. Display the value of this variable
```
echo $x
```
### 3. Add to this value the following text piri pimpon It should contain the following : piri pimpim piri pimpon 
```
x="$x piri pimpon"
```
### 4. Create a folder named my_programs, then enter into that folder 
```
mkdir my_programs
cd my_programs
```
### 5. Create a script named pilou that displays pilou pilou 
```
echo "pilou pilou"
```
### 6. Run this script 
```
./pilou
```
### 7. Make this script executable
```
chmod +x pilou
```
### 8. Run the script by writting its name only 
```
pilou
```
### 9. Programs called from the terminal are usually found thanks to a variable named PATH Display the content of the variable PATH 
```
echo $PATH
```
### 10. Add the path of your current location to the global variable PATH 
```
export PATH=$PATH:/path/to/current/location
```
### 11. When you are sure of the result, export it 
```
export PATH
```
### 12. Go to your home directory 
```
cd ~
```
### 13. Run your script by writting its name only 
```
pilou
```
### 14. Change the value of the PATH in the .profile file in order to make it permanent 
```
echo 'export PATH=$PATH:/path/to/current/location' >> ~/.profile
```
### 15. Create a new shell and run your script using its name only 
```
bash
pilou
```
## Exercice 3 : Scheduling task - daemon


