
# Git Cheat Sheet (Terminal)

## Table of Contents

<details>

   <summary>Contents</summary>

1. [1) Começar um repositório](#1-comear-um-repositrio)
   1. [Iniciar repo local](#iniciar-repo-local)
   1. [Clonar repo remoto](#clonar-repo-remoto)
1. [2) Checar o estado e entender o que mudou](#2-checar-o-estado-e-entender-o-que-mudou)
1. [3) Adicionar mudanças (stage)](#3-adicionar-mudanas-stage)
   1. [Adicionar arquivo específico](#adicionar-arquivo-especfico)
   1. [Adicionar tudo](#adicionar-tudo)
   1. [Remover do stage (sem apagar o arquivo)](#remover-do-stage-sem-apagar-o-arquivo)
1. [4) Commit (salvar versão)](#4-commit-salvar-verso)
   1. [Commit simples](#commit-simples)
   1. [Commit com descrição mais longa (abre editor)](#commit-com-descrio-mais-longa-abre-editor)
   1. [Commit incluindo arquivos já rastreados (sem git add)](#commit-incluindo-arquivos-j-rastreados-sem-git-add)
1. [5) Branches (linhas de trabalho)](#5-branches-linhas-de-trabalho)
   1. [Ver branches](#ver-branches)
   1. [Criar branch](#criar-branch)
   1. [Trocar para branch](#trocar-para-branch)
   1. [Criar e trocar de uma vez](#criar-e-trocar-de-uma-vez)
   1. [Deletar branch local](#deletar-branch-local)
   1. [Forçar delete (se não foi mergeada)](#forar-delete-se-no-foi-mergeada)
1. [6) Merge (juntar branches)](#6-merge-juntar-branches)
   1. [Merge da branch X na branch atual](#merge-da-branch-x-na-branch-atual)
1. [7) Remote (conectar com GitHub)](#7-remote-conectar-com-github)
   1. [Ver remotes](#ver-remotes)
   1. [Adicionar remote](#adicionar-remote)
   1. [Trocar URL do remote](#trocar-url-do-remote)
1. [8) Pull e Push (sincronizar)](#8-pull-e-push-sincronizar)
   1. [Baixar alterações do remoto e aplicar](#baixar-alteraes-do-remoto-e-aplicar)
   1. [Enviar commits para remoto](#enviar-commits-para-remoto)
   1. [Primeiro push (setando upstream)](#primeiro-push-setando-upstream)
1. [9) Stash (guardar mudanças sem commitar)](#9-stash-guardar-mudanas-sem-commitar)
   1. [Guardar mudanças temporariamente](#guardar-mudanas-temporariamente)
   1. [Listar stashes](#listar-stashes)
   1. [Voltar o stash mais recente](#voltar-o-stash-mais-recente)
   1. [Aplicar stash sem remover da lista](#aplicar-stash-sem-remover-da-lista)
1. [10) Desfazer coisas (com menos drama)](#10-desfazer-coisas-com-menos-drama)
   1. [Desfazer mudanças em um arquivo (voltar ao último commit)](#desfazer-mudanas-em-um-arquivo-voltar-ao-ltimo-commit)
   1. [Voltar tudo ao último commit (cuidado)](#voltar-tudo-ao-ltimo-commit-cuidado)
   1. [Voltar para um commit anterior mantendo histórico (safe)](#voltar-para-um-commit-anterior-mantendo-histrico-safe)
   1. [Resetar para um commit (perigoso)](#resetar-para-um-commit-perigoso)
1. [11) Tags (marcar versões)](#11-tags-marcar-verses)
1. [12) Fluxo diário recomendado (o básico que evita desastre)](#12-fluxo-dirio-recomendado-o-bsico-que-evita-desastre)
1. [13) Mensagens de commit (padrão sugerido)](#13-mensagens-de-commit-padro-sugerido)
1. [✅ Criar o arquivo no terminal](#-criar-o-arquivo-no-terminal)

</details>

> Cola rápida para uso diário no terminal.


## 1) Começar um repositório

### Iniciar repo local
```bash
git init
````

### Clonar repo remoto

```bash
git clone <url>
```

---

## 2) Checar o estado e entender o que mudou

```bash
git status              # Mostra o estado atual
git diff                # Diferenças do que NÃO foi staged
git diff --staged       # Diferenças do que JÁ foi staged
git log --oneline       # Histórico resumido
git log --graph --oneline --decorate --all  # Histórico visual completo
```

---

## 3) Adicionar mudanças (stage)

### Adicionar arquivo específico

```bash
git add arquivo.md
```

### Adicionar tudo

```bash
git add .
```

### Remover do stage (sem apagar o arquivo)

```bash
git restore --staged arquivo.md
```

---

## 4) Commit (salvar versão)

### Commit simples

```bash
git commit -m "mensagem"
```

### Commit com descrição mais longa (abre editor)

```bash
git commit
```

### Commit incluindo arquivos já rastreados (sem git add)

```bash
git commit -am "mensagem"
```

---

## 5) Branches (linhas de trabalho)

### Ver branches

```bash
git branch
git branch -a           # Inclui remotas
```

### Criar branch

```bash
git branch minha-branch
```

### Trocar para branch

```bash
git switch minha-branch
```

### Criar e trocar de uma vez

```bash
git switch -c feature/login
```

### Deletar branch local

```bash
git branch -d minha-branch
```

### Forçar delete (se não foi mergeada)

```bash
git branch -D minha-branch
```

---

## 6) Merge (juntar branches)

### Merge da branch X na branch atual

```bash
git merge minha-branch
```

Dica: sempre rode `git status` e `git pull` antes de fazer merge.

---

## 7) Remote (conectar com GitHub)

### Ver remotes

```bash
git remote -v
```

### Adicionar remote

```bash
git remote add origin <url>
```

### Trocar URL do remote

```bash
git remote set-url origin <url>
```

---

## 8) Pull e Push (sincronizar)

### Baixar alterações do remoto e aplicar

```bash
git pull
```

### Enviar commits para remoto

```bash
git push
```

### Primeiro push (setando upstream)

```bash
git push -u origin main
```

---

## 9) Stash (guardar mudanças sem commitar)

### Guardar mudanças temporariamente

```bash
git stash
```

### Listar stashes

```bash
git stash list
```

### Voltar o stash mais recente

```bash
git stash pop
```

### Aplicar stash sem remover da lista

```bash
git stash apply
```

---

## 10) Desfazer coisas (com menos drama)

### Desfazer mudanças em um arquivo (voltar ao último commit)

```bash
git restore arquivo.md
```

### Voltar tudo ao último commit (cuidado)

```bash
git restore .
```

### Voltar para um commit anterior mantendo histórico (safe)

```bash
git revert <hash>
```

### Resetar para um commit (perigoso)

```bash
git reset --soft <hash>   # Mantém mudanças staged
git reset --mixed <hash>  # Mantém mudanças unstaged (padrão)
git reset --hard <hash>   # APAGA mudanças
```

---

## 11) Tags (marcar versões)

```bash
git tag                  # Lista tags
git tag v1.0.0           # Cria tag
git push origin v1.0.0   # Envia tag
git push --tags          # Envia todas as tags
```

---

## 12) Fluxo diário recomendado (o básico que evita desastre)

```bash
git status
git pull
# trabalha...
git add .
git commit -m "feat: descreve alteracao"
git push
```

---

## 13) Mensagens de commit (padrão sugerido)

* feat: nova funcionalidade
* fix: correção de bug
* docs: documentação
* refactor: refatoração sem mudar comportamento
* chore: tarefa interna (config, build, etc)

Exemplos:

* feat(docs): adiciona aula de permissões
* fix(scripts): corrige caminho do backup
* docs: melhora cheat sheet do git



---

## ✅ Criar o arquivo no terminal

Dentro do seu repo (`linux-commands/`):

```bash
nano cheatsheets/git-cheat-sheet.md
````

Cole o conteúdo, salve.

Depois:

```bash
git add cheatsheets/git-cheat-sheet.md
git commit -m "docs: adiciona git cheat sheet"
```

---

Pronto. Agora temos uma cola que evita 80% das cagadas comuns no Git.
Os outros 20% são criatividade humana mesmo.
