
- [x] Class Tp01 @votrenom.tp01
	- [x] Aller chercher le code pré-fait
	- [x] Faire & implémenter les fonctions 
		- [x] `joursDansMois()`
			- [x] Retourne le nombre de jours dans le mois spécifié.
				- [x] Demande aussi l'année afin de comprendre les années bissextile
					- [x] **SI** l'année est divisible par 4, mais non par 100 **OU**
					- [x] **SI** l'année est divisible par 400
			- [x] Documentation
			- [x] Commit `Méthode jours dans mois`
		- [x] `reculerDate()`
			- [x] Retourne un string formaté `String.format()`
				- [x] EX : `24 MAR 2018`
				- [x] Vous pouvez écrire directement `return String.format(...);`, car la valeur de retour de `String.format()` est de type String.
				      Indice : inspirez-vous de la fonction `avancerDate()`
			- [x] Documentation
			- [x] Commit `Reculer la date`
		- [x] `jourHier()`
			- [x] Retourne le jour de la date précédente dans le calendrier. 
			      Indice : utilisez les fonctions `joursDansMois()` et `moisHier()`
			- [x] Documentation
			- [x] Commit `Hier on était...`
		- [x] `moisHier()`
			- [x] Retourne le mois (en int) de la journée précédente
			- [x] Documentation
			- [x] Commit `Le mois d'hier-hivert`
		- [x] `anneHier()`
			- [x] Retourne l'année d'hier.
			- [x] Documentation
			- [x] Commit `On était en quelle année hier?`
	- [x] Faire la documentation de code
- [x] Class Tp01Test @votrenom.tp01
	- [x] 5 tests pour toutes le méthodes
		- [x] `joursDansMois()`
		- [x] `reculerDate()`
		- [x] `jourHier()`
		- [x] `moisHier()`
		- [x] `anneHier()`
- [x] Respecter les normes
- [x] Trace et remises
	- [x] Multiples commit
	- [x] Push
	- [x] Déposer dans Moodle


#### Désiré
```
Entrez une date (JJ MMM AAAA) : 3 MAR 2018
2 Entrez le décalage : 21
3 Date calculée : 24 MAR 2018
```

```
Entrez une date (JJ MMM AAAA) : 30 JUN 2015
2 Entrez le décalage : -21
3 Date calculée : 09 JUN 2015
```

```
Entrez une date (JJ MMM AAAA) : 20 JAN 2020
2 Entrez le décalage : 15
3 Date calculée : 04 FEV 2020
```

```
Entrez une date (JJ MMM AAAA) : 15 OCT 2019
2 Entrez le décalage : -15
3 Date calculée : 30 SEP 2019
```





#### Documentation de code
```java
/**
* Convertit le numéro du mois en la chaîne correspondante
* @param mois Mois qui doit être convertit
* @return Chaine de 3 charactere maj correspondant au nom du mois
**/
```