Un tableau d'objet contient **un lien vers un objet**, sans avoir a lui attribuer un nom.
#### Pour le déclarer
```java
NomClasse[] nomTableau; //Cette syntaxe est meilleure
// OU
NomClasse nomTableau[];
```
Lors de la déclaration, il n'y a pas de [[Tableaux|Tableau]] créé, `nomTableau` est une **référence**. Elle contient **null**.

#### Pour instentier un tableau
**Aussi appelé créer un tableau**
```java
nomTableau = new NomClasse[dimension];
```

#### Déclaration et instanciation en un
```java
NomClasse[] nomTableau = new NomClasse[dimension];
```


##### Exemple
```java
//Déclarer un tableau de Rectangle de taille 3
        Rectangle[] tabRectangles;
        tabRectangles = new Rectangle[3];
        tabRectangles[0] = new Rectangle(3,5);
        tabRectangles[1] = new Rectangle(4,10);
        tabRectangles[2] = new Rectangle(5,7);
        //tout au dessus en une ligne
        Rectangle[] tabRectangles1 = {new Rectangle(2,4), new Rectangle(10,100),
                                      new Rectangle(1, 2)};
        //Appeler une méthode
        tabRectangles[1].Afficher();
        tabRectangles1[0].Afficher();
```