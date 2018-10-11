---
description: "Pelamor, né, gente \U0001F645\U0001F3FC‍♀️"
---

# O que NÃO fazer de jeito nenhum

Para finalizar aqui só vão mais algumas considerações sobre o que NÃO FAZER DE JEITO NENHUM enquanto estiver escrevendo seu código CSS.

* Se você acabou de entrar no time de um projeto já em andamento, tire um tempo para conversar com o time sobre como o desenvolvimento está sendo feito e mais um tempo para estudar o código.
* Em projetos muito grandes, tome bastante cuidado com classes e elementos que são utilizados em diversas partes do código para diferentes propósitos. Essa é uma prática muito ruim, mas em projetos já existentes não há muito o quê fazer... apenas ter muito cuidado e atenção. Na dúvida, crie sua própria classe -- mas antes garanta que uma regra com as mesmas propriedades não exista ainda \(lembra do [DRY](../guia-de-boas/seguindo-alguns-padroes.md#dry-dont-repeat-yourself)?\)
* Evite o uso de espaçamento negativo \(você realmente precisa daquela `margin-right: -12px`?\). Confira o seu código e garanta que não haja problemas em sua estrutura.
* Prefira mover os seus elementos utilizando `translate` ao invés de `position`. [Saiba mais](https://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/)!
* Quando estiver utilizando um pré-processador CSS, tire um tempo para estudar a documentação. Se não fizer isso, você pode estar perdendo tempo e não aproveitando todo o potencial que esses pré-processadores podem oferecer.

{% hint style="info" %}
**Conteúdo extra**

* [Desafios práticos de performance Web](https://www.youtube.com/watch?v=EMCBd3kw4zs)
* [Why moving elements with translate\(\) is better](https://www.paulirish.com/2012/why-moving-elements-with-translate-is-better-than-posabs-topleft/)
* [Sass - Documentação](https://sass-lang.com/documentation/file.SASS_REFERENCE.html)
* [Stylus - Documentação](http://stylus-lang.com)
{% endhint %}

