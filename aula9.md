# Resumo da aula - 09/05/2025

---

# Tarefas Práticas — Administração de Sistemas Linux

## 🎯 Objetivo

Consolidar os conhecimentos adquiridos na disciplina através da realização de tarefas práticas focadas em:

- 📁 Gestão da máquina;
- 👤 Gestão de utilizadores;
- ⚙️ Configuração do ambiente de trabalho via linha de comandos.

---

## 🖥️ 1. Gestão da Máquina

### 🔍 1.1 Verificação de informações do sistema

```bash
uname -a         # Exibe informações completas sobre o sistema
hostname         # Mostra o nome do host da máquina
uptime           # Indica há quanto tempo o sistema está ativo
top              # Exibe os processos em tempo real
df -h            # Mostra o uso de espaço em disco (formato legível)
free -h          # Mostra a utilização da memória (RAM e swap)
```

### 📦 1.2 Gestão de pacotes (Distribuições Debian/Ubuntu)

```bash
sudo apt update                 # Atualiza a lista de pacotes disponíveis
sudo apt upgrade                # Atualiza os pacotes instalados
sudo apt install <pacote>       # Instala um novo pacote
sudo apt remove <pacote>        # Remove um pacote instalado
```

### ⚙️ 1.3 Gestão de processos e serviços

```bash
ps aux                         # Lista todos os processos em execução
kill <PID>                     # Encerra um processo específico
sudo systemctl status          # Mostra o estado geral dos serviços
sudo systemctl restart <serviço>  # Reinicia um serviço (ex: apache2)
```

---

## 👥 2. Gestão de Utilizadores e Grupos

### ➕ 2.1 Criação e remoção de utilizadores

```bash
sudo adduser <utilizador>       # Cria um novo utilizador
sudo deluser <utilizador>       # Remove um utilizador existente
```

### 👥 2.2 Gestão de grupos

```bash
sudo groupadd <grupo>                # Cria um novo grupo
sudo usermod -aG <grupo> <utilizador>  # Adiciona o utilizador a um grupo
groups <utilizador>                  # Lista os grupos de um utilizador
```

### 🔐 2.3 Permissões e propriedade de ficheiros

```bash
chmod 755 <ficheiro>                  # Define permissões para o ficheiro
chown utilizador:grupo <ficheiro>     # Altera o dono e grupo do ficheiro
ls -l                                 # Lista ficheiros com detalhes de permissões
```

---

## 🛠️ 3. Configuração do Ambiente de Trabalho em Linha de Comandos

### 📝 3.1 Personalização do bash

```bash
nano ~/.bashrc              # Edita o ficheiro de configuração do bash
source ~/.bashrc            # Aplica as alterações feitas
```

### 🔁 3.2 Criação de alias úteis

```bash
alias atualizar='sudo apt update && sudo apt upgrade'
alias limpar='clear'
```

### 🌐 3.3 Variáveis de ambiente

```bash
echo $HOME                  # Mostra o diretório pessoal
echo $PATH                  # Lista os caminhos de execução configurados
printenv                    # Exibe todas as variáveis de ambiente
```

---

## ✅ Conclusão

A familiarização com a linha de comandos é essencial para qualquer administrador de sistemas. Estas tarefas práticas reforçam os conhecimentos teóricos e preparam o aluno para resolver situações reais em ambientes Linux.