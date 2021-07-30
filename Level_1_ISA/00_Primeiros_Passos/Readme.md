# INTRODUÇÃO AO LINUX
Baseado no Material do Prof. Leônidas Lima Júnior

leonidas.lima@gmail.com

(2011)

Atualizado por Vinicius Centurion em 2021

## SUMÁRIO

* Conceitos de software livre
* Histórico do Sistema UNIX
* Histórico do GNU/Linux
* Aplicações e uso do Linux
* Distribuições Linux

## SOFTWARE LIVRE

* Possui permissão de ser copiado, usado ou distribuído por qualquer pessoa, seja na sua íntegra ou com modificações.
* Código fonte deve estar disponível
* Distribuído gratuitamente ou sob remuneração
    * Software Livre é questão de liberdade e não de preço
    * Software Livre pode ser pago
* Definição criada pela Free Software Foundation, instituição criada por Richard Stallman

## RICHARD STALLMAN

* Famoso hacker, fundador do movimento free software, do projeto GNU, e da Free Software Foundation.
    * Aclamado programador, seus maiores feitos incluem Emacs (e o GNU Emacs, mais tarde), o GNU C Compiler e o GNU Debugger
    * É o autor da GNU General Public License (GPL), a licença livre mais usada no mundo

![richard stallman](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Richard_Matthew_Stallman.jpeg/330px-Richard_Matthew_Stallman.jpeg)

## PROJETO GNU

* O que é GNU?
    * GNU significa “Gnu is Not Unix”, é o nome de um sistema operacional completo compatível com o UNIX
* Por que do GNU?
    * O Projeto GNU é a concretização de uma filosofia, a filosofia do Software Livre

## Projeto GNU e Software Livre

* Software Livre é uma questão de liberdade:
    * Liberdade de usar os programas para qualquer propósito
    * Liberdade de modificar os programas de acordo com suas necessidades
    * Liberdade de redistribuir cópias seja grátis ou não
    * Liberdade de distribuir versões modificadas, assim toda a comunidade pode usufruir dos benefícios introduzidos

## Software de Domínio Público

* Software Livre é diferente de software de domínio público
    * O primeiro, quando utilizado em combinação com licenças típicas (como GPL e BSD), garante direitos autorais do programador ou organização que o criou
    * No segundo, o autor do software renuncia à propriedade do programa e este se torna um bem comum

## Copylefted Software

* São programas que colocam nas suas licenças uma cláusula que impede aos 
distribuidores incluirem novas cláusulas restritivas às licenças de suas distribuições. Isso garante que todas as cópias do programa distribuído continuam Free Software, mesmo se houver modificações
* No projeto GNU todos os programas são Copylefted, essa é a única forma de garantir o espírito de liberdade associado ao termo “Free Software”

## Non-Copylefted free Software

* Vem com a permissão do autor de modificação e redistribuição, 
permitindo também a adição de novas cláusulas restritivas à licença original
* O sistema X Window é um bom exemplo de programa non-copylefted. O X Consortium mantém uma distribuição básica que pode ser modificada e redistribuída de forma não gratuita

## GPL-covered Software

* A licença GNU GPL (General Public License) estabelece os termos de distribuição e utilização dos programas GNU
* GNU program/GNU software: programa lançado e mantido pelo Projeto GNU. Os programas GNU são escritos principalmente pelos membros ds Free Software Foundation e pela contribuição de inúmeros voluntários
* GNU System: é um sistema Unix-like completo, composto unicamente de programas GNU

## Semi-free Software

* Semi-free Software são programas que possuem permissão individual de uso, cópia e distribuição, mesmo com modificações, mas apenas para uso 
não comercial
* O programa PGP é um exemplo de programa semi-free

## Proprietary Software

* Aqueles programas que não são livres ou semi-free
    * Seu uso é restrito, sua distribuição e modificação são proibidas, ou requer uma permissão especial, ou possui tantas restrições que efetivamente estas iniciativas tornam-se praticamente inviáveis

## Freeware

* O termo Freeware não tem uma definição muito clara, entretanto é usado comumente para designar programas que permitem o uso e redistribuição mas não a modificação (o código fonte não está disponível)
    * Esses programas não são Free Software, portanto não é correto chamar Free Software de Freeware

## Shareware

* São programas que têm permissão de redistribuição
    * geralmente para continuar utilizando o programa, deve-se pagar por uma licença
* Shareware não é Free Software nem semi-free
    * Em geral o código fonte não está disponível, desta forma não é possível fazer modificações

## Commercial Software

* Softwares Comerciais são programas desenvolvidos por empresas que visam 
lucro com o uso dos mesmos. Comercial e proprietário não é a mesma coisa, 
embora a maioria dos programas comerciais sejam proprietários
* Um programa GNU pode ser comercial e também Free software

## HISTORIA DO SISTEMA UNIX

* 1969 - Ken Thompson e Dennis Ritchie entre outros começaram o trabalho usando um velho PDP-7 no Bells labs, nascia o UNIX

![ThompsonRitchie](http://1.bp.blogspot.com/-gVmxTCp5bhI/Tz4UZaFqIkI/AAAAAAAAAC8/p-A5UNK7ikY/s1600/thompson-ritchie.jpg)
* 1971 - Primeira Edição
* 1973 - Quarta Edição. Reescrito em C
* 1975 - Sexta Edição. Início da versão BSD
* 1982 - System III. AT&T UNIX System Group release. Primeira versão pública fora dos [Laboratórios Bell](https://www.youtube.com/watch?v=XvDZLjaCJuw "UNIX: Making Computers Easier To Use")
* 1983 - System V. Início do Projeto GNU
* 1984 - 4.2BSD e SVR2
* 1986 - 4.3BSD
* 1987 - SVR3. 750.000 instalações em uso
* 1988 - POSIX. Criação da Open Software Foundation (OSF) e da UNIX International (UI)
* 1989 - SVR4. Criação da AT&T Unix Software Operation, futuramente USL
* 1991 - Criação da USL (UNIX System Laboratories). Linus Torvalds começa a desenvolver o Linux
* 1992 - SVR4.2. Lançado pela USL. Novell decide adquirir a USL
* 1993 - 4.4BSD. Versão final de Berkeley. Novell adquire a USL, transfere a marca “UNIX” e Single UNIX Specification para a X/Open
* 1994 - 4.4-Lite. É eliminado todo código que infringe padrões USL/Novell
* 1995 - UNIX 95 branding
* 1996 - Formação do Open Group pela fusão da OSF e da X/Open
* 1997 - Single UNIX specification, version 2
* 1998 - UNIX 98 branding
* 1999 - 30 anos de UNIX
* 2001 - Single UNIX Spec, version 3. Unificação total

## A iniciativa GNU

* O projeto GNU teve início em 1983 com a divulgação de um manifesto escrito por Richard Stallman
    * anunciava a intenção da criação de todo um sistema operacional (compatível com UNIX) utilizando única e exclusivamente programas livres (Free Software)
    * Stallman convocava programadores e empresas a investirem na sua idéia, contribuindo com dinheiro, máquinas e tempo

## Projeto GNU

* Em janeiro de 1984, Stallman deixa o laboratório de Inteligência Artificial do MIT e dá início a implementação dos programas GNU
* Em 1985, como mais pessoas já estavam envolvidas no projeto, era hora de buscar mais investimentos a fim de poder manter um grupo permanente de desenvolvimento 
    * Foi criada a Free Software Foundation (FSF)

## Projeto GNU e Free Software

* O objetivo do GNU é dar liberdade ao usuário, não apenas ser popular
    * Os programas GNU utilizam a licença GPL. Ela assegura que programas GNU sejam Copylefted
* Algumas bibliotecas GNU utilizam um tipo diferente de licença Copylefted, chamada de Library General Public License ou LGPL
    * Permite que programas proprietários sejam “linkados” com as funções GNU

## Linux
* O Kernel Linux foi criado originalmente por Linus Torvalds na Universidade de Helsinki na Finlândia, em meados de 1991
    * Kernel é o núcleo do sistema operacional
    
![Torvalds](https://upload.wikimedia.org/wikipedia/commons/thumb/6/69/Linus_Torvalds.jpeg/175px-Linus_Torvalds.jpeg)
* Torvalds começou o seu desenvolvimento utilizando como plataforma o sistema MINIX-386, que também é um clone do UNIX de propósito didático
* As primeiras versões já contavam com applicativos GNU, como: 
bash, gcc, gnu-make, gnu-sed, compress etc.
* Desde o início Torvalds comunicava o seu progresso no Newsgroup comp.os.minix, conquistando rapidamente simpatizantes e colaboradores
* Logo foi criada uma lista de discussão específica para o Linux 
(linux-activists@ niksula.hut.fi)
* Após apenas um ano, o Torvalds já podia continuar o seu desenvolvimento sem o auxílio do MINIX, vários aplicativos estavam disponíveis inclusive o X Window
* Criado para rodar na plataforma PC x86 32-bits, já está disponível na maioria das plataformas: Alpha, SPARC, PowerPC e Intel IA-64
* Seu contínuo desenvolvimento visa total compatibilidade com as especificações POSIX e Single UNIX Specification
* Linus Torvalds coordena o desenvolvimento, divulgando os recentes aprimoramentos através do site http://www.kernel.org/

## GNU/Linux

* Em meados de 1990 o sistema GNU estava praticamente completo faltando um último componente, o Kernel.
* Foi decidido implementar um Kernel baseado no Mach (Universidade Cornegie Mellow e e Universidade de Utah)
* O novo GNU Kernel recebeu o nome de HURD, entretanto, devido a dificuldades técnicas o HURD só veio ficar disponível para uso em 2003
* Em 1992 um outro Kernel Free Software, muito mais simples, já estava dando bons resultados. Foi só uma questão de tempo unir o Kernel Linux ao sistema GNU, daí o nome GNU/Linux
* Apesar de nos referirmos às  várias distribuições como Linux, na verdade “Linux” refere-se somente ao núcleo do sistema operacional. Sendo que a maior parte é composta por programas e aplicações GNU.

## Vantagens do GNU/Linux

* É tão seguro e estável quanto qualquer outro sistema UNIX
* Roda virtualmente em qualquer plataforma, principalmente sobre PCs 
(baixo custo)
* Costuma ser mais rápido que outros sistemas UNIX, quando usado em PCs
* Geralmente as distribuições são bastante completas, contendo tudo o 
que se pode precisar
* É Free Software, é grátis, é Copylefted
* O código fonte está disponível, sendo portanto possível configurá-lo em qualquer nível, inclusive modificá-lo de acordo com as necessidades
* É uma ótima fonte de conhecimento para estudantes, empresas e interessados em computação em geral

## Vantagens de ser UNIX

* Alternativa poderosa e econômica para qualquer aplicação que envolva computadores
    * Atualmente máquinas GNU/Linux são responsáveis por uma série de aplicações comerciais
* Segurança
* Estabilidade
* Multi-usuário, multi-processo
* Escalabilidade
* Servidores podem suportar diversos tipos de clientes
* Completo com todos os recursos de rede
* Baseado em padrões abertos
* Maturidade: 40 anos de existência
* Problemas e furos de segurança são detectados e corrigidos mais rapidamente que qualquer outro Sistema

## Distribuições LINUX

* Kernel do LINUX é único
* Conjunto de ferramentas agregadas ao Kernel pode variar
    * Normalmente estas ferramentas são baseadas na plataforma GNU
    * Cada “empacotamento” diferente forma uma “Distribuição LINUX”
    * Há diversas distribuições diferentes, cada uma se adequando a um perfil diferente de usuário

## Algumas distribuições LINUX

### Linux Debian
![DEBIAN](https://www.shareicon.net/data/256x256/2015/09/16/101872_debian_512x512.png)
* Distribuição Linux mais “pura”
    * Desenvolvida exclusivamente por voluntários, sem vínculos com nenhuma empresa, mantendo o espírito do software livre 
* Distribuição Linux mais estável
    * Todas as novas versões são exaustivamente testadas antes de serem consideradas estáveis 
    * ◦Preocupação principal é sempre a estabilidade 
    * Distribuição mais usada em servidores
* Usada como base para o desenvolvimento de um sem número de distribuições, entre elas o Ubuntu e o Kurumin

### Linux Ubuntu
![UBUNTU](https://cdn.icon-icons.com/icons2/17/PNG/256/ubuntu_linux_2075.png)
* Baseado no Debian, incorpora melhorias e correções, de forma a proporcionar um sistema bastante estável e fácil de usar 
* Em pouco mais de um ano, o Ubuntu se tornou uma das distribuições Linux mais populares
* Utiliza o Gnome como interface padrão, mas é possível instalar os pacotes do KDE através do "kubuntu-desktop"

### Linux KNOPPIX
![KNOPPIX](https://www.softexia.com/wp-content/uploads/2015/11/KNOPPIX_logo.png)
* Knoppix é uma distribuição GNU/Linux baseado no Debian e gravado em CD bootável (Live CD).
* Realiza detecção automática de hardware, suporta vários dispositivos gráficos, de som, SCSI, USB e outros periféricos.
* Ao dar o boot do CD do Knoppix não é preciso instalar nada em seu disco rígido. Devido à sua descompressão, que acontece a partir do CD, estão disponíveis mais de 2 GB de aplicativos, desde aplicações de escritório a ferramentas de sistema. 
* O Knopppix foi um dos primeiros live cds de GNU/Linux.

### Linux Kurumin
![KURUMIN](http://ninjadolinux.com.br/wp-content/uploads/2016/03/tuxkurumin-209x230.png)
* O Kurumin Linux é uma distribuição Linux baseada no Knoppix, e que mantém o mesmo sistema de detecção de hardware desta distribuição. 
* Criado por Carlos E. Morimoto, o Kurumin foi projetado para que fosse bem mais compacto, cabendo em um mini-CD de 80 mm
    * Kurumin vem da língua Tupi, onde Curumim significa homem jovem, em 
uma alusão a uma distribuição Linux mais leve e simples. A letra K no 
início da palavra é uma referência ao Knoppix.
* Distribuição Linux bem popular no Brasil

### Linux Slackware
![SLACKWARE](https://vulners.com/static/img/slackware.png)
* O Slackware é uma distribuição Linux das mais famosas
* Criada por Patrick Volkerding, teve sua primeira versão lançada em Abril de 1992
* Segue filosofia rígida: manter a distribuição o mais parecida possível com o UNIX
* É uma distribuição interessante para PCs com poucos recursos e também para quem procura uma distribuição simples e personalizável
    * possui poucos componentes e tem arquivos de configuração claros
* Recomendada para usuários mais experientes

### Linux SuSE
![SUSE](https://res.cloudinary.com/crunchbase-production/image/upload/c_lpad,h_256,w_256,f_auto,q_auto:eco,dpr_1/ngvrlevjiovyp4ycffw5)
* A SuSE é uma empresa alemã que é uma das maiores influências do Linux no mundo 
* A SuSE baseia-se originalmente no Slackware 
* Oferece uma ferramenta de configuração do sistema chamada YaST, que facilita e muito mexer nas configurações da distribuição
* Atualmente o SuSE é utilizado por muitas máquinas na Europa, incluindo instituições educacionais e governamentais
* Sem dúvida é uma distribuição notável, porém não muito usada no Brasil

### Linux RedHat
![REDHAT](https://b.thumbs.redditmedia.com/7f-_ntVEoHVAbsCrhY0Q-dlba3bpXir9uFxLe_RLHOE.png)
* Criada pela empresa americana Red Hat, foi uma das pioneiras no 
tratamento sério do Linux. 
* Criadora do RPM, o gerenciador de pacotes mais usado atualmente no 
Linux, a Red Hat atualmente tem  uma distribuição mais voltada para o 
mercado empresarial. 
* Uma das principais distribuições mundiais. É líder nos Estados Unidos, 
mas possui influência a nível mundial.
* Sua equipe não ajuda na distribuição em si somente, mas também no próprio Linux. 
* Várias distribuições começaram se baseando nesta distribuição, o que a faz uma boa base para todos.

### Linux Fedora Core
![FEDORA](https://www.softexia.com/wp-content/uploads/2015/11/Fedora-logo-256x256.png)
* O Fedora é o sucessor do antigo Red Hat Desktop, descontinuado em 2003
* Combina os esforços da RedHat, com um bom número de voluntários e usuários fiéis. 
* Graças a inovações como o SeLinux, é uma distribuição muito usada em servidores 
* Também possui um público fiel para Desktop, em função da sua facilidade de uso

### Linux Mandrake
![MANDRAKE](https://cdn.iconscout.com/icon/free/png-256/mandrake-202403.png)
* Esta empresa francesa resolveu apostar no Linux como um sistema fácil para todos 
* Baseada na americana Red Hat, o Mandrake vem com vários programas de configuração fáceis de serem utilizados e bem úteis
* Durante o crescimento mundial do Linux, o Mandrake adquiriu muitos fãs e uma popularidade incrível, principalmente na América do Norte, através de sua interface fácil e dinamismo

### Conectiva Linux
![CONECTIVA](https://archive.org/download/tucows_155612_Conectiva_Linux/conectiva.jpg)
* Criada pela empresa brasileira Conectiva, foi denominada inicialmente de Parolin, e não continha muita coisa além de traduções da distribuição Red Hat. 
* O seu desenvolvimento cresceu e resolveram partir para um rumo próprio,  fazendo suas próprias alterações e ideologias na distribuição em uma rota diversa da empresa americana Red Hat. Então surgiu o Conectiva Linux.
* A partir de 1999, com o aumento do uso do Linux no Brasil, o 
Conectiva Linux, que já estava na sua versão 3.0, ficou muito popular 
entre os usuários brasileiros, provando ser tão boa quanto as estrangeiras.

### Linux Mandriva
![MANDRIVA](https://lh3.googleusercontent.com/-ZfchwhBCQUA/YG8UvQFJBZI/AAAAAAAAfAA/Txppx1ajf64WAf96sJLtIvcDcysRJ4qugCLcBGAsYHQ/s16000/mandriva.png)
* O Mandriva Linux é resultado da fusão ocorrida em 24 de fevereiro de 2005 entre a MandrakeSoft, uma das principais distribuições Linux da 
Europa e a Conectiva
* A Mandriva possui escritórios nos Estados Unidos, França e Brasil, tem 
mais de 8 milhões de usuários e uma carteira de 170 grandes clientes corporativos, além de contar com 130 funcionários.
