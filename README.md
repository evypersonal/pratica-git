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
git commit -a
~~~

### Fazer comunicação de uma branch local para a branch remoto
~~~bash
git push -u origin nomeDaBranch
git push nomeDaBranch
~~~


