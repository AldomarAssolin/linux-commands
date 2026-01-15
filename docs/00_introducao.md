

# 📘 Aula 00 – Introdução ao Linux

## Table of Contents

<details>

   <summary>Contents</summary>

1. [1️⃣ Explicação da aula](#1-explicao-da-aula)
   1. [O que é Linux](#o-que--linux)
   1. [Terminal ≠ coisa de velho](#terminal--coisa-de-velho)
   1. [Conceitos fundamentais](#conceitos-fundamentais)
1. [2️⃣ Exemplos práticos (execute no terminal)](#2-exemplos-prticos-execute-no-terminal)
   1. [📌 Saber quem você é](#-saber-quem-voc-)
   1. [📌 Onde você está](#-onde-voc-est)
   1. [📌 Informações do sistema](#-informaes-do-sistema)
   1. [📌 Informações da distribuição](#-informaes-da-distribuio)
   1. [📌 Data e hora](#-data-e-hora)
1. [3️⃣ Lista de comandos apresentados nesta aula](#3-lista-de-comandos-apresentados-nesta-aula)
1. [4️⃣ Arquivo Markdown para salvar no repositório](#4-arquivo-markdown-para-salvar-no-repositrio)
1. [O que é Linux](#o-que--linux)
1. [Por que aprender Linux](#por-que-aprender-linux)
1. [Conceitos fundamentais](#conceitos-fundamentais)
1. [Comandos iniciais](#comandos-iniciais)
   1. [Usuário atual](#usurio-atual)
   1. [Diretório atual](#diretrio-atual)
   1. [Informações do sistema](#informaes-do-sistema)
   1. [Informações da distribuição](#informaes-da-distribuio)
   1. [Data e hora](#data-e-hora)
1. [Lista de comandos](#lista-de-comandos)
1. [Observações](#observaes)
1. [5️⃣ Missão antes da próxima aula](#5-misso-antes-da-prxima-aula)

</details>

## 1️⃣ Explicação da aula

### O que é Linux

Linux **não é**:

* uma tela bonita
* um sistema “alternativo”
* algo só para hacker de filme ruim

Linux é:

* um **kernel** (o coração do sistema)
* usado em **servidores, nuvem, Docker, Kubernetes**
* a base de Android, servidores web, VPS, DevOps, CI/CD

Quando você aprende Linux, você aprende a:

* conversar direto com o sistema
* entender o que está rodando
* resolver problema sem clicar desesperado

GUI é conforto.
Terminal é **controle**.

---

### Terminal ≠ coisa de velho

O terminal existe porque:

* é rápido
* é scriptável
* é previsível
* funciona igual em qualquer servidor do planeta

Se você sabe Linux:

* você não depende de interface
* você não fica refém de botão
* você trabalha remoto, local, VPS, container, tanto faz

Linux é coerência. Humanos raramente são.

---

### Conceitos fundamentais

* **Tudo é arquivo**

  * dispositivos
  * processos
  * configurações
* O sistema é organizado em diretórios
* Comandos seguem uma lógica simples:

  ```
  comando + opção + alvo
  ```

Exemplo:

```bash
ls -l /home
```

---

## 2️⃣ Exemplos práticos (execute no terminal)

### 📌 Saber quem você é

```bash
whoami
```

### 📌 Onde você está

```bash
pwd
```

### 📌 Informações do sistema

```bash
uname -a
```

### 📌 Informações da distribuição

```bash
lsb_release -a
```

### 📌 Data e hora

```bash
date
```

---

## 3️⃣ Lista de comandos apresentados nesta aula

| Comando          | Função                   |
| ---------------- | ------------------------ |
| `whoami`         | Mostra o usuário atual   |
| `pwd`            | Mostra o diretório atual |
| `uname -a`       | Informações do kernel    |
| `lsb_release -a` | Informações da distro    |
| `date`           | Data e hora do sistema   |
| `clear`          | Limpa o terminal         |
| `exit`           | Sai do terminal          |

Esses comandos não impressionam ninguém.
Mas sem eles, você se perde em 5 minutos.

---

## 4️⃣ Arquivo Markdown para salvar no repositório

Agora a parte importante: **material organizado**.

Crie o arquivo:

```bash
docs/00_introducao.md
```

E cole exatamente isto abaixo 👇

---

# Aula 00 – Introdução ao Linux

## O que é Linux

Linux é um kernel de sistema operacional amplamente utilizado em servidores,
ambientes de nuvem, containers e sistemas embarcados. Diferente de sistemas
baseados apenas em interface gráfica, o Linux prioriza o uso do terminal,
permitindo controle total do sistema.

## Por que aprender Linux

- Base da maioria dos servidores web
- Essencial para DevOps, Docker e Cloud
- Maior controle e previsibilidade
- Automação e scripts

## Conceitos fundamentais

- Tudo no Linux é tratado como arquivo
- O sistema é organizado em diretórios
- Os comandos seguem o padrão: comando + opção + alvo

## Comandos iniciais

### Usuário atual
```bash
whoami
````

### Diretório atual

```bash
pwd
```

### Informações do sistema

```bash
uname -a
```

### Informações da distribuição

```bash
lsb_release -a
```

### Data e hora

```bash
date
```

## Lista de comandos

| Comando        | Descrição             |
| -------------- | --------------------- |
| whoami         | Usuário atual         |
| pwd            | Diretório atual       |
| uname -a       | Informações do kernel |
| lsb_release -a | Informações da distro |
| date           | Data e hora           |
| clear          | Limpa o terminal      |
| exit           | Encerra a sessão      |

## Observações

O terminal é a principal ferramenta de trabalho no Linux.
Dominar comandos básicos é essencial para avançar com segurança.


---

## 5️⃣ Missão antes da próxima aula

1. Execute todos os comandos
2. Crie o arquivo `00_introducao.md`
3. Faça pelo menos **uma anotação sua** no final do arquivo
4. Commit no Git

Quando você fizer isso, seguimos para:

👉 **Aula 01 – Navegação no sistema de arquivos**

Linux não exige genialidade.  
Ele exige método, atenção e respeito.  
Você está no caminho certo.

