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