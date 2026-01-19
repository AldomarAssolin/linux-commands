
# 📘 Aula 04 – Redirecionamento e Pipes

## 1️⃣ Explicação da aula

### Entrada, saída e erro (a base de tudo)

Todo comando no Linux trabalha com **três fluxos**:

| Fluxo          | Nome   | Número |
| -------------- | ------ | ------ |
| Entrada padrão | stdin  | 0      |
| Saída padrão   | stdout | 1      |
| Erro padrão    | stderr | 2      |

Você não vê isso normalmente porque o terminal **esconde a complexidade**.
Redirecionamento é você dizendo ao sistema:
“não manda isso pra tela, manda pra outro lugar”.

---

### Redirecionamento (`>`, `>>`, `<`)

#### Saída para arquivo

```bash
ls > arquivos.txt
```

* Cria o arquivo
* Sobrescreve se existir

#### Anexar saída

```bash
ls >> arquivos.txt
```

* Não apaga o conteúdo anterior

#### Entrada a partir de arquivo

```bash
sort < nomes.txt
```

O comando acha que você digitou tudo à mão. Ingênuo.

---

### Pipes (`|`) – a alma do Unix

Pipe conecta a saída de um comando **diretamente** na entrada de outro.

```bash
comando1 | comando2
```

Exemplo simples:

```bash
ls | wc -l
```

Você acabou de contar arquivos sem escrever uma linha de código.

---

## 2️⃣ Exemplos práticos (execute no terminal)

### Redirecionar saída

```bash
ls -l > lista.txt
cat lista.txt
```

### Anexar conteúdo

```bash
echo "nova linha" >> lista.txt
```

### Pipe básico

```bash
ls -l | less
```

### Pipe com filtro

```bash
ls -l | grep ".sh"
```

### Contar linhas

```bash
ls | wc -l
```

---

## 3️⃣ Redirecionando erros (importante)

### Enviar erro para arquivo

```bash
ls arquivo_inexistente 2> erro.txt
```

### Enviar saída e erro juntos

```bash
ls arquivo_inexistente > tudo.txt 2>&1
```

Ou versão moderna:

```bash
ls arquivo_inexistente &> tudo.txt
```

📌 Isso aqui salva sanidade em script.

---

## 4️⃣ `tee` – ver e salvar ao mesmo tempo

```bash
ls -l | tee lista.txt
```

* Mostra na tela
* Grava no arquivo

Modo append:

```bash
ls -l | tee -a lista.txt
```

---

## 5️⃣ Combinações úteis (vida real)

```bash
ps aux | grep python
```

```bash
cat arquivo.txt | sort | uniq
```

```bash
dmesg | less
```

Você não “aprende” pipes.
Você **acostuma a pensar em fluxo**.

---

## 6️⃣ Lista de comandos e operadores desta aula

| Item   | Função                |      |
| ------ | --------------------- | ---- |
| `>`    | Redireciona saída     |      |
| `>>`   | Anexa saída           |      |
| `<`    | Entrada de arquivo    |      |
| `      | `                     | Pipe |
| `tee`  | Mostra e grava        |      |
| `grep` | Filtra texto          |      |
| `wc`   | Conta linhas/palavras |      |
| `less` | Paginação             |      |
| `2>`   | Redireciona erro      |      |
| `&>`   | Redireciona tudo      |      |

---

## 7️⃣ Mini-laboratório (faça pensando)

```bash
ls -l > arquivos.txt
ls -l | grep ".sh" >> arquivos.txt
cat arquivos.txt | wc -l
```

Depois:

```bash
ls inexistente 2> erros.log
cat erros.log
```

Se você entende por que **nada apareceu na tela**, parabéns.

---

## 8️⃣ Arquivo Markdown para salvar no repositório

Crie:

```bash
docs/04_redirecionamento_pipes.md
```

Cole exatamente isto 👇

---

````markdown
# Aula 04 – Redirecionamento e Pipes

## Conceito

Redirecionamento permite controlar para onde vai a saída, entrada e erros
dos comandos. Pipes conectam comandos, formando fluxos de processamento.

## Redirecionamento

```bash
comando > arquivo.txt
comando >> arquivo.txt
comando < arquivo.txt
````

## Pipes

```bash
comando1 | comando2
```

Exemplo:

```bash
ls | wc -l
```

## Redirecionamento de erros

```bash
comando 2> erro.txt
comando &> tudo.txt
```

## Tee

```bash
ls -l | tee arquivo.txt
```
