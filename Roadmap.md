# Roadmap du Développement sur base d'exemple : ChatROOM

Les étapes sont les mêmes pour n'importe quel projet qui requiert REDUX

## Étape 1 : Configuration
- **Récupération du Modèle** : Je commence par récupérer un modèle initial de l'application, qui peut servir de base pour mon projet.
  - *Où* : N/A
  - *Pourquoi* : Le modèle fournit une structure de départ pour le développement de mon application.
- **Installation des Dépendances** : J'installe les bibliothèques et les modules nécessaires à mon projet à l'aide de gestionnaires de paquets comme npm.
  - *Où* : Terminal
  - *Pourquoi* : Les dépendances contiennent des outils et des fonctionnalités essentiels pour le développement.

## Étape 2 : Rendu Initial
- **Vérification du Rendu** : Je m'assure que je peux afficher un élément React dans le DOM réel à l'aide de la fonction render de ReactDOM.
  - *Où* : Fichier d'entrée (ex : main.tsx)
  - *Pourquoi* : C'est la première étape pour confirmer que React est configuré correctement.

## Étape 3 : Découpage
- **Identification des Zones** : Dans le composant racine, j'identifie les zones principales de l'application, telles que la liste des messages et le formulaire de saisie.
  - *Où* : Composant Racine (ex : App.tsx) ici on a changé le nom en Chat.tsx (dans le components/Chat/Chat.tsx)
  - *Pourquoi* : Cette étape m'aide à planifier la structure globale de l'interface utilisateur.

## Étape 4 : Composants
- **Description des Composants** : Je décris les composants nécessaires pour représenter différentes parties de l'interface utilisateur, tels que Form pour le formulaire, Messages pour la liste des messages, et Message pour le contenu d'un message.

  - *Où* : Composants individuels (ex : Form.tsx, Messages.tsx, Message.tsx)
  - *Pourquoi* : Les composants me permettent de découper l'interface en morceaux réutilisables.

📝 A moi de bien définir le découpage et créer les composants selon le projet. 

## Étape 5 : Utilisation de Props
- **Configuration avec Props** : J'utilise les props pour configurer les composants en leur transmettant des données et en définissant leur comportement.
  - *Où* : Composants (ex : Form.tsx, Messages.tsx, Message.tsx)
  - *Pourquoi* : Les props me permettent de personnaliser et de paramétrer les composants de manière flexible.

## Étape 6 : Gestion de l'État avec Redux
- **Installation de Redux** : J'installe la bibliothèque Redux, qui offre un moyen de gérer l'état global de l'application.
  - *Où* : Terminal
  - *Pourquoi* : Redux me permet de centraliser et de contrôler l'état de manière prévisible.
  
- **Création du Store** : Je crée un magasin (store) qui contient l'état global de l'application, en utilisant Redux.
  - *Où* : Fichier "index.ts" (ex : index.ts)
  - *Pourquoi* : Le store est responsable de la gestion de l'état global.
  
- **Mise en Place du Reducer** : Je configure un reducer pour gérer les actions qui modifient l'état de l'application, en suivant le modèle Redux.
  - *Où* : Fichier de reducer (ex : reducers/chat.ts)
  - *Pourquoi* : Le reducer décide comment l'état doit évoluer en réponse aux actions.
  
- **État Initial** : Je configure un état initial qui comprend les données nécessaires au démarrage de l'application, telles que la liste des messages initiaux.
  - *Où* : Fichier "index.ts" (ex : index.ts)
  - *Pourquoi* : L'état initial assure que l'application démarre avec des données de base.

## Étape 7 : Provider Redux
- **Installation de React-Redux** : J'installe la bibliothèque React-Redux, qui facilite l'intégration de Redux avec React.
  - *Où* : Terminal
  - *Pourquoi* : React-Redux rend Redux accessible dans les composants React.
  
- **Utilisation du Composant Provider** : J'utilise le composant Provider pour rendre le store Redux accessible dans toute l'application, en le plaçant à la racine de ma hiérarchie de composants.
  - *Où* : Fichier racine (ex : ici c'est main.tsx)
  - *Pourquoi* : Le Provider permet aux composants de souscrire au store Redux.

- **Importation du Store** : J'importe le store dans mon application et le passe en tant que prop au composant Provider.
  - *Où* : Fichier racine (ex : ici c'est main.tsx)
  - *Pourquoi* : Le store doit être accessible pour que les composants puissent l'utiliser.

## Étape 8 : Utilisation de useSelector

- **Utilisation de useSelector** : J'utilise le hook useSelector fourni par React-Redux pour lire les données depuis le store Redux, comme les messages dans le composant Messages.
  - *Où* : Composants concernés (ex : Messages.tsx)
  - *Pourquoi* : useSelector me permet de connecter les composants à l'état du store.

## Étape 9 : Utilisation de useDispatch

- **Utilisation de useDispatch** : J'utilise le hook useDispatch pour obtenir la fonction dispatch qui me permet d'émettre des actions.
  - *Où* : Composants concernés (ex : Form.tsx)
  - *Pourquoi* : useDispatch me permet de déclencher des actions en réponse aux interactions de l'utilisateur.

- **Gestion des Actions** : J'ajoute des gestionnaires d'événements (onClick, onSubmit, onChange, etc.) dans les composants pour réagir aux interactions de l'utilisateur.
  - *Où* : Composants concernés (ex : Form.tsx)
  - *Pourquoi* : Les actions sont émises en réponse aux interactions de l'utilisateur.

- **Émission d'Intentions** : J'émet des intentions (actions) en utilisant dispatch en réponse à ces interactions pour signaler les changements d'état souhaités.
  - *Où* : Composants concernés (ex : Form.tsx)
  - *Pourquoi* : Les actions décrivent les actions spécifiques à effectuer, comme l'ajout d'un message, afin de mettre à jour l'état de l'application.


