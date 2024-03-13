```bash
#!/bin/bash
firefox &
memoire="0"
ps -eo %mem,args | 
	grep -i firefox | 
	cut -f2 -d" " | 
	while read i; do 
		echo > $memoire+="+$i"
	quit 
echo $memoire
echo bc $memoire
```
