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
```
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

```
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
```
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
  ```
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

```event.target : Pour cibler un élément sur lequel on agit```
