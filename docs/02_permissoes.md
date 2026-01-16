# Aula 02 – Permissões de arquivos

## Conceito

O Linux utiliza permissões para controlar quem pode ler, escrever ou executar
arquivos e diretórios. Cada arquivo possui permissões para dono, grupo e outros.

## Estrutura das permissões

Exemplo:
-rwxr-xr--

- Primeiro caractere indica o tipo
- Três blocos de permissões (user, group, others)

## Permissões básicas

- r (4): leitura
- w (2): escrita
- x (1): execução

## Exemplo numérico

chmod 755 script.sh

- Dono: rwx
- Grupo: r-x
- Outros: r-x

## Comandos principais

```bash
ls -l
chmod 644 arquivo.txt
chmod +x script.sh
chown usuario arquivo.txt
chown usuario:grupo arquivo.txt
umask
