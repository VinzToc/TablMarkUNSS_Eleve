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

## Transmission par QR code

À la clôture, l'élève peut afficher un **QR code pour le prof** : il contient un résumé compact de la feuille (rencontre, équipes, score par période ou sets, jeunes officiels et n° JO). Le prof le scanne dans TablMarkUNSS Prof (« Feuilles reçues → Scanner un QR code », ou photo du QR code). Le fichier .json reste le moyen de transmettre la feuille complète ; importé ensuite, il remplace le résumé.

Dans l'autre sens, la **feuille préparée par le prof** (équipes, joueurs, licences, jeunes officiels) passe aussi par QR code : l'appli prof affiche un ou plusieurs QR codes qui défilent automatiquement, et la tablette de la table de marque les scanne (« Importer une feuille du prof → Scanner le QR code du prof »), dans n'importe quel ordre, jusqu'à « Feuille reçue ».

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | l'application complète (HTML, CSS, JS dans un seul fichier) |
| `manifest.webmanifest` | nom, couleurs et icônes pour l'installation |
| `sw.js` | mise en cache pour le fonctionnement hors ligne |
| `icons/` | icônes 192 et 512 px |
| `lib/jsQR.js` | jsQR (licence Apache 2.0) lit les QR codes du prof |
| `lib/qrcode.js` | qrcode.js (Kazuhiko Arase, licence MIT) génère le QR code |

Après une modification de `index.html`, changer le numéro de version `CACHE` dans `sw.js` pour que les appareils récupèrent la nouvelle version.
