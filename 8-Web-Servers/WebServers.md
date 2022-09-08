>## O que é e por que usar o servidor Apache

O Apache é um software de código aberto de propriedade da Apache Software Foundation (ASF) que garante desempenho, estabilidade e segurança para um servidor web. Ele se tornou muito popular entre os programadores devido à sua modularidade e constante atualização pela comunidade, o que contribui ativamente para a alta capacidade dessa ferramenta.

`O que é o Apache?`
Apache Software Foundation (ASF) ou Fundação Apache é uma organização sem fins lucrativos que, segundo o site Apache.org:

“(…) desenvolve, orienta e incuba centenas de projetos de nível empresarial, disponíveis gratuitamente, que servem como espinha dorsal de alguns dos aplicativos mais visíveis e amplamente utilizados na computação atualmente.

Por meio do processo baseado em mérito da ASF conhecido como “The Apache Way”, mais de 730 membros voluntários individuais e mais de 7.000 colaboradores de códigos em seis continentes colaboram com sucesso em inovações em Inteligência Artificial e Deep Learning, Big Data, Gerenciamento de Compilação, Computação em Nuvem, Conteúdo Gerenciamento, DevOps, IoT e Edge Computing, Mobile, Servidores e Web Frameworks, entre outras categorias”.

O Apache foi criado em 1995 e é a tecnologia central responsável pelo crescimento inicial da Internet. Resumidamente, é um software de código aberto, ou seja, recebe contribuições de desenvolvedores de todo o mundo, já que o código-fonte original está disponível gratuitamente para visualização e colaboração.

Por esse motivo, se tornou muito popular entre programadores, que configuram seus próprios módulos, aplicam funcionalidades específicas e aprimoram seus recursos para atuar em projetos variados na área da tecnologia.

**Segundo o próprio site, são:**

mais de 200 milhões de linhas de código em administração;
1.058.321.099 linhas de código confirmadas;
3.022.836 confirmações de código;
730 membros individuais do ASF;
7.000 confirmadores de código Apache;
comunidade atuante de voluntários;
mais de 350 projetos e iniciativas;
mais de 300 projetos de nível superior;
52 projetos na incubadora Apache.
Junto a outros componentes (LAMP — Linux, Apache, MySQL e PHP), atua no fornecimento de conteúdos na web. Enquanto o Linux é o sistema operacional que executa as operações, o Apache é o software que processa as solicitações via HTTP.

O MySQL é um banco de dados, que armazena todas as informações processadas em um formato inteligível e o PHP é a linguagem de programação que cria conteúdos dinâmicos.

Grande parte das aplicações é executada a partir dos componentes LAMP, especialmente porque é de fácil elaboração e gratuito. O Apache se comunica na rede por meio do protocolo TCP/IP ou HTTP/S (Hyper Text Transfer Protocol Secure), que define como as mensagens são formatadas e transmitidas a partir de solicitações e comandos na porta 443.

**Como funciona o Apache?**

O processo de execução do Apache é simples e compreende basicamente as seguintes etapas:

obtenção do endereço IP do domínio a partir da pesquisa em cache ou por meio do servidor DNS (Domain Name System) — todos os sites recebem um endereço IP ao ser criado pela primeira vez no servidor web;
solicitação da URL completa pelo navegador;
resposta do servidor, que envia as páginas solicitadas ou uma mensagem apropriada ao usuário, nos casos em que as páginas não existem (mensagem de erro 404) ou na ocorrência de outro erro — o erro 401, por exemplo, que ocorre quando o acesso é negado em função da falta de credenciais.

`Quais as vantagens e desvantagens do Apache em relação a outros servidores web?`

O software NGINX foi criado para solucionar o problema de falha de processamento quando mais de 10 mil conexões de usuários aconteciam simultaneamente (c10k) e também tem ganhado popularidade.

Essa é basicamente a maior vantagem do NGINX sobre o Apache. Ele lida com uma solicitação por vez a partir de um único processo e por isso tem melhor desempenho frente ao maior volume de solicitações. Em contrapartida, o Apache tem configuração mais fácil e é mais amigável.

Já o Tomcat foi criado pela própria ASF e por isso seu nome oficial é Apache Tomcat. Assim como a Apache, é um servidor HTTP, mas serve solicitações do tipo Java, em vez de sites estáticos.

A superioridade do Apache sobre o Tomcat é que ele entende outras linguagens de programação, sendo mais flexível. Além disso, o Tomcat tem uma configuração mais difícil, especialmente se a demanda for a de executar um site ou landing page em WordPress, independente de ter sido criado por conta própria ou via Stage.

>## Por que utilizar o Apache?

`Preço`

O Apache é um software de código aberto, o que significa que está disponível para download ou para modificação por qualquer pessoa, gratuitamente. Seu código-fonte pode ser adaptado para atender às necessidades individuais de cada negócio.

Isso permite que o Apache tenha uma vantagem significativa sobre os demais servidores: nenhum recurso precisa ser sacrificado, não são incididas taxas de licença de software e de suporte para manter a continuidade dos programas que o utilizam como servidor web.

`Recursos`

O Apache é uma poderosa ferramenta, com recursos que se comparam aos seus concorrentes de alto valor. O software inclui:

    painel de controle administrativo;
    envio de mensagens de erro personalizadas;
    esquemas de autenticação;
    módulo de host virtual que permite executar vários sites simultaneamente;
    Serviço de Nome de Domínio;
    SMTP (Simple Mail Transfer Protocol);
    FTP (File Transfer Protocol).
    Além disso, há vários outros recursos adicionados por terceiros passíveis de instalação, para que seja possível personalizar o servidor web. Isso porque a comunidade de desenvolvedores do Apache atualiza constantemente os códigos, sem restringir o acesso aos recursos e patches de segurança mais recentes para os demais usuários.

`Compatibilidade`

O Apache é compatível com inúmeras configurações de hardware e sistemas operacionais. Ele roda em:

    Linux;
    Windows NT;
    MacOS;
    Unix, entre outros sistemas.
    Cada instalação pode ser ajustada para se adequar aos recursos técnicos do hardware utilizado. O Apache inclui suporte para linguagens de programação como PHP, Perl e Python. Adicionalmente, permite criptografia SSL e TLS para sites que exigem um nível de segurança mais elevado.

`Suporte`

A documentação para suporte técnico do Apache se encontra disponível em vários sites em diferentes idiomas. Isso permite que os proprietários do software acessem artigos de referência e recebam ajuda sempre que necessário.

Isso permite que o Apache seja mais vantajoso sobre os demais programas que têm apenas o site institucional como fonte de suporte. Quando um novo bug é encontrado, a comunidade de usuários de código aberto normalmente cria um patch para corrigi-lo imediatamente e publica a resolução do problema gratuitamente em fóruns e sites de tecnologia em geral.

`Modularidade`

Um dos recursos mais fantásticos do Apache é sua capacidade de lidar com um alto volume de tráfego com uma mínima configuração adicional. Ele é dimensionado com facilidade por meio de módulos, que podem ser configurados de forma individual para personalizar a demanda do usuário.

Também é possível remover módulos indesejados para tornar o servidor Apache mais leve e eficiente. Os módulos mais populares que podem ser adicionados são:

`SSL (Secure Sockets Layer);`

PHP (Server Side Programming Support);
configurações de balanceamento de carga.
Na hospedagem de sites é essencial que o Apache seja a ferramenta escolhida, pois garante flexibilidade e desempenho necessários a uma aplicação web. Se você não sabe como criar um site institucional ou um blog, a partir deste artigo já começa a entender como funcionam os processos por trás de toda a capacidade dessa tecnologia.

A maior vantagem do Apache é seu código fonte, que está disponível gratuitamente para qualquer pessoa, sem que nenhuma licença seja requerida. A facilidade na correção de erros também garante a estabilidade da página, fator essencial para a credibilidade da sua empresa na Internet.

Além disso, sua capacidade modular, com a possibilidade de adição constante de novos recursos torna-o um software escalável, confiável e requisitado pela maioria de desenvolvedores e técnicos.

# Links Úteis 

Servidor: https://rockcontent.com/br/blog/servidor-dedicado/

Documentação Ngnix é uma alternativa ao Apache : https://docs.nginx.com/nginx/admin-guide/installing-nginx/installing-nginx-docker/

Docker Compose e Servidor Ngnix : https://rafaeldalsenter.medium.com/docker-compose-nginx-aplica%C3%A7%C3%A3o-web-banco-de-dados-d8f6f33adfd2

Imagem Docker do Ngnix : https://hub.docker.com/_/nginx

