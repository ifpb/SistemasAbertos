# CONCEITOS BASICOS DE LINUX

## SUMÁRIO
* Login, terminais e consoles, logout
* Interpretador de comandos
* Arquivos e diretórios
* FHS (Filesystem Hierarchy Structure)
* Comandos básicos

## LOGIN
* Após o termino da instalação inicia-se realmente o primeiro contato com o novo SO.
Essa interação se dá através do acesso ao sistema utilizando um login e senha que possuam acesso ao shell
* Usuário administrador: root
    * Possui permissões para realizar qualquer operação no sistema, por isso o seu uso tem que ser bastante disciplinado

## TERMINAIS E CONSOLES
* Partindo-se do princípio de que o Linux é um SO com características de multi-usuário é possível abrir mais de uma seção usando os terminais virtuais
* O Linux possui até 63 terminais virtuais sendo que apenas 6 são usados por padrão
* Para mudar de terminal basta apertar as teclas: ALT + Fx onde x representa o número do terminal

## LOGOUT
* Para sair da console em que se encontra basta digitar um dos comando abaixo:
    * exit
    * logout
    * CTRL + D

## CASE SENSITIVE

* Ao contrário do Windows o Linux é Case Sensitive ou seja, ele diferencia maiúsculo de minúsculo
* O comando ls é diferente de LS ou mesmo o arquivo texto fstab é diferente de Fstab 
* LS diferente de ls
* fstab diferente de Fstab
* Casa , CaSa, CAsa, caSA, cASA, ... são todos diferentes


## PROMPT DE COMANDO

* Aviso de comando (ou prompt) é a linha mostrada pelo interpretador de comandos(shell) para entrada de comandos pelo usuário.
    * O prompt para o usuário root é identificado por um #
    * O prompt para usuários normais é identificado por um $

## INTERPRETADOR DE COMANDOS

* O interpretador de comandos ou shell, é o programa responsável por receber e tratar as instruções enviadas pelo usuário e seus programas ao sistema operacional (o kernel) 
* Principais interpretadores de comando:
    * sh (Bourne Shell)
    * bash (criado pelo projeto GNU)
    * csh (C shell, mais popular em sistemas *BSD, incompatível com sh)
    * ksh (Korn Shell, mais popular em sistemas Unix, compatível com sh)

## ARQUIVOS

* O Linux não interpreta extensão de arquivos para identificação. Utiliza-se a extensão como parte do nome: arquivo.c
* Arquivos começados com “.” (ponto) são ocultos. Eles não são listados com o comando “ls”, a menos que a opção “-a” seja utilizada
* Arquivos podem ser do tipo texto ou binário
* Nomes de arquivo são case sensitive (distinção entre maiúsculas e minúsculas)

## DIRETÓRIOS

* No Linux/Unix são separados ‘/’ e não ‘\’
* O diretório atual é especificado por um ‘.’
* O diretório home é especificado por um ‘~’
* O diretório superior é especificado por ‘..’
* O diretório anterior é especificado por ‘-’
* Exemplos de diretórios em um SO Linux:
    * /
    * /etc
    * /root
    * /home

## FHS - FILESYSTEM HIERARCHY STANDARD

* Filesystem Hierarchy Standard (padrão para sistema de arquivos hierárquico), ou FHS, define os principais diretórios, e o seu conteúdo, em
um sistema operacional Linux ou do tipo Unix 
* O desenvolvimento de um sistema de arquivos padronizado começou em agosto de 1993 com o esforço para redefinir a estrutura de diretórios do Linux. O FSSTND (Filesystem Standard), um padrão para sistemas de arquivos
hierárquicos específico para o sistema Linux, foi lançado em 02/1994
* Foram lançadas revisões em 10/1994 e 03/1995
* No início do ano de 1996, surgiu um movimento, com o apoio da comunidade de desenvolvedores do BSD, que visava o desenvolvimento de versões do FSSTND para outros sistemas do tipo Unix, além do Linux
* A partir desta iniciativa foi realizado um esforço para determinar os problemas comuns aos sistemas do tipo UnixComo resultado da ampliação do escopo do problema, o nome do padrão foi alterado para FHS
* O FHS é mantido pelo Free Standards Group, uma organização sem fins lucrativos formada por importantes empresas de hardware e software, como HP, Red Hat, IBM e Dell 
* O Sistema proposto não obteve aceitação total, porém é sempre tido como ponto de referência

## DIRETÓRIOS NO FHS

Diretório | Descrição
------------ | -------------
/bin/ | Comandos binários essenciais
/boot/ | Arquivos de boot do sistema
/dev/ | Dispositivos
/etc/ | Arquivos de configuração do sistema
/home/ | Diretórios de usuários
/lib/ | Diretório com as bibliotecas
/mnt/ | Sistemas de arquivos montados
/media/ | Pontos de “montagem” para mídia removível
/opt/ | Pacotes estáticos de aplicações
/proc/ | Sistemas de arquivo virtual, com estado do Kernel
/root/ | Diretório home para o super usuário (root)
/sbin/ | Arquivos binários para propósito de administração
/tmp/ | Arquivos temporários
/srv/ | Dados específicos que são servidos pelo sistema
/usr/ | Hierarquia secundária para dados compartilhados
/var/ | Arquivos "variáveis", como logs, páginasWeb, etc.

## COMANDO BÁSICOS

* Comandossão ordens enviadas ao sistema operacional para executar tarefas
* Comandos podem receber opções e parâmetros
    * Opções são usadas para controlar como o comando será executado
        * -Opção identificada por uma letra
        * --Opção identificada por um nome
    * Parâmetros são dados passados ao comando

## COMANDO: ls

* Lista os arquivos de um diretório
* Sintaxe:
ls [opções] [caminho1/arquivo1] ...
    diretóriox - diretórios que deseja listar
    arquivox - arquivos que deseja listar
* Algumas opções:
    * -a, --all = Lista todos os arquivos (inclusive os ocultos)
    * -d, --directory = Lista o diretório ao invés do seu conteúdo
    * -l = Formato longo para listagem de arquivos
    * -s, --size = Mostra o tamanho de cada arquivo

## COMANDO: cd

* Troca de diretório. É preciso ter a permissão de execução para entrar no diretório
* Sintaxe: cd [diretório]
    diretório - diretório que deseja entrar.
* Exemplos:
    * cd sem parâmetros ou cd ~, retorna ao diretório home
    * cd / troca para o diretório raiz
    * cd - retornará ao diretório anteriormente acessado
    * cd .. sobe um nível na árvore de diretórios

## COMANDO: pwd

* Mostra o diretório corrente ou atual
* Sintaxe: pwd
* Exemplo:
    * # pwd
    * /root


## COMANDO: mkdir

* Cria novos diretórios
* Sintaxe: mkdir [caminho1/]diretório1 ...
    caminhox = Caminho onde o diretório será criado
    diretóriox = Nome do diretório que será criado
* Exemplo:
    '# mkdir /root/teste
    Cria-se o diretório teste no diretório /root

## COMANDO: rmdir

* Remove diretórios. Estes devem estar vazios
* Sintaxe: rmdir [caminho1/]diretório1 ...
    caminhox = Caminho onde o diretório será removido
    diretóriox = Nome do diretório a ser eliminado
* Exemplo:
    '# rmdir /root/teste
    Elimina-se o diretório teste no diretório /root

## COMANDO: cat

* Mostra o conteúdo de um arquivo
* Sintaxe: cat [opções] [diretório1/arquivo1]...
    diretório1/arquivo1 = Arquivo que deseja visualizar o conteúdo
* Opções
    -n, --number = Mostra o número das linhas enquanto o conteúdo do arquivo é mostrado
    -s, --squeeze-blank = Não mostra mais que uma linha em branco entre um parágrafo e outro

## COMANDO: tac

* Mostra o conteúdo de um arquivo em ordem inversa
* Sintaxe: tac [opções] [diretório1/arquivo1]...
    diretório1/arquivo1 = Arquivo que deseja visualizar o conteúdo
* Opções
    -b, --before = Coloca o separador antes ao invés de após
    -s, --separator=STRING – Usa STRING como separador de linhas ao invés de newline

## COMANDO: rm

* Apaga arquivos, diretórios e sub-diretórios
* Sintaxe: rm [opções] [diretório1/arquivo1]...
    diretório1/arquivo1 = Arquivo que deseja excluir
* Opções
    -i, --interactive = Confirma antes de remover. É opção padrão no caso do usuário root
    -v, --verbose = Mostra arquivos na medida que são removidos
    -r, --recursive = Usado para remover arquivos em sub-diretórios
    -f, --force = Não confirma antes de excluir

## COMANDO: cp

* Copia arquivos e/ou diretórios
* Sintaxe: cp [opções] [origem] [destino]
    origem = arquivos ou diretórios a serem copiados
    destino = local para onde os arquivos serão copiados
* Opções
    -i, --interactive = Confirma ao substituir um arquivo existente
    -f, --force = Não pergunta, substitui os arquivos caso já existam
    -R/ -r, --recursive = Copia arquivos e sub-diretórios
    -v, --verbose = Mostra arquivos enquanto estão sendo copiados

## COMANDO: mv

* Move e/ou renomeia arquivos e diretório
* Sintaxe: mv [opções] [origem] [destino]
    * origem = arquivos ou diretórios a serem movidos/renomeados
    * destino = local para onde os arquivos serão movidos ou novo nome
* Opções
    * -i, --interactive = Confirma ao substituir um arquivo existente
    * -f, --force = Não pergunta, substitui os arquivos caso já existam
    * -v, --verbose = Mostra arquivos enquanto estão sendo copiados

## REFERÊNCIAS

* MAZIOLI, Gleydson. Guia Foca Linux Intermediário – versão 5.60. Publicação própria, 2007