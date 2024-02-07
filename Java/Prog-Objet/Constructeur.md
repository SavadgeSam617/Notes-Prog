Le constructeur définissent les [[Attributs]] de l'[[objet]] lors de la **déclaration** d'un [[objet]].

### Un Exemple
    //Constructeur titre & auteur
    public Livre(String t, String a) {
        titre = t;
        auteur = a;
    }
*pour appeler un constructeur a partir d'un autre constructeur, DANS LA PREMIÈRE LIGNE, faire*
`this(<1erVar>, <2eVar>);`

### Gabarit
//Constructeur ...
public <Class>(<type> <1erVar>, <type> <2eVar>) {
	<Var1> = <1erVar>;
	<Var2> = <2eVar>;
}