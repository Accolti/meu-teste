# Meu projeto teste

git init
- iniciar novo projeto

git add <nome-do-arquivo>/.
- add os arquivos prontos para serem comitados

git commit -m "mensagem commit"
- comiit os arquivos no histórico

git log 
- mostra os ultimos commit, log fe alteração

git status
- como está o estado da nossa ramificação

git diff
- mostra o que foi alterado
- o que tem de alteração na ramificação

git merge
- merge de ramificações, mesclagem

git branch
- mostfa a branch atual

git checkout <nome-branch>
- muda para essa branch

git checkout -b <nome-branch>
- criar uma nova branch a partir da branch atual que estamos

git remote add <nome> <url>
- add um novo repositório remoto

git puch <nome> <nome da branch>
- manda nossas alterações locais para o repositorio remoto, para cada branch

git pull <nome> <nome da branch>
- pega as alterações do repositório remoto, e joga para nossa máquina

git fetch
- atualiza o novo histarioco local de acordo com o historico salvo la no repositorio remoto
- sicronização do local com o remoto

O git checkout não foi removido (ele continua funcionando normalmente), mas a equipe do Git resolveu dividi-lo em dois comandos mais simples e diretos para evitar confusões.

O problema do git checkout é que ele fazia coisas totalmente diferentes usando o mesmo comando (mudar de branch E descartar alterações em arquivos).

Os dois novos substitutos (desde o Git 2.23):
1. git switch (Exclusivo para Branches)
Usado apenas para navegar, criar e alternar entre branches.

Mudar de branch:

git switch nome-da-branch

(Antes: git checkout nome-da-branch)

Criar e mudar para uma nova branch:

git switch -c nome-da-branch

(Antes: git checkout -b nome-da-branch)

2. git restore (Exclusivo para Arquivos)
Usado apenas para desfazer alterações e restaurar arquivos no seu ambiente de trabalho.

Descartar alterações locais em um arquivo (limpar modificações):

git restore index.html

(Antes: git checkout -- index.html)

Tirar um arquivo da Área de Staging (dar "unstage" após um git add):

git restore --staged index.html

(Antes: git reset HEAD index.html)

Preciso parar de usar o git checkout?
Não obrigatoriamente. Se você já tem a memória muscular do git checkout, pode continuar usando! No entanto, usar git switch e git restore é a boa prática recomendada atualmente por ser mais seguro e intuitivo.

