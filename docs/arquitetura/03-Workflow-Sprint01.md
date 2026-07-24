# Workflow - Sprint 01

## Objetivo

Desenvolver o primeiro fluxo funcional do Professor Arthur.

Ao final desta Sprint, um novo aluno deverá conseguir iniciar sua jornada no English AI Tutor de forma totalmente personalizada.

---

# Fluxo Geral

Novo usuário

↓

Arthur identifica se o aluno já possui cadastro.

↓

Se não possuir:

- Arthur realiza a apresentação.
- Arthur explica como pode ajudar.
- Arthur inicia a entrevista inicial.
- Arthur cria o perfil do aluno.
- Arthur salva as informações.
- Arthur cria o plano de estudos.
- Arthur inicia a primeira aula.

↓

Se possuir cadastro:

- Arthur recupera o perfil.
- Arthur recupera a memória.
- Arthur continua exatamente de onde o aluno parou.

---

# Workflow do n8n

## Node 01

### Chat Trigger

Função:

Receber mensagens do usuário.

Status:

⬜ Não iniciado

---

## Node 02

### Buscar Aluno

Função:

Consultar a aba "Alunos" do Google Sheets utilizando o identificador do usuário.

Entradas:

- ID do usuário

Saída:

- Aluno encontrado
- Aluno não encontrado

Status:

⬜ Não iniciado

---

## Node 03

### Verificar Cadastro

Função:

Decidir qual fluxo deverá ser executado.

Condição:

Aluno existe?

Sim → Fluxo de aluno existente.

Não → Fluxo de novo aluno.

Status:

⬜ Não iniciado

---

# Fluxo do Novo Aluno

## Node 04

### Apresentação do Arthur

Arthur deverá:

- cumprimentar;
- apresentar-se;
- explicar como pode ajudar;
- informar que poderá atuar como Professor ou Tutor.

Status:

⬜ Não iniciado

---

## Node 05

### Entrevista Inicial

Arthur deverá perguntar:

- Como gostaria de ser chamado?
- Já estudou inglês?
- Qual seu objetivo?
- Em qual área trabalha?
- Como prefere aprender?

Status:

⬜ Não iniciado

---

## Node 06

### Avaliação Inicial

Arthur realizará uma pequena conversa para estimar o nível do aluno.

Status:

⬜ Não iniciado

---

## Node 07

### Salvar Perfil

Salvar na aba:

Alunos

Campos:

- Nome
- Objetivo
- Área
- Método
- Nível
- Data Cadastro
- Status

Status:

⬜ Não iniciado

---

## Node 08

### Criar Plano de Estudos

Arthur cria um plano personalizado.

Salvar na aba:

Plano_Estudos

Status:

⬜ Não iniciado

---

## Node 09

### Primeira Aula

Arthur inicia o primeiro conteúdo.

Status:

⬜ Não iniciado

---

# Fluxo do Aluno Existente

## Node 10

### Recuperar Perfil

Consultar:

- Alunos
- Plano_Estudos
- Histórico_Aulas

Status:

⬜ Não iniciado

---

## Node 11

### Recuperar Memória

Consultar:

- Sessões

Status:

⬜ Não iniciado

---

## Node 12

### Continuar Aula

Arthur continua exatamente do ponto onde o aluno parou.

Status:

⬜ Não iniciado

---

# Critério de Conclusão

A Sprint será considerada concluída quando:

- Um novo aluno conseguir realizar o cadastro.
- Arthur salvar todas as informações.
- Arthur criar um plano de estudos.
- Arthur iniciar a primeira aula.
- Um aluno já cadastrado conseguir continuar seus estudos automaticamente.
