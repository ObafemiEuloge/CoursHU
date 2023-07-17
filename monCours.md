## VueJS
VueJS est un framework JavaScript créé par Evan You un chinois de nationalité américaine. 

## Comment installer VueJS
Trois manières d'installer Vue:
En exportant ou en copiant le script fourni sur cdnjs.com

## Clarification conceptuelle. 

- Vue utilise des modèles (template) semblables au HTML mais usage aussi des Etats
-  Un état (en : state) est une variable qu'on utilise dans notre application (ou plus précisement dans le template !)
- Dans la méthode "createApp", nous avons l'option 'data()' qui retourne un objet contenant des états.
- En VueJS, tous les états sont réactifs.
- Moustache "```{{ }}```" : marqueur utilisé pour interpoller des états. Il peut aussi contenir tout script Javascript valide
  Interpoller : insérer ou introduire du texte qui n'existait au préalable

## Comment monter l'application ?
- Première méthode
```js
<script>
    const {createApp} = Vue ;

    createApp({
        data(){
            return {

            }
        }
    }).mount("#app")
</script>
``` 
- Deuxième méthode

```js
 <script type="module">
    import {createApp} from "https://cdnjs.cloudflare.com/ajax/libs/vue/3.3.4/vue.esm-browser.min.js";

    createApp({
        data(){
            return {

            }
        }
    }).mount("#app")
</script>

```
## Monter l'application dans la div ...
```js
createApp({
    // list des options

    data () {
        // les états

    }
}).mount("#app")
```

## Les options
Après avoir monté l'application, nous avons des options: 
  - le ```data()``` qui est un option contenant une fonction retournant des objets contenant des états.
  - le ```methods()``` qui est un option contenant des fonctions.
  - le ```computed()``` qui est un option pour gérer les propriétés calculées.
  - le ```watch()``` qui est un option pour observer un événement dans notre code.
  - le ```components()``` qui est un option pour ajouter des composants dans notre code.





## Les directives 
Une directive est un mot clé qui demande à VueJS d'exécuter une instruction donnée.
- ```v-bind```:attribut (il est remplacé par (:attribut))
Il est utilisé pour rendre dynamique tout attribut d'un élément.
- ```v-on```:event (il est remplacé par (```@event```))
Il est utilisé pour mettre un événement sur un élément.
Pour empêcher le rafraîchissement de la page, il faut mettre la méthode preventDefault. Pour raccourcir, VueJS nous permet de le mettre sur l'attribut 'click' en faisant : ```@event.prevent```
- ```v-model``` : synchronise la valeur du champ associé à l'Etat (state) correspondant. Plus précisement, il est utilisé pour la gestion des formulaires. Il en existe plusieurs cas d'usage.
- ```v-if, v-else-if, v-else```: Il est utilisé pour afficher ou cacher des éléments donnés remplissant une condition donnée.
- ```v-for``` permet d'afficher une liste d'éléments basée sur un tableau
  ```js
  <tr v-for="student of/in students">
      <td>{{student.element1}}</td>
      <td>{{student.element2}}</td>
  </tr>

  //////////////////////////

  <ul>
      <li v-for="s in/of students">{{student.element1}} {{student.element2}}</li>
  </ul>
  ```
## Les propriétés calculées
En Vue.js, il existe 2 principales options pour définir les fonctionnalités réactives : "computer" et "methods".

- 1- ```computed``` : utilisez ```computed``` lorsque vous avez besoin de calculer une propriété basée sur les valeurs existantes des propriétés réactives (states | états). Les propriétés calculées (en : computed properties) sont mises en cache et ne son recalculés que lorsque leurs dépendance changent.

  
**Exemple**
  ```js
  computed: {
        fullname () {
            return this.firstname + ' ' + this.lastName;
  },
  sortedList () {
            return this.list.sort()
  }
  }
  ```

- ```methods``` : utilisez ```methods``` lorsque vous souhaitez définir des méthodes réutilisables ou lorsque vous devez effectuer une action spécifique en réponse à un événement. Les méthodes ne sont pas mises en cache et recalculées chaque fois qu'elles sont appelées. Les appels HTTP ou exécuter des opérations complexes.
  
**Exemple**
```js
  methods: {
        handClick () {
            return this.counter++;
  },
  fetchDate () {
           //Effectuer une requête HTTP pour récupérer des données.
  }
  }
  ```

**NB**
  - Quand on veut modifier un état, on appelle la fonction responsable de la modification dans l'option ```methods```.
  - Quand on veut juste utiliser un état sans le modifier pour exécuter un calcul, il faut mettre la fonction responsable dans l'option ```computer```

```event.target : Pour cibler un élément sur lequel on agit.```

## Les hooks en Vue.JS
Chaque application Vue passe par une série d'étapes d'initialisation lorsqu'elle est créée. Par exemple, il faut :
- récupérer les états, fonctions et propriétés réactives de notre application;
- compiler le template;
- monter l'instance sur le DOM et
-  mettre à jour lorsqueles données changent.
En cours de route, des fonctions appelées ```hooks``` sont également exécutées, donnant la possibilité d'ajouter son propre code à des étapes spécifiques.

En Vue.JS, ```$refs``` est un objet qui récupère tous les éléments qui ont l'attribut ref.


### ANGULAR JS 
Quelques rappels:

**NPM** : (Node Package Manager) est un gestionnaire de paquets pour l'écosystème Node.js. Il est utilisé pour installer, mettre à jour et gérer les dépendances des projets Node.js. NPM permet aux développeurs de partager et de réutiliser des bibliothèques de code (appelées "paquets" ou "modules") développés par d'autres, ainsi que de publier leur propres paquets pour être utilisés par la communauté.
**Les packages JSON** sont des fichiers JSON comportant des objets qui ne sont pas des objets car les propriétés sont des chaines de caractères.
**Les versions des frameworks ou d'autres programmes** sont composés de trois versions : la version majeure, la version mineure et la version de patch
**Les chapeaux devant les versions en JSON** sont utilisés pour imposer la version que l'on veut.

# TYPESCRIPT
**TypeScript** est un langage de programmation open source développé par Microsoft. Il est conçu comme un sur-ensemble typé de JavaScript; ce qui signifie que tout code JavaScript valide est également du code TypeScript valide. Cependant, TypeScript offre des fonctionnalités supplémentaires qui améliorent le développement et la maintenance des applications JavaScript à grande échelle. 

**LES PRINCIPALES FONCTIONNALITES**
- **Typage statique** TypeScript permet de définir des types pour les variables, les paramètres de fonction, les valeurs de retour et d'autres éléments du code. Cela permet de détecter les erreurs de typage lors de la phase de développement plutôt qu'à l'exécution, ce qui peut améliorer la fiabilité du code.
- **Prise en charge des fonctionnalités ECMAScript récentes :**
- **Outils de développement avancés :**
- **Intégration avec JavaScript existant**
- **Ecosystème et prise en charge :**

**Création d'un fichier de configuration**
- Commande pour générer le fichier de configuration:
  ```git init``` puis valider
  
