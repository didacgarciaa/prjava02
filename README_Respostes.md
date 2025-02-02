1. Clonació del dipòsit
git clone https://github.com/dacomo2021daw2/prjava02.git
cd prjava02
git status

5. Canvi a la branca main i comprovació de l'historial
git checkout main
git status
git log --oneline --graph --decorate

7. Comprovació de l'última línia afegida a Prjava02.java des de branca00
git checkout branca00
git status
geany Prjava02.java

10b. Fusió de la branca branca00 amb la branca main
git checkout main
git merge branca00

12. Pujar els canvis al dipòsit remot
git push origin main

14a. Pujar la branca branca01 al dipòsit remot
git checkout branca01
git push origin branca01


Respostes

6. Pots veure l'última línia afegida? Per què?
No, perquè la línia es va afegir a branca00, i actualment ens trobem a main, on aquest canvi encara no ha estat fusionat.

7. Pots veure l'última línia afegida? Per què?
Sí, perquè hem canviat a branca00, que és on es va afegir la línia en el commit anterior.

12c. Per què només s'ha actualitzat la branca main?
Perquè el git push origin main només puja els canvis de la branca main al dipòsit remot. Per pujar altres branques, s'han de fer git push específics per a cadascuna.

14c. A quants commits de distància (commit ahead) està de la branca main?
Per comprovar-ho:
git checkout branca01
git log --oneline main..branca01

El resultat mostra quants commits té branca01 que no estan en main. Això indica la distància en commits entre les dues branques.

