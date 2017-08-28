# Structure des fichiers CSS

## Un composant par fichier
Placez la définition de chaque composant dans son propre fichier.

  ```scss
  /* css/components/search-form.scss */
  .search-form {
    > .button { /* ... */ }
    > .field { /* ... */ }
    > .label { /* ... */ }

    // variants
    &.-small { /* ... */ }
    &.-wide { /* ... */ }
  }
  ```

## Utilisez les correspondances glob
C'est possible avec sass-rails and stylus. Cela rend l'inclusion plus facile.

  ```scss
  @import 'components/*';
  ```

## N'imbriquez pas trop
N'utilisez pas plus d'un niveau d'imbrication. En effet, il est très facile de se perdre avec trop de niveaux d'imbrications.

  ```scss
  /* ✗ À éviter : 3 niveaux d'imbrications */
  .image-frame {
    > .description {
      /* ... */

      > .icon {
        /* ... */
      }
    }
  }

  /* ✓ La même chose en mieux : 2 niveaux seulement */
  .image-frame {
    > .description { /* ... */ }
    > .description > .icon { /* ... */ }
  }
  ```
