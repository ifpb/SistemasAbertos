# PERMISSÕES DE ARQUIVO

Baseado no Material do Prof. Leônidas Lima Júnior, leonidas.lima@gmail.com, (2011)

Atualizado por Vinicius Centurion em 2021

## SUMÁRIO

* Permissões de arquivos e diretórios
* Permissões especiais
* Comandos de manipulação das permissões
* Comandos de alteração do dono e grupo

## PERMISSÕES DE ARQUIVOS E DIRETÓRIOS

* Permissões de acesso protegem o sistema de arquivos Linux do acesso indevido de pessoas ou programas não autorizados
* Donos, Grupos e outros 
    * O princípio da segurança no sistema de arquivos GNU/Linux é definir o acesso aos arquivos por donos, grupos e outros usuários
* Tipos de Permissões de acesso
    * r - Permissão de leitura para arquivos e diretórios
    * w - Permissão de gravação para arquivos e diretórios
    * x - Permite executar um arquivo e acessar diretórios

* Etapas para acesso a um arquivo/diretório
    * Inicialmente, verifica-se se o usuário pertence a uma das classes (dono, grupo ou outros) e em seguida são verificadas as permissões específicas atribuídas ao arquivo ou diretório para aquela classe.

## PERMISSÕES DE ACESSO ESPECIAIS

* Em adição às três permissões básicas (rwx), existem permissões de acesso especiais (st) que afetam arquivos executáveis e diretórios
    * s - Quando é usado na permissão de acesso do Dono, ajusta a identificação efetiva do usuário do processo durante a execução de um programa, também chamado de bit setuid. Quando usada em diretórios faz com que os arquivos criados no diretório pertençam ao grupo do diretório setguid
    * t - Em diretórios, impede que outros usuários removam arquivos dos quais não são donos (stick-bit)

## COMANDOS DE MANIPULAÇÃO DAS PERMISSÕES

### Comando chmod
* chmod é responsável pela manipulação de permissões em arquivos e diretórios no Linux chmod [opções] [permissões] [diretório/arquivo] ugoa+-=rwxXst
* ugoa: Controla que nível de acesso será alterado.
    * Especificam, em ordem, usuário (u), grupo (g), outros (o), todos (a).
* +-= -
    * `+` insere a permissão, 
    * `-` retira a permissão do arquivo, e
    * `=` define a permissão exatamente como especificado.
* rwx
    * r permissão de leitura do arquivo;
    * w permissão de gravação;
    * x permissão de execução (ou acesso a diretórios)
* Exemplo:
    
    ```
    chmod a+x teste.txt
    ```

### Modos de permissão
* Modo octal:
    * 0 - Nenhuma permissão de acesso. Equivalente a -rwx.
    * 1 - Permissão de execução (x).
    * 2 - Permissão de gravação (w).
    * 3 - Permissão de gravação e execução (wx).
    * 4 - Permissão de leitura (r).
    * 5 - Permissão de leitura e execução (rx).
    * 6 - Permissão de leitura e gravação (rw).
    * 7 - Permissão de leitura, gravação e execução. Equivalente a +rwx.
* Exemplo:
    
    ```
    # chmod 755 /home/aluno/teste.txt
    ```

## COMANDOS DE ALTERAÇÃO DO DONO E GRUPO

### Comando chgrp
* Muda o grupo de um arquivo/diretório # chgrp [opções] [grupo] [arquivo/diretório]. 
* Onde opções:
    * -c, --changes: mostra os arquivos/grupos alterados
    * -f, --silent: não mostra mensagens de erro
    * -v, --verbose: mostra todas as mensagens e arquivos sendo modificados
    * -R, --recursive: altera os grupos de arquivos/sub-diretórios do diretório atual

### Comando chown
* Muda dono/grupo de um arquivo/diretório # chown [opções] [dono.grupo] [arquivo/diretório] 
* As opções são as mesmas dos comandos chgrp e chmod mostradas anteriormente
* O dono.grupo pode ser especificado usando o nome de grupo ou o código numérico correspondente ao usuário (UID) e grupo (GID)
* Exemplos:

    ```
    # chown aluno /home/aluno/teste.txt
    # chown -R jose.professores /home/jose
    ```