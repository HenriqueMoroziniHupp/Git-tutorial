# aula-youtube
Aprendendo a usar o git com o canal "Thi Code"

Aula de git com "Thi Code" no Youtube;

AULA 1: https://www.youtube.com/watch?v=Ckig8H_h538

AULA 2: https://www.youtube.com/watch?v=o_ECnZ8zk_Q


# AULA 1

CRIANDO REPOSITORIO NO GITHUB O PASSANDO PARA O PC:

1 - Se criar o repositorio pelo github, você pode clona-lo pra memória do pc usando o seguinte comando:

>> git clone <link do repositorio, https, ssh ou github CLI>

-------------------

2 - Se criar mais um arquivo dentro da pasta do projeto, verifique como esta o status da pasta para ver se existe arquivos que estão fora do monitoramento do git

>> git status

-------------------

3 - Caso tenha arquivos não monitorados e queira monitora-lo, use:

>> git add <nome do arquivo>
ou
>> git add .

A primeira forma adiciona arquivo individualmente, a segunda adiciona todos arquivos onde se encontram fora do monitoramento

-------------------

4 - Para passar os arquivos que estão sob monitoramento para a área de versionamento, para que você possa controlar a versão e voltar as versões:

>> git commit -m <"Mensagem para descrição do commit">

Esse comando fará com que todos os arquivos monitorados fiquem salvo caso exista alguma alteração, estes arquivos ficam salvo na posta .git

-------------------

5 -  Para ver o histórico e descrição dos versionamento, realize o comando de log:

>> git log

-------------------

6 - Gerenciar o git com o GitHub:

6.1 - Enviar os arquivos para o GitHub:

>> git push origin <Nome da branch>

----

6.2 - Salvar arquivos do GitHub na memória em disco, caso realize alguma alteração pelo site do GitHub:

>> git push origin <Nome da branch>



# AULA 2

CRIANDO REPOSITORIO NO PC O PASSANDO PARA O GITHUB:

1.1 - Etre na pasta do seu projeto e dê o comando:

>> git init

Será criado na pasta do projeto uma pasta chamada ".git"

1.2 - Adicione os arquivos ao monitoramento

>> git add .

1.3 - Passe os arquivos monitorados para a área de versionamento

>> git commit -m <"First commit">

1.4 - Mude no nome da branch de master para main (opicional?)

>> git branch -M main

-------------------

Depois de configurado o git localmente, segue a parte 2:

2 - Na conta do GitHub, crie um repositório e aplique o comando mostrado na criação do portifólio:

>> git remote add origin https://github.com/HenriqueMoroziniHupp/Portifolio-Marcos.git

Dessa forma o git e o GitHub estarão conectados

-------------------

3 - Faça o upload dos arquivos locais para o GitHub

>> git push -u origin <"nomeDaBranch">
 

# AULA 3
	TRABALHANDO COM BRANCH
	
Branch são versões diferente do projeto, caso queira trabalhar em uma versão 2.0 por exemplos, mexer no projeto sem modificar o original

1 - Crie uma nova branch

>> git branch <"NomeDaNovaBranch">

Essa branch foi criada localmente, para ver as branch:

>> git branch

-------------------

2 - Para mudar de branch:

>> git checkout <"NomeDaBranchSelecionada">

No "VS Code", quando mudando de branch o código muda automaticamente :O

-------------------

Agora é só seguir com os mesmo passos, add, commit, push, etc;


3 - Para subir, vamos usar o push com o nome da nova branch

>> git push -u origin <"NomeNovaBranch">

-------------------

4 - Agora, para atualizar a branch main com as alterações, ou seja, aplicar as mudanças que você fez em outra branch, faça:

>> git merge <"NomeDaBranchQueQueroJuntarNaBranchAtual">

Explicando melhor:
Você entra na branch que quer receber a atualização, usando o "git checkout <NomeDaBranch>" e depois usa o comando "git merge <NomeDaBranch>" com o nome da branch que possui as mudanças.
Ex: 
git checkout main
git merge versao2

Neste caso a branch main recebe as alterações da branch "versao2"

Não precisa fazer "add" e "commit" na main, pois é realizado automaticamente quando é feito um "merge"

Precisa apenas realizar um push
