# Preparando o Ambiente para Criar o portal com os Codigos Atualizados

*1-Atualizando os Repositórios local e remoto*

**cdt** (ir para o repositório liferay-portal)
**g pull upstream master** (para atualizar os codigos no repositorio local)
**g push origin master** (para atualizar o codigo no Github)

*2-Entrando no repositório do Portal e construindo a pasta Bundles*

`Observação !!`
    Verificar se na pasta ~/dev existe dentro dela a pasta Bundles que pode ter sido criada com o comando ant all que foi rodado outras vezes se caso já foi feito o ant all na sua máquina.

    Dentro da pasta ~/dev - Com o comando 'la' vamos listas as pastas e ver se existe a Bundles, existindo vamos apagar com o seguinte comando 

**rm -rf Bundles/** (vamos apagar a pasta e rodar o comando ant all novamente para fazer uma nova pasta Bundles com os codigos atualizados)

**ant clean** (limpar os Caches de outro portal que estava rodando anteriormente) fazendo isso a pasta bundles continua existindo ,mas o novo comando de ant all vai substituir a pasta bundles pelos novos arquivos atualizados)

**ant all** (refazer a pasta Bundles) rodar esse comando dentro do 'cdt'

`Observação !!`
    Se der algum erro no processo do "ant all" pode está relacionado com o banco de dados do Mysql 
    para resolver devemos prosseguir com o passo-a-passo e apagar o banco e Recriar ele - no topico seguinte
        # Subindo o portal e rodando o Banco de dados no Docker
            *3- Criando um novo banco de dados*

Ou pode utilizar o comando
**ps aux | grep java** - para ver os Processos em execução e poder para-los , e depois rodar o ant all novamente com o ambiente totalmente limpo, para evitar erros por causa de interferencias de dados e Caches ou lixo eletronico 

**kill-9 ou sudo kill-9** + 'numero dos processos em execução do java' - vai parar os processos e não dar conflitos com o banco de dados

`Observação !!`
    Tudo ocorrendo bem com o "ant all"  vamos para o próximo passo


# Subindo o portal e rodando o Banco de dados no Docker

*1-Baixando a Imagem do MYSQL*

**d run --name galatians -d -e MYSQL_ROOT_PASSWORD=lovethepoor -p 3306:3306 mysql:8.0.22.** (Baixa a imagem do MySQL)

*2-Rodando a Imagem do Docker para poder subir o portal* 

**d ps -a** ( lista as imagens)
**d start galatians** (rodar o banco de dados no Docker)
**d ps** (ver que a imagem está em execução)

`Observação !!`
    Agora que a imagem esta em execução podemos fazer a configuração do banco de Dados
    no caso criar um banco de dados usando a imagem Docker do Mysql (galatians)

*3-Criando um novo banco de dados*

**d exec -it galatians mysql -uroot -p** (Entra no banco de dados do MYSQL)

`Observação !!`
    Vai pedir a senha de acesso (colocar a senha que vem junto com o comando que foi utilizado logo acima , o comando para baixar a imagem - a senha é a seguinte PASSWORD=lovethepoor)

    Agora estando com acesso ao Mysql seguir os proximox passos

**show databases;** (ver os bancos existentes)
**drop database lportal;** (exclui um banco de banco de dados)
**create database lportal;** (cria o banco de dados)
**show databases;** (repetir o comando para confirma que esta Criado o banco de dados novo )
**exit;** (sair do Mysql)

`Observação !!`
    Agora com o banco de dados Criado podemos rodar o comando do "Catalina.sh run" dentro da pasta Bundles que o comando ant all Criou para nós 

    Onde fica a pasta Bundles? no repositorio ~/dev

Vamos fazer o caminho até chegar no local onde vamos executar o comando "Catalina.sh run"

# Rodando o Catalina Junto com o banco de dados e subindo o portal

Ir para o local 
**~/dev/bundles/master/tomcat-9.0.53/bin/** (dentro dessa pasta bin rodar o comando)
**./catalina.sh run** (esse comando vai subir o portal e conectar com o banco de dados para podermos acessar no Browser)

`Observação !!`
    Finalizando o comando, automaticamente ele vai abrir uma aba do navegador com o portal funcionando 
    mas se não abrir voce pode ir no local de busca de endereço do browser e digitar 'localhost:8080' que vai ser direcionado para o portal 

# Abrindo os Codigos no Vscode  para ver os Testes 

*1-Com a aba do terminal rodando o portal , vamos abrir uma nova aba e estando dentro do cdt abrir o Vs code*

**Ctrl + t** (abrir uma nova aba)
**cdt** (ir para o repositório liferay-portal)

`Observação !!`
    Antes de começar a fazer qualquer mudança nos codigo para treinar com os testes, vamos criar uma branch para que as mudanças que vamos fazer não mude o codigo original que eu ja deixei atualizado na maquina

*2-Criando uma Branch para fazer as mudanças sem interferir no Codigo Original da minha máquina*

**g br 'NomeDabranch** (cria a branch)
**g co 'NomeDabranch'** (Vai entrar na branch que foi criada)

Ou pode fazer também os dois comando de uma unica vez
**g co -b 'NomeDabranch** (cria a branch e entra nela na mesma hora) 

*3- Comandos para manipular as branch's*

**g br** (vai listar as branch)
**g co 'NomeBranch'** (vai mudar de branch)
**g br -D 'NomeBranch'**(vai apagar a branch)

Depois de criar a branch , vamos manipular os arquivos de teste no VScode

# Trabalhando com ticket - colocando as informações do jira no VScode

**Boards** aba para abrir o Kanban do **Time | Automation** com os Ticket's

**SELECT FOR DEVELOPMENT*** - local para pegar os ticket's e assign e dar o **Start Progress**

**Como vem o ticket do jira, o titulo** ( INTERNAL - Liferay QA /`LRQA-69472` Automate Tests for Workflow - DDL / `**LRQA-69472**`) esse último número é o que vai ser o nome da branch.

Criando a branch baseado no  titulo do Jira (LRQA-xxxx)
**g co -b 'LRQA-69472'** de acordo com o exemplo acima (cria a branch e entra nela)

# Atalhos Úteis para Manipular e Encontrar os Arquivos Dentro do Vscode

*1-Abrindo todos os arquivos do portal no vscode*

**code .** fazer esse comando dentro da pasta cdt ( esse comando vai abrir o Vscode  com todo o codigo do portal Liferay, o ponto indica justamente para que todos os arquivos sejam abertos)

*2-Pesquisando pelo nome que vem antes do# | que é o nome do testcase que contem os casos de teste para ser executados*

**Ctrl + p** Tecla de atalho para abrir uma aba de  pesquisa geral entre todos os arquivos dentro dos codigos do portal - (se Colocarmos .testcase vai listar todos os arquivos de testcase que existem no portal atualmente)

`Observação !!`
    Exemplo de nome do arquivo testcase onde contem os caso de teste para poder rodar  (`Forms`#AddFormInGlobal) - o nome do arquivo testcase é o que vem antes do# 

    Para encontrar vamos colocar o nome na pesquisa que abrimos com a tecla de atalho "Ctrl + p" e Digitar o nome Forms.testcase 

*3-Pesquisando pelo nome que vem Depois do# | que é o nome do caso de teste que esta existe dentro do testcase*

**Ctrl + f** Tecla de atalho para abrir uma aba de pesquisa dentro do arquivo.testcase e assim poder encontrar os caso de teste que existem ali dentro daquele arquivo especifico que é o Forms.testcase do Exemplo

`Observação !!`
    Exemplo de nome de um  caso de teste que existe dentro do testcase (Forms#`AddFormInGlobal`) o nome do caso de teste é o que vem depois# 

    Para encontrar vamos colocar o nome na pesquisa que abrimos com  a tecla de atalho "Ctrl + f"  Digitamos o nome que vem depois do # - AddFormInGlobal então com isso ele vai nos direcionar para esse caso de teste e podemos ver todos os passos que foram feitos nele

# Rodando os Testes que já Existem e vendo os comportamentos 
**rp testcase#funcaoTestada** (alias para rodar )
**ant -f build-test.xml run-selenium-test -Dtest.class=**( o que vem depois do = é o nome do arquivo no caso do exemplo é o Forms#AddFormInGlobal) 

Então ficaria assim ---->> ant -f build-test.xml run-selenium-test -Dtest.class=Forms#AddFormInGlobal

*Esses são alguns casos de testes que existem dentro desse arquivo Forms.testcase*

    AddFormToUserSiteAndViewNoDuplicates
    AutosaveDisplaysANotification
    AutosaveIntervalCanBeConfigured
    BelongsToRuleCanPairWithGuestUser
    CanBeCreated
    CanBeCreatedFromAutosavedDraft   
    CanBeCreatedWithMultiplePages
    CanBeCreatedWithoutTitle
    CanBeDeleted

*Para ir rodando cada um e vendo os comportamentos vai substituindo no comando de execução*
    ant -f build-test.xml run-selenium-test -Dtest.class=Forms# > e aqui vai colocando o nome de cada teste e vai rodando um por um e vendo as coisas acontecendo.

# Quando Finaliza os Testes podemos ver mais detalhes por Dois Caminhos 

*ver os logs de erro*
**index** 
/home/me/dev/projects/liferay-portal/portal-web/test-results  >> `esse é um caminho onde encontramos 2 arquivos nessa pasta com os resultados, podemos abrir os arquivos no Browser e ver os detalhes`

*ver sumário detalhado dos erros*
**indexFolder**
/home/me/dev/projects/liferay-portal/portal-web/tests/index.html >> `esse link fica no log quando finaliza o teste , Clicando nele vai levar para uma pagina no Browser com as informações`

*verificar se a sintaxe do teste esta correta e LImpando o banco de dados*

**runPoshiValidation*** (validar a syntax do Poshi)
**removeData**(limpeza do banco)
**removeState**(limpeza de estado)

# Finalizando o teste - hora do pull request

*Fluxo do pull request* (apos finalizar o teste no mesmo dia que iniciou)

cdt

git status

git clean . -f 

git add . ou <file>

git  commit -m <LRQA-XXXX Add 'NomeQueVemDepoisDo#' test>

git log (verificar seus commits - acima da master)

cd portal-impl

afcb

aflc

cd ..

runPoshiValidation 

git status

git add . <file>

git commit -m "LRQA-XXXX SF"

git log (verificar seus commits - acima da master)

g rebase -i master
"i -insert"
"f-fixup" no commit do SF
esc ":wq!" para salvar e mesclar os dois commits num unico

gpr submit -u <id> (Ex.: <Italo-gabriel>)

# Resolvendo problemas num PR que ja foi enviado , e enviando as modificações

Para enviar novamente

**g push origin 'LRQA-XXXX -f** = assim ele manda as modificações para a branch com todas as atualizações que foram feitas

# Ordenando os arquivos no GitHub e no Jira Após o Pull Request 

*Fluxo do Github*

1-titulo do pull request nessa ordem 
(LRQA-xxxx Workflow Automated Test 'Nometeste') // o nome que fica depois do #//

2- coloca link do ticket do jira anexado ao github // no canto onde fica os 3 pontinhos //

3- Rodar o comando ci:test:sf ( no  comentário do commit )

*Fluxo do Liferay issues (Jira)*

1- No jira coloca o link do pull request do github na aba (Submit for review) e coloca (QA suporte)no [LugardoNomedaPessoa]

2- coloca também o index do testcase Anexado ao jira.

# Fluxo de trabalho de um dia para o outro dia (caso o teste não finalize no mesmo dia e tenha que guardar as informações)

1- salva as informações na branch **git stash** e continua no outro dia 

*No dia seguinte segue o fluxo*

2- Entrando no repositório do Portal e refazendo o catalina

**cdt** (ir para o repositório liferay-portal)
**ant clean** (limpar o banco)
**ant all** (refazer o portal no catalina )

**g br** (listar as branch e pegar a que estava trabalhando no dia anterior)
**g co "LRQA-xxxx"** (entra na branch)
**g stash** (para arquivar as informações)

**g co master** (para voltar para a master e fazer a atualização)
**g pull upstream master** (para atualizar os codigos no repositorio local)
**g push origin master** (para atualizar o codigo no Github)


**g co 'LRQA-xxxx'** (entra na branch do teste)
**g rebase master** (traz as atualizações que foram baixadas para a branch)
**g stash apply** (Dentro da branch que estava trabalhando aplica as informações que foram arquivadas)

**g clean . -f** (apaga os arquivos que aparecem do selenium, para não mandar junto na hora de commitar)
**code .** ( vamos para o code e continuamos de onde paramos)

# Dica do Git Stash
**g stash list** ( se precisar ver a lista com todos os arquivamentos que ja foram feitos)
**g stash 'numero Identificaçao'** (para entrar em algum stash especifico)
**g stash apply** ( vai aplicar as últimas informações que foram guardadas)
**g stash clear** ( vai apagar todas as informações guardadas)
**g stash drop 'numero Identificaçao'** ( vai apagar as informações daquele stash especifico)

![Documentação de todo o Fluxo detalhado](https://liferay.atlassian.net/wiki/spaces/ENGWORKFLOW/pages/1595212576/Workflow+Automation+Guide#Workflow-Tests-Overview)





