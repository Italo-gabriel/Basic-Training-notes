># Preparando o Ambiente para Criar o portal com os Codigos Atualizados

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


># Subindo o portal e rodando o Banco de dados no Docker

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

># Rodando o Catalina Junto com o banco de dados e subindo o portal

Ir para o local 
**~/dev/bundles/master/tomcat-9.0.53/bin/** (dentro dessa pasta bin rodar o comando)
**./catalina.sh run** (esse comando vai subir o portal e conectar com o banco de dados para podermos acessar no Browser)

`Observação !!`
    Finalizando o comando, automaticamente ele vai abrir uma aba do navegador com o portal funcionando 
    mas se não abrir voce pode ir no local de busca de endereço do browser e digitar 'localhost:8080' que vai ser direcionado para o portal 