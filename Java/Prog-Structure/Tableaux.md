# Copier un tableau
```java
String[] nomProd = {"Ananas","Brocoli","Carotte","Navet","Patate",
"Poire","Pomme","Raisin","Tomate"};
String[] nomCopie = new String[nomProd.length];
for (int i = 0; i < nomProd.length; ++i) {
	nomCopie[i] = nomProd[i]; // Copie de chaque élément
}
// nomCopie = nomProd.clone(); // Utilisation de la méthode clone()
nomCopie[3] = "Banane"; // N’affecte pas le tableau nomProd
for (int i = 0; i < nomProd.length; ++i) {
	System.out.println(nomProd[i] + " : " + nomCopie[i]);
}
```
# Recherche d'info
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

# Tableau non ordonné
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
# Tri par échange 
```java
int[] quant = {3, 5, 1, 2, 4, 5, 5, 2, 1};
int posMin;
int temp;
for (int i = 0; i < quant.length; ++i) { // Pour chaque case successive du tableau
	posMin = i; // On choisit la case actuelle (i) comme minimum initial
	for (int j = i+1; j < quant.length; ++j) { // Pour toutes les cases suivantes (i+1 à n)
		if (quant[j] < quant[posMin]) { // On recherche le minimum
			posMin = j;
		}
	}
	if (posMin != i) { // Si la case actuelle ne contient pas le minimum
		temp = quant[i]; // Alors on échange les valeurs des cases i et posMin
		quant[i] = quant[posMin];
		quant[posMin] = temp;
	}
}
// Affichage du tableau trié
for (int val : quant) {
	System.out.print(val + ", ");
}
```

### Tri par échange - multiples
```java
String[] nomProd ={"Patate", "Carotte", "Navet", "Brocoli", "Tomate", "Pomme", "Poire", "Raisin", "Ananas"};
int[] quant = {3, 5, 1, 2, 4, 5, 5, 2, 1}; 
int posMin; 
int tempInt; 
String tempStr; 
for (int i = 0; i < quant.length; ++i) { 
	posMin = i; 
	for (int j = i+1; j < quant.length; ++j) { 
		if (quant[j] < quant[posMin]) { 
			posMin = j; } // On trie selon la quantité 
		} 
		if (posMin != i) { // On doit échanger les éléments dans TOUS les tableaux manuellement 
			tempInt = quant[i]; 
			quant[i] = quant[posMin]; // Échange de la quantité 
			quant[posMin] = tempInt; 
			tempStr = nomProd[i]; 
			nomProd[i] = nomProd[posMin]; // Échange du nom 
			nomProd[posMin] = tempStr; 
		} 
	} 
	for (int i = 0; i < quant.length; ++i) { 
		System.out.print(nomProd[i] + "(" + quant[i] + "), "); 
	} 
```

# Tableau ordonné

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

# Fusion de tableaux
```java
String[] fruits = {"Ananas","Orange","Pomme","Raisin","Tomate"};
String[] legumes = {"Brocoli","Carotte","Navet","Patate"};
String[] nomProd = new String[fruits.length + legumes.length];
int posFruits = 0, posLegumes = 0, posProd = 0;
if (fruits.length + legumes.length <= nomProd.length) { // Assez de place?
// Tant qu’il reste des éléments dans les deux tableaux
	while (posFruits < fruits.length && posLegumes < legumes.length) {
	// On copie la plus petite valeur et on avance dans le tableau
		if (fruits[posFruits].compareTo(legumes[posLegumes]) < 0) {
		nomProd[posProd] = fruits[posFruits];
		posFruits++;
	} else {
		nomProd[posProd] = legumes[posLegumes];
		posLegumes++;
	}
	posProd++; // On avance toujours dans le tableau fusionné
}
// Complète la fusion en concaténant les éléments restants
while (posFruits < fruits.length) {
	nomProd[posProd++] = fruits[posFruits++];
}
while (posLegumes < legumes.length) {
	nomProd[posProd++] = legumes[posLegumes++];
}
while (posProd < nomProd.length) {
	nomProd[posProd++] = ""; // On efface les cases superflues
}
```
