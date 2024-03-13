```bash
#!/bin/bash
firefox &
ps -eo %mem,args | grep -i firefox | cut -f2 -d" " | while read i; do 
```
