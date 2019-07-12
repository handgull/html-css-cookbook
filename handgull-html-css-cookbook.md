## HTML & CSS cookbook by hangull
Table of Contents
---
---
- [Introduction](#Introduction)
- [HTML](#HTML)
  - [Formatting](#Formatting)
- [CSS](#CSS)
# Introduction
- HTML scheletro, struttura
- CSS style, rifinitura

<img alt="AwesomeCV" src="./meme.png" width="200px" height="200px">

# HTML
```html
<!DOCTYPE html><!--Specifica il tipo di documento, primo TAG da includere nel documento-->
<html>
  <head>
    <title>Document title</title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0"><!--user's visible area of the page, ottimo meta per gli smartphone-->
    <link type="text/css" rel="stylesheet" href="path">
    <style><!--regole CSS direttamente nel documento-->
      h1 {
        color: #123456
      }
    </style>
  </head><!--metatag e.g. charset, viewport, ... + descrizione, titolo, fogli di stile, script, font, logiche di zoom...-->
  <body>
    <div style="display: none">Inline styling con il CSS</div>
    <img src="path" alt="text"><!--il testo nell'attributo alt è visto se l'immagine non carica-->
  </body>
</html><!--TAG che include tutto il resto del documento, HEAD e BODY-->
```
## Formatting
TAG di formattazione del testo
> Una delle prime cose da notare nella formattazione del testo è che il testo non va a capo seguendo le line break nel codice, e che più spazi consecutivi risulteranno come uno soltanto.
```html
<h1></h1><!--Per i titoli, da 1 a 6-->
<!--NOTA: non è come span, di default ha display: block-->
<p>text</p><!--paragrafo-->
<b>grassetto</b><!--dico al browser semplicemente di mettere il grassetto-->
<i>corsivo</i>
<strong>grassetto</strong><!--dico al browser che è un testo importante-->
<!--La differenza si vede negli screen reader, per i ciechi-->
```
# CSS
Cascading Style Sheets
```css
/*Regole*/
div { /*a chi devo applicarla? in questo caso ad ogni tag div*/
  width: 800px / 2em / 0.4rem / calc(100% - 8px);
  margin: auto;
}

/*Formatting*/
p {
  font-size: 25px;
  line-height: 25px; /*altezza della riga*/
  text-align: left / right / center / justify; /*justify è come un align left + right
}
```
> se ho le stesse regole, con la stessa priorità verrà applicata la regola scritta dopo o del file caricato dopo