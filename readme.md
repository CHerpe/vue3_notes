# Formation Vue 3

## API d'options VS API composition

Composition = nouveauté de vue 3
- une clé setup dans laquelle on met tous les éléments de notre composant
- On integre setup directement dans la balise script et Vue fera le travail seul sans qu'on ai besoin d'exporter un objet
- Meilleures compréhension, lecture, performances

## Directives

- **v-text** : permet de passer une variable en tant que texte à une balise html (équivaux à {{machin}}) - peu utilisé car doit être seul dans la balise cible
- **v-html** : permet de passer un contenu html avec une balise (ne fonctionnera pas avec la synthaxe au dessus car converti en string)
- **v-bind** : permet de passer une variable à un attribut HTML (classe, id, ect) - ex : `v-bind:class="variable"`
- - Cette directive est si utilisée qu'elle a une forme simpliée : `:class="variable"`
- - On peut lui passer une fonction qui retourne une valeur aussi

### gestion d'évènements

- **v-on** : ex: `v-on:click="myfunction`
- - Comme le v-bind, cette directive étant très utilisée elle a une forme abbrégée : `@click="myfunction`

On peut ajouter des **modifiers** (par ex pour empècher la propagation aux parents ou un rafraichissement au submit).  
Quelques exemples utiles :
- - **Stop** : `@click.stop="myfunction"` 
- - **Prevent** : `@submit.prevent="myfunction"`
- - **Escape** : `@keyup.escape="myfunction"`
- - **Enter** : `@keyup.enter="myfunction"`

## Lexique

- **SPA** : Single page application 
- **SFC** : Single file component
- **Directives** : v-if, v-bind, ect... = options que vue reconnait
