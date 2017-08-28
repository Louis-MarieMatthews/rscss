# Les agencements

![](images/layouts.png)

## Éviter les propriétés de positionnement
Les composants doivent être définis de telle sorte à pouvoir être ré-utilisés dans n'importe quel contexte. Évitez de définer ces propriétés dans la définition des composants :

  * Positionnement (`position`, `top`, `left`, `right`, `bottom`)
  * Flottants (`float`, `clear`)
  * Marges (`margin`)
  * Dimensions (`width`, `height`) *

## Au sujet des dimensions fixes

Il ne faut pas appliquer cette règle à certains éléments qui nécessitent des dimensions précises comme les avatars ou les logos. Ils constituent une exception à la règle.

## Définir le positionnement depuis les parents

Si vous devez définir une de ces propriétés (taille, positionnement…), faites-le depuis le composant parent.
Dans l'exemple plus-bas, les propriétés `width` et `float` sont définies depuis le composant parent, et non depuis le composant `.article-card`.

  ```css
  .article-list {
    & {
      @include clearfix;
    }

    > .article-card {
      width: 33.3%;
      float: left;
    }
  }

  .article-card {
    & { /* ... */ }
    > .image { /* ... */ }
    > .title { /* ... */ }
    > .category { /* ... */ }
  }
  ```

Comment ajouter des marges sans passer par un agencement ? Utilisez des assistants.
[Continuer →](helpers.md)
<!-- {p:.pull-box} -->
