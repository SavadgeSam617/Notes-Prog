

```java
public static float moyenne(int nb1, int nb2, int nb3) {
        // Option 1 : Calcul moyenne
        float dMoyenne=-1;
        dMoyenne = (nb1 + nb2 + nb3);
        dMoyenne = dMoyenne/3;
        return dMoyenne;
    }
```

```java
    public static int notePonderee(int pondEx, int noteEx, int pondTp, int noteTp) {
        // Option 2 : Calcul note pondérée
        int iNotePond = -1;
        if(!(pondEx > 101 || pondEx < 0 || pondTp > 101 || pondTp < 0 || noteEx > 101 || noteEx < 0 || noteTp > 101 || noteTp < 0 || pondEx+pondTp != 100)){
            iNotePond = ((noteEx * pondEx) + (noteTp * pondTp))/100;
            //iNotePond = iNotePond/100;
        }
        return iNotePond;
    }
```

```java
public static char conversionNote(float notePct) {

        char cReponce = '\0';
            if (notePct < 101 && notePct >= 90) {
                cReponce = 'A';
            }else if (notePct < 90 && notePct >= 75) {
                cReponce = 'B';
            }else if (notePct < 75 && notePct >= 60) {
                cReponce = 'C';
            }else if (notePct < 60 && notePct >= 50) {
                cReponce = 'D';
            }else if (notePct < 50 && notePct >= 0) {
                cReponce = 'F';
            }else {
                cReponce = 'X';
            }

        return cReponce;

    }
```

```java
    public static String ordre(int nb1, int nb2, int nb3) {
        // Option 4 : Détermine ordre
        String sReponce = "N/A";
        if (nb1 < nb2 && nb2 < nb3) {
            sReponce = "décroissant";
        }else if (nb1 > nb2 && nb2 > nb3) {
            sReponce = "croissant";
        }else if (nb1 == nb2 && nb2 == nb3) {
            sReponce = "constant";
        }else{
            sReponce = "quelconque";
        }
  
        return sReponce;
    }
```

