Explications sur comment lancer les tests de performances.

Dans tous les cas, il faut extraire les tests de perfs.zip dans
le répertoire tests/ sans créer de sous-répertoire
(les fichiers seront donc du type tests/perfs/testXXXXX.test)

Il faudra désactiver les affichages (print / printf). 

****************************************************************
*  Langage C                                                   *
****************************************************************

La méthode recommandée est de les effectuer sur le serveur Turing.


Désactiver les affichages (printfs) ainsi:
  => mettre tous les affichages dans des blocs conditionnels du type:

  if (! silent_mode) {
     /* code d'affichage */
  }

  => recompiler avec les options de performance
     (modifiez les CFLAGS comme indiqué dans le Makefile
      puis lancez 'make -B')

Vous pouvez lancer individuellement un test de performance ainsi:
> ./main -silent tests/perfs/<nom de test de performance>.test


Ou lancer une batterie de tests de performance (avec génération de courbes):
> ./tests/performance/perf.py c



*************
* Sous MacOS

Sur un ordinateur personnel, il faut installer la librairie python 
'matplotlib'.  (avec 'python -m pip install -U matplotlib')
Les scripts fournis sont prévus pour être sur un unix (non testé sous windows)


Sous MacOS un étudiant a réussi à utiliser le script fourni mais quelques modifications sont nécessaires. Les voici rapportées par cet étudiant :


1. Il n’y a pas le flag format dans l’exécution de « time » de macOS, il faut donc installer gnu-time avec:
brew install gnu-time

2. Aussi, la commande « timeout » n’existe pas de base dans macOS, il faut donc installer avec:
brew install coreutils

3. remplacer dans perf.py « time » par « gtime » (apparait sur la ligne "which -a time")


***********************
* Avoir les graphiques

Pour avoir la génération des graphiques, il faut installer matplotlib qui a plusieurs dépendances (normalement installé sur les machines du DLST).
Sinon, il est possible de désactiver la génération en mettant à False la variable suivante dans run.py:
GRAPHIQUES=False


Il faut tout d'abord visual build c++ 14.0+
=>  installer visual studio build tools, avec outils de développement c++ (case à cocher)

Puis installer les packages python nécessaires :
ouvrir une invite de commande windows puis taper (ou copier-coller) les commandes suivantes

python -m pip install -U pip
(python -m pip install -U wheel)    <- peut être pas nécessaire
python -m pip install -U matplotlib


