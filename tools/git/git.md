<div align="center">
  <img alt="Git" height="100" src="https://git-scm.com/images/logos/downloads/Git-Logo-Black.png">
</div>

# 💻 Git
🗃 Sistema de controle de versões de arquivos distribuídas.
<br>
📑 [Leia a documentação](https://git-scm.com/docs/git/pt_BR)

## 🔗 Instalação
⬇️ [Download Git](https://git-scm.com/).
<br>
✅  Durante a instalação deixe marcada as opções: **"Git Bash Here"** e **"Git GUI Here"**.


## ⌨️ Comandos básicos 

Comando                                   | Função
----------------------------------------- | -------------------------------------------------------------------------------
`git --version`                           | Consulta a versão instalada
`git init`                                | Cria um repositório
`git status`                              | Exibe o status da árvore de trabalho 
`git add`                                 | Adiciona os arquivos ao índice
`git commit - m"commit message"`          | Cria um commit (grava as alterações) adicionando mensagem sobre o que se trata
`git push`                                | Upa os arquivos atualizando a branch no repositório remoto
`git branch`                              | Cria, lista ou exclui branches
`git clone`                               | Clona um repositório
`git pull`                                | Atualiza a branch local a partir da branch remota
`git merge nomeDaBranch`                  | Mescla a branch atual com a descrita
`git checkout main`                       | Alterna para a branch main

<br>

## ⚙️ Funcionalidades básicas 

### Subir um repositório local para a branch main do repositório remoto no GitHub
📁 Clique com o botão direito na pasta e clique em **"Git Bash Here"**.
```bash
# Transforme a pasta existente em um repositório
$ git init
```
```bash
# Caso haja arquivos dê um "git add ." para adicionar todos ao índice
$ git add .
```
```bash
# Crie um commit e adicione uma mensagem descritiva
$ git commit -m "first commit"
```
```bash
# Adicione a URL do repositório remoto onde deseja upar o seu local
$ git remote add origin https://github.com/username/nome-do-repositorio.git
```
```bash
# Envie os objetos, atualizando a branch main no repositório remoto
$ git push origin main
```

<br>

### Alterar a branch em que estou trabalhando pela branch main
📁 Clique com o botão direito na pasta do repositório local e clique em **"Git Bash Here"**.
```bash
# Alterne para a branch main
git checkout main
```
🛑 Caso exiba o erro: `error: pathspec 'main' did not match any file(s) known to git` dê um `git checkout -b main`


```bash
# Mescle a branch main com a que deseja (nesse caso a que estava trabalhando e vai alterar pela main) 
git merge nomeDaBranch
```
```bash
# Envie os objetos atualizando a branch main no repositório remoto 
git push
```
```bash
# OPCIONAL: Delete a branch antiga do repositório local e remoto caso não deseje mais

# Deletar a branch antiga do repositório local
git branch -d nomeDaBranch

# Deletar a branch antiga do repositório remoto
git push origin --delete nomeDaBranch
```

<br>

### Solucionar o erro `fatal: refusing to merge unrelated histories`
```bash
git pull origin nomeDaBranchAtual --allow-unrelated-histories
# Em seguida adicione uma mensagem ou aperte ESC e digite `:wq` para fechar e salvar
```

<br>

### Deletar histórico de commits no github

```bash
git checkout --orphan latest_branch

git add -A

git commit -m "commit message"

git branch -D main

git branch -m main

git push -f origin main
```
