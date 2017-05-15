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

### Variáveis e Constantes###

#### Variáveis ####

CoffeeScript
~~~~
number = 10
number = 5.5
~~~~

JavaScript
~~~~
var number = 10
var number = 5.5
~~~~

### Operadores relacionais e lógicos ###

CoffeeScript
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

JavaScript
~~~~
a === b
a !== b
a < b
a > b
a <= b
a >= b
!condicao
a && b
a || b
~~~~

### Operadores Aritméticos ###
Os operadores aritméticos do CoffeeScript seguem todos a mesma sintaxe do Javascript

### Estruturas de Controle Condicional ###

Nestes tópicos, é importante considerar a importância da tabulação na sintaxe do CoffeeScript, como será visto a seguir:
CoffeeScript
~~~~
if condição
	comando

else
	comando
  
comando if condição 

switch variavei
  when comparacao comando
  else comando
~~~~

Javascript
~~~~
if (condição){
	comandos
}

else{
	comando
}

switch (variavei) {
    case comparacao:
      comando
      break;
    default:
      comando
  }
~~~~
## Sintaxe OO ##

O CoffeeScript conta com uma sintaxe OO própria, diferentemente do JavaScript, que utiliza de vários artifício dentro da linguagem, tais como a utilização de funções ou variáveis populadas por outras variáveis e funções, atuando respectivamente como objetos e métodos. Veja um pouco do funcionamento dessa sintaxe:

Criando classe:
~~~
class Animal
~~~
Instanciando classe :
~~~
animal = new Animal
~~~

Criando construtor:

Com um único objeto
~~~
class Animal
  constructor: (name) ->
    @name = name
~~~
Com mais de um objeto
~~~
class Person
  constructor: (options) ->
    {@name, @age, @height = 'average'} = options
~~~
Perceba que é definida previamente o valor de um objeto height como average.





