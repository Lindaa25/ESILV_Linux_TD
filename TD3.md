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
cat cyberattacks.txt | grep -oP "meta\s\w+"  #-o : output ; -P : Perl regex syntax)
cat cyberattacks.txt | grep -oP "(?<=meta\s)\w+" #ce qui est après meta
cat cyberattacks.txt | grep -P 'A cyberattack is' #ne va pas marcher (voir ligne suivante)
cat cyberattacks.txt | grep -P 'A <a href="/wiki/Cyberattack" title="Cyberattack">cyberattack</a> is any type'
cat cyberattacks.txt | grep -A1 'mw-content-text' | grep -v 'mw-content-text' 
cat cyberattacks.txt | grep -P "(?<=<title>)"
cat cyberattacks.txt | grep -P "(?<=<title>).*(?=</title>)" #pour avoir ce qu'il a entre les balises title
cat cyberattacks.txt | grep -oP "(?<=<title>).*(?=</title>)" #avoir -o récupère uniquement le titre
```
<span class="c-instrument c-instrument--last" data-ist-last="">21.74</span>
