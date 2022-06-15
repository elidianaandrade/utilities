<div align="center">
  <img alt="JavaScript" height="100" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/js-square.svg">
</div>

<br>

# 💻 Módulos
📝 Anotações do Curso Módulos em JavaScript do [Curso em Vídeo](https://youtube.com/playlist?list=PLntvgXM11X6pi7mW0O4ZmfUI1xDSIbmTm) e dos Cursos de JavaScript da [Digital Innovation One](https://www.dio.me/)
<br>


## 📄 1. O que são?
- São arquivos JavaScript que tem a capacidade de exportar e importar informações de outros arquivos do mesmo tipo.

<br>

### **2. Exportar**

#### **2.1.1 Named exports**
```javascript
export function mostrarIdade(pessoa) {
  return `A idade de ${pessoa.nome} é ${pessoa.idade}`;
}

export function mostrarCidade(pessoa) {
  return `A cidade de ${pessoa.nome} é ${pessoa.cidade}`;
};

export function mostrarHobby(pessoa) {
  return `O hobby de ${pessoa.nome} é ${pessoa.hobby}`
}
```

```javascript
function mostrarIdade(pessoa) {
  return `A idade de ${pessoa.nome} é ${pessoa.idade}`;
}

function mostrarCidade(pessoa) {
  return `A cidade de ${pessoa.nome} é ${pessoa.cidade}`;
};

function mostrarHobby(pessoa) {
  return `O hobby de ${pessoa.nome} é ${pessoa.hobby}`
}

export {
  mostrarIdade,
  mostrarCidade,
  mostrarHobby
}
```

#### **2.1.2 Default exports**
- Só pode haver um por arquivo;
- Será o retorno padrão do seu arquivo.

```javascript
function mostrarIdade(pessoa) {
  return `A idade de ${pessoa.nome} é ${pessoa.idade}`;
}

function mostrarCidade(pessoa) {
  return `A cidade de ${pessoa.nome} é ${pessoa.cidade}`;
};

function mostrarHobby(pessoa) {
  return `O hobby de ${pessoa.nome} é ${pessoa.hobby}`
}

export {
  mostrarIdade,
  mostrarCidade,
}

export default mostrarHobby;
```

<br>

### **3. Importar**

#### **3.2.1 Importar Named exports**
```javascript
import {funcao, variavel, classe} from './arquivo.js'
```

#### **3.2.2 Importar Default exports**
```javascript
import valorDefault from './arquivo.js'
```

#### **3.2.3 Trocando nome de imports**
```javascript
import {arquivo as Apelido} from './arquivo.js';

Apelido.metodo();
```

#### **3.2.4 Importando todos os dados de um arquivo**

```javascript
import * as INFOS from './arquivo.js';

INFO.metodoA();

console.log(INFOS.variavel);
```

### **4. Vinculando ao HTML**

```javascript
<script type="module" src="./main.js"></script>
```

<br>

## 📋 Notas
- Módulos sempre estão em "strict mode";
- Extensões podem ser .js e .mjs;
- Ao importar sempre utilize "./" como ponto de partida.

<br>

## 📚 Referências e leituras adicionais
- Curso de JavaScript do [Curso em Vídeo](https://youtube.com/playlist?list=PLntvgXM11X6pi7mW0O4ZmfUI1xDSIbmTm)
- Referência JavaScript da [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
- Cursos de JavaScript da [Digital Innovation One](https://www.dio.me/)