# Installation du module

L'installation du module est très simple, il suffit de récupérer l'ensemble des scripts du module et de les coller dans l'espace de travail des scripts de votre app.

Le module ne fait pas usage de fonctions personnalisées. Les scripts sont autonomes.

Il faut juste prévoir dans votre app une table contenant une rubrique avec un seul enregistrement. La rubrique doit être de type texte, sans aucune option. Cette rubrique ne doit pas être de type globale. Si vous avez une table servant à stoker des rubriques globales c'est parfait.

### Fichiers sources :

* Au format .fmp12 : [lst - Gestion des préférences.zip](https://github.com/djulot/GitBook/blob/master/CM%20lst%20-%20gestion%20des%20préférences.zip)
* Au format Clip Manager 5 : [CM lst - Gestion des préférences.zip](/CM lst - gestion des préférences.zip)

### Initialisation

Une fois les scripts copiés dans votre app, il faut initialiser le module pour cela :

1. Éditer le script nommé **lst\_pref.Init** ;
2. Dans la variable **$layout** y définir le nom du modèle associé à l'occurrence de table où se trouve la rubrique servant à stocker le flux JSON ;
3. Dans la variable **$table** y définir le nom de l'occurrence de table où se trouve la rubrique servant à stocker le flux JSON ;
4. Dans la variable **$field** y définir le nom de la rubrique \(au format table::rubrique\) servant à stocker le flux JSON.



