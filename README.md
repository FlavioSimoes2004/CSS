Pode usar o css dentro do código html, mas é muito melhor deixar separado.

# COMO CONECTAR O ARQUIVO HTML COM CSS?
Com a tag link, ela tem os seguintes atributos:
- href: pra dizer qual o arquivo css que será usado
- rel: esse atributo descreve o relacionamento entre o arquivo HTML e CSS

# RULESET
E um jeito de escrever um codigo css, ele consiste em colocar o elemento a ser editado e depois colocar dois colchetes.
Dentro desses colchetes estarão as coisas a serem mudadas
#### TYPE SELECTOR
Escolhe uma tag(tipo) e personaliza todas deste tipo presentes no arquivo html.
Exemplo:
p {
    color : red;
}

agora TODOS os paragrafos ficarao com o texto vermelho

#### UNIVERSAL SELECTOR
Todos os elementos serão mudados
Exemplo:
*{
    font-family: Verdana;
}

#### CLASS SELECTORS
sabemos que no html, um elemento tem o atributo class que recebe um valor, como no exemplo abaixo:
- < p class='brand'>Sole Shoe Company</ p>

para selecionarmos esse elemento com o valor da classe em específico, iremos colocar um '.' e em seguida o valor da classe.
Exemplo:
.brand {

}

Um elemento pode ter várias classes do jeito do exemplo abaixo:
- < p class='brand seila'>Sole Shoe Company</ p>

Agora o elemento tem a classe brand e seila, e tmb pode ser referenciado por .seila no CSS

#### ID SELECTORS
tambem podemos escolher um elemento com o id, diferente da classe, o id so tem um valor e para usar ele no CSS colocamos
um hashtag antes.\
exemplo:\
< p id="teste"></ p>

#teste {

}

#### ATTRIBUTE SELECTORS
Atributos tambem podem ser modificados no CSS, para modificar um atributo em todos os elementos seria assim:\
[href]{

}
todos os href's de todos os elementos serao modificados.

para escolher modificar um atributo especifico em um elemento especifico, podemos fazer do seguinte jeito
a[href*='florence'] {
  color: lightgreen;
}
escolhemos o elemento com o atributo, botamos o atributo entre '[]' e depois botamos o simbolo de 'aproximado ou igual', assim, a única coisa
que vai modificar é o elemento com o atributo com aquele valor.

#### PSEUDO-CLASS SELECTORS
usadas para certas acoes, como um mouse clica num input e ele muda de cor pra dizer que ele ta selecionado.\
Exemplo:\
p:hover {
  background-color: lime;
}
Quando o mouse passar em cima dos elementos p's, eles vao ficar com cor limao.

#### ORDEM
- ID
- CLASSE
- ELEMENTO
QUANTO MAIS ESPECIFICO, MAIS PRIORIDADE TEM

#### CHAINING
Coloca o elemento + '.' + valor da classe, isso ira personalizar o elemento que tem a classe colocada.
Exemplo:
h1.special {

}

#### DESCENDANT COMBINATOR
CSS tambem suporta elementos que estao dentro de outros elementos. Como numa lista, que tem o 'li'.
Exemplo:
.main-list li {

}
uma lista com classe com valor igual a 'main-list' tem elementos li, esse exemplo acima pega todos os elementos li da lista

Exemplo 2:
.heading-background li h4{
  color: gold;
}
elemento que tem 'li' e que 'li' tem 'h4'

#### MULTIPLE SELECTORS
Exemplo:
h1, 
.menu {
  font-family: Georgia;
}
todos os elementos 'h1' e o elemento que tem valor da classe igual a menu terao suas fontes alteradas

# FONT
Muda a fonte do texto.
Exemplo:
h1 {
  font-family: Georgia;
}
Caso a fonte seja algo baixado, ela precisa estar na pasta ou no servidor.
Caso a fonte tenha mais de uma palavra, coloca ela desse jeito:
h1 {
  font-family: 'Courier New';
}

# FONT-SIZE
Muda o tamanho do texto.
Exemplo:
p {
  font-size: 18px;
}

# FONT-WEIGHT
Controla a grossura das letras do texto.
Exemplo:
p {
  font-weight: bold;
}

# TEXT-ALIGN
Para alinhar o texto em uma posição.
Exemplo:
h1 {
  text-align: right;
}
Ela pode ser colocada como left, center, right ou justify.

# COLOR AND BACKGROUND-COLOR
h1 {
  color: #F0F8FF; ou color: rgb(255, 0, 0);
  background-color: blue;
}

# OPACITY
O quão transparente um elemento é.
Exemplo:
.overlay {
  opacity: 0.5;
}

# BACKGROUND-IMAGE
Exemplo:
.main-banner {
  background-image: url('images/mountains.jpg');
}

# IMPORTANT
Quase nunca é usada pois se usada, nao tem como mudar o estilo
Exemplo:
p {
  color: blue !important;
}

# BOX MODEL
#### HEIGHT AND WIDTH
Uma caixa tem duas dimensões, comprimento(width) e altura(height)
Exemplo:
p {
  height: 80px;
  width: 240px;
}

podemos fazer assim tmb
p {
  width:100%;
}

colocando 100%, significa que o tamanho do conteúdo ocupará 100% do comprimento.

#### BORDERS
p {
  border: 3px solid coral;
}

o primeiro é a grossura, depois o estilo da borda e depois a cor

##### BORDER-RADIUS
Para modificar as beiradas da borda de um elemento.
Exemplo:
div.container {
  border: 3px solid blue;
  border-radius: 5px;
}

#### PADDING
É o espaço entre o conteúdo e a borda, ou seja, quanto mais pixel ele tiver, mais espaçosa a borda será
Exemplo:
p.content-header {
  border: 3px solid coral;
  padding: 10px;
}

Para mover partes específicas de um padding, voce pode usar:
- padding-top
- padding-right
- padding-bottom
- padding-left

##### PADDING SHORTHAND
Deixa voce especificar os tamanhos dos 4 padding em uma só linha.
Exemplo:
p.content-header {
  padding: 6px 11px 4px 9px;
}

#### MARGIN
Se refere ao espaço fora da caixa, pode ser usada para aumentar a distancia entre elementos
Exemplo:
p {
  border: 1px solid aquamarine;
  margin: 20px;
}

Se quiser ser mais específico em que parte mudar, pode usar o:
- margin-top
- margin-right
- margin-bottom
- margin-left

margin pode ser definido desta maneira também:
p {
  margin: 6px 10px 5px 12px;
}

ou

p {
  margin: 20px 10px;
}

#### AUTO
O margin também permite centrar conteúdos, porém, você precisa seguir alguns requerimentos de sintaxe.
Isto serve para centralizar seções como div, section, nav, article, etc.
Exemplo:
div.headline {
  width: 400px;
  margin: 0 auto;
}

Em ordem para centralizar um elemento, um valor width deve ser colocado, caso contrário, o width será igual ao valor máximo.
Não é possível centralizar um elemento que está com o width máximo.

#### MARGIN COLLAPSE
Pulei pq n achei necessário

#### MIN AND MAX WIDTH AND HEIGHT
Para dizer qual o mínimo e máximo width ou height de um elemento
p {
  min-width: 300px;
  max-width: 600px;
}

#### OVERFLOW
Essa propriedade controla o que acontece com um elemento que acaba sendo maior que a caixa, como uma imagem com dimensao 364x244 e a sua caixa é
300x200
Exemplo:
p {
  overflow: scroll; 
}

Valores do overflow:
- hidden: Esconde os elementos que estão em oveflow
- scroll: Adiciona um scrollbar para que o resto do elemento seja visualizado
- visible: O conteúdo que está em overflow será mostrado, mesmo ele ultrapassando a caixa (esse é o valor padrão do overflow)

#### RESETTING DEFAULTS
Muitos desenvolvedores escolhem resetar os valores para o padrão para assim eles poderem trabalhar num ambiente limpo.
* {
  margin: 0;
  padding: 0;
}
Quando essas duas propriedades são igual a 0, elas não precisam de 'px'

#### VISIBILITY
Elementos podem ser escondidos visualmente do site usando a propriedade visibility(visibilidade)
Ela pode ter os seguintes valores:
- hidden
- visible
- collapse

Exemplo:
.future {
  visibility: hidden;
}

#### BOX-SIZING
Controla o modelo de caixa usado pelo browser.
O valor padrão para box-sizing é content-box.
Aquele fundo cinza e as bordas de um botão é a caixa.

## AJUSTANDO POSIÇÕES DE ELEMENTOS
### POSITION
Block-level elements são elementos elementos que possuem um width máximo até o seu parent, e previnem que outros elementos fique ao seu lado.
o position pode ter os seguintes valores:
- static (valor padrão do position)
- fixed
- relative
- absolute
- sticky

Exemplo:
.question {
  text-align: center;
  position: static;
}

##### POSITION RELATIVE
Permite mover o elemento a partir da posição que está do static.
Para mover o elemento, podemos usar:
- top
- right
- bottom
- left

Exemplo:
.green-box {
  background-color: green;
  position: relative;
  top: 50px;
  left: 120px;
}

#### POSITION ABSOLUTE
Quando a posição de um elemento recebe absolute, todos os outros elementos irão agir como se esse elemento não estivesse presente no site.


#### POSITION FIXED
Quando botamos para abaixar a página, todos os elementos se movem, mas podemos usar o fixed para fixar elementos naquela posição, mesmo
quando a página se move.

Exemplo:
.title {
  position: fixed;
  top: 0px;
  left: 0px;
}

#### POSITION STICKY