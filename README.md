###Présentation du projet Calendrier



# ReadMe.md

![](https://pandao.github.io/editor.md/images/logos/editormd-logo-180x180.png)




**Contenu**

[TOC]

# # Présentation global de l'application
Ce projet consiste en le développement d'une application web, "un calendrier". Les technologies utilisées pour le réaliser sont EJS, CSS, JavaScript, node.js, et une base de données no sql avec  MongoDb.
##  Fonctionnalités de l'application
En général, le principe est de réaliser un calendrier d'événements, qui permets de créer, modifier et supprimer un événement donné sans pour autant qu'il y ait de chauvauchement. Les principales fonctionnalités sont décrites brièvement  dans ce qui suite:
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
##  Structure de l'application
#### Page d'accueil
L'application a comme page d'accueil dont le root /home,  nous donne la possibilité de s'inscrire ou de se connecter à l'application. Une fois connecté, l'utilisateur aura accées au calendrier d'énénements. sinon il nous redirige vers la même page d'accueil.
#### Calendrier
Le root ici c'est le /dashboard on y accède après la connexion. C'est le Calendier décrit au-dessus.
#### Sortir de l'application
Lorsque l'utilisateur clique sur logout, il sera redirigé vers /home la page d'accueil. 
##  Technologies Utilisées
#### EJS
Il a été utilisé pour la création des différentes pages web.
#### CSS
Il a été utilisé pour  mettre en forme les pages web
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
####Pages web
Nous avons développer les pages web comme ceci:
##### dashboard.ejs
V'est le tableau de bord, la page web principale  du projet, elle contient un lien vers la template calendrier.js , un autre lien vers le css ainsi que les balises pour la structuration de la page web.
##### Home.ejs
Elle dispose des balises qui  structure  la  page web que l'utilsateur aura tout au début qui lui premt de se connecter, de s'inscrire et à laquelle il sera redirigée une fois déconnecté. ainsi qu'un lien vers le CSS

##### footer et Header.ejs
Elle contiennent les balises qui structurent l'en tête et les pieds de la page web dashboard.
##### les  pages de styles CSS
Ils permettent de donner une meilleure présentation, un meilleur style au différentes pages ejs présentées ci-dessus.

##  Lancement de l'application
Le lancement de l'application nécessite certains prérequis :
###### Installation  de MongoDB
###### Installation  de npm
###### Installation  de nodejs
L'application étant en local elle se  lance comme suit:
`$ mongod`  
`$ install npm`
`$ node index.js`
**NB**: Mongod se lance sur un terminal et les deux autres sur un autre terminal.
On ouvre le navigateur et on tape :
`<link>` : <https://localhost:8082>

##  Apperçue de l'application
Image:

![](https://pandao.github.io/editor.md/examples/images/4.jpg)

> Follow your heart.

![](https://pandao.github.io/editor.md/examples/images/8.jpg)

> 图为：厦门白城沙滩 Xiamen

图片加链接 (Image + Link)：

[![](https://pandao.github.io/editor.md/examples/images/7.jpg)](https://pandao.github.io/editor.md/examples/images/7.jpg "李健首张专辑《似水流年》封面")

> 图为：李健首张专辑《似水流年》封面
                
----

###Lists

####Unordered list (-)

- Item A
- Item B
- Item C
     
####Unordered list (*)

* Item A
* Item B
* Item C

####Unordered list (plus sign and nested)
                
+ Item A
+ Item B
    + Item B 1
    + Item B 2
    + Item B 3
+ Item C
    * Item C 1
    * Item C 2
    * Item C 3

####Ordered list
                
1. Item A
2. Item B
3. Item C
                
----
                    
###Tables
                    
First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell 

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |

| Function name | Description                    |
| ------------- | ------------------------------ |
| `help()`      | Display the help window.       |
| `destroy()`   | **Destroy your computer!**     |

| Item      | Value |
| --------- | -----:|
| Computer  | $1600 |
| Phone     |   $12 |
| Pipe      |    $1 |

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |
| zebra stripes | are neat        |    $1 |
                
----

####HTML entities

&copy; &  &uml; &trade; &iexcl; &pound;
&amp; &lt; &gt; &yen; &euro; &reg; &plusmn; &para; &sect; &brvbar; &macr; &laquo; &middot; 

X&sup2; Y&sup3; &frac34; &frac14;  &times;  &divide;   &raquo;

18&ordm;C  &quot;  &apos;

##Escaping for Special Characters

\*literal asterisks\*

##Markdown extras

###GFM task list

- [x] GFM task list 1
- [x] GFM task list 2
- [ ] GFM task list 3
    - [ ] GFM task list 3-1
    - [ ] GFM task list 3-2
    - [ ] GFM task list 3-3
- [ ] GFM task list 4
    - [ ] GFM task list 4-1
    - [ ] GFM task list 4-2

###Emoji mixed :smiley:

> Blockquotes :star:

####GFM task lists & Emoji & fontAwesome icon emoji & editormd logo emoji :editormd-logo-5x:

- [x] :smiley: @mentions, :smiley: #refs, [links](), **formatting**, and <del>tags</del> supported :editormd-logo:;
- [x] list syntax required (any unordered or ordered list supported) :editormd-logo-3x:;
- [x] [ ] :smiley: this is a complete item :smiley:;
- [ ] []this is an incomplete item [test link](#) :fa-star: @pandao; 
- [ ] [ ]this is an incomplete item :fa-star: :fa-gear:;
    - [ ] :smiley: this is an incomplete item [test link](#) :fa-star: :fa-gear:;
    - [ ] :smiley: this is  :fa-star: :fa-gear: an incomplete item [test link](#);
            
###TeX(LaTeX)
   
$$E=mc^2$$

Inline $$E=mc^2$$ Inline，Inline $$E=mc^2$$ Inline。

$$\(\sqrt{3x-1}+(1+x)^2\)$$
                    
$$\sin(\alpha)^{\theta}=\sum_{i=0}^{n}(x^i + \cos(f))$$
                
###FlowChart

```flow
st=>start: Login
op=>operation: Login operation
cond=>condition: Successful Yes or No?
e=>end: To admin

st->op->cond
cond(yes)->e
cond(no)->op
```

###Sequence Diagram
                    
```seq
Andrew->China: Says Hello 
Note right of China: China thinks\nabout it 
China-->Andrew: How are you? 
Andrew->>China: I am good thanks!
```

###End
