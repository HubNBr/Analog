# Utilitaire d'analyse de logs HTTP

Avec Analog vous pouvez :

- Faire des statistiques sur des logs HTTP
- Créer des graphiques représentants les trafics entre vos pages web
- Ajuster l'analyse avec des options telles que l'analyse sur une période de temps précise

## Prise en main

La commande de base d'utilisation du logiciel est :

'$./analog [options] nomfichier.log'

Elle vous permettre d'afficher la liste des 10 documents les plus consultés par ordre décroissant de popularité.

## Les options d'Analog

### -g (graphique)

L'option suivante :

'-g nomfichier.dot'

Permet de créer un fichier au format GraphViz du graphe analysé.

### -e (exclure)

L'option suivante :

'-e'

Permet d'exclure les documents ayant une extension de type image, css ou javascript, lors de l'analyse du log par Analog.

### -t (temps)

L'option suivante :

'-t heure'

Permet de ne prendre en compte que les hits présents dans l'intervalle horaire [heure,heure+1[.