## Ajout
```java
Scanner clavier = new Scanner(System.in);
String[] nomProd = {"Brocoli","Carotte","Céleri","Navet","Patate","",""};
int[] quant = {2,5,4,1,3,-1,-1};
int nbItems = 5;
String nomItem;
int qteItem;
System.out.print("Indiquez l'item à ajouter : ");
nomItem = clavier.next();
System.out.print("Indiquez la quatité : ");
qteItem = clavier.nextInt();
if (nbItems < nomProd.length) {
	int curPos = nbItems; // On débute à la première case vide
	// Tant que item à ajouter < item de la case précédente
	while (curPos > 0 && nomItem.compareTo(nomProd[curPos-1]) < 0) {
		nomProd[curPos] = nomProd[curPos-1]; // On le décale
		quant[curPos] = quant[curPos-1]; // vers la droite
		curPos--; // On se déplace d’une case à gauche
	}
	nomProd[curPos] = nomItem;
	quant[curPos] = qteItem; // Ajout de l’item dans la case libre
	nbItems++;
}
for (int i = 0; i < nomProd.length; ++i) {
	System.out.println(nomProd[i] + " : " + quant[i]);
}
```
## Retrait
```java
Scanner clavier = new Scanner(System.in);
String[] nomProd = {"Brocoli","Carotte","Céleri","Navet","Patate","",""};
int[] quant = {2,5,4,1,3,-1,-1};
int nbItems = 5;
String nomItem;
int posItem;
System.out.print("Indiquez l'item à retirer : ");
nomItem = clavier.next();
posItem = trouve(nomItem, nomProd); // Voir p19
if (posItem != -1) {
	nbItems--; // Pointe sur la case du dernier item
	// À partir de l’item à effacer jusqu’au dernier item
	for (int curPos = posItem; curPos < nbItems; curPos++) {
		nomProd[curPos] = nomProd[curPos+1]; // On décale le
		quant[curPos] = quant[curPos+1]; // suivant à gauche
	}
	nomProd[nbItems] = ""; // On libère la case du dernier item
	quant[nbItems] = -1;
}
for (int i = 0; i < nomProd.length; ++i) {
	System.out.println(nomProd[i] + " : " + quant[i]);
}
```
