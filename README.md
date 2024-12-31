# Quête-Partage-de-fichiers-Windows

## :one: Installation du rôle Partage de fichiers  
  
Dans le cas où le Partage de fichiers n'est pas déjà installé sur le serveur, suivre les étapes suivantes :  
  
➡️ Sur le Server Manager, cliquer sur `Add roles and features`  
  
➡️ Cliquer sur `Next` 3 fois jusqu'à arriver à la fenêtre de séléction de rôles  
  
➡️ Séléctionner `File and Storage Services` et cliquer sur `Next`  
  
➡️ Suivre les étapes jusqu'à la fin de l'installation  

## :two: Création d'un partage  
  
Maintenant que nous avons installé le rôle, nous allons créer un nouveau partage.  
  
Avant toute chose, rendez-vous sur C:\ et créez un dossier `Documents_Entreprise`  
  
➡️ Se rendre sur Server Manager  
  
➡️ Dans le menu de gauche, cliquer sur `File and Storage Services` puis sur `Shares`  
  
➡️ Faire un clic droit sur la fenêtre et cliquer sur `New Share...`  
  
➡️ Choisir `SMB Share - Quick` et `Next`  
  
➡️ Pour la localisation du partage, nous allons cocher `Type a custom path` et entrer le chemin suivant : `C:\Documents_Entreprise`  
  
➡️ En face de `Share name:`, entrer le nom `Docs`  
  
➡️ Cliquer sur `Next` jusqu'à terminer l'installation  

## :three: Création des utilisateurs dans l'Active Directory  
  
Nous avons besoin de créer des utilisateurs dans différents groupes pour tester si les permissions configurées fonctionnenent bien.  
  
Suivez ces étapes :  
  
➡️ Server Manager -> **Tools** -> **Active Directory Users and Computers**  
  
➡️ Clic droit sur le nom de domaine puis cliquer sur `New` -> `Organizational Unit`  
  
➡️ Répéter l'opération 3 fois avec comme noms `RH`, `Comptabilité` et `Direction`  
  
➡️ Dans chaque OU, créer un nouveau groupe que l'on appellera `Users RH` `Users Compta` `Users Dir`
  
## 4️⃣ Configuration des permissions pour les sous dossiers en fonction des groupes  
  
Créez trois sous dossiers sous `Documents_Entreprise` : `RH` `Comptabilité` et `Direction`  
  
Se rendre dans l'explorateur de fichiers, `This PC` -> `Local Disk (C:)` -> `Documents_Entreprise`  
  
🍀 **Comptabilité**  
Faire un clic droit sur le nom du dossier puis `Properties`. Dans l'onglet `Security`, cliquer sur le bouton 'Edit' puis 'Add'
