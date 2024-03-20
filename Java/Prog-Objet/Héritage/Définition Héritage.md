---
Type: Note
tags: 
Racine:
---
- Permet de **dériver une nouvelle [[class]]e à partir d'une autre [[class]]e existante** pour récupérer les champs et les méthodes et en rajouter de nouvelles fonctionnalités. Ceci au lieu de réécrire une [[class|classe]] à zéro.
- En gros, on crée une [[class]]e gabarit et on la modifie pour chaque spécialisation.



### VOCABULAIRE
- la classe **B** qui hérite de la classe **A**  s'appelle : 
	- #Classe_Enfant ou #sous-classe .
- La classe **B** =="dérive de" / "étend(extends)"== la classe **A**
- La classe **A** s'appelle :
	- #classe_mère #classe_parent ou #super-classe \>
- La #Classe_Enfant  peut
	- **Redéfinir** des méthodes de la #classe_parent (même signature) (nécéssite `@Override`)
	- **Surcharger** des méthodes de la même classe (même nom mais pas la même signature)

### Kessé qui change
- Le code source de **B** ne comporte que ce **qui a changé** par rapport au code de **A**
- **On a pas besoin de recopier tout le code qui est dans A pour le mettre dans B**
- On peut par exemple faire les modifications suivantes :
	- Ajouter de nouvelles méthodes dans **B** ( #spécialisation )
	- Ajouter de nouveaux champs dans **B** ( #spécialisation )
	- Modifier certaines méthodes de **A** qui se retrouve ainsi dans **B** mais avec d'autres fonctionnalités

### Syntaxe
```java
private class Rectangle extens Forme {}
```

Aller chercher un [[Constructeur]] dans la #classe_parent 
```java
super(); // a la première ligne du nouveau constructeur
```
