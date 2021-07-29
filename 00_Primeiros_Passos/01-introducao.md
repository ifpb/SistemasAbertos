# INTRODUÇÃO AO LINUX


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

![richard stallman](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/Richard_Matthew_Stallman.jpeg/1200px-Richard_Matthew_Stallman.jpeg)

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

