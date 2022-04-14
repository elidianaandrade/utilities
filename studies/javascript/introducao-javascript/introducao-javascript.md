<div align="center">
  <img alt="JavaScript" height="100" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/js-square.svg">
</div>

<br>

# 💻 Introdução ao JavaScript
👩‍💻 Linguagem de programação interpretada estruturada, de script, client side.
<br>
📑 [Documentação ECMAScript](https://www.ecma-international.org/publications-and-standards/standards/ecma-262/) (linguagem JavaScript padronizada.)

<br>

## ⏳︎ Breve histórico 
- Criado em 1995 por **Brendan Eich** a pedido da **Netscape**;
- O pedido visava uma linguagem com **mais funcionalidades que o HTML**;
- Batizada a princípio de linguagem Mocha, seguida de **LiveScript**;
- Devido ao sucesso da linguagem **Java** na época, seu nome passou a ser **JavaScript** (estratéga de marketing);
- Microsoft lança o **JScript**, que rodava apenas no navegador **Internet Explorer**;
- Então, em 1997, a Netscape cede o código JavaScript para a **ECMA** padronizar, surgindo a **ECMAScript** (linguagem de scripts padronizada);
- A padronização pela **ECMA** possibilitou o funcionamento da linguagem em todos os navegadores.

<br>

## ⌨ Comandos básicos 

Classificação               | Definição
--------------------------- | ---------------------------------------
typeof                      | tipo de 

 <br>

### **Comentáros**
- `//` para comentar uma única linha;
- `/* */` para comentar mais de uma linha


 <br>

## 🔡 Variáveis, Constantes e Tipos Primitivos

### **Identificadores**
- O mais comum é iniciar com **letra**, mas também podem ser **$** ou **_** ;
- Não pode iniciar com número, mas é possível utilizar letras e números;
- Não pode utilizar **palavras reservadas**, como **function** etc.;
- Não pode conter **espaço** entre as palavras;
- Pode utilizar símbolos e acentos;
- É **case-sensitive** (uso de maiúsculas e menúsculas fazem diferença);
- Adote nomes coerentes;

### **Variáveis**

```
var nome = prompt ('Qual é seu nome'?)

let

```

<br>

### **Constantes**
```
const
```

<br>

### **Tipos primitivos**
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

### **Formatando strings**
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

### **Formatando números**
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

---

<br>

## ➕ Operadores
- aritméticos
- atribuição
- relacionais
- lógicos
- ternário

### **Operadores Aritméticos**

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

**Ordem de precedência dos operadores aritméticos**
1. `( )`
2. `**`
3. `* / %`
4. `+ -`

<br>


#### **Atribuições Simples**
```javascript 
// Atribuição Simples
var a = 5 + 3                = 8
var b = a % 5                = 3
var c = 5 * b ** 2           = 45
var d = 10 - a / 2           = 6
var e = 6 * 2 / d            = 2
var f = b % e + 4 / e        = 3

```

#### **Auto-atribuições**
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

#### **Incremento**
```javascript 
// Incremento
var x = 5
x = x + 1        = 6  // x+=1
x = x - 1        = 5 // x-=1

// Simplificando ainda mais
x += 1        = x++
x -= 1        = x--

```

#### **Exemplos**
```javascript 
preço >= 100              // o preço é maior ou igual a 100?
idade < 18                // a idade é menor do que 18?
curso == 'JavaScript'     // o curso é JavaScript? 
n1 != n2                  // o primeiro número é diferente do segundo?
```

#### **Identidade**
```javascript 
5 == 5       = true
5 == '5'     = true
5 === '5'    = false
5 === 5      = true

```


#### **Lógicos**
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

**Ordem de precedência**
1. `( )`  `**`  `/`    ...
2. `>` `<`  `>=`       ...
3. `!`
4. `&&`
5. `||`


### Ternário
- Junta 3 operandos
`teste` `?` `true` `:` `false`

<br>

Exemplo:
`média >= 7.0` `?` `'Aprovado'` `:` `'Reprovado'`

```javascript
// Exemplo
var média = 5.5
`média >= 7.0` `?` `'Aprovado'` `:` `'Reprovado'`
'Reprovado'

```





<br>

## 📚 Referências
- Curso de JavaScript do [Curso em Vídeo](https://youtube.com/playlist?list=PLntvgXM11X6pi7mW0O4ZmfUI1xDSIbmTm)
- Referência JavaScript da [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- Cursos de JavaScript da [Digital Innovation One](https://www.dio.me/)