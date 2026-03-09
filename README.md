Projet réalisé dans le cadre d'une activités scolaire toutes les informations du projet pourrons être retrouvée ci dessous: 
première activité:

Activité : Créer son profil GitHub et déposer son premier projet
1. Contexte : Qu'est-ce que GitHub ?
Dans les métiers de l’informatique et de l’électronique, les techniciens et développeurs utilisent souvent des outils pour stocker et partager leur travail.

Un des outils les plus utilisés dans le monde est GitHub.

GitHub permet de :

Sauvegarder ses projets de code.
Suivre les modifications d’un programme (l'historique).
Travailler à plusieurs sur un même projet.
Montrer son travail aux entreprises lors de recherches de stage ou d'emploi.

Important : Dans la poursuite d’étude en BTS SIO (Services Informatiques aux Organisations), cet outil est très souvent utilisé.
2. Intérêt pour votre avenir
Créer un profil GitHub permet :

De conserver vos projets scolaires (Bac Pro, TP Arduino, etc.).
De montrer concrètement vos compétences en programmation et électronique.
De préparer vos études en BTS SIO ou autres formations supérieures.
De présenter un portfolio technique à jour.

Dans les métiers de l’informatique, on dit souvent : GitHub est le CV des développeurs.

Même des petits projets simples sont utiles pour montrer que vous pratiquez.
3. Objectifs de l’activité
À la fin de l’activité vous serez capables de :

Créer un compte GitHub.
Créer un dépôt (ou repository).
Publier un projet.
Ajouter une description (fichier README).
Comprendre le principe du versionning (historique des versions).
4. Guide Pas à Pas
Étape 1 : Créer un compte GitHub
Aller sur le site : https://github.com
Cliquer sur Sign up (S'inscrire).
Choisir vos informations :
Nom d’utilisateur : Choisir un nom d’utilisateur sérieux et professionnel.
Adresse mail : Utiliser votre adresse mail professionnelle ou scolaire.
Mot de passe : Choisir un mot de passe sécurisé.

À faire (Sérieux)
À éviter (Non professionnel)
prenom-nom
killer59
nom.prenom
darkmaster
prenom-nom-dev
gamerpro2000

Étape 2 : Compléter son profil
Cliquer sur votre photo de profil (en haut à droite) puis Your profile.
Ajouter une Bio pour vous présenter.

Exemple de Bio :Étudiant en Bac Pro CIEL - Passionné par l’électronique et la programmation Arduino. Objectif : Poursuite d’études en BTS SIO.

Ajouter une Photo (facultatif, mais recommandé pour un profil professionnel).
Étape 3 : Créer un premier dépôt (Repository)
Un dépôt est l'espace où vous allez stocker les fichiers d'un projet.

Cliquer sur New Repository (Nouveau dépôt).
Nom du dépôt : Projets-Bac-Pro-CIEL
Cocher l'option : ✅ Add README

Le README est un fichier important. C'est la première chose que les visiteurs verront. Il sert à expliquer ce qu'est le projet, comment l'utiliser et quel matériel est nécessaire.
Étape 4 : Comprendre le versionning (Historique)
Le versionning permet de garder l’historique des modifications d’un projet.

Chaque modification enregistrée s’appelle un commit.

Version
Modification
Description du Commit
v1
Allumage LED simple
Version initiale du projet LED.
v2
Ajout bouton poussoir
Commande la LED avec le bouton.
v3
Ajout de la mémoire
La LED change d'état à chaque appui.


Ce système permet de :

Revenir facilement à une ancienne version du code.
Comprendre comment le projet a évolué.
5. Exemple de projet à déposer : TP LED
Vous allez déposer votre code Arduino d'un TP sur GitHub.

Projet : Allumage LED avec bouton poussoir

Matériel Utilisé
Carte Arduino
LED
Résistance
Bouton poussoir
Fils de connexion

Version 1 : LED + bouton poussoir (sans mémoire)
Principe : La LED s’allume uniquement quand on appuie sur le bouton.

Pseudo Code
Programme Arduino (simplifié)
si bouton appuyé
int etat = digitalRead(bouton);
ALORS LED allumée
if (etat == HIGH) { digitalWrite(led, HIGH); }
SINON LED éteinte
else { digitalWrite(led, LOW); }


int bouton = 2;
int led = 13;
void setup() {
  pinMode(bouton, INPUT);
  pinMode(led, OUTPUT);
}
void loop() {
  int etat = digitalRead(bouton);
  if (etat == HIGH) {
    digitalWrite(led, HIGH);
  } else {
    digitalWrite(led, LOW);
  }
}

Commit GitHub : Version 1 : LED commandée par bouton poussoir
Version 2 : LED avec mémoire
Principe : Chaque appui sur le bouton change l’état de la LED.

Appui 1 → LED ON
Appui 2 → LED OFF
Appui 3 → LED ON

Pseudo Code
Programme Arduino (simplifié)
si bouton appuyé
if (digitalRead(bouton) == HIGH)
ALORS changer état LED
etatLed = !etatLed;


int bouton = 2;
int led = 13;
bool etatLed = false; // Variable pour garder l'état
void setup() {
  pinMode(bouton, INPUT);
  pinMode(led, OUTPUT);
}
void loop() {
  if (digitalRead(bouton) == HIGH) {
    etatLed = !etatLed; // Inversion de l'état (true devient false et inversement)
    delay(300); // Pause pour éviter plusieurs changements en un seul appui
  }
  digitalWrite(led, etatLed);
}

Commit GitHub : Version 2 : ajout mémoire LED
6. Travail demandé
Créer votre compte GitHub (File Lien vers le formulaire d'inscription GitHub).
Créer un repository nommé Projets-Bac-Pro-CIEL.
Dans ce repository, ajouter le code de votre TP LED (le code de la Version 2 est préférable car plus complet).
Écrire dans le fichier README du projet :
Objectif du projet (Allumer une LED avec un bouton poussoir et une fonction mémoire).
Matériel utilisé (Liste complète du matériel).
Fonctionnement (Explication simple des deux versions).
7. Conclusion
Cette activité permet de :

Découvrir un outil utilisé par les professionnels (les développeurs et les techniciens).
Conserver vos projets de manière sécurisée.
Préparer votre poursuite d’étude en BTS SIO.

Plus vous mettrez de projets sur GitHub, plus votre profil montrera vos compétences !

Deuxième activité:

Pour aller plus loin : associer Visual Studio Code et GitHub (guide pas à pas)
Dans les métiers de l’informatique, les développeurs écrivent leur code dans un éditeur puis l’envoient vers une plateforme de gestion de versions comme GitHub. Un éditeur très utilisé est Visual Studio Code.

Vous allez apprendre à relier votre projet local à GitHub pour publier votre travail.
Étape 1 : installer les outils
Vérifier que les logiciels suivants sont installés :

Visual Studio Code
Git

Git permet de gérer les versions du projet.
Étape 2 : se connecter à GitHub dans Visual Studio Code
Ouvrir Visual Studio Code
Cliquer sur l’icône Compte (en bas à gauche)
Cliquer sur Sign in with GitHub
Autoriser la connexion dans le navigateur

Votre éditeur est maintenant relié à votre compte GitHub.
Étape 3 : créer un dossier de projet
Créer un dossier sur votre ordinateur : TP_LED_BOUTON

Puis ouvrir ce dossier dans Visual Studio Code : File → Open Folder
Étape 4 : créer le fichier du programme
Créer un fichier : led_bouton.ino

Ajouter votre programme Arduino : Version simple (sans mémoire).
Étape 5 : initialiser le projet Git
Dans Visual Studio Code :

Cliquer sur l’icône Source Control
Cliquer sur Initialize Repository

Votre projet est maintenant suivi par Git.
Étape 6 : faire le premier commit
Dans l’onglet Source Control :

Écrire un message de modification : Version 1 : LED commandée par bouton poussoir

Puis cliquer sur : Commit

Un commit correspond à l’enregistrement d’une version du projet.
Étape 7 : publier le projet sur GitHub
Cliquer sur : Publish to GitHub

Votre projet est maintenant visible sur votre profil GitHub.

Vous venez de publier votre premier projet.
Étape 8 : améliorer le projet
Modifier votre programme pour créer une seconde version :

Projet : LED avec mémoire.

Principe :

appui 1 → LED ON
appui 2 → LED OFF
Étape 9 : enregistrer la nouvelle version
Retourner dans Source Control.

Écrire un message : Version 2 : ajout mémoire LED

Cliquer sur : Commit

Push

La nouvelle version est envoyée sur GitHub.
Résultat final
Votre projet GitHub contient maintenant :

le code du TP
plusieurs versions du programme
l’historique des modifications

Voici un exemple d’évolution de votre projet :

Version
Description
Version 1
LED contrôlée par bouton
Version 2
LED avec mémoire

Ce que vous venez d’apprendre
Avec cette activité vous avez appris à :

utiliser Visual Studio Code
utiliser Git
publier un projet sur GitHub
enregistrer différentes versions d’un programme

Ces compétences sont très utilisées dans les métiers de l’informatique et dans les études en BTS SIO. 🚀
