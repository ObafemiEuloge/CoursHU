## VueJS
VueJS est un framework JavaScript créé par Evan You un chinois de nationalité américaine. 

## Comment installer VueJS
Trois manières d'installer Vue:
En exportant ou en copiant le script fourni sur cdnjs.com

## Clarification conceptuelle.

- Vue utilise des modèles (template) semblables au HTML mais usage aussi des Etats
-  Un état (en : state) est une variable qu'on utilise dans notre application (ou plus précisement dans le template !)
- Dans la méthode "createApp", nous avons l'option 'data()' qui retourne un objet contenant des états.

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


## Les directives 
Une directive est un mot clé qui demande à VueJS d'exécuter une instruction donnée.
- v-bind
Il est utilisé pour rendre dynamique tout attribut d'un élément
