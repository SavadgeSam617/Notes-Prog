
## Début & fin
`^` début de la chaine
`$` fin de chaine
`\b` début ou fin de MOTS
`\B` Tout sauf début ou fin de mots
## Equivalences
`[]` correspond à un char dans le string  
`[aA]` Correspond au a min et Maj
`[a-z]` une lettre min
`[0-9]`, `\p{javaDigit}`  ou `\d` un chiffre!
`[^0-9]` ou `D` pas un chiffre
`$` finit par
`\$` contient le symbole $
`.` n'importe quoi SAUF `\n`
`\w` ou `[a-zA-Z_0-9]`
`\W` ou `[^a-zA-Z_0-9]`
`\p{javaLowerCase}` ou `[a-zàâäèéêëîïôùûüÿçœ]` Lettre minuscule incluant accent
`\p{javaUpperCase}` ou `[A-ZÀÂÄÈÉÊËÎÏÔÙÛÜŸÇŒ]` Lettre majuscule incluant accent
`\p{javaLetter}` ou `[a-zàâäèéêëîïôùûüÿçœ A-ZÀÂÄÈÉÊËÎÏÔÙÛÜŸÇŒ]` Minuscule ou majuscule incluant accent
`\p{Alpha}` ou `[a-zA-Z]` Minuscule ou majuscule sans accent
`\p{javaLetterOrDigit}` une lettre ou chiffre, incluant accent
`\p{javaWhitespace}` ou `[ \t\n\r\f]` Espace blanche, incluant le retour de chariot 8 F


## Quantificateurs
`{n}` exactement n occurences
`{n,}` au moin n occurences
`{n, m}` au moin n mais sous m
`?` Élément optionnel (`tes?\b` fini par te ou tes) 
`*` ou `{0,}`0 occurences ou plus
`+` ou `{1,}` au moin un occurance

## OU logique
`|`
