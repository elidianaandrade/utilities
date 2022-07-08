<div align="center">
  <img alt="JavaScript" height="100" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/js-square.svg">
</div>

<br>

# 💻 Introdução ao JavaScript
👩‍💻 Linguagem de programação interpretada estruturada, de script, client side.
<br>
📑 [Documentação ECMAScript](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/) (linguagem JavaScript padronizada)
<br>
📝 Anotações do Curso de JavaScript do [Curso em Vídeo](https://youtube.com/playlist?list=PLntvgXM11X6pi7mW0O4ZmfUI1xDSIbmTm) e dos Cursos de JavaScript da [Digital Innovation One](https://www.dio.me/)

<br>

## ⏳︎ 1. Breve histórico 
- Criado em 1995 por **Brendan Eich** a pedido da **Netscape**;
- O pedido visava uma linguagem com **mais funcionalidades que o HTML**;
- Batizada a princípio de linguagem Mocha, seguida de **LiveScript**;
- Devido ao sucesso da linguagem **Java** na época, seu nome passou a ser **JavaScript** (estratéga de marketing);
- Microsoft lança o **JScript**, que rodava apenas no navegador **Internet Explorer**;
- Então, em 1997, a Netscape cede o código JavaScript para a **ECMA** padronizar, surgindo a **ECMAScript** (linguagem de scripts padronizada);
- A padronização pela **ECMA** possibilitou o funcionamento da linguagem em todos os navegadores.

<br>

## 🔡 2. Variáveis e constantes

### **2.1 Identificadores**
- O mais comum é iniciar com **letra**, mas também podem ser **$** ou **_** ;
- Não pode iniciar com número, mas é possível utilizar letras e números;
- Não pode utilizar **palavras reservadas**, como **function** etc.;
- Não pode conter **espaço** entre as palavras;
- Pode utilizar símbolos e acentos;
- É **case-sensitive** (uso de maiúsculas e menúsculas fazem diferença);
- Adote nomes coerentes;

<br>

Case Type                   | Exemplo
--------------------------- | ---------------------------------------
Original Variable as String | exemplo case type
Camel Case                  | exemploCaseType **(utilizado para nomear funções e variáveis)**
Snake Case                  | exemplo_case_type
Kekab Case                  | exemplo-case-type
Pascal Case                 | ExemploCaseType
Upper Case Snake Case       | EXEMPLO_CASE_TYPE **(utilizado para nomear constantes)**

<br>

### **2.2 Var, let e const**


Tipo      | Descrição            | Escopo          | Declaração      | Redeclaração             | Reatribuição            | [Hoisting](https://developer.mozilla.org/pt-BR/docs/Glossary/Hoisting)
--------- | ---------------------|-----------------|-----------------|--------------------------|-------------------------|--------------
**var**   | identifica variáveis | global ou local | camelCase       | pode ser redeclarada     | pode ser reatribuída    | faz hoisting
**let**   | identifica variáveis | bloco           | camelCase       | não pode ser redeclarada | pode ser reatribuída    | não faz hoisting
**const** | identifica constantes| bloco           | SNAKE_UPPER_CASE| não pode ser redeclarada | não pode ser reatribuída| não faz hoisting


<br>

```javascript
var a = 1;
var b = 2;

if (a === 1) {
  var a = 11; // o escopo é global
  let b = 22; // o escopo é dentro do bloco if

  console.log(a); // 11
  console.log(b); // 22
}

console.log(a); // 11
console.log(b); // 2
```

<br>

> **Hoisting:** "as declarações de variável e função são colocadas na memória durante a fase de compilação. O JavaScript apenas eleva (hoists) as declarações, não as inicializações. Se uma variável for declarada e inicializada após usá-la, o valor será undefined. Se você declarar a variável depois que ela for usada, mas inicializá-la antecipadamente, ela retornará o valor." [Fonte: MDN](https://developer.mozilla.org/pt-BR/docs/Glossary/Hoisting). *Antes de utilizar **const**, deve declarar e atribuir um valor, e antes de usar **let** deve ao menos declarar.

<br>

## **3. Tipos**
- JavaScript é uma linguagem de tipagem dinâmica, então ao declarar um valor **não** é necessário especificar o tipo dele;
- A estrutura de dados é formada por dados primitivos e compostos / não primitivos.

<br>

### **3.1 Tipos Primitivos**

<br>

Classificação               | Definição
--------------------------- | ---------------------------------------
string                      | sequências de caracteres alfanuméricos ( `""`, `''`, ` `` ` )
number                      | números (Infinity, NaN)
bolean                      | true or false
null                        | nulo
undefined                   | não definido
object                      | (Array)
function                    | função 

<br>

#### **3.1.1 Formatando strings**
```javascript
var js = 'JavaScript' 
'Eu estou aprendendo js' // não faz interpolação
'Eu estou aprendendo' + js // usa concatenação
`Eu estou aprendendo ${js}` // usa template string
```
```javascript
var js = 'JavaScript' 
js.length // quantos caracteres a string tem
js.toUpperCase() // tudo para 'MAIÚSCULAS'
js.toLowerCase() // tudo para 'minúsculas'
```

<br>

#### **3.1.2 Formatando números**
```javascript
var n1 = 2500.5
n1

n1.toFixed(2) // fixo com 2 casas
2500.50

n1.toFixed(2).replace('.',',') // substituindo ponto por vírgula
2500,50
```
```javascript
var n1 = 2500.5
n1.toLocaleString('pt-BR', {style: 'currency', currency: 'BRL'})
'RS 2.500,50'
```

<br>

#### **3.1.4 Booleans**
- True or false.

```javascript
let validation = 3 === 0 // false
validation = 3 === 3 // true

validation.toString()
"true"

!validation
false
```

<br>

#### **3.1.5 Arrays**
- Lista iterável de elementos;
- Primeiro índice é **0**.

```javascript
let array = []

array.push() // adiciona um elemento no final da lista

array.pop() // retira o último elemento do array

array.shift() // retira o primeiro elemento do array

array.unshift() // adiciona um elemento no começo da lista

array.includes()

array.every()

array.length()

array.some()

array.reverse()
```

<br>

#### **3.1.6 Objetos**
- Estrutura do tipo chave e valor

```javascript
let person = {
    name: 'Eli',  // name = chave, Eli = valor
    age: 23       // age = chave, 23 = valor
};

Object.values(person)
(2) ["Eli", 23]

Object.keys(person)
(2) ["name", "age"]

person.name
"Eli"

person["name"]
"Eli"
```

<br>

#### **3.1.7 Empty, undefined e null**
- empty = declarado, vazio, sem valor;
- null = declarado, valor definido como nulo;
- undefined = não declarado, valor indefinido.

<br>

## ➕ 4. Operadores
- aritméticos
- atribuição
- relacionais
- lógicos
- ternário

<br>

### **4.1 Operadores Aritméticos**

Operador  | Definição                                             |  Exemplo
:-------: | ----------------------------------------------------- | -----------------------------------------------
 ͏+        | Adição para tipo number, e concatenação para string   | `2+2 = 4`; `'2'+'2'= 22`;`'e'+'u' = eu`  
 ͏-        | Subtração para tipo number                            | `2-1 = 1`
 ͏*        | Multiplicação para tipo number                        | `4*2 = 8`
  /       | Divisão Real para tipo number                         | `5/2 = 2.5`
 ͏%        | Divisão Inteira (resto da divisão) para tipo number   | `5%2 = 1`  
  ͏**      | Potenciação para tipo number                          | `5**2 = 25`  


<br>

> Atente-se para a **precedência de operadores**. Ex.I: 5 + 6 / 2 = 8. Ex.II: (5 + 3) / 2 = 4.

<br>

#### **4.1.1 Ordem de precedência dos operadores aritméticos**
1. `( )`
2. `**`
3. `* / %`
4. `+ -`

<br>

#### **4.1.2 Atribuições Simples**
```javascript 
// Atribuição Simples
var a = 5 + 3                = 8
var b = a % 5                = 3
var c = 5 * b ** 2           = 45
var d = 10 - a / 2           = 6
var e = 6 * 2 / d            = 2
var f = b % e + 4 / e        = 3

```

<br>

#### **4.1.3 Auto-atribuições**
```javascript 
// Auto-atribuições 
var n = 3
n = n +  4        = 7
n = n -  5        = 2
n = n *  4        = 8
n = n /  2        = 4
n = n ** 2        = 16
n = n %  5        = 1 


// Simplificando
var n = 3
n +=  4        = n = n + 4
n -=  5        = n = n - 5 
n *=  4        = n = n *  4 
n /=  2        = n = n /  2 
n **= 2        = n = n ** 2
n %=  5        = n = n %  5

```

<br>

#### **4.1.4 Incremento**
```javascript 
// Incremento
var x = 5
x = x + 1        = 6  // x+=1
x = x - 1        = 5 // x-=1

// Simplificando ainda mais
x += 1        = x++
x -= 1        = x--

```

<br>

#### **4.1.5 Exemplos**
```javascript 
preço >= 100              // o preço é maior ou igual a 100?
idade < 18                // a idade é menor do que 18?
curso == 'JavaScript'     // o curso é JavaScript? 
n1 != n2                  // o primeiro número é diferente do segundo?
```

<br>

#### **4.1.6 Identidade**
```javascript 
5 == 5       = true
5 == '5'     = true
5 === '5'    = false
5 === 5      = true

```

<br>

#### **4.1.7 Lógicos**
```javascript 
// Lógicos
!       // negação
&&      // conjunção (um e outro)
||      // disjunção (um ou outro)

// Exemplos
idade >= 15 && idade <= 17          // a idade está entre 15 e 17?
estado == 'RJ' || estado == 'SP'    // o estado é RJ ou SP?
salário > 1500 && sexo != 'M'       // o salário é acima de 1500 e não é homem?
```

<br>

> Atente-se para a **precedência de operadores**

<br>

#### **4.1.8 Ordem de precedência**
1. `( )`  `**`  `/`    ...
2. `>` `<`  `>=`       ...
3. `!`
4. `&&`
5. `||`


<br>

### **4.2 Ternário**

- Junta 3 operandos: `teste` `?` `true` `:` `false`
- Exemplo: `média >= 7.0` `?` `'Aprovado'` `:` `'Reprovado'`

```javascript
// Exemplo I
var média = 5.5
`média >= 7.0` `?` `'Aprovado'` `:` `'Reprovado'`
'Reprovado'


// Exemplo II
var x = 8
var res = x % 2 == 0 ? 5 : 9
res = 5


// Exemplo III
var r = idade >= 18 ? 'Maior' : 'Menor'
idade = 15
r = 'Menor'
```

<br>

## 📚 Referências e leituras adicionais
- Curso de JavaScript do [Curso em Vídeo](https://youtube.com/playlist?list=PLntvgXM11X6pi7mW0O4ZmfUI1xDSIbmTm)
- Cursos de JavaScript da [Digital Innovation One](https://www.dio.me/)
- Referência JavaScript da [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

<br>

<div align="right">
  <a href="#top">
    <img alt="Up" height="25" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/angle-up.svg">
  </a>
</div>