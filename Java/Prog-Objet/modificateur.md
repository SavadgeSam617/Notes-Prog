Le modificateur est un **composant** important de la [[class]] qui permet de modifier les [[Attributs]] de l'[[objet]].

## Exemple de modificateur
    // Modificateur de titre
    public void setTitre(String titre) {
        this.titre = titre;
    }

### Gabarit
//Modificateur de <variable>
public void set<NomDeLaVariable>() {
	this.<nomDeLaVariable> = <nomDeLaVariable>;
}