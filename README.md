# Comandos_Linux


# 🚀 **Linux Cheat Sheet – Guia De Comandos**

## 📌 **Comandos Básicos**

```bash
pwd                # Exibe o diretório atual (equivalente ao `pwd`)
ls                 # Lista arquivos no diretório
cd <diretório>     # Muda para um diretório
mkdir <pasta>      # Cria um novo diretório
rmdir <pasta>      # Remove um diretório vazio
rm <arquivo>       # Remove um arquivo
rm -r <pasta>      # Remove um diretório e seu conteúdo
cp <origem> <destino>  # Copia um arquivo ou diretório
mv <origem> <destino>  # Move ou renomeia um arquivo ou diretório

```

---

## 📂 **Gerenciamento de Arquivos (geral**

```bash
touch <arquivo>    # Cria um arquivo vazio
cat <arquivo>      # Exibe o conteúdo de um arquivo
head <arquivo>     # Exibe as primeiras linhas de um arquivo
tail <arquivo>     # Exibe as últimas linhas de um arquivo
find <diretório> -name <nome_arquivo>  # Busca arquivos por nome
grep "texto" <arquivo>  # Busca por um texto dentro de um arquivo

```

## 📂 **Manipulação de Arquivos no Linux**

### **Criando, Movendo e Removendo Arquivos**

```bash

touch <arquivo>          # Cria um arquivo vazio
echo "Olá, mundo!" > arquivo.txt  # Cria e escreve no arquivo
mv <arquivo_origem> <arquivo_destino>  # Move ou renomeia um arquivo
cp <arquivo_origem> <arquivo_destino>  # Copia um arquivo
rm <arquivo>             # Remove um arquivo

```

---

### **Visualizando Arquivos**

```bash

cat <arquivo>            # Exibe o conteúdo completo de um arquivo
less <arquivo>           # Exibe o conteúdo de um arquivo com navegação (scroll)
more <arquivo>           # Exibe o conteúdo de um arquivo com navegação por página
head <arquivo>           # Exibe as primeiras 10 linhas do arquivo
head -n 20 <arquivo>     # Exibe as primeiras 20 linhas do arquivo
tail <arquivo>           # Exibe as últimas 10 linhas do arquivo
tail -n 20 <arquivo>     # Exibe as últimas 20 linhas do arquivo
tail -f <arquivo>        # Exibe novas linhas de um arquivo em tempo real (útil para logs)

```

### **Buscando no Arquivo**

```bash
alavra" <arquivo> # Busca por uma palavra no arquivo e exibe as linhas que a contêm
grep -r "palavra" <diretório>  # Busca recursivamente por uma palavra dentro de um diretório
grep -i "palavra" <arquivo>    # Busca sem diferenciar maiúsculas de minúsculas
grep -v "palavra" <arquivo>    # Exibe todas as linhas do arquivo que **não** contêm a palavra

```

### **Manipulando Arquivos com `sed` e `awk`**

```bash
sed 's/velho/novo/g' <arquivo>   # Substitui 'velho' por 'novo' em um arquivo
awk '{print $1}' <arquivo>        # Exibe a primeira coluna de um arquivo (delimitado por espaços)

```

---

## 🔍 **Permissões de Arquivos e Diretórios**

```bash
chmod 755 <arquivo>  # Concede permissões de leitura, escrita e execução ao dono; leitura e execução ao grupo e outros
chmod +x <script.sh> # Torna um arquivo executável
chown <usuario>:<grupo> <arquivo>  # Muda o dono e grupo de um arquivo ou diretório
ls -l <arquivo>     # Exibe as permissões de um arquivo

```

### **Permissões de Diretórios**

```bash
chmod 700 <diretório>  # Permissões totais para o dono (leitura, escrita e execução) e sem permissões para outros

```

---

## 🔄 **Processos e Recursos do Sistema**

```bash
ps aux             # Exibe todos os processos em execução
top                # Exibe os processos em tempo real
htop               # Exibe processos interativamente (precisa ser instalado)
kill <PID>         # Finaliza um processo pelo ID (PID)
killall <processo> # Finaliza todos os processos com o nome
free -h            # Exibe o uso de memória RAM
df -h              # Exibe o uso do espaço em disco
du -sh <diretório> # Exibe o tamanho total de um diretório
```

### **Gerenciamento de Processos**

```bash
nohup <comando> &          # Executa um comando em segundo plano e ignora o encerramento do terminal
bg                        # Move um processo em segundo plano para execução
fg                        # Traz um processo para o primeiro plano
```

---

## 🌍 **Rede e Conectividade**

```bash
ping <host>            # Verifica a conectividade com um servidor
ifconfig              # Exibe informações de rede (em algumas distribuições, use 'ip a')
ip a                  # Exibe informações detalhadas sobre as interfaces de rede
curl <url>            # Faz uma requisição HTTP
wget <url>            # Baixa arquivos da internet
netstat -tulnp        # Exibe as portas abertas e processos em execução

```

### **Configuração de Rede**

```bash
sudo ifconfig eth0 up        # Ativa a interface de rede eth0
sudo ifconfig eth0 down      # Desativa a interface de rede eth0

```

---

## 🛠 **Gerenciamento de Pacotes**

### **Debian/Ubuntu (APT)**

```bash
sudo apt update       # Atualiza a lista de pacotes
sudo apt upgrade      # Atualiza todos os pacotes instalados
sudo apt install <pacote>  # Instala um novo pacote
sudo apt remove <pacote>   # Remove um pacote instalado

```

### **RedHat/CentOS (YUM/DNF)**

```bash
sudo yum update       # Atualiza os pacotes
sudo yum install <pacote>  # Instala um pacote
sudo yum remove <pacote>   # Remove um pacote

```

### **Pacotes em Arch Linux (pacman)**

```bash
sudo pacman -Syu       # Atualiza o sistema
sudo pacman -S <pacote> # Instala um pacote
sudo pacman -R <pacote> # Remove um pacote

```

---

## ⏪ **Compactação e Extração de Arquivos**

```bash
tar -cvf arquivo.tar <diretório>  # Cria um arquivo .tar
tar -xvf arquivo.tar              # Extrai um arquivo .tar
tar -czvf arquivo.tar.gz <diretório>  # Cria um arquivo .tar.gz
tar -xzvf arquivo.tar.gz            # Extrai um arquivo .tar.gz
zip -r arquivo.zip <diretório>      # Cria um arquivo .zip
unzip arquivo.zip                  # Extrai um arquivo .zip

```

---

## 🔑 **Gerenciamento de Usuários e Grupos**

```bash
whoami                    # Exibe o nome do usuário atual
id                        # Exibe o ID do usuário e grupos
sudo useradd <usuario>     # Cria um novo usuário
sudo passwd <usuario>      # Define a senha de um usuário
sudo userdel <usuario>     # Remove um usuário
sudo groupadd <grupo>      # Cria um novo grupo
sudo usermod -aG <grupo> <usuario>  # Adiciona um usuário a um grupo

```

---

## 🔄 **Tarefas Agendadas com Cron**

```bash
crontab -e               # Edita o crontab (agendador de tarefas)
crontab -l               # Lista tarefas agendadas

```

### **Exemplo de agendamento**

Agendar uma tarefa para rodar todos os dias às 3h:

```
0 3 * * * /caminho/do/script.sh

```

---

## 💾 **Montando e Desmontando Dispositivos**

```bash
mount /dev/sda1 /mnt   # Monta o dispositivo /dev/sda1 no diretório /mnt
umount /mnt            # Desmonta o diretório /mnt

```

### **Montando uma Imagem ISO**

```bash
mount -o loop arquivo.iso /mnt/iso  # Monta uma imagem ISO no diretório /mnt/iso

```

---

## 🛠 **Sistema de Arquivos**

```bash
df -h                # Exibe o uso do sistema de arquivos
mount                # Exibe dispositivos montados
fsck /dev/sda1       # Verifica e corrige o sistema de arquivos de uma partição

```

---

## 🏗 **Trabalhando com Git**

```bash
git init               # Inicializa um repositório Git
git clone <url>        # Clona um repositório remoto
git status             # Exibe o status atual do repositório
git add <arquivo>      # Adiciona alterações ao stage
git commit -m "mensagem"  # Faz o commit das alterações
git push               # Envia as alterações para o repositório remoto

```

---

## 📡 **Trabalhando com Docker**

```bash
docker pull <imagem>    # Baixa uma imagem do Docker Hub
docker build -t <nome> .  # Cria uma imagem a partir de um Dockerfile
docker run -d -p 8080:80 <imagem>  # Roda um container a partir de uma imagem
docker ps              # Lista containers em execução
docker stop <id>       # Para um container
docker rm <id>         # Remove um container
docker rmi <imagem>    # Remove uma imagem

```

---

🔥 **Dicas Extras:**

- **`man <comando>`**: Mostra o manual de qualquer comando.
- **`alias <nome>='<comando>'`**: Cria um atalho para comandos usados frequentemente.
- **`history`**: Exibe os últimos comandos executados.
- **`nohup`**: Executa comandos que continuam rodando após fechar o terminal.
