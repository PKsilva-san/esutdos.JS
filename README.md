# esutdos.JS
meu desenvolvimento em JS, esse arquivo vai ser atualizado com frequencia

# Anotações JS - PK

Eu uso o VS code com uma extensão para node.js (node.js exec), use o que preferir.

# Modulo B

Bibliografia: JavaScript guia definitivo; 

JS guia do programador; 

guia mozila e ecma

# Aula 04

(corpo de um site)

HTML: 5

Lang = “pt-br”

Body <h1> </h1> <p> </p>

Head <style>

Body {

Background-color: cor; //fundo

Color: cor; //letra

Font: normal pt arial; // fonte da letra

}

</style>

Dentro de body

<script>

Window.alert(‘ ‘);

Window.confirm(‘ ‘);

Window.prompt(‘ ‘);

</script>

obs: para criar um arquivo JS externo use 

`<script src="script.js" defer></script>`

o ‘script src’ ira conectar o arquivo com o html ‘script.js’ é o arquivo (lembre-se de sempre usar o .js) o ‘defer’ serve para que tanto o arquivo .js quanto o html carreguem simultaneamente

# Aula 05

Um sinal de = significa receber um valor

Os dados ficam armazenados na memoria

Criar variável se usa Var,  Let ou Const

Quando usar uma das 3? o Var não se utiliza mais, simplificando Let é quando você sabe que provavelmente no codigo essa variavel vai ser difierente da original do começo e o Const quando é uma variavel que você sabe que não vai mudar de jeito nenhum (caso você tente mudar vai dar erro, e voce vai precisar trocar para o Let)

Var n1 = 1 (antes do sinal = é a variante/indentificador após é o dado)

Var s1 = “ “, ‘ ‘, ` ` (aspas dupla, simples e crase para string)

Ctrl + shift + aspa simples == terminal: node

Identificadores: pode começar com letra, $ ou _

Pode usar letras, números, acentos e símbolos

Não pode começar com numero, não pode ter espaço e não pode ser palavras reservadas ex: function

Letras maiúsculas e minúsculas tem diferença

Sempre por nomes coerentes para as variantes (uma variável para se por nome não pode se chamar ‘quadrado’ por exemplo pois pode te confundir depois ou quando alguém for ler o código)

Resultado no console:

```jsx
var nome = "João";
var idade = 30;
var resultado = nome + " tem " + idade + " anos";
console.log(resultado);

```

Resultado no console:

```
João tem 30 anos

```

```jsx
let idade = 30
const nome = 'PK'
idade = 21 // aqui de 30 mudou para 21
nome = 'Higor' //esse não vai funcionar
```

Aqui estão os tipos de dados que se podem usar em uma variavel

Números == Number

Escrita == String

True && False == Boolean

Array == pode armazenar varios dados em uma variavel

Object == tambem pode armazenar varios dados porem em uma variavel de cade vez

Null e Undefined == Null é quando você escolhe não ter nada, Undefined é quando voce esquece de definir a variavel ou simplesmente colocou algo que não existe no codigo

```jsx
//mesmo sem vocês entender agora vou dar um exemplo
const nome = 'pk'//string
const idade = 21//number
let casado = true// boolean
let conjuge = null//null

const lista = [1,2,3]//array

const usuario = {
	nome: 'pk',
	idade: 21,
	casado: true,
	conjuge: 'dona gatinha'
}//object
/* mais para frente eu ensino como acessar cada coisa disso, foquem no basico primeiro*/
```

# Aula 06

Var nome = windown.prompt

Alert (‘string’ + nome) concatenação

```jsx
var nome = window.prompt("Digite seu nome:");

alert("Olá, " + nome + "! Seja bem-vindo(a)!");

```

Quando o trecho de código é executado, o seguinte acontece:

1. `var nome = window.prompt("Digite seu nome:");`
    - Uma caixa de diálogo aparece no navegador com a mensagem "Digite seu nome:".
    - O usuário deve inserir seu nome e clicar em "OK".
    - O nome inserido pelo usuário é armazenado na variável `nome`.
2. `alert("Olá, " + nome + "! Seja bem-vindo(a)!");`
    - Uma outra caixa de diálogo aparece no navegador.
    - Esta caixa exibe a mensagem "Olá, [nome]! Seja bem-vindo(a)!".
    - `[nome]` é substituído pelo nome inserido pelo usuário na etapa anterior.

Por exemplo, se o usuário inserir "Carlos" na caixa de diálogo do prompt, a mensagem exibida no alerta será: "Olá, Carlos! Seja bem-vindo(a)!".

/* + serve para adição e concatenação number + number == adição string + string ou string + number concatenação*/

```jsx
// Exemplo de adição
var numero1 = 10;
var numero2 = 5;
var soma = numero1 + numero2;
console.log("A soma de " + numero1 + " e " + numero2 + " é: " + soma);

// Exemplo de concatenação
var parte1 = "Olá, ";
var parte2 = "mundo!";
var mensagem = parte1 + parte2;
console.log(mensagem);

```

```
A soma de 10 e 5 é: 15
Olá, mundo!

```

Conversão de string para number: Number(n); Number.parseInt(n); Number.parseFloat(n)/*Int numero inteiro, Float números decimais*/

```jsx

var idade = '18'
typeof idade
Number(idade)
typeof idade
console.log(idade+5 + 'anos')

o resultado vai ser: 23 anos

```

(// comentário de 1 linha,  /**/ comentário com mias de 1 linha, comentários não influenciam o código mas ajuda a saber o que cada coisa faz)

Conversão de number para string: String(n); n,ToString

```jsx
var idade = 18
typeof idade
String(idade)
typeof idade
console.log(idade+5 + 'anos')

o resultado vai ser: 185 anos
```

Template String

`string ${variante}` //só funciona entre crase 

```jsx
var horas = 13
console.log(`Agora são ${horas} horas`)
```

S.Length // mostra quantos caracteres tem uma palavra ou frase

```jsx
var nome = 'PK'
var quant = S.length(nome)
console.log(`${nome} tem ${quant} caracteres`)
```

S.toUpperCase// deixa as letras tudo em maiúsculas

```jsx
var nome = 'pk'
S.toUpperCase(nome)
console.log(nome)
/* caso você não queira que a variavel em sí fique em maiusculo só em momentos especificos
pode fazer console.log(S.toUpperCase(nome))*/
```

S.toLowerCase// deixa as letras tudo em minúsculas

```jsx
var nome = 'PK'
S.toLowerCase(nome)
console.log(nome)
//console.log(S.toLowerCase(nome))
```

Document.write()//mostra escrita na tela

```jsx
document.write('olá mundo!')
```

Document.writeln()// deveria ir para linha de baixo

```jsx
document.writeln('olá mundo!')
```

Da para usar alguns html dentro do script entre crase

<Strong></Strong> // deixa em negrito

<br/> quebra para a linha de baixo

```jsx
document.write(´olá <stong> mundo </strong>! </br>´)
```

N1.toFixed(n)// casas decimais

```jsx
var numero = 10
numero = numero.toFixed(2)
console.log(numero)
```

N1.’comando’().replace(‘n’,’n’) //troca um pelo outro

```jsx
var numero = 10
numero = numero.toFixed(2)
numero.replace('.' , ',')
console.log(numero)
```

N1.toLocaleString(‘idioma’, {style: ‘currency’, currency ‘moeda’})// converte para moeda só funciona com  number

```jsx
var dinheiro = 100
dinheiro.toLocalString('pt-br', {style: 'currency', currency 'moeda'})
console.log(dinheiro)
```

# Aula 07

Operadores

Aritméticos:

- adição 5+2 == 7
- subtração 5-2 == 3
- multiplicação 5*2 == 10
- / divisão 5/2 == 2.5
- % resto divisão 5%2 == 1
- * potencia 5**2 == 25

Ordem de predencia

- () //básico tudo nos parênteses vem primeiro
- ** // potencia
- /, %, *  /*multiplicação, divisão, e resto de divisão, faz o que aparecer primeiro da esquerda para a direita*/
- +, - //soma e subtração sempre os últimos caso não esteja em parênteses

Auto atribuição

N = N + N /* o valor de N + ele mesmo, se N for 5 o valor de N passaria a ser 10*/

N+= (n)//se acima o valor de N é 10, n+= 5, N passaria a ser  15

N-=(n)/* se acima o valor de N foi para 15, N-= 3, N passaria a ser 12*/

N++ e N— /*soma ou subtrai 1 se N agora é 12 N++ ficaria 13 e N—11*/

```jsx
var N = 5
N = N + N
console.log(N)
N+= 5
console.log(N)
N-= 3
console.log(N)
N++
console.log(N)
N--
console.log(N)
```

/*lembrando letra MAIUSCULAS e minúsculas tem diferença se você por um N ele vai ser != de n*/

# Aula 08

Operadores relacionais

-  >Maior
-  < Menor
-  >=Maior ou Igual
-  <= Menor ou Igual
-  == igual
-  != Diferente
-  === Idêntico

Operadores lógicos

! == ‘Não’ operador unário (true ou false/ false ou true)

&& == ‘E’ operador binário (só dá certo se os dois valores forem true)

|| == ‘OU’ operador binário (só dá errado se os dois valores forem false)

Ordem de precedência

!

&&

||

Ordem de precedência

1º operadores aritméticos

2º operadores relacionais

3º operadores lógicos

Operador ternário

? : (teste? True : false)

```jsx
Var idade = 18

Var nome = João

Var ConsegueVotar = (idade >= 18)? ‘sim’ : ‘não’

Console.log(´${nome} tem idade suficiente para votar? ${ConsegueVotar}.´

/* o resultado seria: João tem idade suficiente para votar? Sim.*/

//basicamente é assim que funciona o operador ternario
```

# Modulo C

# Aula 09

DOM à Document Object Model

Conjunto de objetos dentro do navegador

Arvore DOM

Window

Location  Document  History

HTML

Head Body

Meta Title / H1 P div

Strong

Parent fica em cima e child fica em baixo

getElementsBy

id = “ ”

class = “ ”

name = “ ”

tag = “ ”

querySelector/All

# == id

. == class

var a = document.querySelector(“div#id”)

a.style.backgroundcolor = “color”

eventos DOM é tudo que se pode acontecer com um objeto

eventos de mouse

- Mouseenter (quando ao seta do mouse entra)
- Mousemove (quando a seta do mouse se move)
- Mousedown (quando aperta e segura o botão do mouse)
- Mouseup (quando solta o botão do mouse)
- Click (quando clica no botão do mouse)
- Mouseout (quando sai com a seta do mouse)

Função: linha que só executa quando um evento ocorrer

Função com varias linhas se chama bloco, bloco começa com {}

Function *ação* (parâmetro) {}

```jsx
var verify = document.querySelector('input#id)
verify.addEventListener('click', clicar)

function clicar(){
verify.InnerHTML = 'verificado'
}
```

# Aula 11

Condições

If(condição){

True} else{

False}

```jsx
var numero = 5
var valor = 10
if(numero < valor){
console.log(`${numero} é menor que ${valor} `)
}else{
console.log(`${numero} é maior que ${valor} `)
}
```

Condição simples

If(){

True}

```jsx
if(1 < 10){
		console.log('esse valor é menor que 10')
}
```

Arquivo JS // console.log() /*coloquei isso para lembrar que para algo aparecer no console tem que usar essse comando mas vai usar isso poucas vezes já que a maioria do trabalho é para sites ai tem o poderoso HTML*/

Não esquecer # para id e . para class CSS //outro lembrete

# Aula 12

Condições aninhadas

If(cond1){

Bloco1

}else if(cond2){

Bloco 2

}else{

Bloco3

}

```jsx
var numero = 10
if(numero < 10){
	console.log(`${numero} é uma unidade`)
}else if(numero < 100 && numero > 9){
	console.log(`${numero} é uma dezena`)
}else if(numero < 1000 && numero > 99){
	console.log(`${numero} é uma centena`)
}else{
	console.log(`${numero} é uma unidade de milhar ou mais`)
}

```

Condições múltiplas

Switch (expressão){

Case 1:

break

Case 2:

break

Case 3:

break

Default:

break

}

```jsx

let diaDaSemana = 3; // Domingo é 0, Segunda-feira é 1, e assim por diante

// Usando switch para determinar o nome do dia
switch (diaDaSemana) {
    case 0:
        console.log('Domingo');
        break;
    case 1:
        console.log('Segunda-feira');
        break;
    case 2:
        console.log('Terça-feira');
        break;
    case 3:
        console.log('Quarta-feira');
        break;
    case 4:
        console.log('Quinta-feira');
        break;
    case 5:
        console.log('Sexta-feira');
        break;
    case 6:
        console.log('Sábado');
        break;
    default:
        console.log('Número do dia inválido');
        break;
}

```

Depois de cada case obrigatório por um ‘break’ default opcional mas é melhor por.

- Use **`let`** quando precisar de escopo de bloco e deseja garantir que a variável não seja redeclarada no mesmo bloco ou para escopo global.
- Use **`const`** quando quiser garantir que a variável não seja reatribuída, mas permita a modificação das propriedades ou elementos se a variável contiver um objeto ou array.

Em geral, é recomendável usar `let` e `const` em vez de `var`, pois eles oferecem um comportamento mais previsível e menos propenso a erros.

//eu mesmo vou começar a usar let

# Modulo E

O sistema de repetições com teste no inicio são `while` com teste no final são `do while` com controle se usa o `for`

# Aula 13

O sistema de repetições é usado quando precisa repetir algo varias vezes /*oh my god não me diga*/ enquanto alguma condição não é atendida.

```jsx
let c = 1
while(c <= 10){
console.log(`passo ${c}`)
c++ /*lembra quando se põe o valor com ++ adiciona +1 ou seja isso vai 
ficar adicionando +1 a nossa variavel até chegar em 10*/
}
```

```jsx
let c = 1

do {
  console.log(`passo ${c}`)
  c++
} while (c <= 10)
 

```

```jsx
for(let c = 1; c <= 10; c++){
	console.log(`passo ${c}`)
}
```

vou por aqui um exercício e vocês se virem pra resolver isso com HTML e CSS eu sei que to anotando coisas de JS porém não sei um jeito de explicar ele.

```jsx
 //fazendo um let para poder servir dentro e fora do escopo e não dar nenhum problema
 let n1 = document.querySelector('#num')
 //criando um const para a variavel de evento
const btn = document.querySelector('#btn')
//adicionando o evento a variavel com JS
btn.addEventListener('click', clicar)
//criando a let result para mostrar o resultado no HTML
let result = document.querySelector('#result')
//fazendo o result mostrar uma mensagem para não ficar em branco até o evento
 result.innerHTML = 'aguardando valor...'
 //criando o que ira acontecer na funcção clicar caso seja ativado o evento 'click'
function clicar(){
//criando um if para se caso não inserir nenhum dado e clicar a aparecer uma mensagem de erro
    if(n1.value.length == 0){
        result.innerHTML = 'insira um valor'
        //isso aqui é muito importante o return vai evitar que o codigo continue rodando caso esse if seja true
        return;
    }
			//criando let num para converter string para number
    const num = Number(n1.value)
    //criando let vazio para o resultado
    let algo = ''
   
   /*aqui estou criando um if para que não de erro quando 
   inserir um numero menor igual ou maior a 10*/
    if(num <= 10 || num > 10){
		    // o for esta adicionando +1 a i até chegar no 10
        for(let i = 1; i <= 10; i++ ){
		        //criando a conta para o resultado
           let multi = num * i
           /*num vai ser o numero inserido, i ira de 1 a 10 e multi mostrara 
           o resultado da multiplicação entre eles*/
            algo += `${num}x${i} = ${multi}</br>`
        }
        //aqui fara o resultado ser mostrado na tela
        result.innerHTML = algo
    }
}
/*isso é o codigo para fazer uma tabuada aquele </br> e para ir pra linha de
 baixo ou seja enquanto i não chegar até 10 ele continuara 
 pondo resultados embaixo totalizando uma tabuada do 1 a 10*/
```

# Modulo F

Arrays/Vetores/Variáveis compostas 💀☠️

# Aula 14

Como sou um bom brasileiro vou chamar de vetor, em resumo um vetor é uma variável que tem vários elementos cada elemento com um valor e cada valor com seu índice

```jsx
let num = [1,2,3]
/* 'num' é o vetor
[ , , ] é o elemento
1 2 3 é o conteudo/valor
e existe o indice que são a localizção do conteudo que começa em 0
ou seja nesse vetor temos o indice 0,1,2*/

```

Vamos para mais umas dicas de vetores, no caso de variáveis simples além de não poder criar mais de 1 valor, também não pode adicionar mais de 1 valor, segue meu exemplo para entender melhor.

```jsx
//aqui criamos num valendo 1
let num = 1
//aqui adicionamos a num o valor 4, aqule 1 não existe mais
num = 4
//aqui vamos dar um console.log para confirmar
console.log(num)
```

agora vamos mostrar a diferença no vetor.

```jsx
//aqui criamos num com todos esses valores
let num = [2,4,1,3]

/*aqui adicionamos ao indice 4 o valor 5 (nesse caso o valor entre colchetes é o indice)
esse metodo serve para quando você quer adicionar um valor em uma posição especifca*/
num[4] = 5

/*aqui estamos adicionando o valor 0 o comando 
.push diz para o JS que você quer por o valor na ultima posição do indice*/
num.push(0)

//caso você queira saber quantos elementos (elementos e não indice) tem no seu vetor use
num.length

//caso você queira por em ordem crescente, mesmo que esteja tudo embaralhado
num.sort()

/*para saber qual é o indice do valor temos o .indexOf()
o numero que fica dentro do parenteses é o valor/conteudo e não o indice lembre-se
disso 
*/

num.indexOf(4)

//use isto para testar tudo que eu falei
console.log(`nosso vetor é o ${num}, na primeira poisção está o numero ${num[0]}, 
o vetor tem ${num.length} elementos, 
e essa é a ordem do menor ao maior ${num.sort()}`)

let pos = num.indexOf(4)
console.log(`o valor proucurado está no indice: ${pos}`)

/*caso voce insria um valor que n tenha no vetor 
ele vai retorna -1 que é igual a não existe*/

```

aqui é um método para mostrar os valores de uma forma mais ‘bonitinha’

```jsx

for(let i = 0 ; i < num.length ; i++){
    num.sort()
    console.log(`indice ${i} e nele está o valor ${num[i]}`)
}
/* i ele vai ser o indice começando sempre do 0, vai ser feito
 o preocesso de repetição padrão
ali no console o num[i] vai trazer os valores de cada indice*/

```

algo interessante que pensei depois de um tempo (literalmente os vetores serve pra isso mas eu fui noob) da pra simplificar muito os cod. com ele

```jsx
let a = 1
let b = 10
for(let i = a; i<=b; i++){
	console.log(`${a} X ${i} = ${a*i}`)
}
```

aqui ja é um codigo curto, mas esse estilo que fiz pode simplificar muito um codigo longo

```jsx
let a = [1,10]
for(let i = a[0]; i <= a[1]; i++){
	console.log(`${a[0]} X ${i} = ${a[0]*i}`)
}

```

```jsx
for(let j in num){
    console.log(`indice ${j} e nele está o valor ${num[j]}`)
}
/*esse metodo serve apenas para vetores e objetos (no caso em JS vetores são considerados
objetos também)*/
```

aqui vou mostrar um array + objeto

```jsx
let user = [
    {
        nome: 'PK',
        idade: 21,
        casado: true, 
        conjuge: null
    },
    {
        nome: 'higor',
        idade: 18,
        casado: false, 
        conjuge: null
    }
     
]

  user.forEach((u) => {
    if(u.casado === true){
        u.conjuge = 'dona bonita'
    }
  })

   console.log(user)
```

# Aula 16 Funções

uma função tem Chamada, Parâmetro, Ação e Retorno, nem todas as funções tem parâmetros ou retornos

funções são `ações` executadas quando são `chamadas` ou em decorrência de algum `evento`

uma `função` pode receber `parâmetros` e retornar um `resultado`
