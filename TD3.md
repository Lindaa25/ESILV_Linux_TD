# TD3 : Work with text manipulation tools in Linux
## Exercise 1 : Grep and awk on tabular data
```
cd /
ls -l
ls -l | grep bin
ls -l | grep bin | awk '{print $5}'
ls -ld bin | awk '{print $6, $7, $8}'
ls -ld bin | awk '{printf("%s-%s-%02d\n", $8, substr($6, 1, 3), $7)}'
```

## Exercise 2 : Grep with Regex, and sed on unstructured data
```
curl https ://en.wikipedia.org/wiki/List_of_cyberattacks > cyberattacks.txt 
cat cyberattacks.txt | grep meta
cat cyberattacks.txt | grep -oP "meta\s\w+"
cat cyberattacks.txt | grep -oP "(?<=meta\s)\w+"
cat cyberattacks.txt | grep -A1 'mw-content-text' | grep -v 'mw-content-text' 
cat cyberattacks.txt | grep -P "(?<=<title>)"
```
