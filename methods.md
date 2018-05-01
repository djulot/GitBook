Voici les méthodes disponibles pour le module **lst - Gestion des préférences**.

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
// pour une préférence liée à un compte utilisateur pour un poste donné
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "valeur" ; True ; JSONBoolean ] ;	[ "type" ; "boolean" ; JSONString ] )

// pour une préférence lié à un compte utilisateur
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "valeur" ; True ; JSONBoolean ] ;	[ "type" ; "boolean" ; JSONString ] ;	[ "user" ; True ; JSONBoolean ]))

// pour une préférence générale à l'app
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "valeur" ; True ; JSONBoolean ] ;	[ "type" ; "boolean" ; JSONString ] ;	[ "general" ; True ; JSONBoolean ])
```
{% sample lang="json" %}
```json
// pour une préférence liée à un compte utilisateur pour un poste donné
{	"clef" : "majEmails",	"type" : "boolean",	"valeur" : true}

// pour une préférence liée à un compte utilisateur
{	"clef" : "majEmails",	"type" : "boolean",	"user" : true,	"valeur" : true}

// pour une préférence générale à l'app
{	"clef" : "majEmails",	"general" : true,	"type" : "boolean",	"valeur" : true}
```

{% common %}
La méthode ne retourne aucune valeur.

{% endmethod %}

{% method %}
## lst_pref.Lecture
Permet de récupérer une valeur d'une préférence.

On envoi au script un paramètre au format JSON, avec les clefs suivantes :

<table><thead><tr><th>clef</th><th>dispo</th><th>description</th></thead></tr><tr><td>clef</td><td>obligatoire</td></tr></table>

- `clef` *obligatoire*<br>le nom de la clef à récupérer
- `general` *optionnel* booléen<br>si vrai alors la préférence à récupérer est générale
- `user` *optionnel* booléen<br>si vrai alors la préférence à récupérer est liée au compte utilisateur

*Si les paramètres *general* et *user* sont tous les deux à faux ou ne sont pas envoyés, alors la préférence à récupérer est liée au compte utilisateur associé au poste.*


{% sample lang="fmp" %}
```fmp
// pour une préférence liée à un compte utilisateur pour un poste donné
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ]  )

// pour une préférence lié à un compte utilisateur
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "user" ; True ; JSONBoolean ]))

// pour une préférence générale à l'app
JSONSetElement ( "" ;	[ "clef" ; "majEmails" ; JSONString ] ;	[ "general" ; True ; JSONBoolean ])
```
{% sample lang="json" %}
```json
// pour une préférence liée à un compte utilisateur pour un poste donné
{	"clef" : "majEmails"
}

// pour une préférence liée à un compte utilisateur
{	"clef" : "majEmails",	"user" : true
}

// pour une préférence générale à l'app
{	"clef" : "majEmails",	"general" : true
}
```

{% common %}
La méthode retourne la valeur lue.

{% endmethod %}
