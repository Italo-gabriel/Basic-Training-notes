>## Introduçào ao Mysql

`**Introdução**`

![](Imagens/001.jpg)

Um pouco sobre MySQLé um SGBD (Sistema Gerenciador de Banco de Dados) relacional, que utiliza a linguagem SQL (Structured Query Language, ou traduzindo, Linguagem de Consulta Estruturada). MySQL também é multiusuário e multitarefas.

Este SGBD inicialmente foi desenvolvido para trabalhar com projetos de pequeno e médio porte, com a capacidade de suportar por volta de cem milhões de registros em cada tabela, podendo chegar ao tamanho médio de aproximadamente cem megabytes por tabela, entretanto, esses eram os tamanhos recomendados nas primeiras versões. Porém, hoje em dia o MySQL ultrapassa extraordinariamente esses limites e capacidades das versões anteriores.

MySQL é conhecido por ser de fácil utilização, e usado por empresas que trabalham com grandes volumes de dados, tais como, NASA, Bradesco, HP, Sony entre outras grandes empresas de renome. Possui uma interface extremamente simples e é compatível com grande parte dos sistemas operacionais. Podemos dizer que essas são duas das grandes características que fazem o MySQL ser tão utilizado atualmente e estar em constante crescimento.

Mesmo sendo um dos bancos de dados mais utilizando em todo o mundo, MySQL continua em constante desenvolvimento, com atualizações frequentes.

`**Compatibilidade**`

MySQL é compatível com a maioria dos sistemas operacionais existentes atualmente no mercado. Pelo fato de ser desenvolvido em C e C++, isso faz com que seja extremamente fácil sua acessibilidade entre os diversos sistemas operacionais. Vejamos alguns desses sistemas.

    Windows: Compatível com todas as versões
    Linux: Sendo compatível com as principais versões, como Fedora, Core, Debian, SuSE e RedHat.
    Unix: Sendo compatível com as versões Solaris, HP-UX, AIX, SCO.
    FreeBSD.
    Mac OS X Server.

`**Licença**`

O MySQL é de Código Aberto (Open-Source), desenvolvido e distribuído sob as licenças GNU/GLP (General Public Licence, ou traduzindo, Licença Publica Geral), q qual determina o que se pode ou não fazer à ferramenta e demais recursos. Além do programa, o seu código-fonte também é disponibilizado para que qualquer usuário possa edita-lo de forma que atenda suas necessidades.

`**Os princípios básicos da licença GNU/GLP são:**`

    Utilização: Permite que o usuário faça uso do software para qualquer finalidade.
    Distribuição: Livre distribuição do software entre quaisquer pessoas.
    Didática: Permite que seu funcionamento seja estudado através de seu código-fonte
    Colaboração: Possibilita que seu código-fonte seja modificado para evoluir a ferramenta. Como regra seu novo código-fonte tem que permanecer sendo livre segundo essa licença.

`**Características**`

Portabilidade: Devido o MySQL ter sido desenvolvido em C e C++, tornou-se extremamente fácil a portabilidade entre os diferentes sistemas, plataformas e compiladores. Possui também módulos de interface para múltiplas linguagens, tais como Delphi, Java, Python, PHP, ASP, Ruby e entre outras linguagens mais.

**Formas de Armazenamento**: O MySQL possibilita diversos tipos de tabela para o armazenamento dos dados, tendo em conta que cada tipo tem suas próprias características. Dessa maneira temos a possibilidade de escolhermos o tipo de acordo com cada situação diferente. Enquanto um tipo tem como prioridade a velocidade, outro da prioridade ao volume de dados, entre outras características.
Velocidade: Alta velocidade no acesso dos dados em razão de diversos motivos em seu desenvolvimento com tabelas ISAM, que foi substituído pelo novo sistema MyISAM na versão 5 do MySQL, além de utilização de caches em consultas, utilização de indexação BTREE para as tabelas do tipo HEAP, algoritmos de busca, entre outros recursos.

**Capacidade**: O MySQL possui um alto poder de execução e de armazenamento. De acordo com a plataforma em que seja usado, suas tabelas poderão armazenar grandes volumes de dados, o limite ficará por conta somente do tamanho máximo de arquivos que a plataforma que estiver sendo utilizada puder manipular. Já no caso de tabelas do tipo InooDB, onde o armazenamento pode ser realizado em um ou vários arquivos separados, fica possível armazenar volumes de dados equivalentes a TB (Terabytes) de tamanho. E referente a expressões SQL, o MySQL suporta execuções de script SQL com até 61 milhões de tabelas “joins”. E no quesito de velocidade de execução, o MySQL pode ser considerado um dos mais velozes, isso é, se não podemos dizer que é o mais veloz.

O MySQL, por ser um banco de dados poderoso, tem a capacidade de realizar bilhões de consultas em um único dia em um site e também fazer o processamento de milhões de transações por minuto.

**SQL**: Como já sabemos, o MySQL trabalha com a linguagem SQL (Structured Query Language, ou traduzindo, Linguagem de Consulta Estruturada), sendo extremamente rápido. E isso foi possível devido a SQL ter sido implementada no MySQL através de códigos e funções altamente customizadas pelos seus desenvolvedores. Isso gerou a grande vantagem de velocidade no processamento dos códigos SQL, porém, ao mesmo tempo trouxe um ponto negativo, sendo ele o fato de que com essa customização, nem todos os padrões das versões mais atuais do SQL tenham sido trazidos para o MySQL, porque poderiam prejudicar consideravelmente a velocidade do banco de dados. Entretanto, essa desvantagem não influencia em nada na aplicação.

`**Conclusão**`

o MySQL é um excelente banco de dados para ser utilizado em aplicações que trabalham com grandes volumes de dados, além de ser compatível com diversos sistemas operacionais e que vem em constante evolução ao decorrer de cada nova versão lançada. Espero que o tema tenha sido do agrado e compreensão de todos os leitores. Fiquem à vontade para deixar suas opiniões, criticas, duvidas e sugestões.


> ## Subindo o portal e rodando o Banco de dados Mysql no Docker

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

    Agora estando com acesso ao Mysql seguir os proximos passos

**show databases;** (ver os bancos existentes)
**drop database lportal;** (exclui um banco de banco de dados)
**create database lportal;** (cria o banco de dados)
**show databases;** (repetir o comando para confirma que esta Criado o banco de dados novo )
**exit;** (sair do Mysql)

>## Principais Comandos do Sql ( Mysql )

**Comandos de Criação**
- create database 'NomeDB';
- create table 'Nome';
- use 'NomeDB';

**Comandos para apagar**
- drop database 'NomeDB';
- drop table 'Nome';

**Comandos para Visualizar informações**
- show tables'NomeDB';
- show databases;
- exit;

**Comando para Manipular as Informações**
- insert 'informaçãoASerInserida';
- select 'informaçãoASerInserida';
- delete 'informaçãoASerInserida';

>## Documentação Comandos terminal 

**Sites relacionados**

Comandos no Terminal  (https://dev.mysql.com/doc/mysql-getting-started/en/)

Documentação: http://dev.mysql.com/doc/

Download: http://dev.mysql.com/downloads/

Site oficial : http://www.mysql.com/

Suporte: http://www.mysql.com/support/