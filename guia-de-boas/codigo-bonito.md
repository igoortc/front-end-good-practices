---
description: "Por que quem gosta de código feio, né? \U0001F9DF‍♂️"
---

# Código limpo e bonito

Eu não sei você, mas eu conheço muitos desenvolvedores que não conseguem lidar com código feio e desorganizado. Às vezes um código mal escrito pode até influenciar na produtividade -- tanto na sua, quanto na dos outros que, assim como você, passarão horas tentando encontrar uma agulha em um palheiro.

![S&#xE9;rio... pra mim n&#xE3;o d&#xE1;](../.gitbook/assets/canteven.jpg)

### gandalf-lint 🧙🏼‍♂️

É claro que os seus amigos da Soft já vão te dar um empurrãozinho para que você possa produzir códigos lindos 🦄 e acessíveis para todo mundo. Nós temos o nosso próprio [linter](https://willianjusten.com.br/analisando-seu-codigo-js-com-linter/) que irá prevenir você de commitar um código que não funciona ou que não segue algum padrão que já foi definido previamente pelo **Front-end chapter**. O uso da [**gandalf-lint**](https://github.com/SoftboxLab/gandalf-lint) é obrigatório para todos os front-enders da Soft, garantindo que _your bad code shall not pass_ nem causar mil tretas em produção.

### Algumas diquinhas

Temos algumas dicas básicas que, se seguidas corretamente, farão uma grande diferença para você e para os seus colegas desenvolvedores. Às vezes, segui-las com cuidado pode ser a diferença entre conseguir estender um pouquinho o seu café ☕️ e passar duas horas tentando entender aquele código que você escreveu um mês atrás!

* Utilize nomes coerentes com o que está sendo feito.

  Exemplo: `function tomarCafe()`, ao invés de `function cafe()`e `var xicara` ao invés de `var xic`.

* Crie funções pequenas e específicas.

  Exemplo:

  ```js
  function irAteACozinha() {

      //ir até a cozinha

  }

  function tomarCafe() {

      //tomar café

  }

  function tirarIntervaloDeCafe() {

      irAteACozinha()

      tomarCafe()

  }
  ```



  ao invés de:

  ```js
  function cafe() {

      //ir até a cozinha

      //tomar café

  }
  ```

* Não seja redundante \(lembre-se dos [padrões](seguindo-alguns-padroes.md)!\)
* Refatorar! Se você viu um código \(seu ou de outra pessoa\) que poderia ser simplificado ou escrito de uma forma mais legível, refatore! 

{% hint style="danger" %}
**Atenção**

Se estiver refatorando, tome apenas cuidado para não quebrar o código caso ele esteja sendo invocado em outras partes do sistema. Se planeja mudar algum método muito grande ou uma variável que aparece em várias partes do código, valide junto com seus colegas se a refatoração é realmente viável e necessária.
{% endhint %}

{% hint style="info" %}
**Leitura extra**

* [Analisando seu código JS com um linter](https://willianjusten.com.br/analisando-seu-codigo-js-com-linter/)
* [Clean Code: boas práticas para manter o seu código limpo!](https://becode.com.br/clean-code/)
* [Deixe o ESLint trabalhar para você, no Visual Code!](http://vuejs-brasil.com.br/deixe-o-eslint-trabalhar-para-voce-no-visual-studio-code/)
{% endhint %}

