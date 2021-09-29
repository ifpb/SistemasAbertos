# REDIRECIONAMENTO E EDITORES

Baseado no Material do Prof. Leônidas Lima Júnior, leonidas.lima@gmail.com, (2011)

Atualizado por Vinicius Centurion em 2021

## SUMÁRIO
* Entrada e saídas padrão
* Redirecionadores
* Pipes
* Editores de texto
* Editor vi

## ENTRADA E SAÍDAS PADRÃO

* Cada processo no Linux ganhaautomaticamente 3 tipos de streams de I/O:
1. stdin (Standard Input)
    * Normalmente associado ao teclado
    * Descritor de arquivo 0
2. stdout (Standard Output)
    * Normalmente associado ao vídeo
    * Descritor de arquivo 1
3. stderr (Standard Error)
    * Normalmente associado ao vídeo
    * Descritor de arquivo 2

## REDIRECIONADORES

* Cada um dos streams padrão do Linux pode ser redirecionado para um arquivo ou para outro processo usando redirecionadores
* Exemplos de redirecionadores:

    ```
    <   <<
    >   >>
    2>  2>>
    ```

    ## Redirecionador >
    * Redireciona a saída padrão de um programa/comando/script para algum dispositivo ou arquivo em vez do dispositivo de saída padrão (vídeo)
    * Quando usado com arquivos, cria ou substitui o conteúdo do arquivo
    * Exemplos:
        
        ```
        # ls -la > listagem
        # cat /etc/passwd > passwd_copia
        ```

    ## Redirecionador >>
    * Redireciona a saída padrão de um programa/comando/script para algum dispositivo ou final de arquivo em vez do dispositivo de saída padrão (vídeo) 
    * A diferença é que ao ser usado com arquivos, adiciona a saída ao final do arquivo existente em vez de substituir seu conteúdo
    * Exemplo:
        
        ```
        # echo "Leônidas Lima" >> lista-nomes.txt
        ```

    ## Redirecionador 2>
    * Redireciona a saída padrão de erros de um programa/comando/script para algum dispositivo ou arquivo em vez do dispositivo de saída padrão de erros (vídeo)
    * Quando usado com arquivos, cria ou substitui o conteúdo do arquivo 
    * Exemplos:
        
        ```
        $ find / -type d -print 2> erros.txt
        $ find / -type d -print > diretorios.txt 2>
        erros.txt
        ```

    ## Redirecionador 2>>

    * Redireciona a saída padrão de erros de um programa/comando/script para algum dispositivo ou final de arquivo em vez do dispositivo de saída padrão de erros (vídeo)
    * A diferença é que ao ser usado com arquivos, adiciona a saída ao final do arquivo existente em vez de substituir seu conteúdo
    * Exemplo:
        
        ```
        $ find / -type d -print 2>> erros-log.txt
        ```

    ## Redirecionador <

    * Redireciona a entrada padrão de um programa/comando/script para algum dispositivo ou arquivo em vez do dispositivo de entrada padrão (teclado)
    * Exemplos:
        
        ```
        # cat < /etc/passwd
        # cat < /etc/passwd > copia-passwd
        # sort < /etc/passwd
        # sort < /etc/passwd > passwd-ordenado
        ```

    ## Redirecionador <<

    * Estabelece um identificador para encerrar o fluxo de entrada padrão em vez da marca de fim de arquivo (Ctrl+D)
    * Não realiza exatamente um redirecionamento, apenas controla o término da entrada padrão
    * Exemplo:

        ```
        # sort << final
        Daniel
        Alice
        final
        ```

## PIPES |
    
* O pipe liga a saída de um comando com a entrada do próximo comando. Os dados enviados são processados pelo próximo comando que mostrará o resultado do processamento
* Exemplos
    
    ```
    # ls -la /etc | more
    # cat /etc/passwd | grep bash | sort
    ```

## EDITORES DE TEXTO

* Os editores de texto para console mais conhecidos e mais utilizados no Linux são:
    * vi
    * joe
    * pico
    * mcedit
    * jed
    * elvis
    * emacs

## EDITOR VI

* O vi é um editor de texto que integra praticamente todos os sistemas Linux e Unix
    * Atualmente muitas distribuições estão vindo com o vim uma versão mais completa do vi mas mantendo as suas características básicas
* Modos do vi
    * Modo de comando
    * Modo texto
    * Modo linha

### MODO COMANDO DO VI

* No modo comando o usuário vai poder fazer buscas, deletar texto, mudar texto e várias outras operações de manipulação
* Existem vários comandos para o editor vi, os próximos slides vão apresentar os principais destes comandos, agrupados de acordo com suas funcionalidades

### COMANDOS DO VI

* Movimentação de palavra

    * w - pula uma palavra
    * 2w - pula duas palavras
    * b - volta uma palavra
    * 3b - volta três palavras
    * $ - vai para o fim da linha
    * ^ - vai para o inicio da linha

* Controle do cursor

    * G - final do arquivo
    * #G - vai para uma linha qualquer
    * Ctrl g - informa a linha que você foi
    * Ctrl b - retorna página
    * Ctrl f - avança página
    * Ctrl u - retorna metade da página
    * Ctrl d - avança metade da página
    * L - última linha da tela
    * H - início da tela


* Entrada de dados (ativa modo de edição)
    * a - acrescenta texto depois do cursor
    * i - insere texto antes do cursor
    * o - abre uma linha de texto abaixo
    * O - abre uma linha de texto
    * A - acrescenta texto no fim da linha
    * I - insere texto no início da linha

* Remoção texto
    * x - deleta um caractere
    * 3x - deleta três caracteres
    * dw - deleta palavra
    * 2dw - deleta duas palavras
    * dd - deleta linha corrente
    * dG - deleta até a última linha do arquivo
    * d$ - deleta até o fim da linha
    * d^ - deleta até o início da linha

* Alteração de texto

    * r - substitui caractere
    * R - substitui todas as letras até pressionar ESC
    * cw - altera palavra
    * cc - altera a linha inteira
    * cG - altera até a última linha do arquivo
    * c$ - altera até o fim da linha
    * u - desfaz última alteração

* Cópia de texto

    * yw - copia palavra corrente
    * yy - copia a linha corrente
    * yG - copia até a última linha do arquivo
    * y$ - copia até o fim da linha
    * y^ - copia até o início da linha
    * p - cola abaixo do cursor
    * P - cola acima do cursor


* Busca de texto

    * /busca - Procura por expressões abaixo do cursor
    * ?busca - Procura por expressões acima do cursor
    * n - Repete a última busca na mesma direção

### MODO TEXTO DO VI

* No modo texto o usuário pode inserir texto de maneira natural, sem que nenhuma tecla seja interpretada como comando
* Para entrar no modo texto o usuário deve inserir algum comando de inserção ou alteração de texto como i, a, R, etc.
* Para sair do modo texto o usuário deve digitar a tecla ESC

### MODO LINHA DO VI

* No modo linha o usuário envia comandos especiais denominados comandos de linha
* Para entrar no modo o usuário digita o caractere “:”, seguido do comando a ser executado
* Para sair do modo linha o usuário deve digitar ESC ou Ctrl+C, ou completar a execução do comando pressionando ENTER