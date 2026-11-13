# Jonukas Wood – Tactique seule

Version personnelle du skin « Jonukas Skin – Wood ». Elle garde l'interface de base de FM27, y compris les fonds qui changent selon la compétition, et ne conserve que les éléments liés à la tactique et à la composition.

## Installation

1. Garde le dossier original `jonukas-wood` intact comme sauvegarde.
2. Copie ce dossier `jonukas-tactique` au même endroit que `jonukas-wood`, dans le dossier de skins de ton jeu.
3. Dans FM27 : Préférences › Interface, choisis « Jonukas Wood - Tactique seule », puis recharge ou réapplique le skin.
4. Si rien ne change, redémarre le jeu.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `skin.json` | Nom du skin et liste des feuilles de style chargées, dans l'ordre. |
| `tactique-ressources.uss` | Déclare les images (gazons, croquis de terrain) et les deux polices utilisées. |
| `tactique-terrain.uss` | **Actif.** Gazon du terrain tactique, croquis de terrain dans les tuiles et le profil joueur, noms et rôles des joueurs sur le terrain, couleurs d'aptitude aux postes, jauges d'efficacité tactique, plans de terrain (Team News, équipe type, planificateur d'effectif, assistant de formation). |
| `tactique-papier.uss` | **Désactivé.** Panneaux « papier » clairs autour des écrans tactiques, onglets, ajustements tactiques et couleurs encre du skin d'origine. |

## Activer l'aspect papier des écrans tactiques (optionnel)

Le skin d'origine passe toute l'interface en clair. Sans le reste du skin, certains textes du jeu restent blancs. Ils peuvent donc devenir peu lisibles sur les panneaux papier. Pour essayer quand même :

```json
"Sheets": ["tactique-ressources.uss", "tactique-terrain.uss", "tactique-papier.uss"]
```

Si c'est illisible, retire `"tactique-papier.uss"` de la liste.

## Retirer un élément précis

Dans `tactique-terrain.uss`, chaque règle garde son commentaire d'origine, en allemand, qui explique ce qu'elle modifie. Pour en désactiver une, entoure-la de `/* ... */`, enregistre, puis réapplique le skin. Exemples :

- `.tactics-tile-4x4` : croquis beige du terrain dans la tuile tactique de l'accueil.
- `.pitch-small, .pitch-small-bg` : croquis beige de la carte des postes dans le profil joueur.
- `.tactics-collapsable-pitch-grass-colour` : gazon rayé de l'écran Tactique.

Remarque : les règles `.heft-gesicht` (photos des joueurs sur le terrain) ne fonctionnent qu'avec le correctif `gesichter.py` du créateur. Sans lui, elles n'ont aucun effet.
