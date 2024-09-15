# Consolidação de CSS

**Colaboradores**: Marcio Barcellos, Igor Chupel, Felipe ???


## Capitulo 1

## Introdução ao CSS

### O que é o CSS?

* CSS, ou Cascading Style Sheets, é a linguagem que utilizamos para estilizar páginas da web, definindo cores, fontes, layouts e muito mais.

### Historia

* 1994: Håkon Wium Lie, frustrado com a dificuldade de estilizar páginas web usando apenas HTML, propôs a criação do CSS. A ideia era separar a estrutura do conteúdo (HTML) da sua apresentação visual (CSS), tornando a manutenção e a criação de sites mais eficientes.
* 1996: O CSS1 foi lançado pelo World Wide Web Consortium (W3C), estabelecendo os primeiros padrões para a linguagem. Navegadores como o Internet Explorer 3 começaram a adotar o CSS, mas a compatibilidade entre diferentes navegadores ainda era um grande desafio.
A Evolução do CSS

* CSS2: Introduziu novas funcionalidades, como layouts mais complexos e suporte a diferentes mídias.
 *CSS3: A versão mais recente trouxe um grande número de novas propriedades e módulos, como sombras, transições, animações, flexbox e grid, permitindo a criação de designs mais sofisticados e interativos.

* Pré-processadores CSS: Linguagens como Sass, Less e Stylus surgiram para adicionar funcionalidades avançadas ao CSS, como variáveis, mixins, aninhamento e outras ferramentas para facilitar a escrita de código CSS.
Por que o CSS é tão importante?

Separação de preocupações: Permite que designers e desenvolvedores trabalhem de forma mais independente, focando cada um em suas respectivas áreas.
Manutenção: Facilita a atualização de estilos em um único lugar, evitando a necessidade de alterar o código HTML.
Reutilização: Permite a criação de estilos reutilizáveis em diferentes partes de um site ou em vários projetos.
Acessibilidade: Ajuda a criar sites mais acessíveis para pessoas com deficiência.
Responsividade: Permite que os sites se adaptem a diferentes dispositivos e tamanhos de tela.


### O CSS hoje:

O CSS continua evoluindo e se tornando cada vez mais poderoso e expressivo. Com o surgimento de novas tecnologias, como o JavaScript e frameworks CSS, as possibilidades de criação de experiências web ricas e interativas são infinitas.

### Exemplos

#### HTML
~~~ HTML

<!DOCTYPE html>
<html>
<head>
    <title>Minha primeira página com CSS</title>
<link rel="stylesheet" href="EXcss.css">
</head>
<body>
    <h1>Bem-vindo!</h1>
    <p>Este é um parágrafo.</p>
</body>
</html>
~~~

#### CSS
~~~CSS

EXcss.css

body {
    font-family: Arial, sans-serif;
    background-color: cyan;
}

h1 {
    color: #333;
    text-align: center;
}

p {
    font-size: 16px;
    line-height: 1.5;
    color: Red;   

}

a {
    color: blue;
    text-decoration: none;
}
~~~

Exemplo 1 - [https://repositoriofsg.github.io/trabalho17set/pratica1/](https://repositoriofsg.github.io/trabalho17set/pratica1/)


## Capitulo 2

## Selectores e Especificidade

### Seletores Básicos (Revisão)

* **Elemento**: Seleciona todos os elementos de um determinado tipo (p, h1, div).
  
* **Classe**: Seleciona elementos com uma determinada classe (ex: .destaque).
  
* **ID**: Seleciona um elemento único com um ID específico (ex: #cabecalho).


### Seletores Avançados


* **Agrupamento**: Permite aplicar o mesmo estilo a múltiplos elementos (ex: h1, h2 { color: blue; }).
  
* **Descendente**: Seleciona todos os descendentes de um elemento (ex: div p { font-size: 16px; }).


* **Filho**: Seleciona apenas os filhos diretos de um elemento (ex: div > p { color: red; }).

* **Adjacente**: Seleciona o elemento imediatamente seguinte a outro (ex: h2 + p { margin-top: 0; }).

* **General sibling**: Seleciona todos os elementos seguintes a outro (ex: h2 ~ p { font-style: italic; }).


### Especificidade


* **Determinando qual estilo aplicar**: O navegador calcula a especificidade de cada regra CSS e aplica a regra com maior especificidade.

### Ordem de especificidade:

* **Elementos inline**: Estilos definidos diretamente no elemento HTML (maior especificidade).

* **IDs**: Seletores com IDs.

* **Classes**, atributos e pseudo-classes: Seletores com classes, atributos ou pseudo-classes.

*  **Elementos**: Seletores de elementos.

* **Seletores universais e combinadores**: Seletores como * e +, respectivamente.


### Herança de Propriedades

* **Passagem de estilos**: Algumas propriedades CSS são herdadas pelos elementos filhos (ex: font-family, color).

* **Propriedades não herdáveis**: Outras propriedades não são herdadas (ex: margin, padding).

#### EXEMPLO

#### HTML

~~~
Ex2.html

<!DOCTYPE html>
<html>
<head>
    <title>Minha primeira pagina com CSS</title>
<link rel="stylesheet" href="EXcss2.css">
</head>
<body>
  <div class="container">
  <h1>Titulo Exemplo</h1>
  <p class="destaque">Este e um paragrafo destacado.</p>
  <ul>
    <li>Teste 1</li>
    <li>Teste 2</li>
    <li>Teste 3</li>
  </ul>
</div>
</body>
</html>
~~~

#### CSS
~~~
Excss2.css

.container {
  background-color: Cyan;
  padding: 20px;
}

.destaque {
  color: blue;
  font-weight: bold;
}

h1 + p {
  margin-top: 0;
}

ul li:nth-child(odd) {
  background-color: gray;
}
~~~
Exemplo 2 - [https://repositoriofsg.github.io/trabalho17set/pratica2/](https://repositoriofsg.github.io/trabalho17set/pratica2/)


## Capítulo 3

### Cores e Unidades

#### Unidades de Medida

Ao definir tamanhos, espaçamentos e outras medidas em CSS, você pode utilizar dois tipos principais de unidades:

* **Absolutas**:
    1. **px (pixels)**: A unidade mais comum, representa um único pixel na tela.
    
    2. **cm, mm, in**: Unidades de medida físicas, como centímetros, milímetros e polegadas.

* **Relativas**:

    1. **em**: Relativa ao tamanho da fonte do elemento pai.
    2. **rem**: Relativa ao tamanho da fonte da raiz (geralmente o elemento HTML).
    3. **%**: Porcentagem em relação ao tamanho do elemento pai.
    4. **vw**: Viewport width (largura da viewport).
    5. **vh**: Viewport height (altura da viewport).



As unidades relativas proporcionam maior flexibilidade e responsividade, adaptando o layout a diferentes tamanhos de tela.

#### Cores em CSS

* **Nomeadas**: Nomes pré-definidos de cores (ex: red, blue, green).

* **HEX**: Código hexadecimal de seis dígitos (ex: #FF0000 para vermelho).

* **RGB**: Combinação de vermelho, verde e azul em valores de 0 a 255 (ex: rgb(255, 0, 0)).

* **RGBA**: Igual ao RGB, mas com um canal alfa para transparência (ex: rgba(255, 0, 0, 0.5)).

* **HSL**: Hue (matiz), Saturation (saturação) e Lightness (luminosidade) (ex: hsl(0, 100%, 50%)).

* **HSLA**: Igual ao HSL, mas com um canal alfa para transparência (ex: hsla(0, 100%, 50%, 0.5)).


### Transparência e Opacidade

A propriedade opacity controla a transparência de um elemento inteiro. O valor varia de 0 (totalmente transparente) a 1 (totalmente opaco). A propriedade rgba() ou hsla() permite definir a transparência de uma cor individual.

### Gradientes

* **Lineares**: Cria um efeito de transição suave entre duas ou mais cores em uma direção linear.

* **Radiais**: Cria um efeito de transição suave entre duas ou mais cores a partir de um ponto central.


#### EXEMPLO

#### CSS

~~~

Ex3css.css

background: linear-gradient(to right, red, yellow);

~~~
Exemplo 3 - [https://repositoriofsg.github.io/trabalho17set/pratica3/](https://repositoriofsg.github.io/trabalho17set/pratica3/)

### Capítulo 4: Tipografia

Fontes web: Font-family, fallback fonts.<br>
**Fallback font é a fonte alternativa que será utilizada se a fonte especificada no CSS não puder ser carregada.**
```html
font-family: "Times New Roman", Times, serif;
```

Google Fonts e fontes personalizadas.
No código abaixo será carregado a fonte do Google Montserrat e se ela não estiver disponível será carregada uma fonte da família sans-serif.

```html
<head>
<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Montserrat">
<style>
body {
  font-family: "Montserrat", sans-serif;
}
</style>
</head>
```

Propriedades tipográficas: Tamanho, altura da linha (line-height), espaçamento entre letras (letter-spacing) e entre palavras (word-spacing).

```html
font-size: 0.875em;
line-height: 30px;
letter-spacing: 1px;
word-spacing: 5px;
```

Estilização de texto: Negrito, itálico, sublinhado, alinhamento, decoração e transformação.

```html
<b>Texto em negrito</b>
<i>Texto em itálico</i>
<u>Texto sublinhado</u>
<p align="center">Texto alinhado no centro</p>
text-decoration: line-through; /* Adiciona uma linha no meio do texto */
text-transform: lowercase; /* Transforma o texto para minúsculo */
```
Prática 4 - [https://repositoriofsg.github.io/trabalho17set/pratica4/](https://repositoriofsg.github.io/trabalho17set/pratica4/)
<br>*Criar um layout de texto para um artigo, explorando fontes e estilos.*



### Capítulo 5: Box Model e Layout

Box Model: Margem (margin), borda (border), padding, conteúdo.
```html
div {
  width: 300px;
  border: 15px solid green;
  padding: 50px;
  margin: 20px;
}
```

Box-sizing: Content-box vs. border-box.
```html
box-sizing: content-box; /* Largura e altura somente são aplicados ao conteúdo do elemento */
box-sizing: border-box; /* Largura e altura são aplicados em todas as partes do elemento; conteúdo, preenchimento e bordas */
```


Display: Block, inline, inline-block.
```html
p.exemplo1 {
  display: block;
  }
p.exemplo2 {
  display: inline;
  }
p.exemplo3 {
  display: inline-block;
  }
```

Manipulação de largura e altura.
```html
div {
  width: 500px;
  height: 200px;
}
```
Prática 5 - [https://repositoriofsg.github.io/trabalho17set/pratica5/](https://repositoriofsg.github.io/trabalho17set/pratica5/)
<br>*Criar um layout simples aplicando conceitos do Box Model e do display.*


### Capítulo 6: Flexbox

Conceito de Flexbox:
```html
Modo mais eficaz de distribuir e alinhar espaços entre intes em um container, mesmo quando as dimensões dos itens não estão especificadas.
```

Container flex:

```html
display, flex-direction, flex-wrap, flex-flow, justify-content, align-items, align-content, gap, row-gap, column-gap
```

Itens flex:
```html
Order, flex-grow, flex-shrink, flex-basis, flex, align-self
```


Propriedades do container flex:
```html
display: flex;
flex-direction: row | row-reverse | column | column-reverse;
flex-wrap: nowrap | wrap | wrap-reverse;
flex-flow: column wrap;
justify-content: flex-start | flex-end | center | space-between...;
align-items: stretch | flex-start | flex-end | center | baseline...;
align-content: flex-start | flex-end | center | space-between...;
gap: 10px;
row-gap: 10px;
column-gap: 20px;
```

Propriedades dos itens flex:
```html
order: 5;
flex-grow: 4
flex-shrink: 3;
flex-basis: auto;
align-self: auto | flex-start | flex-end | center | baseline | stretch;
```


Prática 6 - [https://repositoriofsg.github.io/trabalho17set/pratica6/](https://repositoriofsg.github.io/trabalho17set/pratica6/)
<br>*Criar um layout de galeria de imagens utilizando Flexbox.*


## Capítulo 7: Grid Layout 
### **Objetivo**
<center>Apresentar o CSS Grid e suas capacidades para criação de layouts complexos.</center>

### Conteúdo
* **Introdução ao CSS Grid:** 
  O CSS Grid é uma ferramenta poderosa para criação de layouts em duas dimensões, permitindo um controle preciso sobre o posicionamento de elementos no eixo vertical e horizontal.
* **Containers e Itens de Grid:** 
  Um layout baseado em grid começa com um container de grid que abriga itens, permitindo a distribuição dos elementos de maneira fluida e adaptável.
* **Definindo Colunas e Linhas:** 
  Utilizando `grid-template-columns` e `grid-template-rows`, é possível definir o número de colunas e linhas e suas dimensões.
* **Áreas de Grid e Alinhamento de Itens:** 
  A técnica de criar áreas no grid facilita a organização de elementos, enquanto as propriedades de alinhamento controlam o posicionamento exato desses itens no layout.
* **Prática:** 
  Desenvolver um layout de página simples com cabeçalho, conteúdo principal e rodapé utilizando o CSS Grid.

Grid_Layout - [https://repositoriofsg.github.io/trabalho17set/pratica7/](https://repositoriofsg.github.io/trabalho17set/pratica7/)


## Capítulo 8: Estilização Avançada e Animações 
### **Objetivo**
<center>Explorar técnicas avançadas de estilização e introduzir animações em CSS.</center>

### Conteúdo
* **Pseudo-classes e Pseudo-elementos:** 
  Ferramentas como `:hover`, `:before`, e `:after` permitem aplicar estilos condicionais e adicionar elementos estilísticos sem precisar modificar o HTML.
* **Animações Básicas:** 
  O uso de `@keyframes` permite a criação de animações complexas, enquanto `animation` e `transition` possibilitam transições suaves e dinâmicas.
* **Efeitos de Hover e Foco:** 
  Esses efeitos são usados para interações com o usuário, melhorando a experiência ao navegar ou focar em elementos da interface.
* **Transições Suaves e Animações Personalizadas:** 
  Além de animações básicas, é possível criar transições fluidas com propriedades como `ease-in`, `ease-out`, e `cubic-bezier` para um controle maior.
* **Prática:** 
  Criar um menu de navegação interativo com animações e efeitos visuais utilizando as propriedades de animação do CSS.

Estilo_Animacao - [https://repositoriofsg.github.io/trabalho17set/pratica8/](https://repositoriofsg.github.io/trabalho17set/pratica8/)


## Capítulo 9: Responsividade e Media Queries
### **Objetivo**
<center>Criar layouts responsivos que se adaptam a diferentes dispositivos.</center>

### Conteúdo
* **Conceito de Design Responsivo:** 
  O design responsivo garante que uma página web se ajuste de maneira adequada a diferentes tamanhos de tela, proporcionando uma boa experiência em qualquer dispositivo.
* **Media Queries:** 
  Media Queries são usadas para aplicar estilos específicos com base na largura ou altura da tela, permitindo ajustes no layout conforme a resolução do dispositivo.
* **Layouts Fluidos e Imagens Responsivas:** 
  Utilizando porcentagens, `vw`, `vh` e outras unidades relativas, é possível criar layouts que se ajustam dinamicamente. Imagens responsivas são otimizadas para diferentes tamanhos de tela.
* **Unidades Relativas para Responsividade:** 
  Unidades como `em`, `rem`, `vw` e `vh` ajudam a garantir que o layout e os textos sejam dimensionados proporcionalmente às diferentes resoluções de tela.
* **Prática:** 
  Desenvolver um layout que se adapta a diferentes tamanhos de tela, usando Media Queries e técnicas de responsividade.

Responsividade_MediaQ - [https://repositoriofsg.github.io/trabalho17set/pratica9/](https://repositoriofsg.github.io/trabalho17set/pratica9/)


## Capítulo 10: Boas Práticas e Otimização
### **Objetivo**
<center>Consolidar os conceitos aprendidos e introduzir boas práticas e técnicas de otimização.</center>

### Conteúdo
* **Estruturação e Organização de CSS:** 
  Métodos como o BEM (Block Element Modifier) ajudam a manter o código CSS modular e escalável, facilitando a manutenção.
* **Minificação e Compressão de Arquivos CSS:** 
  Para melhorar a performance, o CSS pode ser minificado e comprimido, reduzindo o tempo de carregamento.
* **Ferramentas de Desenvolvimento:** 
  Ferramentas como DevTools auxiliam na depuração de problemas de layout, enquanto o linting verifica a qualidade do código. Pré-processadores como **Sass** oferecem funcionalidades adicionais ao CSS.
* **Acessibilidade em CSS:** 
  As boas práticas de CSS também devem considerar a acessibilidade, garantindo que as páginas sejam navegáveis por pessoas com deficiência.
* **Prática:** 
  Revisar um projeto CSS existente, implementando melhorias na organização e performance, utilizando técnicas de otimização e acessibilidade.
