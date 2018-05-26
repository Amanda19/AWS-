# Présentation du projet Calendrier 



### ReadMe.md

![](https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png)




**Contenu**

[TOC]

## Présentation global de l'application
Ce projet consiste en le développement d'une application web, "un calendrier". Les technologies utilisées pour le réaliser sont EJS, CSS, JavaScript, node.js, et une base de données no sql avec  MongoDb.
##  Fonctionnalités de l'application

####  Login 
Permet à l'utilisateur de se connecter à l'application pour y accéder.
#### Logout
Un lien permettant à l'utilisateur de se déconnecter à l'application.
#### SignIn
Permet à l'utilisateur de s'inscrire à l'application.
#### Interface du Calendrier
Un Calendrier contenant 48 lignes de 30 minutes et de 7 colonnes pour les jours, qui peut être changé en une jours ou mois selon les besoins de l'utilisateur.
#### Ajout d'un événement
Un utilisateur connecté clique sur n'importe quelle case vide pour ajouter un événement. Un popUp sera alors affiché lors du clique, il permet à l'utilisateur de rédiger le titre de l'événement, de modifier la date s'il souhaite et de confirmer. Une fois l'event est ajouté, la case aura le titre et le login de l'utilisateur ainsi la couleure choisie
#### Supression d'un événement
L'utilisateur ayant créer l'événement a le droit de supprimer  son/ses événement(s), s'il le désire. Un PopUp de confirmation sera alors affiché.
#### Modification d'un événement
L'utilisateur  ayant créer un événement donné, peut modifier le titre et la date de début et de fin de l'événement
## Structure de l'application
#### Page d'accueil
L'application a comme page d'accueil dont le root /home,  nous donne la possibilité de s'inscrire ou de se connecter à l'application. Une fois connecté, l'utilisateur aura accées au calendrier d'énénements. sinon il nous redirige vers la même page d'accueil.
#### Calendrier
Le root ici c'est le /dashboard on y accède après la connexion. C'est le Calendier décrit au-dessus.
#### Sortir de l'application
Lorsque l'utilisateur clique sur logout, il sera redirigé vers /home la page d'accueil. 
## Technologies Utilisées
#### EJS
Il a été utilisé pour la création des différentes pages web.
#### CSS
Il a été utilisé pour  mettre en forme les pages web
#### Bootstrap
Nous avons utilisé ce framework pour donner un bon designe à l'application
#### JacaScript
Il a été utilisé pour développé l'application du coté client. Nous avons utilisé une Template pour la création du calendrier et certaines fonctionnalités tels que: création des cases, création des boutons..etc. Nous l'avons aussi utilisé pour la création de la page d'accueil et la gestion des événements.
#### Node.js
Un framework utilisé pour développer le côté serveur. Organiser les différents root ainsi que  la création des schémas de  base de données
#### MongoDB
Base de données NoSql, qui a le format Json et qui est plus adaptée aux téchnologies citées précédemment.
##  Structure du code
La structure du code sera expliqué dans ce qui suit:
#### côté Serveur
Dans le fichier** index.js **se trouve la partie** serveur** où nous avons utilisé les différents **packages** dont nous avons besoins que ce soit pour le *démarrage de l'application, *le port utilisé*, *la base de données utilisée*...  etc
Puis, on retrouve** les chemins** (**root**) de l'application. les chemins sont** /home **pour la **page d'accueil**, **/dashboard** pour le **calendrier**, **/register **pour le **signin** mais qui nous redirige toujours vers le **/home**.
**/login** qui redirige soit vers** /dashboard** si la~~ connexion~~ a été effectuée avec *succè*s. dans le cas contraire** redirection**  vers** /Home.**
On retrouve ainsi la** gestion **des **événements** qui  est un bout de **code** qui** intéragit** avec la **base de données.**
**/data** nous donne les différentes** informations****** sur le *contenu de la BD*
#### côté Client
Concernant le Calendrier dans le **dashboard.ejs** nous avons utilisé une **Template** qui génère et qui gère le **calendrier**.
#### Pages web
Nous avons développer les pages web comme ceci:
##### dashboard.ejs
V'est le tableau de bord, la page web principale  du projet, elle contient un lien vers la template calendrier.js , un autre lien vers le css ainsi que les balises pour la structuration de la page web.
##### Home.ejs
Elle dispose des balises qui  structure  la  page web que l'utilsateur aura tout au début qui lui premt de se connecter, de s'inscrire et à laquelle il sera redirigée une fois déconnecté. ainsi qu'un lien vers le CSS

##### footer et Header.ejs
Elle contiennent les balises qui structurent l'en-tête et les pieds de la page web dashboard.

##### les  pages de styles CSS

##  Lancement de l'application
Le lancement de l'application nécessite certains prérequis :
###### Installation  de MongoDB
###### Installation  de npm
###### Installation  de nodejs
L'application étant en local elle se  lance comme suit:
###### `$ mongod`  
###### `$ install npm`
###### `$ node index.js`
**NB**: Mongod se lance sur un terminal et les deux autres sur un autre terminal.
On ouvre le navigateur et on tape :
###### `<link>` : <https://localhost:8082>







