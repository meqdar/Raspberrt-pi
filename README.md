# Raspberrt-pi
Étape 1 : Aller dans le dossier du projet
```bash
cd raspberry-pi
```
Étape 2 : créer le fichier .gitignore
```bash
touch .gitignore
```
Étape 3 : ouvrir le fichier .gitignore et ajouterr les protections
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
Étape 4 : Retirer les clés déjà envoyées à Git
```bash
git rm --cached *.key
```
Étape 5 : sauvegarde leschangements
```bash
git commit -m "remove sensitive keys from repository"
```
Étape 6 : envoyer le projet sur github
```bash
git push -u origin master
```
