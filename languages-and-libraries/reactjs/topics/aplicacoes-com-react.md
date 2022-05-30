<div align="center">
  <img alt="JavaScript" height="100" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/js-square.svg">
</div>

<br>

# 💻 Aplicações com ReactJS

## CSS componentes e elementos 

### **1. Inline**

```jsx
const divStyle = {
  color: 'blue',
  backgroundImage: 'url('+ imgUrl +')'
};
function HelloWorldComponent() {
  return <div style={divStyle}>Hello World!</div>;
}
```

```jsx
function App() {
  return (
    <HelloWorld style={{ marginTop: '10px' }} />
  )
}
```
**Prós**
- Maneira mais prática e direta
- Ajustes Rápidos
- Testes de Estilo

**Contras**
- Difícil manutenção


### **2. Classes**
```css
.div-style {
  color: blue;
  background: url('');
}
```
```jsx
import './HelloWorldComponent.css';

function HelloWorldComponent() {
  return <div className="div-style">Hello World!</div>;
}
```
**Prós**
- Em JSX, define-se classes pelo atributo className 
    - Maneira mais prática e direta

**Contras**
- Difícil manutenção
- Pouca flexibilidade 
- Conflitos com nomes


### **3. CSS in JS**
```
npm install --save styled-components
```

```jsx
const DivStyle = stylled.div
  color: 'blue';
  backgroundImage: url('${props => props.imgUrl}');

function HelloWorldComponent() {
  const url = ;
  return <DivStyle imageUrl={url}>Hello World</DivStyle>
}
```
**Vantagens**
- Manutenção
  - Facilidade para remover CSS
  - Estilos dinâmicos
- Perfomance
- Injeção automática de prefixos vendor


## Statefull vs Stateless 
- Stateful: componente usa estados
- Statelless: componente não usa estados
- A nomenclatura foi atuaizada
  - Class Components
  - Function Components
- Com hooks, estados são manipuláveis em function componentes


### Stateful
- Possui gerenciamento de estados no componente
- Construídos usando classes em JS

**Ciclo de vida**
- Initialization
- Mounting
- Updation
- Unmounting


### Stateless
- Não possui gerenciamento de estados no componente
- Construídos usando funções em JS


## Formuários
- Mantém um estado interno

```html
<form>
  <label>
    Nome:
    <input type="text" name="nome" />
  </label>
  <input type="submit" value="Enviar" />
</form>
```
- Em HTML, <input>, <textarea> e <select> tem um estado interno 
- Em react podemos controlar o estado: state, setState
- Tanto sellect, input ou textarea aceitam um atributo value
- Podemos mudar esse valor usando o atributo onChange


## Introdução ao Flux

### O que é Flux?
- É um padrão de projeto para tráfego de dados de maneira unidirecional

**Action:** É como um telégrafo formata a mensagem a ser enviada
**Dispatcher:** é como um telefonista ele sabe todos os callbacks para diferentes stores
**Store:** é como um gerente super controlador, guara a informação e todas as alteraçãoes tem que ser feitas por ele mesmo, mais ninguém
**View:** é como um gerente intermediário (middleware) que recebe as notificações da store e passa os dados para as visões abaixo dela

**Diversas implenentações**
Redux (mais popular)
Reflux
Mobx
Vuex (baseado em Redyx e Elm)
NgRx/store (baseada em Redux e RdxJS)












<br>

## 📚 Referências e leituras adicionais
- Cursos de ReactJS da [Digital Innovation One](https://www.dio.me/)

<div align="right">
  <a href="#top">
    <img alt="Up" height="25" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/solid/angle-up.svg">
  </a>
</div>