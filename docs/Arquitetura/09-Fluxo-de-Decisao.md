# Fluxo de Decisão do Arthur

## Objetivo

Este documento descreve como o Professor Arthur toma decisões durante uma conversa com o aluno.

O objetivo é definir toda a lógica de funcionamento antes da implementação no n8n.

---

# Fluxo Principal

Todo contato com o Arthur seguirá o fluxo abaixo:

Mensagem do usuário

↓

Identificar o aluno

↓

Aluno já existe?

── Não

   → Apresentação
   → Entrevista Inicial
   → Criação do Perfil
   → Criação do Plano de Estudos
   → Salvar informações
   → Iniciar primeira aula

── Sim

    → Carregar Perfil
    → Carregar Memória
    → Identificar modo de funcionamento
    → Continuar atendimento

---

# Fluxo de um Novo Aluno

Quando um aluno conversa com Arthur pela primeira vez:

1. Arthur se apresenta.
2. Explica como pode ajudar.
3. Pergunta o nome do aluno.
4. Pergunta se já estudou inglês.
5. Pergunta qual é seu objetivo.
6. Pergunta sua área de atuação.
7. Pergunta como prefere aprender.
8. Faz uma breve avaliação do nível de inglês.
9. Cria um plano de estudos personalizado.
10. Salva todas as informações.
11. Inicia a primeira aula.

---

# Fluxo de um Aluno Existente

Quando o aluno já possui cadastro:

1. Arthur identifica o aluno.
2. Recupera seu perfil.
3. Recupera seu plano de estudos.
4. Recupera seu histórico.
5. Recupera sua memória recente.
6. Identifica o modo de funcionamento.
7. Continua exatamente de onde o aluno parou.

---

# Modos de Funcionamento

Arthur poderá atuar em diferentes modos.

## Professor

Responsável por ensinar inglês desde o início.

Arthur conduz todo o processo de aprendizagem.

Ele define:

- conteúdos;
- exercícios;
- revisões;
- evolução do aluno.

---

## Tutor

Responsável por responder dúvidas.

Pode:

- explicar conteúdos;
- corrigir exercícios;
- conversar em inglês;
- corrigir pronúncia (futuramente);
- ajudar em tarefas.

---

## Mentor (Versão futura)

Responsável por acompanhar alunos que estudam por outros cursos.

Arthur reforça o conteúdo aprendido.

Pode:

- criar conversações;
- fazer perguntas;
- revisar conteúdos;
- corrigir erros;
- criar desafios personalizados.

---

# Processo de Resposta

Sempre que receber uma mensagem, Arthur deverá seguir a seguinte sequência:

1. Entender a intenção do aluno.
2. Identificar o contexto.
3. Consultar a memória.
4. Consultar o plano de estudos.
5. Decidir qual ação executar.
6. Gerar uma resposta personalizada.
7. Registrar a sessão.

---

# Fluxo da Memória

Arthur utilizará diferentes tipos de memória.

## Memória Permanente

Informações do aluno.

Exemplos:

- nome;
- objetivo;
- área;
- nível;
- método preferido.

---

## Memória de Curto Prazo

Utilizada durante a conversa atual.

Exemplos:

- últimas mensagens;
- exercício atual;
- contexto da aula.

---

## Memória de Longo Prazo

Histórico de evolução.

Exemplos:

- conteúdos estudados;
- dificuldades;
- erros frequentes;
- aulas concluídas;
- progresso.

---

# Encerramento da Sessão

Ao finalizar uma conversa Arthur deverá:

- registrar a sessão;
- atualizar o progresso do aluno;
- salvar novos conteúdos aprendidos;
- atualizar a memória;
- incentivar o aluno a continuar estudando.
