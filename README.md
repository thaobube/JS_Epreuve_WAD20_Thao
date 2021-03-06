# Covid Killer

## Infos
Décembre 2020

JavaScript: Epreuve pratique en 7h

Répartition sur 100 pts
- épreuve théorique: 20 pts
- épreuve pratique:
  - qualité du code: 20 pts
  - javascript statique (génération HTML): 30 pts
  - javascript dynamique (interactions utilisateur): 30 pts

## Consignes
*Toutes sources d'information autorisées, mais pas de communication interpersonnelles pendant l'épreuve. L'aspect individuel/unique de la résolution des questions et du problème fait partie de la note.*

*Deux langues autorisées: français, anglais.*

*Copier/coller de code d'internet sanctionnés.*

*Pas le droit de toucher au HTML. Tout le site est généré depuis le JavaScript. Par contre on peut changer le SCSS.*

*Frameworks/Librairies de SPA non autorisés (Angular, React, Vue, Jquery...).*

*Les questions au formateur à propos des consignes ou liées aux problèmes techniques sont autorisées.*

- Envoyez votre travail aux formateurs (ltruchot) via un lien vers un repo github AVANT 16h45 le 18/12/2020
- Ne touchez plus jamais à ce repo après 16h45 sous peine de malus important

## Épreuve théorique sur 20pts

Pour chaque question, répondre avec **vos propres mots**, sans copier/coller, en au moins 2 phrases.
Les réponses peuvent être subjectives si il y a le signe **(s)** à la fin de la question.

Vous pouvez répondre à même ce document ou dans un fichier à part.

- Qu'est-ce que JavaScript vanilla ?
JavaScript vanilla is a term used to refer to the pure JavaScript (we can say regular/ordinary/plain Javascript). So, it means that is the Javascript WITHOUT additional libraries or frameworks (like jQuery, React, Angular...).

- Qu'est-ce qu'AJAX ?
AJAX is an acronym that stands for Asynchronous JavaScript and XML, its core function is to help to update the content of the website asynchronously - it means when the user change a small content of the web, he/she doesn't need to reload the entire page.

- Pourquoi JavaScript est parfois mal-aimé des devs ? **(s)**
From my personnal point of view, there are 2 weak points of the Javascript: 
1. Security :JavaScript is explicitly added to web pages and client browsers, and the JavaScript code is viewable to the user, others may use it for malicious purposes.
2. Lack of Debugging Facility:it is not as efficient as other editors like C# editor, it is difficult for the developer to detect the problem.

- Y a-t-il des types en JavaScript ? Si oui, lesquels ?
Yes, Javascript has many data types: numbers, string, object (includes array), booleans, null and undefined.

- Est-ce que SASS est un langage qui est interprété par les navigateurs ?
No. 
SASS in an acronym that stands for syntactically awesome style sheets - it is a CSS pre-processor scripting language. So it is necessary to compile the SASS into the CSS and the browser can use this CSS (only CSS is used by the browser, not SASS)

- Pourquoi peut-on dire que JavaScript est un langage "multi-paradigmes" ? **(s)**
"Maybe", because JavaScript has functional capabilities and OOP capabilities. 
However, the core building blocks of a functional program are variables and functions rather than objects and methods. In JavaScript functions are first class which are treated as a data type and can be used like any other value. 
Moreover, the characteristics/ main features of an Object-oriented programming (Abstraction, Inheritance, Polymorphism, Encapsulation) are not really clear in JS compared with other languages like C# or Java. 
So, in my opinion, JS is almost a functional programming. 

- En JS, une fonction peut-elle retourner une fonction ?
Yes, in JavaScript functions are first classes Functions. We can assign function to variable, pass function as argument, return function from another function.

- Est-ce que `alert` existe en Node.JS ?
I think the method window.alert() is used to show a popup message in the browser (a client-side). However, the Node.JS is the back-end (server side), so we cannot use it.

- Est-ce que `window.console.log === console.log` dans le navigateur ?
It depends on the Javascript environment. By defautl, in the browser JS environment, 'window' is the global object so it will be 'true'. However, in the NodeJS (there is no 'window') or other non-default browser environments which don't have 'window' => we can't access the 'window' => it will fail.

- Quel est votre aspect préféré de JavaScript ? **(s)**
In my opinion, there are 2 mains reasons make the JS is a good choice:
1. Simplicity - JavaScript's syntax is relatively simple to learn and to get started compared to other popular languages like C# or Java.
2. Popularity & Versatility - JavaScript is used everywhere on the browser side and nowadays on the server (Node JS). So, it is possible to develop an entire JavaScript app from front to back using only JavaScript. It is one of the most popular versatile scripting language.


## Épreuve pratique sur 80pts
Vous êtes codeuse/codeur JavaScript dans une clinique du centre-ville.
Vous développez un outil de pré-commande de vaccins dans les stocks publics de la ville, pour les responsables d'équipes médicales.
Votre site doit permettre à ces personnes de réserver différents types de vaccins parmi ceux en cours de développement.

Cloner et utiliser cette "seed" pour produire votre Single Page Application.

Le script `./script.js` est déjà lié à la page `./index.html` grâce à Parcel, de même que `style.scss` - il ne faut donc rien changer dans cette architecture (ne jamais toucher le HTML, garder le lien vers les styles dans le script).

- supprimer le dossier ".git" à la racine du clone
- créer votre propre repo/remote sur votre github et l'associer à votre clone du projet
- `npm install` installe les packages de la seed
- `npm start` lance la seed en mode "développement"
- add, commit, et push réguliers sont recommandés

### Modéliser les données
Produire un fichier data.js dans `./src`, qui exporte un Array d'objets avec les data suivantes:
#### Vaccin 1
Nom: BBIBP-CorV  
Inventeurs: Sinopharm  
Lieux de production: Chine  
Technologie: virus inactivé  
Quantité: 420  
Prix unitaire: 17$  
Approuvé: oui  
#### Vaccin 2
Nom: Sputnik V  
Inventeurs: Gamaleya  
Lieux de production: Russie, Inde  
Technologie: adenovirus  
Quantité: 130  
Prix unitaire: 12$  
Approuvé: non  
#### Vaccin 3
Nom: AZD1222  
Inventeurs: AstraZeneca, University of Oxford  
Lieux de production: Royaume Unis, Brésil, Inde  
Technologie: adenovirus  
Quantité: 5028  
Prix unitaire: 1.78$  
Approuvé: non  
#### Vaccin 4
Nom: Tozinameran  
Inventeurs: BioNTech, Pfizer, Fosun Pharma  
Lieux de production: Allemagne, USA  
Technologie: ARN messager  
Quantité: 980  
Prix unitaire: 14$  
Approuvé: oui  
#### Vaccin 5
Nom: mRNA-1273  
Inventeurs: Moderna, NIAID, BARDA  
Lieux de production: USA  
Technologie: ARN messager  
Quantité: 240  
Prix unitaire: 28$  
Approuvé: non  
#### Vaccin 6
Nom: Ad26.COV2.S  
Inventeurs: Johnson & Johnson, BIDMC  
Lieux de production: USA, Amérique du Sud, Ukraine, Afrique du Sud  
Technologie: adenovirus  
Quantité: 110  
Prix unitaire: 31$  
Approuvé: non  

### Transformer les données en éléments du DOM
Les éléments suivants sont créés dans la div `#app` via JavaScript:
- un `h1` avec le nom du site
- un élément `header`, présentant 
  - un bouton pour classer les vaccins par prix
  - un bouton pour cacher les vaccins "non approuvés" 
- un élément HTML `main`. 
  - c'est le catalogue montrant tous les vaccins sous forme de "cartes", côte à côte ou à la ligne
  - chaque carte présente 
    - une image de vaccin (présente dans le dossier "static")
    - toutes les infos disponibles pour ce vaccin
    - un "input" de "quantité" et un bouton "réserver" à côté
- un élément `footer` résume la commande en cours (vide au début), et contient un bouton "passer la commande"

### Manipulation du DOM et interaction utilisateur
- Lorsque l'utilisateur clique sur "cacher les vaccins non approuvés" les vaccins non approuvés sont cachés. On peut désormais les re-montrer grâce au même bouton
- Lorsqu'un utilisateur clique sur le bouton "réserver" d'une carte de vaccin
  - le vaccin apparaît dans la commande du `footer`, avec la quantité demandée (ex: Tozinameran x3)
  - l'input de quantité disparaît de la carte
  - le bouton "réserver" de ce vaccin devient `disabled`
- Lorsqu'un utilisateur clique sur "passer la commande" dans le `footer`:
  - la page se vide entièrement
  - un message indique "La commande a bien été enregistrée..."

### Bonus (pas compté dans les points - peut réhausser la note finale):
- sur cet écran final, un bouton "Annuler la commande" permet de  recharger automatiquement la page dans son état initial
- le bouton "classer les vaccins par prix" fonctionne, et réordonne les cartes du vaccin le moins cher au plus cher
- Améliorer l'affichage de votre site grâce aux SCSS
- L'action de passer commande lorsqu'il n'y a pas de commande est impossible
- Un bouton dans le `footer` permet d'annuler toute la réservation d'un coup
- Il est impossible de commander plus de vaccins que les quantités existantes
- Le calcul exact des prix, vaccins par vaccins, et le total du prix final sont ajoutés dans le footer
- Ils sont aussi rappelés dans la page suivante
