# INSTALANDO O LINUX

## SUMÁRIO
* Criando uma máquina virtual
* Instalando o Debian 9
* Instalando o Ubuntu 18

## CRIANDO UMA MÁQUINA VIRTUAL
* Baixe e instale um software de virtualização, observando o sistema operacional da sua máquina e a arquitetura do processador:
    * [Oracle VirtualBox](https://www.virtualbox.org/wiki/Downloads); ou,
    * [VmWare Workstation Player](https://www.vmware.com/products/workstation-player.html)

1. Execute o programa de instalação VIRTUALBOX e clique em “NOVO” na tela principal, e a seguir, na janela "criar máquina virtual", escolha o nome, o tipo e a versão do sistema operacional que será instalado. No caso, foi dado o nome "Ubuntu" para máquina, tipo "Linux" e versão "Ubuntu 64-bit). Clique em próximo.

    ![selecione novo](imagens/00.png)
    ![nome, tipo e versão](imagens/01.png)

1. Selecione a quantidade de memória RAM da máquina. Clique em próximo. A seguir, selecione "criar um novo disco rígido virtual agora". Clique em criar. 
    * Observe os requisitos recomendados para instalação do sistema pelos desenvolvedores da distribuição que deseja instalar. Para o [Ubuntu 20.04](https://ubuntu.com/download/desktop), o site da distribuição recomenda 4GB de memória para o sistema e 25GB de espaço de disco, já para o [Debian 11](https://www.debian.org/download), recomenda-se 2GB de memória e 10GB de espaço livre em disco.

    ![memoria RAM](imagens/02.png)
    ![criar disco virtual](imagens/03.png)

1. Na janela "criar disco rígido virtual", selecione "VDI (virtualbox disk image)" para o tipo de arquivo de disco rígido. Clique em próximo. A seguir escolha a opção "dinamicamente alocado" para o armazenamento em disco rígido físico. Por fim, selecione o tamanho do disco a ser criado e clique em "criar".

    ![vdi](imagens/04.png)
    ![dinamicamente alocado](imagens/05.png)
    ![tamanho do disco](imagens/06.png)

1. Na janela inicial, clique em "[disco óptico]Vazio" e selecione a imagem da distribuição linux baixada previamente. Caso o não seja mostrada no menu de seleção, clique em "escolher uma imagem de disco" e selecione o local em que o arquivo de imagem foi salvo em seu computador. Por fim, clique em "INICIAR" para ligar a máquina virtual e começar a instalação do Linux.

    ![selecionando imagem](imagens/07.png)
    ![inicar instalação](imagens/08.png)


## INSTALANDO O DEBIAN 9


## INSTALANDO O UBUNTU 18

