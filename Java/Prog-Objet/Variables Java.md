### Types
- `String` - Stocke du texte. `"Texte enregistré"`
- `int` Stocke un nombre complet, négatif ou positif.
- `float` Stocke un nombre décimal.
- `char` Stocke un characters. `'a'`
- `boulean` Stocke un vrais/faux
### Modificateurs
#### Les variables publiques et privées
- `private` est seulement accessible a partir de la [[Class]]/[[objet]]
- `public` est accessible a partir de l'exterieur de la [[Class]]/[[objet]]

#### Variables statiques
- Les **variables de classe**
- Est utilisé pour les [[Variables Java]] qui ne dépendent pas de l'[[objet]]
- Elle est commune a tous les [[objet]]s de la [[class]]e et elle **peut changer**.
- Indiquée par le modificateur `static`
- Préférablement publique
- Ressemblent aux variables d'instance
	- Aussi connu comme [[Attributs]]
- Déclarée en **dehors des [[méthode]]s**
- **Visibles** partout dans la [[Class]]
- Héritées par les sous classes
- On utilise **JAMAIS** un [[accesseur]] pour l'obtenir
```java
static int nombreDeCampagnes = 3;
```

#### Les variables finales
- Une variable **QUI NE CHANGE PAS**.
- Elles sont **SOUVENT STATIQUE**
- Indiquée par le modificateur `final`
- Elles sont EN MAJUSCULES, AVEC __
```java
static final String JOSEPHER = "C'est l'action d'aller en date";
```

#### Les variables tableau
```java
String[] nomDesJoueurs;
nomDesJoueurs = new String[12];
```
- Il est possible d'en faire en multi-dimensions `String[][]`
	- Par multi je veut dire beaucoup `String[][][][][][][][][]`
##### Attention! La copie est complexe!
1. Copier le tableau avec =  copie LE LIEN VERS LA CASE.
	1. Il est possible d'utiliser cette fonction afin de créer un shortcut vers une ligne du tableau.
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
Le tableau représente notesEtPonctuation.

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
