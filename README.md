# FileMaker - Gestion de préférences

Module de gestion de préférences pour les app FileMaker.

| nom du module | lst - gestion des préférences |
| :--- | :--- |
| dépendance | aucune |
| version FileMaker minimum | 16 |
| compatibilité | Pro - Server - WebDirect - Go |
| licence | [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) |

Ce module permet de sauvegarder, lire et supprimer les préférences d'une app FileMaker en son sein sous forme d'un flux JSON stocké dans une rubrique de votre choix dans la table de votre choix.

L'objectif étant d'éviter d'ajouter une table de préférences avec de multiples rubriques et de multiples enregistrements. Au fur et à mesure du développement d'une app il n'est plus ainsi nécessaire d'ajouter de nouvelles rubriques. Le transfert des préférences d'une app à une autre est aussi simplifié puisqu'il suffit de récupérer le flux JSON stocké dans une rubrique.

Le module permet de stocker des préférences :

* Générales : pour des préférences communes à l'ensemble des utilisateurs de l'app, comme par exemple des valeurs de paramétrages, des constantes, etc.
* Utilisateurs : pour des préférences propres à un compte utilisateur de l'app, quelque soit le poste utilisé.
* Sessions : pour des préférences propres à un compte utilisateur pour un poste donné.

Les types de valeurs gérés par le module sont : texte, nombre, booléen et JSON.



