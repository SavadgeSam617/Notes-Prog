### Tri par échange 
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
