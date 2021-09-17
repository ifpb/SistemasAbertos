# COMANDOS VARIADOS DO LINUX

Baseado no Material do Prof. Leônidas Lima Júnior, leonidas.lima@gmail.com, (2011)

Atualizado por Vinicius Centurion em 2021

## SUMÁRIO
* Comandos diversos
* Comandos de tempo
* Comandos de espaço de disco
* Comandos de manipulação com arquivos
* Comandos de encerramento do sistema
* Comandos de localização
* Comandos TMUX

## COMANDOS DIVERSOS

1. clear
    * Limpa a tela e posiciona o cursor no canto superior esquerdo do vídeo

1. uname
    * Retorna o nome e versão do kernel atual  echo
    * Mostra mensagens. Útil na construção de scripts para mostrar mensagens na tela para o usuário acompanhar sua execução

1. su
    * Permite ao usuário mudar sua identidade para outro usuário sem fazer o logout

1. free
    * Mostra detalhes sobre a utilização da memória RAM do sistema
    * Opções: -b / -k / -m

1. date
    * Permite ver/modificar a data e hora do Sistema. 
    * Apenas root pode modificar a data e hora do sistema: date MesDiaHoraMinuto[AnoSegundos]

    * +[FORMATO] - Define o formato da listagem que será usada pelo comando date. Os formatos mais usados são:
        * %d - Dia do Mês (00-31) %m - Mês do Ano (00-12)
        * %y - Ano (dois dígitos) %Y - Ano (quatro dígitos)
        * %H - Hora (00-24) %I - Hora (00-12)
        * %M - Minuto (00-59) %j - Dia do ano (1-366)
        * %p - AM/PM

## COMANDOS DE TEMPO

1. time
    * Mede o tempo gasto para executar
um processo (programa)
# time [comando]
Onde: comando é o comando/programa que se deseja medir
o tempo gasto para ser concluído
 Exemplo:
# time tar –czf backup.tar.gz /home
real 0m6.345s
user 0m2.848s
sys 0m3.428s
 uptime - Mostra o tempo de execução do
sistema desde que o computador foi
ligado
# uptime
 Exemplo:
# uptime
17:16:48 up 31 days, 10:00, 1 user, load average: 0.32, 0.54, 0.38


## COMANDOS DE ESPAÇO DE DISCO

## COMANDOS DE MANIPULAÇÃO DO SISTEMA

## COMANDOS DE ENCERRAMENTO DO SISTEMA

## COMANDOS DE LOCALIZAÇÃO

## COMANDOS TMUX