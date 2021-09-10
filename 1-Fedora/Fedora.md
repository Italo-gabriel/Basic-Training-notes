># LINUX FEDORA - ***CONHECENDO A COMAND-LINE*** 
>>> ( Curso base das anotacoões ) https://web.digitalinnovation.one/course/linux-a-introducao-ao-sistema-operacional/learning/e7f619cd-dda9-482a-bd09-88e9b1d26098/ 

># COMANDOS INICIAS

***alt+space*** e digita _terminator_ = abre um terminal

***Ctrl+T*** = abre novas guias de terminal dentro de um terminal ja em execucao.

***Ctrl+Super*** (o super é a tecla com a logo do Windows) + Setas De Movimentacao Do Teclado < ou > = alternar entre as guias que estão abertas no terminal

***Ctrl+W*** = fecha a guia do terminal ,mas se caso houver varias guias abertas , esse comando fecha uma guia por vez. 

***Ctrl+Q*** = fecha todas as guias do terminal que estiverem abertas de uma única vez

***Ctrl+Shift+I*** = Abre um terminal com varias guias com varios ramos de desenvolvimento da liferay

>>## São duas formas de representar o mesmo caminho 

    [Usuario administrador]
    [local/usuario]
    [home/me]
    [~]
---
    [~] = significa pasta pessoal (~ é o mesmo que >>> /home/me ) 

    [/] = onde se encontra o diretório raiz do sistema linux , para guarda as informacões de programas instalados no sistems e também pastas de funcionamento do próprio sistema linux.

![](imagens/001.png)

***pwd*** = mostra qual o caminho que está atualmente 

***history*** = tras o histórico de todos os comandos utilizados em execucão do terminal.

***seta ^ para Cima Do Teclado*** = se apertamos na seta para cima do nosso teclado conseguimos navegar entre esse historico de comandos- ele vai alternando e mostrando no terminal.

***!!*** = vai repetir o último comando digitado no terminal

># ATALHOS PARA UTILIZAR DENTRO DO TERMINAL

    Quando entramos em algum editor de texto pelo terminal por exemplo e queremos sair, qual tecla de atalho utilizar ? 
***Ctrl+C*** = cancela o comando atual em funcionamento 

***Ctrl+Z*** = pausa o comando atual, colocando ele em segundo plano

    fechando o terminal

***Ctrl+D*** = faz logout da sessao atual, sai do terminal

***exit***= sai do terminal assim com o Crtl+d

    escrevendo no terminal e manipulando O QUE FOI ESCRITO
***Ctrl+W*** = apaga uma palavra na linha atual

***Ctrl+U*** = apaga a linha inteira

***Ctrl+R*** = busca um comando recente

***!!*** = repete o ultimo comando

># NAVEGANDO ENTRE DIRETORIOS(PASTAS)/ARQUIVOS

***cd 'NomeDaPasta'*** =  Vai mover entre os diretörios(pastas) 

***cd ..*** = os dois pontos indica que queremos voltar uma pasta, retornar 

***cd*** ou ***[cd ~]*** = se for o comando apenas com cd + espaco em branco  ele vai retornar para o diretório /home/me

***cd /*** = vai retornar para o diretorio raiz do Linux 

    [man cd] ou  [cd --help] = manual do comando - vai listar todas as opcões

># LISTANDO OS DIRETÓRIOS (PASTAS)/ARQUIVOS

***ls*** = Lista as pastas de uma Diretório que estamos acessando

***ls -la*** = lista os diretórios e os arquivos existentes na pasta, tanto as pastas/arquivos visiveis, quanto ocultos que inicia o nome com (.)

***ls -l*** = lista diretorios e arquivos com detalhes assim com o -la , so que nao mostra arquivos ocultos 

    outra opcão- pode ser usado junto com o nome da pasta que voce deseja listar
***ls 'NomeArquivo'*** - nesse caso não vai entrar na pasta ele apenas vai listar a pasta que foi especificada e continua no local atual

    [man ls] ou  [ls --help] = manual do comando - vai listar todas as opcões.

># CRIANDO DIRETÓRIOS(PASTAS)

***mkdir 'NomeDaPasta'*** =  cria pastas (diretórios) 

># RENOMEANDO E MOVENDO DIRETÓRIOS(PASTAS) E ARQUIVOS

***mv 'NomeDaPastaOuArquivo'*** [mv NomeAtual novoNome]= Vai renomear uma pasta ou arquivo

***mv NomeDaPasta caminho*** [mv Nome /caminho da pasta que vai receber o arquivo vai mover um arquivo/diretorio(pasta)atual para o caminho que ficou determinado.

># CRIANDO ARQUIVOS

***touch 'Nome'*** = cria arquivos vazios

[CONTINUAR DA AULA 2.3]
