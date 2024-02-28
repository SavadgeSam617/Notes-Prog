```java
String[] nomProd = {"Patate", "Carotte", "Navet", "Brocoli",
"Tomate", "Pomme", "Poire", "Raisin", "Ananas"};
int indexe;
String recherche;
for (int i = 0; nomProd.length > i; i++) {
	if (nomProd[i] == recherche)
	{indexe = i;
	i = nomprod.length;}
}
return indexe;
```

```java
public static int calculerNbNotes(String[] notes) {
	int indexe = -1;
	int i = 0;
	while (notes.length > i) {
		if (extraireTemps(notes[i]) == -1) {
			indexe = i;
			i = notes.length;
		}else{
			i++;
		}
	}
		return indexe;
}
```
