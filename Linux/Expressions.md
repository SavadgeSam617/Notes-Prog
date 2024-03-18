---
Type: Note
tags: 
Racine: Li
---

| Expression | Description                               | Exemple                       | Contre-exemple                                  |
| ---------- | ----------------------------------------- | ----------------------------- | ----------------------------------------------- |
| ab         | Le ET est implicite entre les caractères. | “ab”                          | “a”, “b”, chaine vide                           |
| .          | Un seul caractère                         | “a”, “b”, …                   | “ab”, chaine vide                               |
| ^          | Début de la ligne.                        | ^a: un “a” en début de ligne. | Toutes les lignes ne commençant pas par un “a”. |
| $          | Fin de ligne.                             | a$: un “a” en fin de ligne.   | Toutes les lignes ne finissant pas par un “a”.  |

`egrep 'fich' fichier`
fich1.txt
fich2.txt
fich3.txt

`egrep 'fich[^123]' fichier`
fich4.txt
fich5.txt
fichfind
fichier

Le `[]` correspond a un char, c'est une énumération.
Un suite de nombre est 
```bash
[a-z]
[A-Z]
[0-9]
```

### Quantificateurs

|Quantificateur|Signification|
|---|---|
|?|0 ou 1 fois.|
|+|1 ou plusieurs fois|
|*|0 ou plusieurs fois|
|{2}|2 fois|
|{2,4}|Entre 2 et 4 fois|
|{2,}|Plus de 2 fois|


`egrep '4540 [0-9]{4} [0-9]{4} [0-8]{4}$' carte`
`egrep '^[a-z_][a-z_0-9]$' variable`
