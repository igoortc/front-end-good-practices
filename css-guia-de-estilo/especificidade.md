---
description: "Uma pequena discussão sobre o assunto \U0001F485\U0001F3FC"
---

# Especificidade

## Antes de começar...

Trabalhar com seletores CSS e especificidade é algo que assombra todo mundo de vez em ~~sempre~~ quando. Então, antes de continuar, recomendamos que você complete o joguinho **CSS Diner** para treinar um tanto bom e aprender sobre seletores de forma simples e divertida. Além disso, também seria legal dar uma lida no artigo que colocamos na seção abaixo. 

{% hint style="warning" %}
**Leitura importante**

* [CSS Diner](https://flukeout.github.io/)
* [Hacks for dealing with specificity](https://csswizardry.com/2014/07/hacks-for-dealing-with-specificity/)
{% endhint %}

## Instruções

* Evite utilizar IDs como seletores, mas se não tiver jeito MESMO, use-os, mas não inclua mais que um na sua regra. Utilizar IDs como seletores pode dificultar a estilização devido à alta especificidade e, além disso, não há quase nenhuma diferença de performance em relação às classes.
* Se quiser incluir propriedades novas para um elemento já existente, utilize classes específicas \(leia mais sobre na [próxima página](https://softbox.gitbook.io/front-end/css-guia-de-estilo/oocss-e-bem)\). Exemplo: `.botao.botao-azul` ao invés de `.botao.azul`.
* Nunca crie regras contendo apenas as classes `disabled`, `mousedown`, `danger`, `selected` e `active`. Exemplo: `li.active` ao invés de apenas `.active`.
* Evite utilizar elementos \(`span`, `div`, `p`, etc\) como seletores. No início pode parecer tudo OK, mas quando o seu código for crescendo, você provavelmente vai perceber que acabou dando um tiro no pé. Faça isso apenas quando tiver certeza de que não haverá mudanças na estrutura do código, mas se houver dúvida, utilize classes.
* Dê sentido aos seus seletores. Um `span` ou `div` não têm nenhuma semântica, `header` tem um pouco... é muito melhor criar uma classe com um bom nome, como `.lista-centralizada` ao invés de um outro que não tenha quase nenhum significado \(tipo `.lista`\). Você e seus colegas terão um código muito mais legível e vão gastar muito menos tempo com refatoramento.
* Não aninhe seletores em mais de três níveis. Ao criar regras longas, seu CSS provavelmente estará muito frágil \(bastante associado ao HTML\) ou muito resistente \(bastante específico\) ou não reutilizável.

