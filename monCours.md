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
- v-bind:attribut (il est remplacé par (:attribut))
Il est utilisé pour rendre dynamique tout attribut d'un élément.
- v-on:event (il est remplacé par (@event))
Il est utilisé pour mettre un événement sur un élément.
Pour empêcher le rafraîchissement de la page, il faut mettre la méthode preventDefault. Pour raccourcir, VueJS nous permet de le mettre sur l'attribut 'click' en faisant : ```@event.prevent```

## Les options
Nous avons maintenant deux options:
- data() et methods()
