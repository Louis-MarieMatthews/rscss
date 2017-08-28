# Composants imbriqués

![Le composant « .article-link » (lien d'article) contient un autre composant, « .vote-box » (boîte à votes).](images/component-nesting.png)

```html
<div class='article-link'>
  <div class='vote-box'>
    ...
  </div>
  <h3 class='title'>...</h3>
  <p class='meta'>...</p>
</div>
```

Il est parfois nécessaire d'imbriquer certains éléments. Voici quelques consignes à ce sujet.

## Variantes
Il peut être nécessaire de changer légèrement l'aspect d'un composant quand celui-ci est imbriqué dans un autre. Évitez d'atteindre le composant imbriqué depuis le composant parent.

```scss
.article-header {
  > .vote-box > .up { /* ✗ à éviter */ }
}
```

À l'inverse, définissez une variante que vous spécifiez depuis le code HTML.

```html
<div class='article-header'>
  <div class='vote-box -highlight'>
    ...
  </div>
  ...
</div>
```

```scss
.vote-box {
  &.-highlight > .up { /* ... */ }
}
```

## Simplifier les composants imbriqués
Parfois, quand vous imbriquez des composants, le code HTML peut ne paraître pas très propre.

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='search-button -red -large'></button>
</div>
```

Vous pouvez alors simplifier cela avec la directive `@extend` :

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='submit'></button>
</div>
```

```scss
.search-form {
  > .submit {
    @extend .search-button;
    @extend .search-button.-red;
    @extend .search-button.-large;
  }
}
```

Qu'en est t-il des éléments qui se répètent comme les listes par exemple ? Découvrez les agencements.
[Continuer →](layouts.md)
<!-- {p:.pull-box} -->
