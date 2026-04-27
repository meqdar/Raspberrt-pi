# Raspberrt-pi
Étape 1 : Aller dans le dossier du projet
```bash
cd raspberry-pi
```
Étape 2 : Vérifier l’état du dépôt Git
```bash
git status
```
Étape 3 : créer le fichier .gitignore
```bash
touch .gitignore
```
Étape 4 : ouvrir le fichier .gitignore et ajouterr les protections
```bash
## *.key --> ignore tous les fichier .key
*.key
## *.priv --> ignore clés privées
*.priv
## wg*private.key --> ignore clés wiregaurd
wg*private.key
## *.conf --> ignore les fichiers configuration VPN
*.conf
```
Étape 5 : Retirer les clés déjà envoyées à Git
```bash
git rm --cached *.key
git rm --cached *.conf
git rm --cached *.priv
###git rm --cached retire le fichier de Git sans le supprimer du disque.
```
Étape 6 : Ajouter les nouveaux changements
```bash
git add .gitignore
```
Étape 7 : sauvegarde leschangements
```bash
git commit -m "remove sensitive keys from repository"
```
Étape 8 : envoyer le projet sur github
```bash
git push -u origin master
```
