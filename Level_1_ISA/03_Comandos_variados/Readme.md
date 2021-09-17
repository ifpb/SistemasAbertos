# COMANDOS VARIADOS DO LINUX

Baseado no Material do Prof. Leônidas Lima Júnior, leonidas.lima@gmail.com, (2011)

Atualizado por Vinicius Centurion em 2021

## SUMÁRIO
* [Comandos diversos](#comandos-diversos)
* [Comandos de tempo](#comandos-de-tempo)
* [Comandos de espaço de disco](#comandos-de-espaço-de-disco)
* [Comandos de manipulação de arquivos](#comandos-de-manipulação-de-arquivos)
* [Comandos de encerramento do sistema](#comandos-de-encerramento-do-sistema)
* [Comandos de localização](#comandos-de-localização)
* [Comandos TMUX](#comandos-tmux)

## COMANDOS DIVERSOS

### clear
* Limpa a tela e posiciona o cursor no canto superior esquerdo do vídeo

### uname
* Retorna o nome e versão do kernel atual  echo
* Mostra mensagens. Útil na construção de scripts para mostrar mensagens na tela para o usuário acompanhar sua execução

### su
* Permite ao usuário mudar sua identidade para outro usuário sem fazer o logout

### free
* Mostra detalhes sobre a utilização da memória RAM do sistema
* Opções: -b / -k / -m

### date
* Permite ver/modificar a data e hora do Sistema. 
* Apenas root pode modificar a data e hora do sistema: date MesDiaHoraMinuto[AnoSegundos]

* +[FORMATO] - Define o formato da listagem que será usada pelo comando date. Os formatos mais usados são:
    * %d - Dia do Mês (00-31) %m - Mês do Ano (00-12)
    * %y - Ano (dois dígitos) %Y - Ano (quatro dígitos)
    * %H - Hora (00-24) %I - Hora (00-12)
    * %M - Minuto (00-59) %j - Dia do ano (1-366)
    * %p - AM/PM

## COMANDOS DE TEMPO

### time
* Mede o tempo gasto para executar um processo (programa)
* sintaxe:
    
    ```
    # time [comando] 
    ```

    * Onde: comando é o comando/programa que se deseja medir o tempo gasto para ser concluído
* Exemplo:
    
    ```
    # time tar –czf backup.tar.gz /home
    > real 0m6.345s
    > user 0m2.848s
    > sys 0m3.428s
    ```

### uptime
* Mostra o tempo de execução do sistema desde que o computador foi ligado
* Exemplo:
    
    ```linux
    # uptime
    > 17:16:48 up 31 days, 10:00, 1 user, load average: 0.32, 0.54, 0.38
    ```

## COMANDOS DE ESPAÇO DE DISCO

### df
* Mostra o espaço livre/ocupado de cada partição
* sintaxe:
    
    ```
    # df [opções]
    ```

* Opções:
    * -h, --human-readable – Mostra o espaço livre/ocupado em MB, KB, GB ao invés
    * -H – Idêntico a -h mas usa 1000 ao invés de 1024 como unidade
    * -k – Lista em Kbytes.
    * -l – Somente lista sistema de arquivos locais
    * -m – Lista em Mbytes

### du
* Mostra o espaço ocupado por arquivos e sub-diretórios
* sintaxe:

    ```
    # du [opções] caminhos
    ```

* Opções:
    * -a, --all – Mostra o espaço ocupado por todos os arquivos.
    * -b, --bytes – Mostra o espaço ocupado em bytes.
    * -c, --total – Faz uma totalização de todo espaço listado.
    * -h, --human – Mostra em formato legível por humanos
    * -H – igual a -h mas usa 1000 como unidade de cálculo
    * -k – Mostra o espaço ocupado em Kbytes
    * -m – Mostra o espaço ocupado em Mbytes

## COMANDOS DE MANIPULAÇÃO DE ARQUIVOS

### grep
* Procura por um texto dentro de arquivo(s) ou na entrada padrão
* sintaxe:

    ```
    # grep [opções] [expressão] [arquivo]
    ```

* Opções:
    * -i, --ignore-case – Ignora diferença entre maiúsculas/minúsculas
    * -n, --line-number – Mostra número das linhas encontradas
    * -l – Lista apenas os nomes de arquivos, mas não as linhas
    * -c – Lista apenas a quantidade de linhas onde aparece o texto
    * -v – Lista linhas que não contêm o texto

### head
* Mostra linhas iniciais de um arquivo texto
* sintaxe:

    ```
    # head [opções] [arquivos]
    ```

* Opções:
    -c [numero] – Mostra o [numero] de bytes do inicio do arquivo
    -n [numero] – Mostra o [numero] de linhas do inicio do arquivo

* Caso não seja especificado, mostra as 10 primeiras linhas
* Exemplos

    ```
    # head /etc/passwd
    # head -n 20 /var/log/syslog
    ```

### tail
* Mostra linhas finais de um arquivo texto
* sintaxe:

    ```
    # tail [opções] [arquivos]
    ```

* Opções
    * -c [numero] – Mostra o [numero] de bytes do final do arquivo
    * -n [numero] – Mostra o [numero] de linhas do final do arquivo
    * Caso não seja especificado, mostra as 10 últimas linhas
* Exemplos
    ```
    #tail /etc/passwd
    #tail -n 20 /var/log/syslog
    ```

### more - Faz a paginação de arquivos ou da entrada padrão
* sintaxe:

    ```
    # more [opções] [arquivos]
    ```

### less - Realiza a paginação de arquivos ou da entrada padrão, de maneira semelhante ao more, mas permite o uso do PgUp/PgDn
* sintaxe:

    ```
    # less [opções] [arquivos]
    ```

### wc
* Conta o número de palavras, bytes e linhas em um arquivo ou entrada padrão. Se as opções forem omitidas, o wc mostra a quantidade de linhas, palavras, e bytes.
* sintaxe:

    ```
    # wc [opções] [arquivos]
    ```

* Opções:
    * -c, --bytes – Mostra os bytes do arquivo.
    * -w, --words – Mostra a quantidade de palavras do arquivo
    * -l, --lines – Mostra a quantidade de linhas do arquivo

### sort
* Organiza as linhas de um arquivo texto ou da entrada padrão
* sintaxe:

    ```
    # sort [opções] [arquivos]
    ```

* Opções:
    * -f – Ignora diferenças entre maiúsculas e minúsculas
    * -m – Junta conjunto de arquivos antes de ordenar
    * -r – Inverte o resultado da comparação
    * -n – Caso estja organizando um campo que contém números, os números serão organizados na ordem aritmética

### ln 
* Cria links (pseudônimos) para arquivos e diretórios no sistema
* sintaxe:
    ```
    # ln [opções][origem] [link]
    ```

* Opções mais usada:
    * -s – Cria um link simbólico. Usado para criar ligações com o arquivo/diretório de destino.

* Observações sobre os links
    * Se for usado o comando rm em um link, somente o link será removido 
    * Se for usado o comando cp em um link, o arquivo original será copiado ao invés do link
    * Se for usado o comando mv em um link, a modificação será feita no link 
    * Se for usado um comando de visualização (como o cat), o arquivo original será visualizado

## COMANDOS DE ENCERRAMENTO DO SISTEMA

### poweroff, halt
    * Realiza o encerramento do sistema seguido do desligamento da máquina
    * sintaxe:

        ```
        # poweroff
        # halt
        ```

### reboot
    * Realiza o encerramento do sistema seguido da reinicialização da máquina
    * sintaxe:

        ```
        # reboot
        ```

### shutdown
    * Desliga/reinicia o computador imediatamente ou após determinado tempo (programável) de forma segura
    * sintaxe:

        ```
        # shutdown [opções] [hora] [mensagem]
        ```

    * Opções:
        * -h – Inicia o processo para desligamento do computador
        * -r – Reinicia o sistema
        * -c – Cancela a execução do shutdown

    * Exemplo:

        ```
        # shutdown –h +1
        > “Máquina será desligada em 1 min."
        ```

## COMANDOS DE LOCALIZAÇÃO

### comando which
* Imprime a localização real de um comando. Por exemplo:
    ```
    $ which wget
    > /usr/bin/wget
    ```

* É comum que esta ainda não seja a localização real do comando, algumas vezes é apenas o link que está no PATH. Por Exemplo:
    ```
    $ which python
    > /usr/bin/python
    ```

    ```
    $ ls -l /usr/bin/python
    > lrwxrwxrwx 1 root root 7 abr 15 2020 /usr/bin/python -> python2
    ```

### comando grep
* Usado para filtrar uma saída, exibindo apenas o que quer. Por exemplo:
    
    ```
    $ ls /bin | grep ^pas
    > passwd
    > paste
    > pasteurize
    > pasuspender
    ```

    ```
    $ cat /etc/passwd | grep root
    > root: x:0:0:root:/root:/bin/bash
    ```

### comando find
* Poderoso comando para buscar arquivos em toda a máquina.
* Uso: find [diretório onde iniciar a busca] [padrão de busca]
    ```
    $ find . -name '*bkp*'
    $ find . -iname '*bkp*'
    $ sudo find / -iname '*.jpg'
    $ find /tmp -size +5M
    $ sudo find / -time -2
    $ sudo find ~ -amin -30
    ```

* Uso: find [diretório onde iniciar a busca] [padrão de busca]
* Pode executar um comando para cada arquivo encontrado. Por exemplo, copiar cada arquivo encontrado para uma pasta de backup:
    ```
    $ sudo find /home/images -type f -iname '*.png*' -exec cp {} /dropbox
    ```
* Ou remover todos os arquivos criados no último minuto:
    ```
    $ find /tmp -type f -amin -1 -exec rm -f {}
    ```

## COMANDOS TMUX

### Conhecendo o TMUX

* Tmux é um multiplexador de terminal: ele permite que uma série de terminais sejam criados, acessados e controlados a partir de uma única tela.
* Quando o tmux é iniciado, ele cria uma nova sessão com uma única janela e a exibe na tela. Uma linha de status na parte inferior da tela mostra informações sobre a sessão atual e é usada para inserir comandos interativos.

![tmux2](tmux2.png)

### Instalando o TMUX
* Via apt-get no Debian:
    
    ```
    # apt-get install tmux
    ```

### Inicializando o tmux
* Faça a chamada do tmux no terminal após o login:
    
    ```
    # tmux
    ```

### Dividindo horizontalmente

### Dividindo verticalmente

### Navegando com as setas direcionais

### Encerrando o terminal virtual
