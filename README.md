# 🎓 Sistema de Controle de Aula — Projeto Integrado

> Projeto integrado das disciplinas de **Sistemas Embarcados (SEB)** e **Linguagens de Programação (LPR)**  
> ETE FMC — 3ª Série DS | 2026

---

## 🎬 Vídeo de Apresentação

**[▶ Assistir no YouTube](https://www.youtube.com/watch?v=Jt65S25d4kI)**

---

## 👥 Integrantes

- **Ryan Machado**
- **João Lucas Dionísio**

---

## 📋 Sobre o Projeto

Sistema embarcado interativo desenvolvido para **controle de presença e gestão de alunos em laboratório**, utilizando microcontrolador **STM32** com display e botoeiras físicas.

O sistema simula um fluxo real de controle de aula, do início ao encerramento, com autenticação por senha, registro de entradas, controle de saídas e geração de relatório final.

---

## ⚙️ Funcionalidades

### 🔐 Autenticação
- O sistema gera uma senha numérica aleatória de 2 dígitos ao iniciar
- **PA9 (Botão 1)** — Inicia o sistema / incrementa o dígito atual
- **PA10 (Botão 2)** — Confirma o dígito inserido
- Após inserir os 2 dígitos, a senha é validada
- O sistema bloqueia por **5 segundos** após 3 tentativas incorretas

### 🏫 Configuração de Turma
- Define o número máximo de alunos antes de iniciar a aula
- **PA9 (Botão 1)** — Incrementa o dígito atual
- **PA10 (Botão 2)** — Confirma o dígito inserido
- O limite é definido com 2 dígitos (ex: 25 alunos)

### ✅ Controle de Presença
- Registro da matrícula (RA) do aluno dígito a dígito (5 dígitos)
- **PA9 (Botão 1)** — Seleciona/incrementa o dígito
- **PA10 (Botão 2)** — Confirma o dígito
- **PA11 (Botão 3)** — Encerra o registro e volta ao menu
- Entrada bloqueada automaticamente quando a sala está lotada

### 🚪 Controle de Saída (Banheiro/Água)
- Máximo de **3 alunos fora simultaneamente**
- **PA9 (Botão 1)** — Volta ao menu principal
- **PA10 (Botão 2)** — Registra uma saída
- **PA11 (Botão 3)** — Registra um retorno
- Nova saída bloqueada automaticamente quando o limite de 3 é atingido

### 🖥️ Menu Principal (Display)
Exibe em tempo real:
- Alunos presentes vs. total da turma
- Quantidade de alunos no banheiro
- **PA10 (Botão 2)** — Acessa o registro de matrícula
- **PA11 (Botão 3)** — Acessa o controle de saída
- **PA11 + PA12 (Botões 3 e 4 simultaneamente)** — Encerra a aula

### 📊 Relatório Final
Exibido automaticamente ao encerrar:
- Total de alunos registrados
- Quantidade total de saídas realizadas
