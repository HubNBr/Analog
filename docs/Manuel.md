# Manuel d'utilisation du logiciel

Avec **Analog** vous pouvez :

- Faire des **statistiques** sur des logs HTTP
- Créer des **graphiques** représentants les trafics entre vos pages web
- Ajuster l'analyse avec des options telles que l'analyse sur une **période de temps** précise

## Prise en main

La commande de base d'utilisation du logiciel est :

```$./analog [options] nomfichier.log```

Elle vous permet d'afficher la liste des **10 documents** les plus consultés par ordre décroissant de popularité.

## Les options d'Analog

### -g (graphique)

L'option suivante :

```-g [nomFichier.dot]```

Permet de créer un fichier au format **GraphViz** à partir des logs analysés.

### -e (exclure)

L'option suivante :

```-e```

Permet d'exclure les documents ayant une extension de type **image**, **css** ou **javascript**, lors de l'analyse du fichier de logs par **Analog**.

### -t (temps)

L'option suivante :

```-t [heure]```

Permet de ne prendre en compte que les hits présents dans l'intervalle horaire **[heure,heure+1[**.

L'heure doit être un nombre entre **0** et **23**.

### -help (aide)

L'option suivante :

```-help```

Est l'option qui donne accès à ce manuel.

**Remarque importante :** l'aide du logiciel **Analog** supporte la redirection (le logiciel renvoie alors une aide textuelle). Ainsi, vous pouvez rediriger sa sortie normalement en faisant par exemple :

```./analog -help | grep [motclé]```

Si vous cherchez une information sur une option particulière depuis le terminal.

[Retour vers la page principale](./README.md)