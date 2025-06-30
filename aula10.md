# Resumo da aula - 16/05/2025

---

# Revisão e Tarefas Práticas — Sistemas Unix e Bash

## 🎯 Objetivo

Rever, aplicar e consolidar os conteúdos abordados na disciplina, com foco em:

- Programação em Bash Script;
- Automação de tarefas em Unix via Bash Script;
- Escalonamento e gestão do processador;
- Algoritmos de escalonamento.

---

## 🖥️ 1. Programação em Bash Script

### 📝 1.1 Exemplo simples de script Bash

```bash
#!/bin/bash
echo "Olá, Mundo!"
```

### 1.2 Criar e executar um script

```bash
nano meu_script.sh       # Criar o script
chmod +x meu_script.sh   # Tornar executável
./meu_script.sh          # Executar o script
```

### 1.3 Variáveis e estruturas de controlo básicas

```bash
nome="Utilizador"
echo "Olá, $nome"

if [ $nome == "Utilizador" ]; then
    echo "Bem-vindo!"
else
    echo "Quem és?"
fi

for i in {1..5}; do
    echo "Número $i"
done
```

---

## ⚙️ 2. Automação de Tarefas com Bash Script

### 2.1 Exemplo de backup automático

```bash
#!/bin/bash
tar -czf backup_$(date +%F).tar.gz /caminho/para/dados
```

### 2.2 Agendar tarefas com `cron`

```bash
crontab -e              # Editar crontab do utilizador
# Exemplo: executar backup às 2h da manhã todos os dias
0 2 * * * /caminho/meu_script_backup.sh
```

---

## 🕒 3. Escalonamento e Gestão do Processador

### 3.1 Visualizar processos e uso do CPU

```bash
top                  # Monitorização em tempo real
htop                 # Monitor interativo (se instalado)
```

### 3.2 Prioridade de processos (`nice` e `renice`)

```bash
nice -n 10 ./meu_script.sh    # Executar com prioridade baixa
renice 5 -p <PID>             # Alterar prioridade de um processo em execução
```

### 3.3 Ver escalonadores e afinidade

```bash
cat /sys/devices/system/cpu/sched_debug  # Informação detalhada sobre escalonamento
taskset -c 0,1 ./meu_script.sh           # Executa processo ligado a CPUs específicas
```

---

## 🔄 4. Algoritmos de Escalonamento (Resumo)

| Algoritmo            | Descrição                               | Uso comum                      |
|----------------------|---------------------------------------|-------------------------------|
| FIFO (First In First Out) | Executa na ordem da chegada            | Simples, pouca prioridade       |
| Round Robin          | Tempo de CPU fixo para cada processo   | Multitarefa com tempo justo     |
| Prioridade           | Executa processo com maior prioridade  | Sistemas interativos            |
| Escalonamento por múltiplas filas | Diferentes filas com prioridades     | Sistemas complexos e híbridos   |

---

## ✅ Conclusão

A programação em Bash, aliada ao conhecimento de escalonamento e gestão do processador, permite criar sistemas Unix mais eficientes e automatizados. A prática destas tarefas consolida o domínio teórico com aplicação real.
