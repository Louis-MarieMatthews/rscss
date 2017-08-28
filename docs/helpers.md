# Assistants

Certaines classes peuvent être utilisées de manière générale uniquement pour remplacer certaines propriétés. Placez-les dans un fichier à part et préfixez-les avec un tiret bas. Typiquement, ce sont ces classes-là qui utilisent le mot-clé *!important*. Ces classes-là ne doivent être utilisées que *très, très* rarement.

```css
._unmargin { margin: 0 !important; }
._center { text-align: center !important; }
._pull-left { float: left !important; }
._pull-right { float: right !important; }
```

## Comment appeler ses assistants
Préfixez le nom des classes avec un tiret bas. De cette manière ils sont faciles à distinguer des variantes.
Les tirets bas ne sont pas très beaux. C'est volontaire : c'est un moyen d'essayer de décourager leur utilisation trop fréquente.

  ```html
  <div class='order-graphs -slim _unmargin'>
  </div>
  ```

## Comment ranger ses assistants
Placez les définitions des classes « assistants » dans un fichier `helpers`. Même s'il est possible de séparer les définitions dans plusieurs fichiers, il est préférable de garder le nombre d'assistants aussi bas que possible.
