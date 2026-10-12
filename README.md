# ProjetGlobe — scripts des modèles

| Fichier | Contenu | Où le coller / l'exécuter |
| --- | --- | --- |
| `mcd.mcd` | MCD Merise/2 (16 entités, 21 associations, spécialisation XT) | https://www.mocodo.net → coller, « Générer ». L'onglet MLD donne le schéma relationnel. |
| `mpd_dbdiagram.dbml` | MPD, 24 tables, groupées par domaine | https://dbdiagram.io/d → remplacer tout le contenu de l'éditeur |
| `mpd_mermaid.mmd` | MPD en Mermaid | Miro (app Mermaid), https://mermaid.live, ou directement sur GitHub dans un bloc ```mermaid |
| `mpd_postgresql.sql` | MPD PostgreSQL complet (contraintes, déclencheur XT, vues, rôles et permissions) | `psql -f mpd_postgresql.sql`, DBeaver ou pgAdmin |
| `tests_regles_metier.sql` | Jeu de données + tests des règles (6 erreurs attendues, annoncées) | `psql -f tests_regles_metier.sql` après le MPD |
| `diagramme_classes.puml` | Diagramme de classes UML | https://www.plantuml.com/plantuml ou https://www.planttext.com, draw.io (Organiser > Insérer > Avancé > PlantUML) |
| `diagrammes_comportementaux.puml` | Cas d'utilisation, états d'un projet, séquence du rendu | Idem, un bloc `@startuml … @enduml` à la fois |
| `*.png` | Rendus déjà générés de chaque diagramme | — |

Règle just-in-time : toute migration de la base met à jour `mcd.mcd` et `mpd_dbdiagram.dbml` dans le même ticket (Definition of Done).
