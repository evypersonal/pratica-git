# Praticando Git
Repositório com finalidade de praticar comandos do Git

### Instalação da extensão 'Git Graph'
visualização do histórico de commits

`origin` -> repositório remoto;

`main*` -> está em negrito e com o `*` porque é a branch ativa;

### Fazer um commit sem alterações
~~~bash
git commit --allow-empty -m "msg"
~~~

### Fazer push para enviar alterações locais para o remoto (main/origin)
~~~bash
git push origin main
~~~

### Fazer commit de todos os arquivos modificados e não ignorados ao commit atual (sem utilizar o `add .`).
~~~bash
git commit -a -m "msg"
~~~
O parânmentro `-a` adiciona todos os arquivos modificados;

### Fazer comunicação de uma branch local para a branch remoto
~~~bash
git push -u origin <nomeDaBranch>
git push <nomeDaBranch>
~~~

### Criar uma branch e já ativar ela no mesmo comando 
~~~bash
git checkout -b <nomeDaBranch>
git switch -c <nomeDaBranch>
~~~
O parâmetro `-b` alterna para `novoBranch` criando o branch. (utilizando o `checkout`)
O parâmetro `-c` alterna para `novoBranch` criando o branch. (utilizando o `switch`)

### Deletando uma branch
~~~bash
git branch -D <nomeDaBranch>
git push --delete origin <nomeDaBranch>
~~~
Ao executar o primeiro comando removerá a branch localmente, para que seja removido do remoto é necessário utilizar o segundo comando.

###  Reescrever o commit anterior
~~~bash
git commit --amend (descrever oque alterar)
~~~

### Resetando um commit (branch ativa localmente)
~~~bash
git reset HEAD~1
~~~

### Resetando um commit (branch ativa remotamente)
~~~bash
git revert HEAD
~~~

### Mostrando um grafico de commits através do terminal
~~~bash
git log --graph --oneline
~~~

### Subescrevendo o commit / Rebase Interativo (retirando o autor intruso)
0. Verificar se o editor de mensagem é o vs code:
~~~bash
git config --global core.editor "code --wait"

~~~bash
git rebase -i <hash do commit> ou <HEAD~>
~~~
1. (Dentro do editor posso usar o `edit` para editar o commit);

2. No terminal: 
~~~bash
git commit --amend --author="evypersonal <evellynmaria2015@outlook.com>" --no-edit
~~~
- (Alterando o autor do commit utilizando a flag `--author="username <email>"`);
- (Ultilizar a flag `--no-edit` para manter as alterações feita no commit);

3. Ignorar os outros commits:
~~~bash
git rebase --continue 
~~~

4. Forçar alterações para o remoto:
~~~bash
git push --force
~~~

### Reaproveitando um commit de alguma branch
~~~bash
git cherry-pick <hashDoCommit>
~~~

### Adicionando tags semanticas no commit
~~~bash
git tag <nomeDaTag> <hashDoCommit>
~~~
- Importância da semântica nas tags --> v0.1.0  --> v1.0.0
- Importante para adicionar marcos ('milestones') aos commits ou outras referências no histórico do Git.
- Se não especificar a referência, o Git vai atribuir a tag ao commit apontado por **HEAD**.
- Deve-se fazer o `push` das tags, utilizando o seguinte comando:
~~~bash
git push --tags
~~~

### 