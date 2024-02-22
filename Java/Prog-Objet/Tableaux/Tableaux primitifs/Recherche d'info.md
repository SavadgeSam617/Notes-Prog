## Selon critaire
```java
Scanner clavier = new Scanner(System.in);
String[] nomProd = {"Patate", "Carotte", "Navet", "Brocoli",
"Tomate", "Pomme", "Poire", "Raisin", "Ananas"};
int[] quant = {3, 5, 1, 2, 4, 5, 5, 2, 1};
int nbTrouve = 0;
int valeurCherchee;
System.out.print("Quelle est la quantité recherchée? ");
valeurCherchee = clavier.nextInt();
for (int i = 0; i < quant.length; ++i) {
	if (quant[i] >= valeurCherchee) {
		System.out.println("Produit : " + nomProd[i] + "(" + quant[i] + ")");
		nbTrouve++;
	}
}
if (nbTrouve > 0) {
	System.out.println(nbTrouve + " produit(s) trouvé(s)");
} else {
	System.out.println("Aucun produit trouvé");
}
```
## Min Max
```java
String[] nomProd = {"Patate", "Carotte", "Navet", "Brocoli",
"Tomate", "Pomme", "Poire", "Raisin", "Ananas"};
int[] quant = {3, 5, 1, 2, 4, 5, 5, 2, 1};
int posMin = 0; // Au départ, la 1ière valeur est le min
int posMax = 0; // Au départ, la 1ière valeur est le max
for (int i = 1; i < quant.length; ++i) { // On commence par la 2e valeur (i=1)
	if (quant[i] < quant[posMin]) { // Si on trouve une valeur plus petite
		posMin = i; // Mise à jour de la position du min
	}
	if (quant[i] > quant[posMax]) { // Si on trouve une valeur plus grande
		posMax = i; // Mise à jour de la position du max
	}
}
System.out.println("La quantité minimale achetée est de " + quant[posMin]);
System.out.println("et elle a été observée pour le produit : " + nomProd[posMin]);
System.out.println("La quantité maximale achetée est de " + quant[posMax]);
System.out.println("et elle a été observée pour le produit : " + nomProd[posMax]);
```