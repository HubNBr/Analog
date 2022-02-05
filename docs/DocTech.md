# Documentation technique

## Choix des structures de données pour la sauvegarde des logs

Les structures de données choisies pour la sauvegarde des logs en mémoire sont les suivantes :

	*Une *unordered_map<string, unsigned int>*, renommée **indMapType** ; pour stocker les URLs des différents logs et les associer à un identifiant unique dans le système. Ceci permet la création du fichier **.dot** de manière plus aisée.
	*Une *unordered_map<unsigned int, unsigned in>*, renommée **logsMapType** ; pour stocker les identifiants des pages sources et le nombre de hits vers un log particulier depuis ces pages sources.
	*Une *unordered_map<unsigned int, RefStruct>*, renommée **refMapType** ; pour stocker les identifiants des pages destination et une structure personnalisée qui contient un entier et la *unordered_map* précédente.
	*La stucture personnalisée est construite de telle sorte que l'on ait :

```typedef struct {
		int hitsSum;
		refMapType refMap;
	} RefStruct```
	
	Ainsi, pour chaque log destination on a accès aux logs qui le ciblent et le nombre de hits que chacun des ces logs a effectué ainsi que la somme de tous les hits pour chaque destination dans le **RefStruct**.

[Retour vers la page principale](./README.md)