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
* `&&`   ➜  permite executar dois comando, mas o segundo só é executado se o primeiro for concluído com sucesso
* `>`   :arrow_right:   entrada de um arquivo com a saída / conteúdo de um outro arquivo ou comando


* `pwd`   ➜   mostrar diretório + caminho atual

  ​


### Manipulação e edição de arquivos:

------

* **nano** : editor de arquivos no terminal



* `nano + nome_arq`   ➜  abre o arquivo no editor de texto nano


  * `Ctrl + O`   :arrow_right:   salvar
  * `Ctrl + X`   :arrow_right:   sair

* **vi**  :arrow_right:  editor de texto (no terminal) 

* `vi + nome_arq`    :arrow_right:   abre o arquivo no editor de texto vi


  * `esc + :wq! + enter`  :arrow_right:  salvar e sair
* `cat + nome_arq`   :arrow_right:  visualizar conteúdo do arquivo no terminal
* `tac + nome_arq`   ➜  mesma saída do cat, mas inverte as linhas
* `grep + palavra + nome_arq`  ➜   pesquisa no arquivo a palavra informada
  * ex:   `cat nome_arq | grep palavra_procurar`



* `head + nome_arq`  ➜   mostra as 10 primeiras linhas do conteúdo do arquivo no terminal

* `tail + nome`  :arrow_right:  mostra as 10 últimas linhas do conteúdo do arquivo no terminal

* `tail ou head + nome_arq > novo_arquivo`  :arrow_right:  cria um arquivo com as 10 últimas ou primeiras linhas do arquivo informado


  * ex:  `tail teste.txt > novoteste.txt`
* `comando > nome_arq`   :arrow_right:   joga a saída do comando para dentro do arquivo criado, como conteúdo
  * ex:   `cal > calendario.txt`    



* `cal`   :arrow_right:   exibe calendário do mês atual

* `date`  :arrow_right:   exibe data (dia da semana / dia / mês / ano / hora)

  ​

### Paginação de arquivos:

----------------------

* `cat + nome_arq | more`   :arrow_right:  exibe conteúdo do arquivo até certo ponto e exibe um -----more-----, dai é só clicar para visualizar o resto do arquivo (para utilizar com arquivo com bastante conteúdo)


* `cat + nome_arq | less`   :arrow_right:  igual ao "more"

* *more* (clicar na tecla "enter")  **x**  *less* (rolar o mouse)

*  &    :arrow_right:   2 saídas separadas, tecla enter finaliza

* &&  :arrow_right:  1 saída sem pausa, tudo junto

  * ex:   `cat teste.txt & ou && novoteste.txt` 

* `find + ~ + -name + nome_arq`    :arrow_right:   caminho do arquivo

* `file + nome_arq ou nome_dir`    :arrow_right:   retorna como saída o tipo

* `whatis + comando`  :arrow_right:  retorna o que aquele comando faz

  ​

### Diretórios principais:

-------------------



|   bin    |    lib    |   srv    | proc |
| :------: | :-------: | :------: | :--: |
| **boot** | **media** | **tmp**  |      |
| **dev**  |  **mnt**  | **usr**  |      |
| **etc**  |  **opt**  | **var**  |      |
| **home** | **sbin**  | **root** |      |



### Comando do sistema:

------------

* `lscpu`  :arrow_right:  informações da cpu


* `cat /proc/cpuinfo`  :arrow_right:   informações da cpu

  * `| more`  :arrow_right:  mais informações

* `cat /proc/meminfo`  :arrow_right:  informações da memória

* `lspci`  :arrow_right:   hardware conectados via pci

* `lsusb`  :arrow_right:   hardware conectados via usb

* `lshw`  :arrow_right:  relação dos hardware (modo completo - root)

  * `-short`  :arrow_right:  "detalhes"

* `arch`   :arrow_right:    mostra a arquitetura do kernel

* `uname`  :arrow_right:  nome do kernel

  * `-r`  :arrow_right:  versão do kernel
  * `-m`  :arrow_right:  arquitetura do kernel

* `free`  :arrow_right:  em relação a memória

* `du -h ~`  :arrow_right:   relação de memória usada com diretórios do dir informado

  * h = human readable  :arrow_right:  "leitura para humano facilitada"  

* `cat /etc/passwd`   :arrow_right:   usuários do sistema

* `reboot`  :arrow_right:   reiniciar

* `shutdown + opção + tempo`    :arrow_right:   desliga a máquina com a opção e no tempo informado

* `init O`  :arrow_right:   desliga a máquina

* `telinit O`  :arrow_right:   desliga a máquina

* `halt`  :arrow_right:  autenticação + desliga máquina

* `whereis`  :arrow_right:  caminho do comando e do manual

* `which`   :arrow_right:   caminho do comando

* `logout`  :arrow_right:   finaliza seção

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



- `ls -lh`  :arrow_right:  detalhes sobre arquivos e diretórios do dir atual

- `chmod + permissões + arq. ou dir.`   :arrow_right:  altera as permissões do arq. ou dir.

  - permissões: número de base octal

  ​

| Permissões    | Valores referentes as permissões |
| ------------- | -------------------------------- |
| r - w - x     | 7                                |
| r - w -  -    | 6                                |
| r -  -  - x   | 5                                |
| -  - w - x    | 3                                |
| s/ permissões | 0                                |



### Redes / protocolos:

-----------------

* /dev/   :arrow_right:   interface de rede


* loopback: interface especial - conexão com você mesmo  :arrow_right:  IP: 127.0.1.1

  ​

**Comandos:**

* `ifconfig`  :arrow_right:  informações de rede

* `hostname`  :arrow_right:   nome do host na rede

  * `+ -I`  :arrow_right:  endereço IP do host
  * `+ -i`  :arrow_right:  endereço loopback

* `who`  :arrow_right:  como está logado na rede  (usuário + data e hora)

* `whoami`  :arrow_right:  usuário logado

* `ping + end_host`  :arrow_right:   verifica se o host informado está ativo

  * pong: resposta
  * `Ctrl + z` : parar as respostas

* `dig + end_host`  :arrow_right:   informações sobre o DNS (caminhos de rede)

  * `+short` : mostra o IP

* `traceroute + end_host`  :arrow_right:   caminho (nós) da nossa máquina (host) até o host informado

* `whois + end_host`  :arrow_right:   informações mais detalhadas do comando *dig*

* `finger`   :arrow_right:   informações usuário logado

* `w`  :arrow_right:   informações usuário logado detalhado

  ​

### Comandos diversos:

----------------

* `history -c`   :arrow_right:   limpa o histórico de comandos


* `alias + apelido = 'comando'`   :arrow_right:   atribui um apelido ao comando informado
  * ex:  `alias h='history'`

* `nl + nome_arq`  :arrow_right:  imprime o cat com o número de linhas do arquivo

* `wc -l + nome_arq`  :arrow_right:  saída número de linhas

* `wc -w + nome_arq`   :arrow_right:  saída número de palavras

* `cmp + nome_arq + nome_arq`  :arrow_right:   compara estes dois arquivos

* `diff + nome_arq + nome_arq`  :arrow_right:   diferença entre os arquivos

* `sort -n + nome_arq`  :arrow_right:   organiza de forma crescente o conteúdo do arquivo

* `last reboot`  :arrow_right:  informações sobre reiniciação do sistema

* `route -n`  :arrow_right:  saída tabela de roteamento do kernel

* `time + comando`  :arrow_right:  mostra o tempo de processo do comando

* `uptime`  :arrow_right:  mostra tempo que o sistema está rodando

* `cowsay + "frase"`  :arrow_right:  desenho de uma vaca falando a frase informada

* `xcowsay  + "frase"`  :arrow_right:  desenho de uma vaca falando a frase informada, em 2D

* `cmatrix`  :arrow_right:  efeito de matrix

* *existem outros comandos com esses efeitos no terminal*

  ​

### Usuários:

----------------

* **sudo:** permissão mais "alta" de usuário  :arrow_right:  root

* `sudo + adduser + nome_usuario`  :arrow_right:  adicionar usuário

  * informar: senha  |  nome  |  tel 

* `su + nome_usuario`  :arrow_right:  troca de usuário

  * informar: senha do usuário

* `passwd + nome_usuario`  :arrow_right:  alterar senha

  * informar: atual e nova

* `lastlog`  :arrow_right:  informações sobre usuários logados

* `last`  :arrow_right:  listagem de entrada e saída do usuário

* `logname`  :arrow_right:  usuário atual logado

* `id`  :arrow_right:  todos os identificadores do usuário

* `cat /etc/passwd`  :arrow_right:  exibe todos os usuários

* `userdel -r + nome_usuario`  :arrow_right:   deleta usuário  

  * -r: deleta pasta pessoal do usuário

    ​

### Grupos:

----------------

* `cat /etc/group`  :arrow_right:  exibe todos os grupos do sistema


* `groups`  :arrow_right:  exibe todos os grupos que o usuário pertence

* `sudo addgroup + nome_grupo`  :arrow_right:  cria um grupo

* `sudo adduser + nome_usuario + nome_grupo`  :arrow_right:  adiciona o usuário ao grupo

* `sudo gpasswd -a + nome_usuario + nome_grupo` :arrow_right:  adiciona o usuário ao grupo

* `sudo gpasswd -d + nome_usuario + nome_grupo`  :arrow_right:  remove usuário do grupo

* `groupdel + nome_grupo`  :arrow_right:  remover grupo

  ​

### Compactadores:

-------

* **gzip:**

  `gzip + nome_arq`   :arrow_right:  compactação (arquivo.gz)

  `gunzip + nome_arq.gz`  :arrow_right:   descompactação 

* **zip:**

  * pode compactar mais de 1 arquivo junto (cria um diretório .zip)

  `zip + nome_arq.zip + nome_arq`   :arrow_right:   compactação (cria um outro arq. ou dir com a ext .zip)

  `unzip + nome_arq.zip`    :arrow_right:   descompactação

* **bzip2:**

  `bzip2 + nome_arq`    :arrow_right:   compactação (arquivo.bz2)

  `bzip2 -d + nome_arq.bz2`   :arrow_right:   descompactação

* **rar:**

  * precisa ser instalado
  * consegue compactar mais de 1 arquivo junto (cria um diretório .rar)

  `rar a + nome_arq.rar + nome_arq`   :arrow_right:   compactação (cria um outro arq. ou dir. com a ext .rar)

  `rar x + nome_arq.rar`    :arrow_right:   descompactação

  ​



### Arquivadores:

--------------

* **tar:**

  * depois de arquivar o(s) arquivo(s), pode ser compactado também

  `tar -cf + nome_arq.tar + nome_arquivo(s)`     :arrow_right:    arquivação

  `tar -xvf + nome_arq.tar`    :arrow_right:    desarquivação

  `tar -xvf + nome_arq.tar + -c + nome_dir`    :arrow_right:   desarquivar no diretório informado

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

  `sudo apt install + nome_pacote`   :arrow_right:   instalação do pacote

  `sudo apt upgrade + nome_pacote`   :arrow_right:   atualização do pacote

  `sudo apt remove + nome_pacote`     :arrow_right:   remover o pacote

  `sudo apt update && apt upgrade`   :arrow_right:   atualização de sistema

* **dpkg: gerenciador de pacotes (.deb)** 

  `sudo dpkg -i + nome_dir.deb (download)`  :arrow_right:   instalar pacotes com ext .deb

  `sudo dpkg -I + nome_dir.deb`    :arrow_right:   detalhes do pacote   |  package: nome do pacote

  `sudo dpkg -r + nome_pacote`      :arrow_right:   remover o pacote

* **rpm: gerenciador de pacotes (.rpm)**

  `sudo rpm -ivh --nodeps + nome_dir.rpm (download)`   :arrow_right:   instalar pacotes com ext .rpm

  `sudo rpm -U + nome_dir.rpm`    :arrow_right:   atulização do pacote

  `sudo rpm -e + nome_dir.rpm`    :arrow_right:   remover pacote