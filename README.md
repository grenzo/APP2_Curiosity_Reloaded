Recommandations sur l'utilisation des fichiers pour l'APP2.
A lire absolument !

Renseignez ici les noms des membres de votre binôme :

Nom1 - prénom1 : ....
Nom2 - prénom2 : ....

Si vous avez des commentaires, remarques etc. pour le rendu, vous pouvez les 
mettre ici:

...
...
...


Compilation
-----------
Pour compiler :
> make

ou

> clang -Wall -Wextra main.c -o main curiosity.c interprete.c listes.c
(Nous vous conseillons d'utiliser le compilateur clang plutôt que gcc.)


Lancer un test
--------------

Test complet
> ./main tests/<nom de test>.test

Test en mode "pas à pas" :
> ./main -d tests/<nom de test>.test


Lancer une suite de tests
-------------------------

Tests fonctionnels :
> ./tests/check.py c

Tests en vérifiant les erreurs ou fuites mémoire:
> ./tests/check.py --mem c

Pour les tests de performance : lire le fichier README-perfs.md
