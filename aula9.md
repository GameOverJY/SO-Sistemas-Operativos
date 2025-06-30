# Resumo da aula - 09/05/2025
# Tarefas Práticas - Administração de Sistemas

## Objetivo

Rever, aplicar e consolidar os conteúdos abordados na disciplina, através da execução de tarefas práticas com foco em:

- Comandos para gestão da máquina;
- Comandos para gestão de utilizadores;
- Configuração do ambiente de trabalho em linha de comandos.

---

## 1. Comandos para Gestão da Máquina

### 1.1. Verificar informações do sistema

```bash
uname -a         # Informações gerais do sistema
hostname         # Nome do host
uptime           # Tempo de atividade do sistema
top              # Processos ativos e uso de CPU/memória
df -h            # Espaço em disco
free -h          # Uso da memória RAM
```

### 1.2. Gestão de pacotes (Debian/Ubuntu)

```bash
sudo apt update                 # Atualiza a lista de pacotes
sudo apt upgrade                # Atualiza os pacotes instalados
sudo apt install <pacote>       # Instala um pacote
sudo apt remove <pacote>        # Remove um pacote
```

### 1.3. Gestão de processos e serviços

```bash
ps aux                         # Lista todos os processos ativos
kill <PID>                     # Termina um processo pelo PID
sudo systemctl status          # Verifica o estado dos serviços
sudo systemctl restart <serviço>  # Reinicia um serviço específico
```

---

## 2. Comandos para Gestão de Utilizadores

### 2.1. Gestão de utilizadores

```bash
sudo adduser <nome_utilizador>      # Adiciona um novo utilizador
sudo deluser <nome_utilizador>      # Remove um utilizador existente
```

### 2.2. Gestão de grupos

```bash
sudo groupadd <nome_grupo>          # Cria um novo grupo
sudo usermod -aG <grupo> <utilizador>  # Adiciona um utilizador a um grupo
groups <utilizador>                 # Lista os grupos de um utilizador
```

### 2.3. Permissões de ficheiros

```bash
chmod 755 <ficheiro>               # Altera permissões do ficheiro
chown user:grupo <ficheiro>        # Altera dono e grupo de um ficheiro
ls -l                              # Lista ficheiros com permissões
```

---

## 3. Configuração do Ambiente em Linha de Comandos

### 3.1. Edição de ficheiros de configuração

```bash
nano ~/.bashrc            # Editar ficheiro de configuração do bash
source ~/.bashrc          # Recarregar o ficheiro após alterações
```

### 3.2. Alias e personalização

```bash
alias atualizar='sudo apt update && sudo apt upgrade'
alias cls='clear'
```

### 3.3. Ver variáveis de ambiente

```bash
echo $HOME
echo $PATH
printenv
```

---

## Conclusão

A prática constante com comandos de linha permite o domínio da administração básica de sistemas, essencial para ambientes profissionais e académicos.