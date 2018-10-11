---
description: "Pra manter o seu CSS e o seu JavaScript organizados \U0001F42C"
---

# Acessando a DOM no JavaScript

## Classes específicas para uso em JavaScript

**Não utilize a mesma classe no seu CSS e no seu JavaScript.** Isso pode causar perda de tempo e confusão caso seja necessário refatoramento de código.

Para evitar que isso aconteça, inclua `.js-` no início de todas as classes específicas para JavaScript.

### Exemplos

**Certo ✅**

```markup
<button class="btn btn-blue js-clique-para-ativar">Clique para ativar!</button>
```

```css
.btn-blue {
  color: $white;
  background-color: $blue;
}

// .js-clique-para-ativar nunca é incluída no CSS
```

**Errado ❌**

```markup
<button class="btn btn-blue js-clique-para-ativar">Clique para ativar!</button>
```

```css
.btn-blue {
  color: $white;
  background-color: $blue;
}

.js-clique-para-ativar {
  background-color: $red;
}
```

## Utilizando atributos `data`

Uma forma de acessar informações dos elementos da DOM pelo JavaScript é utilizando os atributos `data`, fazendo com que o seu código fique mais limpo e organizado. Veja o exemplo abaixo.

```markup
<ul>
    <li data-wins="10" data-noms="31" onclick="mostraGrammys(this)">Taylor</li>
    <li data-wins="0" data-noms="13" onclick="mostraGrammys(this)">Katy</li>
    <li data-wins="1" data-noms="8" onclick="mostraGrammys(this)">Britney</li>
</ul>
```

E então, você pode acessar esses valores da seguinte forma no JavaScript:

```javascript
function mostraGrammys(cantora) {
    var grammyWins = cantora.getAttribute(wins);
    var grammyNominations = cantora.getAttribute(noms);
    
    // use as variáveis como quiser
}
```

E dessa forma no CSS:

```css
li[data-wins='0'] {
    color: red;
    font-weight: bolder;
}
```

{% hint style="info" %}
**LEITURA EXTRA**

* [Utilizando data attributes](https://developer.mozilla.org/pt-BR/docs/Web/Guide/HTML/Using_data_attributes)
* [How to use HTML5 data attributes](https://www.sitepoint.com/use-html5-data-attributes/)
{% endhint %}

