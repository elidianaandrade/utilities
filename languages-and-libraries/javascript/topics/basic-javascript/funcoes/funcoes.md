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