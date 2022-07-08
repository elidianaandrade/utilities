<div align="center">
  <img alt="JavaScript" height="100" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/js-square.svg">
</div>

<br>

# 💻 Funções
📝 Anotações do Curso de JavaScript do [Curso em Vídeo](https://youtube.com/playlist?list=PLntvgXM11X6pi7mW0O4ZmfUI1xDSIbmTm) e dos Cursos de JavaScript da [Digital Innovation One](https://www.dio.me/)

<br>

## **⚙ 1. Estrutura**
- Variáveis criadas dentro de uma função, podem ser utilizadas apenas nela.

```javascript
function nome(parametros) {
  // instruções
}
```

### **Return**
- A declaração `return` finaliza a execução de uma função.
```javascript
function nome(parametros) {
  // instruções
  return; // valor de retorno
}
```

<br>

## 🔡 2. Tipos de funções

### **2.1 Função anônima**
- São funções que representam expressões

```javascript
const soma = function (a,b) {
  return a + b;
}

soma(1,2) // 3
soma (2,4) // 6
```

<br>

### **2.2 Função autoinvocável**
- IIFE (Immediately Invoked Function Expression)

```javascript
(
  function() {
    let name = "Digital Innovation One"
    return name;
  }
)();

// Digital Innovation One
```

```javascript
(
  function(a, b) {
    return a + b;
  }
)(1, 2);

// 3
```

```javascript
  const soma3 = (
    function() {
      return a + b;
  }
)(1, 2);

console.log(soma3) // 3
```

<br>

### **2.3 Callbacks**
- Função passada como argumento para outra.

```javascript
const calc = function(operacao,num1,num2){
  return operacao(num1, num2);
}

const soma = function(num1,num2){
  return num1 + num2;
}

const sub = function(num1,num2){
  return num1 - num2;
}

const resultSoma = calc(soma, 1, 2);
const resultSub = calc(sub, 1, 2);

console.log(resultSub); // -1
console.log(resultSoma); // 3
```

<br>

## 🔗 3. Parâmetros

### **3.1 Objeto "arguments**
- Array com todos os parâmetros passados quando a função foi invocada.

```javascript
function showArgs(){
  return arguments;
}
```

### **3.2 Arrays**

### **3.2.1 Spread**
- Forma de lidar separadamente com elementos;
- Utilizado quando está chamando a função.

```javascript
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3]

console.log(sum(...numbers));
```

### **3.2.2 Rest**
- Combina os argumentos em um array;
- Utilizado quando está declarando a função.

```javascript
function confereTamanho(...args) {
  console.log(args.length)
}

confereTamanho() // 0
confereTamanho(1, 2) // 2
confereTamanho (3, 4, 5) // 3
```

### **3.3 Objetos**
- Entre 

```javascript
const user = {
  id: 42,
  displayName: 'jdoe',
  fullName: {
    firstName: 'John',
    lastName: 'Doe'
  }
};

function userId({id}) {
  return id;
}

function getFullName({ fullName: {firstName: 'John', lastName: 'Doe'}}) {
  return '${first} ${last}';
}

userId(user)
// 42

getFullName(user)
// John Doe
```

<br>

## 🔁 4. Loops

### **4.1 If / else**
- If: onde consta a primeira declaração, que ocorre caso seja verdadeira;
- Else: onde consta a segunda declaração, que ocorre caso a primeira seja falsa.
- JavaScript não possui elseif, são sempre separadas.
 
```javascript
function numeroPositivo(num) {
  let resultado;
  
  if(num < 0) {
    resultado = false;
  } else {
    resultado = true;
  }

  return resultado;
}

numeroPositivo(4)
// true

numeroPositivo(-5)
// false
```


```javascript
function numeroPositivo(num) {
  const ehNegativo = num < 0;
  
  if(ehNegativo) {
    return false;
  }

  return true;
}
```

```javascript
function numeroPositivo(num) {
  const ehNegativo = num < 0;
  const maiorQueDez = num > 10;
  
  if(ehNegativo) {
    return "Esse número é negativo!";
  } else if (!ehNegativo && maiorQueDez) {
    return "Esse número é positivo e maior que 10!"
  }

  return "Esse número é positivo!";
}
```

### **4.2 Switch / case**
- Compara tipo e valor (===);
- É sempre necessário um valor "default";
- Indicado quando se precisa comparar muitos valores.

```javascript
function getAnimal(id) {
  switch(id) {
    case 1:
      return "cão";
    case 2:
      return "gato";
    case 3:
      return "pássaro";
    default:
      return "peixe";
  }
}

getAnimal(1) // cão
getAnimal(4) // peixe
getAnimal("1") // peixe
```

### **4.3 for**
- Loop dentro de elementos iteráveis (arrays, strings)

```javascript
function multiplicaPorDois(arr) {
  let multiplicados = [];

  for(let i = 0; i < arr.length; i++) {
    multiplicados.push(arr[i] * 2);
  }

  return multiplicados;
}

const meusNumeros = [5, 20, 400, 254, 40];
    
multiplicadoPorDois(meusNumeros);
// [10, 40, 800, 508, 80]
```

### **4.3.1 for...in**
- Loop entre propriedades enumeráveis de um objeto.

```javascript
function forInExemplo(obj) {
  for(prop in obj) {
    console.log(prop);
  }
}

const meuObjeto = {
  nome: "Eli",
  idade: "23",
  cidade: "Savador"
}

forInExemplo(meuObjeto);
// nome
// idade
// cidade
```

```javascript
function forInExemplo(obj) {
  for(prop in obj) {
    console.log(obj[prop]);
  }
}

const meuObjeto = {
  nome: "Eli",
  idade: "23",
  cidade: "Savador"
}

forInExemplo(meuObjeto);
// Eli
// 23
// Salvador
```

### **4.3.2 for...off**
- Loop entre estruturas iteráveis (arrays, strings).

```javascript
function logLetras(palavra) {
  for (letra of palavra) {
    console.log(letra);
  }
}

const palavra = "abacaxi";

logLetras(palavra)
// a
// b
// a
// c
// a
// x
// i
```

```javascript
function logNumeros(nums) {
  for (num of nums) {
    console.log(num);
  }
}

const nums = [30, 20, 233, 2]

logLetras(nums)
// 30
// 20
// 233
// 2
```

### **4.4 While / do...while**

#### **4.4.1 While**
- Executa instruções até que a condição se torne falsa.

```javascript
function exemploWhile() {
  let num = 0

  while(num <= 5){
    console.log(num);
    num++;
  }
}

exemploWhile()
// 0
// 1
// 2
// 3
// 4
// 5
```

#### **4.4.2 Do while**
- Executa instruções até que a condição se torne falsa. Contudo a primeira execução sempre ocorre.

```javascript
function exemploDoWhile() {
  let num = 0

  do {
    console.log(num);
    num++;
  } while(num <= 5)
}

exemploDoWhile()
// 0
// 1
// 2
// 3
// 4
// 5
```

```javascript
function exemploDoWhile() {
  let num = 6

  do {
    console.log(num);
    num++;
  } while(num <= 5)
}

exemploDoWhile()
// 6
```

<br>

##  5. This
- A palavra reservada This é uma referência de contexto.

<br>

## 🏹 6. Arrow functions
- Caso a função possua apenas uma linha, não é necessário utilizar chaves e return;
- Caso a função possua apenas um parâmetro, não é necessário utilizar os parênteses;
- Não faz hoisting;
- "This" sempre será o objeto global, métodos para alterar o valor não vão funcionar;
- Não existe o objeto "arguments";
- O construtor também não pode ser utilizado (ex.: new MeuObjeto()).

```javascript
const helloWorld = function() {
  return "Hello World";
} 
```

```javascript
const helloWorld = () => {
  return "Hello World";
} 
```

```javascript
const helloWorld = () => "Hello World";
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