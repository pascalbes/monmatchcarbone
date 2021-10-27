# Contribuer à Mon Match Carbone

Bienvenue 👋 ! 

Ce dépôt contient un modèle d'empreinte carbone sportive annuelle, écrit en YAML. Pas de panique, on vous explique plus bas ce que ça veut dire et comment le modifier.

Ce modèle pose des questions sur les aspects de la vie sportive d'un individu qui émettent le plus de gaz à effet de serre (GES) mesuré en CO2e. L'objectif n'est pas d'en faire une comptabilité parfaite, mais la plus représentative en posant un nombre de question qui reste acceptable pour tous.

## 💾 Les modèles carbone

Peu importe la qualité des contributions, nous accueillons tout : un brouillon de calcul en français peut suffire... tant que les modèles carbone proposés *reposent sur données bien sourcées*. 


Par exemple, pour créer un modèle pour la trottinette électrique partagée, il faudrait idéalement réaliser une analyse de cycle de vie complète qui comprendrait : 

- le matériel lui-meme (batterie, trottinette en métal, composants en plastique) et sa durée de vie estimée
- l'entretien, le recyclage, l'acheminement depuis la Chine
- l'électricité et le geste de recharge, parfois par camion, parfois en utilisant les trottinettes elles-memes ! 
- ...

Evidemment, les modèles ne seront pas publiés directement en production, l'équipe Datagir et ses partenaires experts se saisira des propositions pour les enrichir et finalement les valider :)


A noter : tout modèle publié ici est publié sous la license MIT. Les modèles sont donc réutilisables librement par tout un chacun :free:

## 🔣 Le langage d'écriture des modèles

Le langage est décrit et documenté sur https://publi.codes. Il est développé par l'Etat dans le cadre du projet [mon-entreprise](https://github.com/betagouv/mon-entreprise). 

N'hésitez pas à poser des questions sur le langage ou la contribution en créant une nouvelle *issue*, nous serons ravi d'y répondre.


## 🏗️ En pratique

### Avant tout : vérifier que votre question n'est pas déjà posée

Il y a de grandes chances que ce soit déjà le cas : direction [l'onglet *issues*](https://github.com/pascalbes/monmatchcarbone/issues), et son moteur de recherche. La pile est déjà bien remplie !

### Si vous n'avez que ⌛ 2 minutes pour faire une remarque

Si vous avez un compte Github, [créez simplement une issue](https://github.com/pascalbes/monmatchcarbone/issues/new) qui parle de votre idée ou correction et qui contient le calcul ou les interrogations en français.

Sinon, écrivez-nous sur [notre formulaire de retour](https://monmatchcarbone.fr/contribuer).

### Si vous voulez participer à l'amélioration du modèle [⌛ 20 minutes]

Tous les textes, par exemple le texte d'une question ou le texte d'une suggestion de saisie, sont stockés dans une [collection de fichiers texte](https://github.com/pascalbes/monmatchcarbone/tree/master/data), classés par grande catégorie. C'est un langage très accessible que vous pouvez modifier directement. Pour cela il vous faut un compte Github, qui peut se créer gratuitement en 2-3 minutes.
 
Puis suivez ces étapes : 

- rendez-vous sur l'un des modèles classés par grande catégorie [ici](https://github.com/pascalbes/monmatchcarbone/tree/master/data). Sélectionnez-en une. Cliquez sur l'icône ✏ en haut à droite, vous êtes en mode édition !
- cliquez n'importe où dans le contenu du fichier, puis tapez Ctrl-F (pour lancer une recherche), cherchez le texte à modifier (par exemple "Quel est l'age de votre smartphone"), modifiez directement le texte sur cette page (corriger "age" en "âge")
- puis cliquez sur le bouton vert 🟩 `Propose file change`. Sur la page qui s'affiche intitulée "Comparing changes", cliquez sur le bouton vert `Create pull request`
- 🎉 Bravo, l'équipe verra votre contribution et la validera si elle est parfaite. Sinon, on en discutera ensemble 🙂.

- Ce n'est pas tout ! Vous pouvez maintenant tester le site comme si vos changements avaient été validés 😎 : une fois votre pull request (PR) créée, allez sur https://monmatchcarbone.fr/, ajoutez à la fin de l'adresse dans votre navigateur `?PR=X` où X est le numéro de votre pull request (juste après le # dans le titre de votre PR).

### Si vous voulez construire vous-même de nouveaux modèles [⌛ 1 heure ou 2]

Il vous suffit de suivre les étapes ci-dessus, puis d'ajouter plusieurs nouvelles règles de calcul et questions, en s'inspirant de l'existant et en suivant la documentation du langage [publicodes](https://publi.codes). 

> Il faut comprendre publicodes comme une sorte de tableur mais dans un fichier texte. Plutôt que des cases graphiques A1, B13, on nomme des variables, qui sont soit des *questions* à l'utilisateur, soit des *formules de calcul* qui combinent les réponses à ces questions pour calculer de nouveaux chiffres intéressants.

Même si vous avez produit du *pseudo code*, c'est à dire un semblant d'algorithme explicite mais qui ne compile pas, c'est déjà super 🦾. Cela dit, c'est encore mieux si vous pouvez le voir en action vous-même sur une branche de déploiement (voir le dernier item de la section précédente).

Pour bien comprendre comment le langage marche, et tester vous-même vos propres formules, nous avons mis en place un *bac à sable* : une page Web avec un éditeur de texte dans lequel vous pouvez saisir vos formules et vérifier qu'elles fonctionnent. [Rendez-vous ici ⛱️](https://publi.codes/studio/). 

Par défaut, vous aurez une formule toute bête qui somme des carottes et des champignons, que vous pouvez modifier pour multiplier des facteurs d'émission par des distance par exemple.

![](https://i.imgur.com/VhqpVuc.png)

Vous pouvez par exemple transformer cet exemple de modèle pour que le prix de l'avocat soit une question avec une valeur par défaut : 

```yaml 

prix . avocat: 
  question: Quel prix pour tes avocats gros ? 
  par défaut: 2€/avocat
  
``` 

> 💡 Pour faciliter la relecture par les autres contributeurs et l'équipe, la discussion et les itérations, mieux vaut faire une PR (*Pull request*, proposition de changements) par sujet. Par exemple, faite une PR pour votre proposition "ajouter le curling au simulateur".