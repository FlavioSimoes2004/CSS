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