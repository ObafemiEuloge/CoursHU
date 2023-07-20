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
  ```tsc init``` puis valider
  Un fichier de configuration est généré où il faut ajouter le chemin du fichier typescript et celui javascript qu'on veut générer.
- **Les types de variables en TypeScript**
  - ```any``` : représente un type non spécifique ou dynamique.
  - ```unknown```: représente un élément dont on ne connaît pas le type.
  - ```enum``` : rerpésente un ensemble de valeurs nommées (une alternative aux constantes).
  - ```tuple``` :représente un tableau avec un nombre fixe d'éléments fixe d'éléments de types différents.
  - ```object``` : représente les objets. On crée des ```alias de type``` pour représenter les types d'objets. On peut également créer des alias de type pour les autres variables. Il existe aussi les ```interfaces``` pour écrire les types pour les objets. Et ce n'est relatif que pour les objets. 
- **Les unions de types**
  Les unions de types notés ``` | ``` sont utilisées pour donner plusieurs types à une variable donnée. 
  ```js
    let x : number | string | boolean | object ;
    type Rectangle = {
        x : number,
        y : number
    };

     type Circle = {
        cx : number,
        cy : number,
        cr : number,
    }

    let shape : Rectangle | Circle = {
        x : value,
        y : value,
    }

    type Shape = Rectangle | Circle;

    let shape2 : Shape {
        cx : value,
        cy : value,
        cr : value,
    }
  ```
- Rendre une variable optionelle
```js
    type User = {
      readonly id? : number, // id est optionnel (?). Il est en lecture seule (readonly).
      fname: string,
      lname: string,
      age? : number, //age est optionel 
    }

    let u : User = {
      id : 1,
      fname : "John",
      lname : "Doe",
      age : 98 
    }
```

- Les classes en TypeScript

De nouveaux mots clés s'ajoutent en typeScript

```public```: (défaut) permet l'accès à la propriété de partout
```private``` : ne permet l'accès que dans la classe
```protected```: permet l'accès dans la classe et dans les enfants de la classe.

```js
  class Person {
    constructor(
        private fname : string,
        private lname: string,
    ){
        this.fname = fname;
        this.lname = lname;
    }

    getfname(): string {
        return this.fname;
    }
}

const p1 = new Person("John", "Doe");
console.log(p1.getfname());
console.log(p1);
// Héritage en TypeScript
class Programer extends Person {
    constructor(
        fname: string,
        lname: string,
        private languages: string[]
    ) {
        super(fname, lname);
    }
}
```

- **Les classes abstraites.**
  **Une classe abstraite** est un concept de la POO. C'est une classe qui ne peut être instanciée directement, c'est-à-dire qu'on ne peut pas créer d'objets directement à partir de cette classe. Au lieu de cela, elle est conçue pour être utilisée comme une classe à partir de laquelle les autres peuvent hériter.

  ```js
  abstract class Forme {
    afficher() {
        console.log("Je suis une forme géométrique");
    }
  }


  class Rectangle extends Forme {
    constructor(
        public longueur: number,
        public largeur: number
    ) {
        super();
    }

    calculerSurface(): number {
        return this.longueur * this.largeur;
    }

    
  }

  class Circle extends Forme {
    constructor(
        public rayon: number
    ) {
        super();
    }

    calculerSurface(): number {
        return 2 * Math.PI * this.rayon ** 2;
    }

  }

  class Triangle extends Forme {
    constructor(
        public base: number,
        public hauteur: number
    ) {
        super();
    }

    calculerSurface(): number {
        return 0.5 * this.base * this.hauteur;
    }

  }


  let rect = new Rectangle(5, 2);
  rect.afficher();
  console.log(rect.calculerSurface());
  ```

  - Impossible à instancier
  - Méthodes abstraites : une classe abstraite peut déclarer des méthodes abstraites, c'est-à-dire des méthodes qui n'ont pas des corps (pas de code d'implémentation). Ces méthodes sont uniquement déclarées avec leur signature (nom et paramètres). La responsabilité d'implémenter ces méthodes incombe aux classes qui héritent de la classe abstraite.
  - Héritage : Les classes qui héritent d'une classe abstraite (appelées classes dérivées, sous-classes, enfant) doivent fournir une implémentation pour toutes les méthodes abstraites de la classe abstraite.
 
- **CLASSES QUI IMPLEMENTE UNE INTERFACE**
  En TypeScript, lorsqu'une classe implémente une interface, elle doit fournir implémentation pour toutes les propriétés et méthodes déclarées dans l'interface.
  __Exemple__ :

  ```js

      interface MonInterface {
        propriété : type;
        méthode(): returnType;
      }
      class MaClasse implements MonInterface {
        propriété : type;
        constructuor(p: tpe){
          this.propriété = p;
        }

        méthode(){
          return returnValue;
        }
      }


**NB :** Une classe qui a une méthode abstraite doit nécessairement être abstraite.


  ```js
    enum Delivery {
      DoorToDoor = "doortodoor",
      AirDelivery = "airdelivery",
      Special = "special",
    }

    let x = Delivery.special : x est de type Delivery.
  ```

**JSON : JavaScript Object Notation**

- **LES DECORATEURS EN TYPESCRIPT**
    - Les descripteurs en JavaScript
      Ils permettent d'accéder et/ou modifier les propriétés par défaut des éléments d'un objet.
      Nous distinguons trois propriétés par défaut :
        - ```writable``` : Il spécifie si la propriété peut être modifiée après sa création. Si ```writable``` est "false", la propriété en considérée comme en lecture seule.
        -  ```enumerable``` : Il indique si la propriété sera listée lors du parcours de l'objet à l'aide de la boucle ```for...in``` 
        -  ```configurable``` : Il permet d'autoriser ou d'empêcher l'édition des éléments d'un objet.

__Les décorateurs__ 

**NB :** Le décorateur ne s'applique que sur une classe ou dans une classe.

  - Cinq (05) endroits où on peut mettre les décorateurs.
      - classe (décorateur de classe)
      - propriété (décorateur de propriété)
      - méthode (décorateur de méthode)
      - accesseur (getter et setter) (décorateur d'accesseur)
      - paramètres d'une méthode (décorateur de paramètres de méthodes)
