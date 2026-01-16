```bash
mkdir permissao_lab # (make diretory) cria novo diretorio/pasta
cd permissao_lab # (change diretory) acessa diretorio/pasta

touch arquivo.txt # cria arquivo
ls -l # lista o conteudo do diretorio com suas permissoes (-rw-r--r-- 1 aldomarassolin users 0 Jan 16 21:20 arquivo.txt)

chmod 600 arquivo.txt # (change mode) modifica permissoes do arquivo para leitura e escrita apenas
ls -l # -rw------ 1 aldomarassolin users 0 Jan 16 21:20 arquivo.txt

chmod 644 arquivo.txt # modifica permissoes
ls -l # (-rw-r--r-- 1 aldomarassolin users 0 Jan 16 21:20 arquivo.txt)

mkdir scripts # cria pasta /scripts
touch scripts/run.sh # cria arquivo run.sh dentro de scripts
chmod +x scripts/run.sh # torna run.sh executavel
ls -l scripts
```