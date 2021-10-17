## Vamos falar um pouquinho sobre o Linux:



* Root   ➜ Administrador

* /    ➜   /home (diretório raiz)

* ~   ➜    /home/usuario (diretório pessoal)

  ​


### Comandos principais:

----------

* `Ctrl + Alt + t`   ➜  Atalho abrir o terminal

* `cd + nome_dir`   ➜ muda para o diretório informado

* `cd  ..`   ➜ retornar ao diretório anterior

* `cd /`   ➜   muda para o diretório raiz

* `cd ~`   ➜   muda para o diretório pessoal

* `ls`   ➜  listar diretórios / arquivos do diretório atual

* `ls -l`   ➜ listar com detalhes

* `ls + nome_dir`   ➜  listar o diretório informado

* `mkdir + nome_dir`  ➜ cria um diretório 

* `touch + nome_arquivo_com_ext`   ➜ cria um arquivo vazio

* `cp + nome_arq + nome_dir`   ➜  copia arq para o dir informando

* `mv + nome_dir + novo_nome_dir`   ➜    renomear 

* `mv + nome_dir + nome_dir`   ➜   mover diretório

* `rmdir + nome_dir`   ➜   remove diretório vazio

* `rm -r + nome_dir`   ➜  remove diretório cheio

* `rm + nome_arq`   ➜   remove arquivo

* `clear ou Ctrl + l`   ➜   limpa terminal

* `Ctrl + d ou exit`   ➜  sai do terminal

  ​



### Comandos complementares:

--------------------

* `tecla tab`  ➜  alto completa 


* `history`   ➜  histórico de comandos 
* :arrow_up:   ➜  comandos anteriores
* :arrow_down:   ➜  comando posteriores
* `!!`     ➜  último comando digitado
* `man + comando`   ➜   manual do comando informado
* `comando + --help`    ➜   manual do comando informado (em português)
* `|`    ➜   separa um comando do outro
* `&&`  ➜  permite executar dois comando, mas o segundo só é executado se o primeiro for concluído com sucesso
* `>`    ➜   entrada de um arquivo com a saída / conteúdo de um outro arquivo ou comando


* `pwd`   ➜   mostrar diretório + caminho atual

  ​


### Manipulação e edição de arquivos:

------

* **nano** : editor de arquivos no terminal



* `nano + nome_arq`   ➜  abre o arquivo no editor de texto nano


  * `Ctrl + O`    ➜  salvar
  * `Ctrl + X`    ➜  sair

* **vi** : editor de texto (no terminal) 

* `vi + nome_arq`    ➜   abre o arquivo no editor de texto vi


  * `esc + :wq! + enter`   ➜  salvar e sair
* `cat + nome_arq`   ➜  visualizar conteúdo do arquivo no terminal
* `tac + nome_arq`   ➜  mesma saída do cat, mas inverte as linhas
* `grep + palavra + nome_arq`  ➜   pesquisa no arquivo a palavra informada
  * ex:   `cat nome_arq | grep palavra_procurar`



* `head + nome_arq`  ➜   mostra as 10 primeiras linhas do conteúdo do arquivo no terminal

* `tail + nome`   ➜  mostra as 10 últimas linhas do conteúdo do arquivo no terminal

* `tail ou head + nome_arq > novo_arquivo`   ➜  cria um arquivo com as 10 últimas ou primeiras linhas do arquivo informado


    * ex:  `tail teste.txt > novoteste.txt`
* `comando > nome_arq`    ➜  joga a saída do comando para dentro do arquivo criado, como conteúdo
  * ex:   `cal > calendario.txt`    



* `cal`     ➜  exibe calendário do mês atual

* `date`   ➜  exibe data (dia da semana / dia / mês / ano / hora)

  ​

### Paginação de arquivos:

----------------------

* `cat + nome_arq | more`    ➜  exibe conteúdo do arquivo até certo ponto e exibe um -----more-----, dai é só clicar para visualizar o resto do arquivo (para utilizar com arquivo com bastante conteúdo)


* `cat + nome_arq | less`    ➜  igual ao "more"

* *more* (clicar na tecla "enter")  **x**  *less* (rolar o mouse)

*  &     ➜  2 saídas separadas, tecla enter finaliza

* &&  ➜  1 saída sem pausa, tudo junto

  * ex:   `cat teste.txt & ou && novoteste.txt` 

* `find + ~ + -name + nome_arq`     ➜  caminho do arquivo

* `file + nome_arq ou nome_dir`     ➜  retorna como saída o tipo

* `whatis + comando`   ➜  retorna o que aquele comando faz

  ​

### Diretórios principais:

-------------------



|   bin    |    lib    |   srv    | proc |
| :------: | :-------: | :------: | :--: |
| **boot** | **media** | **tmp**  |      |
| **dev**  |  **mnt**  | **usr**  |      |
| **etc**  |  **opt**  | **var**  |      |
| **home** | **sbin**  | **root** |      |

​		

### Comando do sistema:

------------

* `lscpu`   ➜  informações da cpu


* `cat /proc/cpuinfo`   ➜   informações da cpu

  * `| more`   ➜   mais informações

* `cat /proc/meminfo`   ➜   informações da memória

* `lspci`   ➜  hardware conectados via pci

* `lsusb`   ➜  hardware conectados via usb

* `lshw`     ➜  relação dos hardware (modo completo - root)

  * `-short`   ➜ "detalhes"

* `arch`    ➜   mostra a arquitetura do kernel

* `uname`  ➜   nome do kernel

  * `-r`   ➜  versão do kernel
  * `-m`   ➜  arquitetura do kernel

* `free`   ➜   em relação a memória

* `du -h ~`   ➜   relação de memória usada com diretórios do dir informado

  * h = human readable   ➜  "leitura para humano facilitada"  

* `cat /etc/passwd`   ➜   usuários do sistema

* `reboot`    ➜   reiniciar

* `shutdown + opção + tempo`     ➜   desliga a máquina com a opção e no tempo informado

* `init O`    ➜   desliga a máquina

* `telinit O`   ➜   desliga a máquina

* `halt`   ➜  autenticação + desliga máquina

* `whereis`  ➜  caminho do comando e do manual

* `which`      ➜   caminho do comando

* `logout`    ➜   finaliza seção

  ​

### Permissões:

------

- servem para arquivo e diretório

  ​

| Caracter |            Permissões             | Valores |
| :------: | :-------------------------------: | :-----: |
|   `r`    |   Permissão de leitura (*read*)   |    4    |
|   `w`    |  Permissão de escrita (*write*)   |    2    |
|   `x`    | Permissão de execução (*execute*) |    1    |
|   `-`    |      Permissão desabilitada       |    0    |



- `ls -lh`   ➜  detalhes sobre arquivos e diretórios do dir atual

- `chmod + permissões + arq. ou dir.`   ➜  altera as permissões do arq. ou dir.

  - permissões: número de base octal

  ​

| Permissões    | Valores referentes as permissões |
| ------------- | -------------------------------- |
| r - w - x     | 7                                |
| r - w -  -    | 6                                |
| r -  -  - x   | 5                                |
| -  - w - x    | 3                                |
| s/ permissões | 0                                |

​	

### Redes / protocolos:

-----------------

* /dev/   ➜   interface de rede


* loopback: interface especial - conexão com você mesmo   ➜  IP: 127.0.1.1

  ​

**Comandos:**

* `ifconfig`   ➜   informações de rede

* `hostname`   ➜   nome do host na rede

  * `+ -I`    ➜  endereço IP do host
  * `+ -i`    ➜  endereço loopback

* `who`   ➜  como está logado na rede  (usuário + data e hora)

* `whoami`   ➜  usuário logado

* `ping + end_host`   ➜   verifica se o host informado está ativo

  * pong: resposta
  * `Ctrl + z` : parar as respostas

* `dig + end_host`   ➜   informações sobre o DNS (caminhos de rede)

  * `+short` : mostra o IP

* `traceroute + end_host`   ➜   caminho (nós) da nossa máquina (host) até o host informado

* `whois + end_host`   ➜   informações mais detalhadas do comando *dig*

* `finger`    ➜    informações usuário logado

* `w`   ➜   informações usuário logado detalhado

  ​

### Comandos diversos:

----------------

* `history -c`   ➜  limpa o histórico de comandos


* `alias + apelido = 'comando'`   ➜  atribui um apelido ao comando informado
  * ex:  `alias h='history'`

* `nl + nome_arq`   ➜  imprime o cat com o número de linhas do arquivo

* `wc -l + nome_arq`   ➜  saída número de linhas

* `wc -w + nome_arq`   ➜  saída número de palavras

* `cmp + nome_arq + nome_arq`    ➜  compara estes dois arquivos

* `diff + nome_arq + nome_arq`   ➜  diferença entre os arquivos

* `sort -n + nome_arq`   ➜   organiza de forma crescente o conteúdo do arquivo

* `last reboot`   ➜  informações sobre reiniciação do sistema

* `route -n`    ➜   saída tabela de roteamento do kernel

* `time + comando`   ➜  mostra o tempo de processo do comando

* `uptime`   ➜  mostra tempo que o sistema está rodando

* `cowsay + "frase"`   ➜  desenho de uma vaca falando a frase informada

* `xcowsay  + "frase"`   ➜  desenho de uma vaca falando a frase informada, em 2D

* `cmatrix`   ➜  efeito de matrix

* *existem outros comandos com esses efeitos no terminal*

  ​

### Usuários:

----------------

* **sudo:** permissão mais "alta" de usuário   ➜  root

* `sudo + adduser + nome_usuario`   ➜  adicionar usuário

  * informar: senha  |  nome  |  tel 

* `su + nome_usuario`   ➜  troca de usuário

  * informar: senha do usuário

* `passwd + nome_usuario`   ➜  alterar senha

  * informar: atual e nova

* `lastlog`   ➜  informações sobre usuários logados

* `last`   ➜  listagem de entrada e saída do usuário

* `logname`   ➜  usuário atual logado

* `id`   ➜  todos os identificadores do usuário

* `cat /etc/passwd`   ➜  exibe todos os usuários

* `userdel -r + nome_usuario`   ➜  deleta usuário  

  * -r: deleta pasta pessoal do usuário

    ​

### Grupos:

----------------

* `cat /etc/group`   ➜  exibe todos os grupos do sistema


* `groups`   ➜  exibe todos os grupos que o usuário pertence

* `sudo addgroup + nome_grupo`   ➜  cria um grupo

* `sudo adduser + nome_usuario + nome_grupo`   ➜  adiciona o usuário ao grupo

* `sudo gpasswd -a + nome_usuario + nome_grupo`   ➜  adiciona o usuário ao grupo

* `sudo gpasswd -d + nome_usuario + nome_grupo`   ➜   remove usuário do grupo

* `groupdel + nome_grupo`   ➜  remover grupo

  ​

### Compactadores:

-------

* **gzip:**

  `gzip + nome_arq`    ➜  compactação (arquivo.gz)

  `gunzip + nome_arq.gz`   ➜  descompactação 

* **zip:**

  * pode compactar mais de 1 arquivo junto (cria um diretório .zip)

  `zip + nome_arq.zip + nome_arq`    ➜  compactação (cria um outro arq. ou dir com a ext .zip)

  `unzip + nome_arq.zip`    ➜  descompactação

* **bzip2:**

  `bzip2 + nome_arq`     ➜  compactação (arquivo.bz2)

  `bzip2 -d + nome_arq.bz2`   ➜   descompactação

* **rar:**

  * precisa ser instalado
  * consegue compactar mais de 1 arquivo junto (cria um diretório .rar)

  `rar a + nome_arq.rar + nome_arq`   ➜   compactação (cria um outro arq. ou dir. com a ext .rar)

  `rar x + nome_arq.rar`     ➜   descompactação

  ​



### Arquivadores:

--------------

* **tar:**

  * depois de arquivar o(s) arquivo(s), pode ser compactado também

  `tar -cf + nome_arq.tar + nome_arquivo(s)`     ➜   arquivação

  `tar -xvf + nome_arq.tar`    ➜   desarquivação

  `tar -xvf + nome_arq.tar + -c + nome_dir`     ➜   desarquivar no diretório informado

  ​



### Gerenciamento de pacotes:

-------

* método fácil de instalação de pacotes (pelo terminal)

* pacotes: incluem arquivos necessários para instalação de um programa / aplicativo

  * extensões:  `.deb`  |  `.rpm`  | outros

* sites de pacotes:

  * <https://pkgs.org>

  * <http://rpm.pbone.net>

    ​

* **apt:** 

  `sudo apt install + nome_pacote`    ➜  instalação do pacote

  `sudo apt upgrade + nome_pacote`    ➜  atualização do pacote

  `sudo apt remove + nome_pacote`      ➜  remover o pacote

  `sudo apt update && apt upgrade`    ➜  atualização de sistema

* **dpkg: gerenciador de pacotes (.deb)** 

  `sudo dpkg -i + nome_dir.deb (download)`   ➜  instalar pacotes com ext .deb

  `sudo dpkg -I + nome_dir.deb`     ➜   detalhes do pacote   |  package: nome do pacote

  `sudo dpkg -r + nome_pacote`       ➜   remover o pacote

* **rpm: gerenciador de pacotes (.rpm)**

  `sudo rpm -ivh --nodeps + nome_dir.rpm (download)`    ➜  instalar pacotes com ext .rpm

  `sudo rpm -U + nome_dir.rpm`     ➜   atulização do pacote

  `sudo rpm -e + nome_dir.rpm`     ➜   remover pacote

  ​



