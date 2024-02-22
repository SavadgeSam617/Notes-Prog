
## Ajout
```java
Scanner clavier = new Scanner(System.in);
String[] nomProd = {"Navet","Brocoli","Patate","Céleri","Carotte","",""};
int[] quant = {1,2,3,4,5,-1,-1}; // -1 ou "" indique une case vide dans ce cas
int nbItems = 5; // Nombre de cases utilisées
String nomItem;
int qteItem;
System.out.print("Indiquez l'item à ajouter : ");
nomItem = clavier.next();
System.out.print("Indiquez la quantité : ");
qteItem = clavier.nextInt();
if (nbItems < nomProd.length) { // S’il reste de la place
	nomProd[nbItems] = nomItem; // Ajouter l’item dans la
	quant[nbItems] = qteItem; // première case vide
	nbItems++;
}
for (int i = 0; i < nomProd.length; ++i) {
	System.out.println(nomProd[i] + " : " + quant[i]);
}
```
## Retrait
```java
Scanner clavier = new Scanner(System.in);
String[] nomProd = {"Navet","Brocoli","Patate","Céleri","Carotte","",""};
int[] quant = {1,2,3,4,5,-1,-1}; // -1 ou "" indique une case vide dans ce cas
int nbItems = 5; // Nombre de cases utilisées
String nomItem;
int posItem;
System.out.print("Indiquez l'item à retirer : ");
nomItem = clavier.next();
posItem = trouve(nomItem, nomProd); // Voir p19
if (posItem != -1) { // Si l’item existe dans le tableau
	nbItems--; // Libérer la dernière case du tableau
	nomProd[posItem] = nomProd[nbItems]; // en copiant le
	nomProd[nbItems] = ""; // dernier item à la place de
	quant[posItem] = quant[nbItems]; // l’item à enlever
	quant[nbItems] = -1; // et mettre -1 ou "" à la place
}
for (int i = 0; i < nomProd.length; ++i) {
	System.out.println(nomProd[i] + " : " + quant[i]);
}
```