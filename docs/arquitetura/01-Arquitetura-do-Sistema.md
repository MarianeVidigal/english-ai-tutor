# Arquitetura do Sistema

## Objetivo

Este documento descreve como os principais componentes do English AI Tutor interagem entre si para oferecer uma experiência de aprendizado personalizada.

A arquitetura foi projetada para ser modular, permitindo a evolução do sistema sem a necessidade de reestruturar toda a aplicação.

---

# Visão Geral

O English AI Tutor é composto por diversos módulos independentes, cada um responsável por uma função específica.

Quando um aluno envia uma mensagem, Arthur analisa o contexto, consulta as informações necessárias e responde de acordo com seu método de ensino.

---

# Fluxo Geral

Aluno

↓

Recebimento da mensagem

↓

Identificação do aluno

↓

Consulta ao Perfil do Aluno

↓

Consulta ao Sistema de Memória

↓

Identificação do Modo de Funcionamento

↓

Consulta ao Plano de Aprendizagem (quando necessário)

↓

Geração da resposta

↓

Atualização da Memória

↓

Resposta enviada ao aluno

---

# Componentes

## Persona

Responsável por definir quem é Arthur.

Define sua personalidade, comportamento e forma de comunicação.

Documento relacionado:

- 01-Persona-Arthur.md

---

## Método de Ensino

Define como Arthur ensina.

Controla a estrutura das aulas, correções e motivação.

Documento relacionado:

- 02-Metodo-de-Ensino.md

---

## Plano de Aprendizagem

Define todas as trilhas de ensino disponíveis.

Documento relacionado:

- 03-Plano-de-Aprendizagem.md

---

## Perfil do Aluno

Armazena as características individuais de cada aluno.

Exemplos:

- Objetivo
- Nível
- Área profissional
- Preferências
- Ritmo de aprendizagem

Documento relacionado:

- 04-Perfil-do-Aluno.md

---

## Sistema de Memória

Responsável por armazenar informações importantes sobre a evolução do aluno.

Exemplos:

- Histórico de aulas
- Conteúdos estudados
- Últimos erros
- Evolução

Documento relacionado:

- 05-Sistema-de-Memória.md

---

## Modos de Funcionamento

Define o comportamento do Arthur conforme o objetivo do aluno.

Exemplos:

- Professor
- Tutor
- Conversação
- Prática
- Revisão
- Simulações

Documento relacionado:

- 06-Modos-de-Funcionamento.md

---

# Fluxo de Decisão

Sempre que uma mensagem é recebida, Arthur procura responder às seguintes perguntas:

1. Quem é o aluno?
2. Qual é seu nível?
3. Qual é seu objetivo?
4. Existe um histórico anterior?
5. O aluno deseja aprender um novo conteúdo ou praticar algo já estudado?
6. Qual modo de funcionamento deve ser utilizado?
7. Como responder respeitando a personalidade do Arthur?

---

# Escalabilidade

A arquitetura foi desenvolvida para permitir futuras expansões, como:

- Aplicativo mobile.
- Plataforma web.
- Integração com WhatsApp.
- Integração com Telegram.
- Conversação por voz.
- Correção de pronúncia.
- Dashboard de evolução.
- Gamificação.
- Múltiplos professores utilizando a mesma arquitetura.

---

# Princípios da Arquitetura

O sistema deve seguir os seguintes princípios:

- Modularidade.
- Escalabilidade.
- Reutilização.
- Personalização.
- Facilidade de manutenção.
- Experiência centrada no aluno.

---

# Objetivo Final

Criar um assistente inteligente capaz de acompanhar o aluno durante toda sua jornada de aprendizado, adaptando-se às suas necessidades, objetivos e evolução.
