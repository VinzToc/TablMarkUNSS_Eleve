# TablMarkUNSS Élève

Application **élève** de table de marque : les jeunes officiels remplissent en direct la feuille de match UNSS (chrono, score, fautes, cartons, temps morts, sets), la signent puis l'envoient au professeur.

Activités : handball, hand à 4, futsal, basketball, basket 3×3, football, badminton, tennis de table.

Application complémentaire : [TablMarkUNSS_Prof](https://github.com/VinzToc/TablMarkUNSS_Prof)

## Utilisation

- En ligne (GitHub Pages) : https://vinztoc.github.io/TablMarkUNSS_Eleve/ — une fois Pages activé.
- Installable sur tablette / téléphone (« Ajouter à l'écran d'accueil ») et **utilisable hors ligne** après une première ouverture.
- Le fichier `index.html` fonctionne aussi seul (dépôt sur un portail ou ouverture locale), sans l'installation hors ligne.

## Échange élève → prof

L'élève clôture la feuille puis télécharge un fichier `.json` ou copie un code `TMU1:…`. Le professeur importe ces fichiers ou codes dans TablMarkUNSS Prof. Aucune donnée n'est envoyée à un serveur : tout reste dans le navigateur de chaque appareil (pensez aux sauvegardes côté prof).

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | l'application complète (HTML, CSS, JS dans un seul fichier) |
| `manifest.webmanifest` | nom, couleurs et icônes pour l'installation |
| `sw.js` | mise en cache pour le fonctionnement hors ligne |
| `icons/` | icônes 192 et 512 px |

Après une modification de `index.html`, changer le numéro de version `CACHE` dans `sw.js` pour que les appareils récupèrent la nouvelle version.
