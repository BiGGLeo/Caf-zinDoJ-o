Componentes: <br>
Leon Andrade Siqueira (20141011110352) <i>BiGGLeo</i> <br>
João Mendes Lopes Neto (20141011110018) <i>joaomendesln</i> <br>
Gabriel Cardoso Melita (20141011110263) <i>gcmelita</i> <br>

# CoffeeScript

<hr>

## Resumo ##

13 de Dezembro de 2009, Jeremy Ashkenas fez o primeiro commit Git do CoffeeScript.
A regra de ouro do CoffeeScript é: “It’s just JavaScript”.
Segundo o site dos desenvoldores, eles se focaram em reunir as melhores característica do JavaScript, para expor a capacidade dessa linguagem do modo mais simples possível, facilitando o aprendizado.
Além do mais, é dito que o resultado compilado é legível, bem escrito e tende a rodar tão rápido quanto ou até mais rápido do que o JavaScript bruto, já que muitos caracteres na programação são poupados como chaves e parênteses. CoffeeScript é uma linguagem multiparadigma: imperativa, baseada em protótipos, funcional, script.


## Instalação e Uso ##

Antes de começar a instalação, certifique-se de que o seu <a href= 'https://nodejs.org/en/'>Node.js</a> está instalado e funcional na última versão estável.
Agora, baixe via <a href='https://www.npmjs.com/'>npm</a> o CoffeeScript, digitando no seu prompt:	


~~~~
npm install --global coffee-script
~~~~


Para compilar um arquivo em CoffeeScript, basta criar um arquivo de texto com uma extensão **.coffee** e, pelo prompt, dar a localização do arquivo para o CoffeeScpript.


Conteúdo do arquivo referido abaixo:
~~~~
Console.log "Olá, mundo!";
~~~~


Comandos no prompt:
~~~~
cd C:\Users\Ja1\Desktop\CafezinDoJa1
coffee --compile HelloWorld.coffee
~~~~


Resultado: 
~~~~
Olá, mundo!
~~~~


*Caso queira, use o comando **--watch** em conjunto, pois ele fará com que o arquivo seja recompilado toda vez que ele for salvo, poupando possíveis esforços desnecessários.*


Divirta-se!

## Sintaxe Básica ##


O CoffeeScript visa, entre outras coisas, tornar o código menor e mais legível, tornando, por consequência, a sintaxe mais simples e clara para os usuários, como é possível ver a seguir:

### Variáveis e Constantes ###

~~~~
number = 10
~~~~

### Operadores relacionais e lógicos ###

~~~~
a is b
a isnt b
a < b
a > b
a <= b
a >= b
not condicao
a and b
a or b
~~~~


### Operadores Aritméticos ###
Os operadores aritméticos do CoffeeScript seguem todos a mesma sintaxe do Javascript:
~~~~
a + b
a - b
a * b
a / b
a % b
a++
a--
~~~~

### Estruturas de Controle Condicional ###

Nestes tópicos, é importante considerar a importância da tabulação na sintaxe do CoffeeScript, como será visto a seguir:
~~~~
if condição
	comando

else
	comando
  
comando if condição 

switch variavel
  when comparacao comando
  else comando
~~~~

### Estruturas de repetição ###
A maioria dos laços (loops) que você escreverá em CoffeeScript serão compreensões de listas (list comprehensions) em arrays, objetos, e intervalos. Caso se queira fazer um loop com uma quantidade de fixa de iterações sem ser necessário criar uma lista, é só usar o array [1..x], que criará uma repetição crescente a qual acontecerá x vezzes.

~~~~
console.log variavel ; for variavel in listaPercorrida

console.log variavel; for variavel in listaPercorrida when condicao

console.log num for num in [1..10]

for num in [1..10]
	console.log "Iteração: " + i
	console.log num

comando while condicao

~~~~

### Vetores, matrizes e strings ###

~~~~
string = "Oi";

song = ["do", "re", "mi", "fa", "so"]

matriz = [[1, 2], [3, 4]]
~~~~


### Funções ###

A declaração de funções é dada por nomeDaFuncao(atributos) -> comandos retorno. O código a seguir exemplifica essa sintaxe:
~~~~
produto = (a) -> 
	console.log "Produto por 2: "
	a * 2
~~~~
Nesse caso, o retorno da função "produto é dada por'



## Sintaxe OO ##

O CoffeeScript conta com uma sintaxe OO própria, diferentemente do JavaScript, que utiliza de protótipos dentro da linguagem, tais como a utilização de funções ou variáveis populadas por outras variáveis e funções, atuando respectivamente como objetos e métodos. Veja um pouco do funcionamento dessa sintaxe:

### Classe ###
~~~
class Animal
~~~

### Objeto ###

O instaciamento dos objetos pode ser feito baseado nas carecterísticas de uma classe ou atributos e métodos próprios

~~~~
animal = new Animal


math =
  root:   Math.sqrt
  cube:   (x) -> x * square x
~~~~

### Atributos e Construtores ###

No primeiro caso do exemplo anterior, o instaciamento dos atributos são feitos concomitantemente a suas incializações realizadas nos construtores.

~~~~
class nomeClasse
  constructor: (@atributo1, @atributo2) ->
~~~~

### Métodos ###

Já os métodos são declarados independentes dentro da classe, sempre respeitando o tabulamento

~~~~
class nomeClasse
  constructor: (@atributo1, @atributo2) ->

  metodo: (atributoMetodo) ->
    comandos
~~~~

### Herança ###

A herança é um conceito também presente no CoffeScript. Para uma classe herdar atributos de uma classe pai é só declarar a classe e adicionar "extends + classePai"

~~~~
class Animal
  constructor: (@name) ->

class Snake extends Animal
~~~~

### Polomorfismo ###

O polimorfismo é uma característica inerenta ao CoffeScript. Sua realização é dada somente pela criação de métodos herdados da super-classe, mas diferenciado de classe herdada para classe.

~~~~
class Animal
  constructor: (@name) ->

  move: (meters) ->
    console.log @name + " moved #{meters}m."

class Snake extends Animal
  move: ->
    console.log "Slithering..."

class Horse extends Animal
  move: ->
    console.log "Galloping..."
~~~~

### Sobrecarga ###


## Tratamento de exceções ##

### Categorias de exceções ###

O CoffeeScript é uma linguagem estática, tendo os seus erros detectados antes da compilação. O tratamento de erros é feito por meio do objeto da classe error. Alguns dos tipos de erros que podem ser replicados são:

<b>TypeError</b> <br>
<b>RangeError</b> <br>
<b>EvalError</b> <br>
<b>ReferenceError</b> <br>

### Captura e lançamento de exceções ###

A captura e lançamento dos erros encontrados no CoffeeScript são manipulados por meio da cláusala try...catch, como estruturado no exemplo a seguir

~~~~
try
  x = y+20
  console.log "O valor de x é:" +x
catch e 
	console.log "undefined" if e instanceof ReferenceError

	console.log "Tipo de erro: " + e.stack
finally
  console.log "Declaração de fim"
~~~~
