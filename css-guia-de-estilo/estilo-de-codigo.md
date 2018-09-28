# Estilo de código 👠

## Espaçamento
* Use soft tabs com dois espaços de indentação. *
* Inclua espaço após `:` na declaração de propriedades. Não inclua antes.
* Inclua espaço antes de `{` na declaração de regras.
* Encerre declarações de regras com `}` em uma nova linha.
* Inclua espaço após `,`.
* Inclua nova linha antes da declaração de uma nova regra.

## Formatação
* Inclua `;` após **todas** as declarações.
* Não utilize IDs como seletores, pois introduzem um alto nível de especificidade desnecessário às regras e não são reutilizáveis.
  ::: warning CUIDADO
  Se você **precisa** utilizar um ID como seletor, eles nunca devem estar aninhados com outras regras. 
  
  Se você estiver fazendo isso, dá uma olhada no seu código ou investiga porquê você precisa de uma especificidade tão alta. Se o seu HTML e o seu CSS estão bem construídos, você nunca precisará fazer isso.
  :::
* Caso haja múltiplos seletores na declaração de uma regra, coloque cada um em uma linha individual.
* Propriedades definidas dentro de regras devem estar em linhas individuais.
* Utilize hífens ao invés de camelCase ou underline nos nomes de classes.
  * Essa instrução pode se revista caso seja decidido que será utilizado [BEM](https://css-tricks.com/bem-101/) ou outro padrão de CSS no seu projeto.
* Utilize códigos de cores hexadecimais (`#FFF`) ao invés de RGB. Dê preferências para [códigos de três dígitos](https://www.quackit.com/css/color/values/css_hex_color_notation_3_digits.cfm).
  * Utilize `#FFF` ao invés de `white`.
  * Se a mesma cor for utilizada ao menos duas vezes na aplicação, inclua a cor como uma variável.
* Não indique unidades para valores zerados (exemplo: `margin: 0;` ao invés de `margin: 0px;`).
  * Utilize `border: 0;` ao invés de `border: none;`.
  * Não inclua um zero à esquerda em números decimais (exemplo: `.5s` ao invés de `0.5s`). *
* Utilize aspas simples `'` ao invés de aspas duplas `"`. Caso haja situações em que ambos são necessários, as aspas internas devem ser simples.
* Seletores de atributos devem estar entre aspas (exemplo: `[type='submit']` ao invés de `[type=submit]`). *
* Procure aninhar regras em no máximo três níveis.
  ``` css
    .navbar {
      .item {
        .ico {
          // PARE
        }
      }
    }
  ```
  ::: warning CUIDADO 
  Se o seletor estiver muito longo, seu código está provavelmente:
    * Extremamente ligado ao HTML (frágil)
    * Muito específico
    * Não reutilizável

  É melhor dar uma olhada na estrutura do seu código para ver se não dá pra melhorar.
  :::
* Sempre inclua mixins acima de outras propriedades.
* Sempre inclua uma nova linha entre um bloco aninhado, mesmo que o anterior não tenha outras propriedades.
* Não inclua espaços entre parênteses, nem após o nome de um mixin (exemplo: `@include animation(blur 1s linear)` ao invés de `@include animation ( blue 1s linear)`).

### Exemplos

**Certo ✅**
``` css
  .classe-um,
  .classe-dois {
    border: 1px solid $red;
    margin: 0;
    background: rgba(0, 0, 0, .5);

    .classe-quatro {

      &:before {
        content: '❤️'
      }
    }
  }

  .classe-cinco {
    &.classe-seis {
      @include center(vertical);
      color: #0366d6;
      font-size: 13px;

      &:hover {
        color: $red;
      }
    }
  }
```

**Errado ❌**
``` css
  .classeUm,
  .classeDois{
    border : 1px solid red
    margin: 0px
    color: #ff0000;

    background : rgba(0, 0, 0, 0.5)

    .classe_quatro {
      #id1{
        &:before {
          content : '❤️' }
      }
    }
  }

  .classeCinco.ClasseSeis {
    color:#0366d6;
    font-size:13px

    &:hover{
      color: #ff0000;
    }
    
    @include center(vertical);
  }
```

## Comentários
* Utilize apenas comentários do Sass `//`, pois eles não são incluídos no CSS compilado.
  
  O seguinte trecho:
  
  ``` css
  /* Este comentário
   * utiliza sintaxe de CSS. */
    .classe { 
      color: #000; 
    }

    // Estes comentários
    // Não são incluídos no CSS compilado.
    a { 
      color: #FFF; 
    }
  ```

  É compilado como:

  ``` css
  /* Este comentário
   * utiliza sintaxe de CSS. */
    .classe { 
      color: #000; 
    }

    a { 
      color: #FFF; 
    }
  ```

* Escreva comentários para código que não é autoexplicativo (exemplos: usos de `z-index` e hacks para compatibilidade de browsers).

## Unidades de medida
* Use `px` para `font-size` de modo a ter controle absoluto sobre o texto.
* Preferencialmente, não inclua unidade de medida à propriedade `line-height`. Dessa forma, o seu valor se torna um múltiplo de `font-size`.
* Não inclua pixels decimais. Além de [não serem suportados por alguns browsers, pode haver diferença entre monitores](https://stackoverflow.com/a/4309051). Exemplo: `10px` ao invés de `10.4px`.
