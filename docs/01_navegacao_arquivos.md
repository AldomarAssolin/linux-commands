# Aula 01 – Navegação no sistema de arquivos

## Estrutura do sistema Linux

O Linux organiza seus arquivos a partir do diretório raiz `/`.
Cada diretório possui uma função específica dentro do sistema.

## Caminhos

### Caminho absoluto
Começa com `/` e independe do diretório atual.

Exemplo:
```bash
cd /home/usuario/Documentos
````

### Caminho relativo

Depende do diretório atual.

Exemplo:

```bash
cd Documentos
```

## Atalhos importantes

* `.` diretório atual
* `..` diretório pai
* `~` home do usuário
* `/` raiz

## Comandos de navegação

```bash
pwd
ls
ls -l
ls -la
cd pasta
cd ..
cd ~
```

## Manipulação de arquivos e pastas

```bash
touch arquivo.txt
mkdir pasta
mkdir -p a/b/c
cp arquivo.txt copia.txt
cp -r pasta pasta_backup
mv antigo.txt novo.txt
rm arquivo.txt
rm -r pasta
```

## Lista de comandos

| Comando | Descrição           |
| ------- | ------------------- |
| pwd     | Diretório atual     |
| ls      | Lista arquivos      |
| cd      | Navegação           |
| tree    | Estrutura em árvore |
| touch   | Cria arquivo        |
| mkdir   | Cria diretório      |
| cp      | Copia               |
| mv      | Move/Renomeia       |
| rm      | Remove              |
