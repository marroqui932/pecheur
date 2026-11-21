# Le Pêcheur de l'Océan · Commandes des fêtes

Outil de gestion des commandes de plateaux de fruits de mer : saisie des tickets du carnet, planning des retraits, marchandise à prévoir en kilos et impression des bons.

Hébergement : GitHub Pages. Données : Firebase (Firestore + Authentication).

## Mise en route (une seule fois)

### 1. Créer le projet Firebase
1. Va sur https://console.firebase.google.com et connecte-toi avec un compte Google.
2. « Créer un projet », nomme-le `pecheur-ocean`, désactive Google Analytics, puis valide.

### 2. Activer la connexion
1. Menu de gauche : Créer (Build) > Authentication > Commencer.
2. Onglet « Mode de connexion » : choisis « Adresse e-mail/Mot de passe », active-la, puis enregistre.
3. Onglet « Utilisateurs » > « Ajouter un utilisateur » : crée le compte de la poissonnerie, par exemple `commandes@pecheur-ocean.fr` avec un bon mot de passe. L'e-mail n'a pas besoin d'exister vraiment.
4. Onglet « Paramètres » > « Domaines autorisés » > « Ajouter un domaine » : `marroqui932.github.io`.

### 3. Créer la base de données
1. Créer (Build) > Firestore Database > Créer une base de données.
2. Emplacement : `eur3 (europe-west)`. Mode : production.
3. Onglet « Règles » : remplace tout par le contenu du fichier `firestore.rules`, puis clique sur « Publier ».

### 4. Relier le site à Firebase
1. Roue dentée > Paramètres du projet > « Vos applications » > icône Web `</>`.
2. Nom : `site`. Ne coche pas Firebase Hosting. Clique sur « Enregistrer l'application ».
3. Copie les valeurs de `firebaseConfig` (apiKey, authDomain…) dans `firebase-config.js`, à la place des `A_REMPLIR`.

### 5. Premier lancement
1. Ouvre https://marroqui932.github.io/pecheur et connecte-toi.
2. Onglet Produits : « Charger les 20 produits d'exemple », puis corrige les prix et les poids.

## Installer sur l'iPhone
Ouvre le site dans Safari, puis touche Partager > « Sur l'écran d'accueil ». L'app s'ouvre en plein écran avec son icône.

## Bon à savoir
- Le site garde les données sur le téléphone. Sans réseau, tu peux consulter et modifier les commandes : les changements partent au retour du réseau.
- Pour retirer l'accès à quelqu'un, change le mot de passe dans Firebase > Authentication.
