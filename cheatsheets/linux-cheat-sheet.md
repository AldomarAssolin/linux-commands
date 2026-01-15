
# 🧾 Linux Cheat Sheet

## Table of Contents

<details>

   <summary>Contents</summary>

1. [📌 Como usar esta cola](#-como-usar-esta-cola)
1. [📂 Navegação no sistema de arquivos](#-navegao-no-sistema-de-arquivos)
1. [📄 Manipulação de arquivos e pastas](#-manipulao-de-arquivos-e-pastas)
1. [🔐 Permissões](#-permisses)
1. [👤 Usuários e grupos](#-usurios-e-grupos)
1. [⚙️ Processos](#-processos)
1. [🔀 Redirecionamento e Pipes](#-redirecionamento-e-pipes)
1. [🔍 Busca e filtros](#-busca-e-filtros)
1. [🌐 Rede básica](#-rede-bsica)
1. [🧬 Git no terminal (básico)](#-git-no-terminal-bsico)
1. [🆘 Ajuda e documentação](#-ajuda-e-documentao)
1. [📌 Dicas finais](#-dicas-finais)

</details>

</details>



## 📌 Como usar esta cola

* Não é para estudar do zero
* É para **consultar quando a mente dá branco**
* Leia, use, repita
* Com o tempo você vai usar menos. É o objetivo.

---

## 📂 Navegação no sistema de arquivos

```bash
pwd                 # Mostra o diretório atual
ls                  # Lista arquivos
ls -l               # Lista detalhada
ls -la              # Lista tudo (inclusive ocultos)
cd pasta            # Entra na pasta
cd ..               # Volta um nível
cd ~                # Vai para o home
cd /                # Vai para a raiz
tree                # Mostra estrutura de diretórios
```

---

## 📄 Manipulação de arquivos e pastas

```bash
touch arquivo.txt           # Cria arquivo vazio
mkdir pasta                 # Cria pasta
mkdir -p a/b/c              # Cria estrutura de pastas
cp origem destino            # Copia arquivo
cp -r pasta1 pasta2          # Copia pasta
mv arquivo pasta/            # Move arquivo
mv antigo.txt novo.txt       # Renomeia arquivo
rm arquivo.txt               # Remove arquivo
rm -r pasta                  # Remove pasta
rm -rf pasta                 # Remove SEM piedade
```

Use `rm -rf` só quando tiver certeza absoluta.
Linux não pergunta se você tem certeza. Ele assume que você sabe o que está fazendo.

---

## 🔐 Permissões

```bash
ls -l                       # Ver permissões
chmod 644 arquivo.txt       # Define permissões
chmod 755 script.sh         # Torna executável
chmod +x script.sh          # Executável rápido
chown user arquivo.txt      # Muda dono
chown user:grupo arquivo    # Muda dono e grupo
```

Permissões:

* `r` = read
* `w` = write
* `x` = execute

---

## 👤 Usuários e grupos

```bash
whoami              # Usuário atual
id                  # ID e grupos
groups               # Grupos do usuário
su usuario           # Troca de usuário
sudo comando         # Executa como root
```

Se você não entende `sudo`, você ainda não entendeu Linux.

---

## ⚙️ Processos

```bash
ps aux               # Lista processos
top                  # Monitor em tempo real
htop                 # Monitor melhorado
kill PID             # Mata processo
kill -9 PID          # Mata SEM negociação
jobs                 # Processos em background
bg                   # Continua em background
fg                   # Volta para foreground
```

---

## 🔀 Redirecionamento e Pipes

```bash
comando > arquivo.txt        # Redireciona saída
comando >> arquivo.txt       # Anexa saída
comando < arquivo.txt        # Entrada
comando1 | comando2          # Pipe
tee arquivo.txt              # Mostra e grava
```

Exemplo:

```bash
ls -l | grep ".md" | tee arquivos_md.txt
```

---

## 🔍 Busca e filtros

```bash
grep "texto" arquivo         # Busca texto
grep -r "texto" pasta        # Busca recursiva
find . -name "arquivo.txt"   # Busca arquivo
wc -l arquivo.txt            # Conta linhas
sort arquivo.txt             # Ordena
uniq arquivo.txt             # Remove duplicados
cut -d: -f1 arquivo          # Recorta colunas
```

---

## 🌐 Rede básica

```bash
ip a                  # Interfaces de rede
ping google.com       # Teste de conectividade
ss -tulpn             # Portas e serviços
curl site.com         # Requisição HTTP
wget url              # Download
```

---

## 🧬 Git no terminal (básico)

```bash
git status
git add .
git commit -m "mensagem"
git log --oneline
git diff
git pull
git push
```

Sem `git status` antes, você está jogando roleta russa.

---

## 🆘 Ajuda e documentação

```bash
man comando           # Manual do comando
comando --help        # Ajuda rápida
history               # Histórico de comandos
```

`man` é seu melhor amigo. Ele só parece rude no começo.

---

## 📌 Dicas finais

* Linux é previsível
* Se algo deu errado, **leia a mensagem**
* Erros ensinam mais que sucesso silencioso
* Automatize sempre que repetir algo

