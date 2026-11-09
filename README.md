# Merry Google

Un mini-site statique avec connexion Google et un profil professionnel personnalisable.

## Fichiers

- `index.html` : page de connexion Google.
- `home.html` : profil présenté après connexion, avec formulaire de personnalisation.

## Lancer le site

Ouvrez ce dossier dans VS Code et démarrez-le avec une extension de serveur local, par exemple Live Server. La connexion Google ne fonctionne pas de façon fiable en ouvrant simplement le fichier avec `file://`.

Ajoutez l'origine de votre serveur local aux **Authorized JavaScript origins** du client OAuth Google, par exemple `http://localhost:5500`. Pour publier le site, hébergez les fichiers sur un service HTTPS et ajoutez également le nom de domaine publié aux origines autorisées.

## Publier dans le dépôt GitHub

Les fichiers `index.html`, `home.html` et `README.md` sont publiés à la racine du dépôt [`heritierjunior/merry-google`](https://github.com/heritierjunior/merry-google). Pour envoyer des modifications ultérieures depuis un clone local du dépôt, exécutez :

```powershell
git add index.html home.html README.md
git commit -m "Add Google sign-in and professional profile pages"
git push -u origin main
```

Le `git push` nécessite un compte connecté disposant du droit d'écriture sur `heritierjunior/merry-google`.

## README du profil GitHub

Une présentation graphique distincte du site est prête dans `github-profile\README.md`, avec sa bannière `github-profile\banner.svg`. Pour personnaliser le profil, copiez ces deux fichiers à la racine du dépôt spécial `mulekyakavira22-dot/mulekyakavira22-dot` : GitHub affiche alors le README sur la page du profil et retrouve la bannière à côté.

## À savoir

La connexion utilise Google Identity Services dans le navigateur. Les informations de connexion sont conservées dans la session du navigateur et les détails personnalisés du profil dans le stockage local de l'appareil. Un site statique ne remplace pas un serveur qui vérifie les identifiants côté serveur : ne l'utilisez pas pour protéger des données confidentielles.
