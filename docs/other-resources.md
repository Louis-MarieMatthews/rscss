# Autres ressources

 * [ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss#49) (« Inverted Triangle CSS ») est une autre méthode qui se combine très bien avec RSCSS.
 * [rsjs](http://ricostacruz.com/rsjs/) (« Reasonable Standard of JavaScript Structure ») est un document en cours de redaction pour structurer son code JavaScript dans le cas des sites simples.

Autres méthodes
---------------

### BEM
[BEM] est bien, mais certaines personnes peuvent être gênés par sa syntaxe quelque peu particulière. RSCSS suit la plupart des conventions BEM. Sa principale différence est sa syntaxe qui est un peu différente.

```html
<!-- BEM -->
<form class='site-search site-search--full'>
  <input  class='site-search__field' type='text'>
  <button class='site-search__button'></button>
</form>
```

```html
<!-- rscss -->
<form class='site-search -full'>
  <input  class='field' type='text'>
  <button class='button'></button>
</form>
```

## Terminologies

Les concepts décrits pour cette méthode sont similaires à d'autres concepts provenant des autres méthodes.
Voici le tableau des correspondances (en anglais) :

| RSCSS     | BEM      | SMACSS        |
| ---       | ---      | ---           |
| Component | Block    | Module        |
| Element   | Element  | Sub-Component |
| Layout    | ?        | Layout        |
| Variant   | Modifier | Sub-Module & State |

[BEM]: http://bem.info/
[Smacss]: https://smacss.com/
