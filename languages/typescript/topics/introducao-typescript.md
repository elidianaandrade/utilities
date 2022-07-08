# 💻 Introdução ao TypeScript
👩‍💻 Linguagem de programação fortemente tipada que se baseia em JavaScript.
<br>
📑 [Documentação](https://www.typescriptlang.org/docs/)
<br>
📝 Anotações do Curso de TypeScript da [Digital Innovation One](https://www.dio.me/)

<br>

## ⚙ 1. Setup

### 1. Criar um arquivo `package.json`
```
npm init
```

#### 2. Instalar [Typescript](https://www.npmjs.com/package/typescript) como dependência de desenvolvimento 
```
npm install --save-dev typescript 

npm install -g typescript

npm install typescript
```

### 3. Instalar [lite-server](https://www.npmjs.com/package/lite-server)
```
npm install lite-server
```
### 4. Adicionar script no package.json
```
    "start": "lite-server"
```
### 5. Gerar `tsconfig.json`
```
npx tsc --init
```

<br>


## 🔡 2. Tipos
- Boolean
- String
- Listas
- Enums
- Any
- Void
- Função
- Unknown
- Never

### 2.1 Primitivos

### 2.2 Any
- Recebe qualquer tipo: number, string, boolean;
- Má prática.

### 2.3 Unknown
-
- Difere do **any** pois necessita de validação
- Boa prática, porém não muito utilizado

### 2.4 Void
- **void** funções que não retornam nada (undefined)


### 2.5 Never
- Código que não foi finalizado

## 🔡 3. Objeto, enum e interface

<br>

Tipo                        | Definição
--------------------------- | -----------------------------------
objeto                      | e
enum                        | grupo de constantes
interface                   | e

? torna opcional

<br>

### Definindo retorno de uma função
```typescript
function somaNumeros (numero1: number, numero2: number): number {
  return numero1 + numero2;
}
```

<br>

## ⚙ Tsconfig
- Target
- lib
- sourceMap
- outDir/rootDir
- strict

<br>

## 📚 Referências e leituras adicionais
- Curso de TypeScript da [Digital Innovation One](https://www.dio.me/)

<br>

<div align="right">
  <a href="#top">
    <img alt="Up" height="25" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/angle-up.svg">
  </a>
</div>