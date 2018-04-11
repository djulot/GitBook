Voici les méthodes disponibles pour le module **lst - Gestion des préférences**.

# Grl : Préférences sauvegarde

Ce script permet d'ajouter ou modifier une préférence.

{% method %}
## lst_pref.Sauvegarde
Enregistre ou modifie une préférence.

On envoi au script un paramètre au format JSON, avec les clefs suivantes :
- **clef** *obligatoire*<br>le nom de la clef à enregistrer
- **valeur** *obligatoire*<br>valeur de la clef à enregistrer
- **type** *obligatoire* (text|number|boolean|json)<br>type de la valeur à enregistrer
- **general** *optionnel* booléen<br>si vrai alors la préférence sera enregistrée pour l'ensemble de l'app
- **user** *optionnel* booléen<br>si vrai alors la préférence sera enregistrée pour le compte utilisateur

*Si les paramètres *general* et *user* sont tous les deux à faux ou ne sont pas envoyés, alors la préférence sera enregistrée pour le compte utilisateur associé au poste.*


{% sample lang="fmp" %}

```fmp
// pour une préférence lié à un compte utilisateur pour un poste donné
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "valeur" ; True ; JSONBoolean ] ;	[ "type" ; "boolean" ; JSONString ] )

// pour une préférence lié à un compte utilisateur
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "valeur" ; True ; JSONBoolean ] ;	[ "type" ; "boolean" ; JSONString ] ;	[ "user" ; True ; JSONBoolean ]))
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
