---
tags: 
Type: Note
Racine: Li
---
![[vi-vim-cheat-sheet.gif]]

### Mouvement

|Mouvement|Commande|
|---|---|
|Un caractère à gauche|`h`|
|Un caractère à droite|`l`|
|Une ligne en bas|`j`|
|Une ligne en haut|`k`|
|Un mot à droite|`w` (word)|
|Un mot à gauche|`b` (backward)|
|Début de la ligne|`0`|
|Fin de la ligne|`$`|
|Vers un numéro de ligne|`:numéro` `:100` à la 100ème ligne, `:$` fin du fichier|

Ainsi, si je veux me déplacer de 3 mots vers la droite:
- `3w`
Descendre de 50 lignes:
- `50j`
Reculer de 3 caractères:
- `3h`

### Copier/coller

La commande pour copier est `y` (yank en Anglais).

Il faut ensuite spécifier ce que l’on souhaite copier.

|À copier|Commande|
|---|---|
|Une ligne|`yy`|
|De la position du curseur jusqu’à la fin du mot courant|`yw`|
|Un caractère en dessous du curseur|`yl`|
|Trois lignes|`y3y` ou `3yy`|
|Trois mots|`y3w`|
|Trois caractères à partir du curseur vers la droite|`y3l`|

Pour coller en mode normal, on utilise `p` ou `P` (paste).

`p` permet de coller après le curseur s’il s’agit de caractères ou de mots ou en dessous de la ligne s’il s’agit de ligne(s) à coller.

`P` permet de coller avant le curseur s’il s’agit de caractères ou de mot ou au dessus de la ligne s’il s’agit de lignes.

Il est aussi possible de coller plusieurs fois ce qui a été copié en utilisant un quantificateur:

`3p` colle 3 fois ce qui a été copié après ou en-dessous du curseur.

`5P` coller 5 fois ce qui a été copié avant ou au-dessus du curseur.

### Modification, répétitions, recherche

Pour remplacer un caractère, on se positionne sur ce caractère puis on tape la commande `r` suivi du nouveau caractère.

Pour remplacer plusieurs caractères, on se positionne sur le premier caractère à modifier puis on utilise la commande `R`. Tous les caractères ensuite tapés remplaceront ce qui est présent dans le texte jusqu’à la touche `ESC`.

Pour répéter une action, se positionner à l’endroit où on veut avoir la répétition puis utiliser la commande `.` (point).

Pour annuler des actions, utiliser la commande `u` (undo).

La recherche se fait à l’aide `/`. Pour l’élément suivant `n`, pour l’élément précédent `N`.

### Suppression (couper)

Pour supprimer un caractère en dessous du curseur: `x`.

Pour supprimer un caractère à gauche du curseur: `X`.

Les autres commandes de suppression commencent par `d` (delete).

|Suppression|Commande|
|---|---|
|Une ligne|`dd`|
|De la position du curseur jusqu’à la fin du mot courant|`dw`|
|Jusqu’à la fin de la ligne|`d$`|
|Jusqu’au début de la ligne|`d0`|
|Trois lignes|`3dd`|
|Quatre mots|`4dw`|

### Entrer en mode insertion

|Où|Commande|
|---|---|
|À l’emplacement du curseur|`i`|
|Après le curseur|`a`|
|Au début de la ligne|`I`|
|À la fin de la ligne|`A`|
|Insérer une ligne en-dessous|`o`|
|Insérer une ligne au-dessus|`O`|
|Modification de texte|`cw`, `ci"`, `c$`,…(Voir ci-dessous)|

### Modification en basculant du mode normal vers le mode insertion

Si on est en mode normal et qu’on veut modifier du texte tout basculant en mode insertion, on utilisera la commande `c` (change).

Changer de la position du curseur jusqu’à la fin du mot courant: `cw`

Changer jusqu’à la fin de la ligne: `c$`

Changer jusqu’au début de la ligne: `c0`

Changer jusqu’au prochain ‘u’: `ctu` (change to ‘u’)

Si vous êtes dans un mot (pas au début) ou entre deux guillemets ou entre deux parenthèses, il est possible de changer le mot, tout ce qui se trouve entre les " ou les ( à l’aide la commande `ci` (change in), en l’utilisant comme ci-dessous:

Dans le mot: `ciw`

Entre les “: `ci”`

Entre les (: `ci(`