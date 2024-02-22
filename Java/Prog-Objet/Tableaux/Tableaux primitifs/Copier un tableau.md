# Copie Avancée
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

# Copie du Lien
1. Copier le [[Tableaux]] avec =  copie LE LIEN VERS LA CASE.
	1. Il est possible d'utiliser cette fonction afin de créer un shortcut vers une ligne du [[Tableaux]].
```java
public static void main(String[] args) {
int[][] notesEtPonctuation = {{78,2},{12,2},{73,2},{52,2},{48,2},{73,10},{75,10},{18,20},{86,20},{62,30}};
//La premiere colone est la note, la deuxieme la ponctuation
int[] exercice1, exercice2, exercice3, exercice4, exercice5, miniTest1, miniTest2, examen1, examen2, examenFinal;
exercice1 = notesEtPonctuation[0];
exercice2 = notesEtPonctuation[1];
exercice3 = notesEtPonctuation[2];
exercice4 = notesEtPonctuation[3];
exercice5 = notesEtPonctuation[4];
miniTest1 = notesEtPonctuation[5];
miniTest2 = notesEtPonctuation[6];
examen1 = notesEtPonctuation[7];
examen2 = notesEtPonctuation[8];
examenFinal = notesEtPonctuation[9];
}
```
Le [[Tableaux]] représente notesEtPonctuation.

| Note | Ponctuation |
| ---- | ---- |
| 78 | 2 |
| 12 | 2 |
| 73 | 2 |
| 52 | 2 |
| 48 | 2 |
| 73 | 10 |
| 75 | 10 |
| 18 | 20 |
| 86 | 20 |
| 62 | 30 |
