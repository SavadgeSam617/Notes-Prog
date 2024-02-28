[[Bash]]
1. Fait la même chose que ci-haut, mais utilise & pour le faire en arrière plan
2. Les commandes find doivent s’exécuter en même temps
3. Utiliser (CMD1;CMD2;…)& pour lancer plusieurs processus séquentiels en arrière plan
4. À la fin du script, s’assurer de faire wait sur les processus
```bash
#!/bin/bash
types="java conf txt png tiff"
for i in $types; do
	echo $(find / -name "*.$i" 2>/dev/null | wc -l)&; 
done
```
