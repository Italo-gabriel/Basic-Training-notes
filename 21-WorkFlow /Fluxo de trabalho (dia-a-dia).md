> # Subindo o portal e rodando o Banco de dados no Docker

1- Baixando a Imagem do MYSQL
- ***d run --name galatians -d -e MYSQL_ROOT_PASSWORD=lovethepoor -p 3306:3306 mysql:8.0.22.*** (Baixa a imagem do MYSSQL)

2- Criando um novo banco de dados 
- ***d exec -it galatians mysql -uroot -p*** (Entra no banco de dados do MYSQL)
- ***show databases;*** (ver os bancos existentes)
- ***create database lportal;*** (cria o banco de dados)
- ***drop database 'nome';*** (exclui o banco de dados)

3- Rodando no Docker e subindo o portal no Catalina 
- ***d ps -a*** ( lista as imagens)
- ***d start galatians*** (rodar o banco de dados no Deocker)
- ***c*** (subir o catalina) [alias] c="~/dev/bundles/master/tomcat-9.0.53/bin/catalina.sh jpda run"

> # Preparando o ambiente de trabalho (fluxo de trabalho inicial)

1- Entrando no repositório do Portal e refazendo o catalina
- ***cdt*** (ir para o repositório liferay-portal)
- ***ant clean*** (limpar o banco)
- ***ant all*** (refazer o portal no catalina )

Observação !!

se der algum erro após refazer o portal ,fazer o passo 2 do - **Subindo o portal e rodando o Banco de dados no Docker**

ou utilizar o comando de [***ps aux | grep java***] - **para ver os Processos em execução e poder para-los** 

[***kill-9 'numero dos processos em execução do java***] para - **poder parar os processos e nao dar conflito com o banco de dados**

2- Atualizando os Repositórios local e remoto

- ***g pull upstream master*** (para atualizar os codigos no repositorio local)
- ***g push origin master*** (para atualizar o codigo no Github)

3- trabalhando com ticket - colocando as informações do jira no VScode

- ***Boards*** aba para abrir o Kanban do **Workflow|Test Automation** com os Ticket's
- ***SELECT FOR DEVELOPMENT*** - local para pegar os ticket's e assign e dar o **Start Progress**
- ***Como vem o ticket do jira, o titulo*** ( INTERNAL - Liferay QA /LRQA-69472 Automate Tests for Workflow - DDL / **LRQA-69477**) esse último número é o que vai ser o nome da branch.

4- Criando a branch baseado no  titulo do Jira (LRQA-xxxx)

- ***g co -b 'LRQA-xxxx'***(cria a branch e entra nela) 

5- Comandos para manipular as branch's !!!

- ***g br*** (vai listar as branch)
- ***g co 'NomeBranch'*** (vai mudar de branch)
- ***g br -D 'NomeBranch'*** (vai apagar a branch)

6- Depois de criar a branch , vamos manipular o test no VScode

- ***code .***executar esse comando dentro da branch (para abrir o VScode e trabalhar o código)

- ***Crtl + p*** dar esse comando dentro do VScode e  pegar o nome do arquivo de .testcase e coloca na pesquisa 
(exemplo Automate **WorkflowDDL**#DraftEntryIsNotDisplayedOnMyWorkflowTasks)- o nome do arquivo é o que ((vem antes)) do#

- ***Ctrl + f*** dar esse comando dentro do arquivo.testcase e encontrar o caso de teste dentro dele
(exemplo Automate WorkflowDDL#**DraftEntryIsNotDisplayedOnMyWorkflowTasks**)que sera o nome que ((vem depois)) do#

- ***Após encontrar o caso de test*** dentro do arquivo .testcase apagar os seguintes linhas de Codigo para começar a montar o teste 
[***@ignore = "Test Stub"***]
[***// TODO LRQA-XXXX  - "Description do test e Instruction "***]

7- montando  todo o codigo (recursos utéis durante a montagem do teste)

***index*** (ver os logs de erro)
***indexFolder*** (ver  sumario detalhado dos erros)

***rp testcase#funcaoTestada*** (rodar o teste)
***runPoshiValidation*** (validar a syntax do Poshi)

***removeData***(limpeza do banco)
***removeState***(limpeza de estado)

># Finalizando o teste - hora do pull request ***gpr***

**Fluxo do pull request** (apos finalizar o teste no mesmo dia que iniciou)

cdt

git status

git clean . -f 

git add . ou <file>

git  commit -m <LRQA-XXXX Add 'NomeQueVemDepoisDo#' test>

cd portal-impl

afcb

aflc

cd ..

runPoshiValidation 

git status

git add . <file>

git commit -m "LRQA-XXXX SF"

git log (verificar seus commits - acima da master)

gpr submit -u <id> (Ex.: lucasperj)

> # Ordenando os arquivos no GitHub e no Jira Após o Pull Request 

**Fluxo do Github**

1-titulo do pull request nessa ordem 
(LRQA-xxxx Workflow Automated Test 'Nometeste') // o nome que fica depois do #//

2- coloca link do ticket do jira anexado ao github // no canto onde fica os 3 pontinhos //

**Fluxo do Liferay issues (Jira)**

1- No jira coloca o link do pull request do github na aba (Submit for review) e coloca (QA suporte)no [LugardoNomedaPessoa]

2- coloca também o index do testcase Anexado ao jira.

># Fluxo de trabalho de um dia para o outro (caso o teste não finalize no mesmo dia e tenha que guardar as informações)

1- salva as informações na branch ***Crtl + s*** e continua no outro dia 

**No dia seguinte segue o fluxo**

2- Entrando no repositório do Portal e refazendo o catalina

- ***cdt*** (ir para o repositório liferay-portal)
- ***ant clean*** (limpar o banco)
- ***ant all*** (refazer o portal no catalina )

- ***g br*** (listar as branch e pegar a que estava trabalhando no dia anterior)
- ***g co "LRQA-xxxx"*** (entra na branch)
- ***g stash*** (para arquivar as informações)

- ***g co master*** (para voltar para a master e fazer a atualização)
- ***g pull upstream master*** (para atualizar os codigos no repositorio local)
- ***g push origin master*** (para atualizar o codigo no Github)


- ***g co 'LRQA-xxxx'*** (entra na branch do teste)
- ***g rebase master*** (traz as atualizações que foram baixadas para a branch)
- ***g stash apply*** (Dentro da branch que estava trabalhando aplica as informações que foram arquivadas)

- ***g clean . -f*** (apaga os arquivos que aparecem do selenium, para nõa mandar junto na hora de commitar)
- ***code .*** ( vamos para o code e continuamos de onde paramos)

Dica do Git Stash !!
    - ***g stash list*** ( se precisar ver a lista com todos os arquivamentos que ja foram feitos)
    - ***g stash 'numero Identificaçao'*** (para entrar em algum stash especifico)
    - ***g stash apply*** ( vai aplicar as últimas informações que foram guardadas)

![Documentação de todo o Fluxo detalhado](https://liferay.atlassian.net/wiki/spaces/ENGWORKFLOW/pages/1595212576/Workflow+Automation+Guide#Workflow-Tests-Overview)