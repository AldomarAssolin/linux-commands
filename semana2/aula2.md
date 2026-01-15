

# 🧱 SEMANA 2 – AULA 2

## Alterando permissões com `chmod` (sem quebrar o sistema)

---

## 🎯 Objetivo da aula

* Entender **como mudar permissões**
* Usar `chmod` de forma **consciente**
* Saber **quando NÃO usar 777**
* Dominar os dois modos: **numérico** e **simbólico**

---

## 🔐 `chmod` – quem pode fazer o quê

`chmod` significa **change mode**.

Sintaxe geral:

```bash
chmod PERMISSÃO arquivo_ou_pasta
```

---

## 🧠 Modo 1 – Numérico (o mais usado)

Você já viu a tabela, agora vamos **usar de verdade**.

### 🔢 Relembrando os valores

| Valor | Permissão    |
| ----- | ------------ |
| 4     | leitura (r)  |
| 2     | escrita (w)  |
| 1     | execução (x) |

Somando:

* `7` → rwx
* `6` → rw-
* `5` → r-x
* `4` → r--

Formato:

```
chmod XYZ arquivo
```

* X → dono
* Y → grupo
* Z → outros

---

## 📌 Exemplos reais

### 📄 Arquivo de texto comum

```bash
chmod 644 comandos.txt
```

Significa:

* dono: ler e escrever
* grupo: ler
* outros: ler

👉 **padrão profissional para arquivos**

---

### 📜 Script executável

```bash
chmod 755 script.sh
```

* dono: rwx
* grupo/outros: r-x

👉 pode executar, mas não editar

---

### 🔥 O famoso (e perigoso)

```bash
chmod 777 arquivo
```

Todos podem tudo.

⚠️ Isso **não é prática profissional**, é gambiarra temporária.
Em servidor, isso vira **falha de segurança**.

---

## 🧠 Modo 2 – Simbólico (mais legível)

Formato:

```bash
chmod [quem][operação][permissão] arquivo
```

### Quem:

* `u` → usuário (dono)
* `g` → grupo
* `o` → outros
* `a` → todos

### Operação:

* `+` adiciona
* `-` remove
* `=` define exatamente

---

## ✏️ Exemplos simbólicos

### Tornar script executável para o dono

```bash
chmod u+x script.sh
```

### Remover escrita de outros

```bash
chmod o-w arquivo.txt
```

### Definir exatamente

```bash
chmod u=rw,g=r,o=r arquivo.txt
```

Mesma coisa que `644`, só que legível.

---

## 🧪 Prática guiada (faça agora)

Entre na sua pasta:

```bash
cd ~/Estudos/semana1/anotacoes
ls -l
```

### 1️⃣ Remova escrita de grupo e outros:

```bash
chmod 644 anotations.md
```

Confirme:

```bash
ls -l
```

---

### 2️⃣ Crie um script de teste

```bash
touch teste.sh
nano teste.sh
```

Dentro:

```bash
#!/bin/bash
echo "Teste de permissões"
```

Salvar e sair.

---

### 3️⃣ Tente executar

```bash
./teste.sh
```

Vai falhar. Correto.

---

### 4️⃣ Torne executável

```bash
chmod +x teste.sh
./teste.sh
```

Agora funciona.

---

## ⚠️ Erros clássicos (evite)

❌ Usar `chmod 777` sem saber por quê
❌ Dar permissão de execução para arquivo `.txt`
❌ Alterar permissões sem olhar `ls -l` antes

✔️ Sempre verifique **antes e depois**

---

## 🧠 Fixação (importante)

Responda mentalmente, sem tabela:

👉 Qual a diferença prática entre `644` e `755`?
👉 Por que scripts precisam de permissão `x`?

Se isso estiver claro, você já está **operando Linux**, não só aprendendo.

---

## ▶️ Próxima aula – **Semana 2 – Aula 3**

Vamos entrar em:

* `chown`
* dono vs grupo
* por que `sudo` muda tudo

Aqui começa a administração de verdade.

Quando quiser seguir, diga apenas:
**“Semana 2 – Aula 3”**
