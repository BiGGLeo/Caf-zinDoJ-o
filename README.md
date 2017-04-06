Componentes: Leon Andrade Siqueira (20141011110352) João Mendes Lopes

# CoffeeScript

<hr>

## Resumo ##

13 de Dezembro de 2009, Jeremy Ashkenas fez o primeiro commit Git do CoffeeScript.
A regra de ouro do CoffeeScript é: “It’s just JavaScript”.
Segundo o site dos desenvoldores, eles se focaram em reunir as melhores característica do JavaScript, para expor a capacidade dessa linguagem do modo mais simples possível, facilitando o aprendizado.
Além do mais, é dito que o resultado compilado é legível, bem escrito e tende a rodar tão rápido quanto ou até mais rápido do que o JavaScript bruto. CoffeeScript é uma linguagem multiparadigma: imperativa, baseada em protótipos, funcional, script.


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
