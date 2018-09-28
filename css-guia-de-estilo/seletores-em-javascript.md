---
description: "Pra manter o seu CSS e o seu JavaScript organizados \U0001F42C"
---

# Seletores em JavaScript

## Classes específicas para uso em JavaScript

Não utilize a mesma classe no seu CSS e no seu JavaScript. Isso pode causar perda de tempo e confusão caso seja necessário refatoramento de código.

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

