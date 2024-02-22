
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