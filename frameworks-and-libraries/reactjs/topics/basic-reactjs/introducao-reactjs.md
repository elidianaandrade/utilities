<div align="center">
  <img alt="JavaScript" height="100" src="https://raw.githubusercontent.com/FortAwesome/Font-Awesome/6.x/svgs/brands/js-square.svg">
</div>

<br>

# 💻 Introdução ao ReactJS
📚 Biblioteca JavaScript, é uma linguagem declarativa cuja principal função é a construção de interfaces de usuário.
<br>
📑 [Documentação ReactJS](https://pt-br.reactjs.org/docs/getting-started.html)
<br>
📝 Anotações do Curso de ReactJS da [Digital Innovation One](https://www.dio.me/)
<br>

## 🔗 Instalação
⬇️ [Download ReactJS](https://code.visualstudio.com/download).
⬇️ [Download Chocolatey](https://chocolatey.org/install).


## ⏳︎ Breve histórico 
 - Criado em 2011 por **Jordan Walke** no **Facebook**, com base no **XHP**, 
 - Utilizado no mural de notícias da rede social, para solucionar os problemas de **manutenção**, **escalabilidade** etc.;
 - Em 2012, passou a ser utilizado no Instagram;
 - Em 2013, foi anunciada a liberação OpenSource na JSConf US;
 - Em 2015, React Native;
 - UWP (Universal Windows Plataform).

<br>

## ⚙ Configuração do ReactJS
- React Create App
- React Scripts
- Task Runners e Bundler Sizers

### JSX
- const element = <h1>Hello, world!</h1>;

### Webpack
Module bundler: empacotador de módulos para aplicações JS

### **Configuração do webpack**
- Entry
- Output
- Loaders: possibilita gerenciar arquivos que não são JavaScript;
- Plugins
- Mode: production, development ou none;


#### Criação do arquivo **webpack.config.js**
```
npm i -D webpack wepack-cli

"build":"webpack --mode production"

npm i @babel/core babel-loader @babel/preset-env
@babel/preset-react --save-dev
```

### EsLint

### **Configuração do EsLint**
```
npm install --save-dev eslint babel-eslint eslint-plugin-react eslint-watch
```

### Ciclo de vida de um componente
- Inicialização;
- Montagem;
- Atualização;
- Desmontagem.


## Renderização Condicional
- Variáveis de Elementos
- If inline com o Operador Lógico &&
- If-Else inlline com Operador Condicional
- Evitando que um Componente seja Renderizado

## Listas e Chaves
- Renderizando Múltiplos Componentes
- Componente de Lista Básico
- Chaves
- Extraindo Componentes com Chaves
- Chaves devem ser Únicas apenas em Elementos Irmãos

## Manipulando Eventos
- Nomeados usando camelCase
- Com JSX você passa uma função como um manipulador de eventos ao invés de um texto

## Pensando do Jeito React
- Comece com um Mock
- Separe a UI em uma hierarquia de componentes
- Crie uma versão estática em react
- Identifique a representação mínima (mas completa) do State da UI
- Identifique onde o State deve ficar
- Adiocione o fluxo de dados inverso




<br>

## 📚 Referências e leituras adicionais
- Cursos de ReactJS da [Digital Innovation One](https://www.dio.me/)
