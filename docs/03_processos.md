
# Aula 03 – Processos no Linux

## Conceito

Processos são programas em execução no sistema. Cada processo possui um
identificador (PID), usuário, consumo de recursos e estado.

## Visualizando processos

```bash
ps
ps aux
top
htop
````

## Foreground e Background

```bash
sleep 300 &
jobs
fg
bg
```

## Encerrando processos

```bash
kill PID
kill -9 PID
pkill nome
```

## Sinais comuns

* SIGTERM (15): encerramento padrão
* SIGKILL (9): encerramento forçado
* SIGSTOP: pausa
* SIGCONT: continua

