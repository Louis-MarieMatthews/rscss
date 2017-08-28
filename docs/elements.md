# Éléments

Les éléments sont des « choses » au sein de vos composants.

![Un composant peut contenir des éléments. Ici, un formulaire de recherche (le composant) contient un champ et un bouton (les éléments).](images/component-elements.png)

## Comment appeler ses éléments
Chaque composant peut avoir des éléments. Leur classes ne doivent être écrites qu'en **un seul mot**.

```scss
.search-form {
  > .field { /* ... */ }
  > .action { /* ... */ }
}
```

## Sélectionneurs d'éléments
Essayez dans la mesure du possible de n'utiliser que le sélecteur direct `>`.
Non seulement cela permet d'éviter de sélectionner involontairement des éléments imbriqués un niveau plus bas, mais ce sélecteur est également plus efficace.

```scss
.article-card {
  .title     { /* acceptable */ }
  > .author  { /* ✓ mieux */ }
}
```

## S'il faut plusieurs mots
Pour les éléments qui nécessitent vraiment plusieurs mots, fusionnez-les en un seul mot ou utilisez des tirets bas.

```scss
.profile-box {
  > .firstname { /* ... */ }
  > .lastname { /* ... */ }
  > .avatar { /* ... */ }
}
```

## Éviter d'utiliser les sélectionneurs de balises HTML directement
Dans la mesure du possible, utilisez des classes en permanence. Les sélectionneurs d'éléments HTML peuvent être utilisés, mais ils sont légèrement moins performants et peuvent être moins descriptifs.

```scss
.article-card {
  > h3    { /* ✗ à éviter */ }
  > .name { /* ✓ mieux */ }
}
```

Les éléments ne sont pas toujours identiques. Ils ont alors des variantes.
[Continuer →](variants.md)
<!-- {p:.pull-box} -->
