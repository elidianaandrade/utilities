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

## ➕ Operadores

Operador  | Definição                                             |  Exemplo
:-------: | ----------------------------------------------------- | -----------------------------------------------
 ͏+        | Adição para tipo number, e concatenação para string   | `2+2 = 4`; `'2'+'2'= 22`;`'e'+'u' = eu`  
 ͏-        | Subtração para tipo number                            | `2-1 = 1`
 ͏*        | Multiplicação para tipo number                        | `4*2 = 8`
  /       | Divisão Real para tipo number                         | `5/2 = 2.5`
 ͏%        | Divisão Inteira (resto da divisão) para tipo number   | `5%2 = 1`  
  ͏**      | Potenciação para tipo number                          | `5**2 = 25`  


<br>

## 📚 Referências
- Referência JavaScript da [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- Curso de JavaScript do [Curso em Vídeo](https://youtube.com/playlist?list=PLntvgXM11X6pi7mW0O4ZmfUI1xDSIbmTm)
- Cursos de JavaScript da [Digital Innovation One](https://www.dio.me/)