```java
Scanner clavier = new Scanner(System.in); String[] nomProd = {"Avocat","Bleuet","Brocoli","Carotte","Chou","Fraise","Melon", "Navet","Orange","Patate","Pomme","Raisin","Salade","Tomate",""}; 
int[] quant = {1, 4, 2, 5, 1, 3, 1, 1, 5, 4, 7, 2, 1, 6, -1}; 
int nbElem = 14; 
String prodCherche; System.out.print("Entrez le nom d'un produit : "); 
prodCherche = clavier.next(); 
int posGa = 0; 
int posDr = nbElem - 1; 
int posMi = (posGa + posDr) / 2; 
// Division entière pour trouver le milieu 
System.out.println(posGa + " : " + posMi + " : " + posDr); 
// Affichage des bornes 
// On s’arrête lorsque les bornes se croisent ou lorsqu’on a trouvé le produit au milieu 

while (posGa <= posDr && !prodCherche.equals(nomProd[posMi])) { 
	if (prodCherche.compareTo(nomProd[posMi]) < 0) { posDr = posMi - 1; 
		// Si on est à gauche du milieu, on déplace la borne de droite 
	} else { 
		posGa = posMi + 1;
		// Si on est à droite du milieu, on déplace la borne de gauche 
	} 
	posMi = (posGa + posDr) / 2; 
	// Mise à jour du milieu 
	System.out.println(posGa + " : " + posMi + " : " + posDr); 
} 

if (posGa <= posDr) { 
	// Si les bornes ne se croisent pas, on a trouvé 
	System.out.println("Produit trouvé: " + nomProd[posMi] + " (" + quant[posMi] + ")"); 
} else { 
	System.out.println("Aucun produit trouvé"); 
}
```
