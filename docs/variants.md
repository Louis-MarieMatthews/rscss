# Variantes

Les composants comme les éléments peuvent avoir des variantes.

![Le composant .search-form (formulaire de recherche) a une variante, .search-form.-prefixed, et une autre, .search-form.-compact.](images/component-modifiers.png)

<br>

## Comment appeler ses variantes
Le nom des classes de variantes doit commencer par un tiret (`-`).

  ```scss
  .like-button {
    &.-wide { /* ... */ }
    &.-short { /* ... */ }
    &.-disabled { /* ... */ }
  }
  ```

## Variantes d'élément
Les éléments aussi peuvent avoir des variantes.

  ```scss
  .shopping-card {
    > .title { /* ... */ }
    > .title.-small { /* ... */ }
  }
  ```

## À propos du tiret au début
Le tiret est ce qu'il y a de mieux pour préfixer ses variantes.

  * Cela empêche toute ambiguïté avec d'autres éléments.
  * Une classe en CSS ne peut commencer que par une lettre, `_` ou bien `-`.
  * Les tirets sont parfois plus faciles à atteindre sur le clavier que les tirets bas.
  * Cela ressemble légèrement à la syntaxe des commandes UNIX (`gcc -O2 -Wall -emit-last`).

Comment travailler avec des éléments complexes ? Il faut les imbriquer.
[Continuer →](nested-components.md)
<!-- {p:.pull-box} -->
