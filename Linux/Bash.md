Créer un fichier `.sh` avec `vim` la première ligne est très importante.
```bash
#!/bin/bash
echo "Hello world!"
# affiche le repertoire courrant
pwd
# créer les fichier désiré de 1 à 5
touch file{1..5}
(sleep 15; echo "la pause de X")
wait
echo "OK!"
```
