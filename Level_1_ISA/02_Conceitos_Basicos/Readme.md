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