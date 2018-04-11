Voici les méthodes disponibles pour le module **lst - Gestion des préférences**.

# Grl : Préférences sauvegarde

Ce script permet d'ajouter ou modifier une préférence.

{% method %}
## Ajouter une préférence session

On entend par session la session utilisateur d'un poste donné.

On envoi au script un paramètre au format JSON, avec les clefs suivantes :
- **clef** : le nom de la clef à enregistrer
- **valeur** : valeur de la clef à enregistrer
- **type** : type de la valeur à enregistrer <br>valeur acceptée : text | number | boolean | json


{% sample lang="fmp" %}

```fmp
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "valeur" ; True ; JSONBoolean ] ;	[ "type" ; "boolean" ; JSONString ] )
```

{% common %}
La méthode ne retourne aucune valeur.

{% endmethod %}

{% method %}
## Ajouter une préférence générale

On entend par préférence générale une préférence pour l'ensemble de l'app quelque soit l'utilisateur ou la session.

On envoi au script un paramètre au format JSON, avec les clefs suivantes :
- **clef** : le nom de la clef à enregistrer
- **valeur** : valeur de la clef à enregistrer
- **type** : type de la valeur à enregistrer <br>valeur acceptée : text | number | boolean | json
- **general** : flag booléen doit être à vrai

{% sample lang="fmp" %}

```fmp
JSONSetElement ( "" ;	[ "clef" ; "modeleDefaut" ; JSONString ] ;	[ "valeur" ; "tdb - général" ; JSONString ] ;	[ "type" ; "text" ; JSONString ] ;	[ "general" ; True ; JSONBoolean ])
```

{% common %}
La méthode ne retourne aucune valeur.

{% endmethod %}
