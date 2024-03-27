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

#### Les variables [[Tableaux]]
```java
String[] nomDesJoueurs;
nomDesJoueurs = new String[12];

//

String[] nomDesJoueurs = {"", "", ""}
```
