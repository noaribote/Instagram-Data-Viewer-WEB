# Avertissement: Phase de développement

La version web d'Instagram Data Viewer est actuellement en phase de développement et peut contenir des problèmes, bugs ou manques. Veuillez attendre la sortie d'une **version stable** avant toutes utilisations.

# Instagram Data Viewer — version web locale

Cette version reprend [**l'application originale Instagram Data Viewer**](https://github.com/noaribote/Instagram-Data-Viewer) dans une interface responsive web. Les données importées sont désormais stockées dans le IndexedDB du navigateur. Le scraper de profils s’exécute dans un petit serveur local Node.js et enregistre son cache dans le même dossier `model/users/` que l’application Electron.

[Consultez le projet original d'Instagram Data Viewer](https://github.com/noaribote/Instagram-Data-Viewer)

[Consultez le README de l'application originale d'Instagram Data Viewer](https://github.com/noaribote/Instagram-Data-Viewer/blob/main/README.md)

### Lancer le site

Depuis la racine du projet, démarrez le serveur web local :

```sh
node .web/server.js
```

Ouvrez ensuite `http://127.0.0.1:8000` dans le navigateur. Le serveur ne reçoit pas les archives importées. Pour lancer le scraper, Python et `instaloader` doivent être installés; le serveur utilise automatiquement `.venv` s’il existe, ou l’interpréteur indiqué par la variable `PYTHON`.

### Importer les données

Choisissez une archive ZIP de données Instagram ou un dossier décompressé. L’import ZIP est traité dans le navigateur. Les fichiers JSON deviennent consultables et cherchables; les autres fichiers sont conservés localement. Pour libérer l’espace, utilisez le bouton en bas de la barre latérale.

Les données sont rattachées au navigateur et à l’adresse du site. Elles ne sont pas synchronisées avec l’application Electron ni avec les autres appareils. Effacer les données du site dans les paramètres du navigateur les supprimera aussi.

### Fonctions nécessitant encore un service local

Le téléchargement automatisé de stories, highlights, reels et publications repose sur les services Python/Playwright de l’application de bureau; il n’est pas disponible dans cette version web. La consultation des archives, les statistiques locales, la recherche dans les JSON, les contacts et les conversations restent dans le navigateur.

# Avertissement relatif à l'usage de l'IA

Ce logiciel a été conçu et pensé par un humain. Chacun de ses programmes a été créé de manière indépendante par l'auteur.

L'intelligence artificielle a toutefois constitué un atout majeur dans le développement de cette application. Elle a réutilisé l'ensemble des codes indépendants produits par l'auteur, ainsi que ses instructions, afin de concevoir le logiciel "Instagram Data Viewer" avec les technologies choisies par ce dernier.
