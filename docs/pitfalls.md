# Erreurs fréquentes

## Dépasser à travers les composants imbriqués
Soyez prudents avec les composants imbriqués. Il est possible qu'ils contiennent des éléments portant le même nom que d'autres éléments en dehors du composant.

```html
<article class='article-link'>
 <div class='vote-box'>
    <button class='up'></button>
    <button class='down'></button>
    <span class='count'>4</span>
  </div>

  <h3 class='title'>Titre de l'article</h3>
  <p class='count'>3 votes</p>
</article>
```

```scss
.article-link {
  > .title { /* ... */ }
  > .count { /* ... (!!!) */ }
}

.vote-box {
  > .up { /* ... */ }
  > .down { /* ... */ }
  > .count { /* ... */ }
}
```

Dans ce cas-là, si `.article-link > .count` n'utilisait pas le sélecteur direct `>`, il s'appliquerait aussi à l'élément `.vote-box .count`. Cela est une des raisons pour laquelle le sélecteur direct est privilégié.
