# Diário de Desenvolvimento

## Observações

Este é o primeiro dia do projeto.

---

## Expectativas

Meu objetivo é desenvolver um professor particular de inglês utilizando Inteligência Artificial.
Também desejo evoluir profissionalmente na área de Tecnologia da Informação e utilizar este projeto como portfólio.

---

## Objetivo da imersão

Aprender:

- Fundamentos do n8n
- Integração com Google Sheets
- Agentes de IA
- APIs
- Webhooks
- WhatsApp

---

# Dia 0

Data: 08/07/2026

Tempo investido na Aula 1, 2 e 3: 3h16min

## Aula 1: Introdução às Ferramentas do n8n e Organização da Base de Automação.

## O que aprendi

### Trigger

Aprendi que todo fluxo no n8n inicia por meio de um gatilho (Trigger). Nesta aula foi utilizado o node **On Chat Message**, responsável por iniciar o fluxo sempre que uma nova mensagem é enviada no chat.

### Edit Fields

Aprendi como utilizar o node **Edit Fields**, responsável por criar, editar ou organizar informações que serão utilizadas pelos próximos nodes do fluxo.

### Google Sheets

Realizei a integração do fluxo com o Google Sheets utilizando a ação **Append Row in Sheet**, permitindo registrar automaticamente todas as mensagens enviadas no chat.

Também conheci outras possibilidades de integração disponíveis para o Google Sheets.

### Arquitetura de um Agente de IA

Compreendi que um agente normalmente é composto por quatro pilares principais:

- Prompt Base
- Memória (Curto e Longo Prazo)
- Base de Conhecimento (RAG)
- Ferramentas (Tools)

## O que foi desenvolvido

Durante esta aula foi construída a base inicial da automação.

Foi criado:

- um Chat utilizando o node **On Chat Message**;
- um fluxo para registrar automaticamente todas as mensagens em uma planilha do Google Sheets;
- a estrutura inicial para utilização de um Agente de IA.

O agente foi adicionado ao fluxo, porém sua configuração será realizada nas próximas aulas.

---

## Aula 2: Construindo e finalizando o agente de IA

## O que aprendi

## Configuração do Agente
Configurei meu primeiro AI Agent utilizando Groq.
Entendi o papel do System Prompt.
Aprendi que o comportamento do agente pode ser completamente alterado apenas modificando as instruções.

## Memória
Aprendi a adicionar memória ao agente.
Configurei o Context Window Length em 5.
Entendi que a memória permite ao agente lembrar mensagens anteriores.

## Tools
Adicionei uma calculadora.
Adicionei a Wikipedia.
Compreendi que o agente pode utilizar ferramentas externas.

## Deploy
Aprendi a disponibilizar uma URL pública.
Descobri como ativar o Workflow na versão mais recente do n8n.

## O que foi desenvolvido

Nesta aula foi concluída a construção do primeiro Agente de IA funcional utilizando o n8n.

Configurei um agente funcional.
Adicionei memória.
Integrei ferramentas.
Publiquei o agente na Web.
Realizei testes alterando o comportamento do agente.

Para ampliar suas capacidades, foram integradas duas ferramentas (**Tools**):

- Calculadora, permitindo realizar operações matemáticas.
- Wikipedia, possibilitando consultar informações durante a conversa.

Durante os testes, foram realizadas diferentes configurações no System Prompt para observar como as instruções influenciam o comportamento do agente. Entre os experimentos, o agente foi configurado para responder de forma sedutora e, em outro momento, para responder de forma mais ríspida quando recebesse mensagens grosseiras. Esses testes demonstraram, na prática, como o comportamento de um Agente de IA pode ser alterado apenas modificando o prompt, sem necessidade de alterar o fluxo da automação.

---

# Aula 03: Agente Integrado ao WhatsApp com registro automático de leads no Google Sheets utilizando a Z-API.

## O que aprendi

Compreendi a diferença entre APIs e Webhooks.
Aprendi a diferença entre os nodes **Filter**, **If** e **Switch**.
Tive meu primeiro contato com o node **HTTP Request**.
Também compreendi a diferença entre a **Test URL** e a **Production URL** do Webhook.

## O que foi desenvolvido

Durante esta aula foi desenvolvido um fluxo completo de atendimento automático via WhatsApp.

O fluxo passou a receber mensagens enviadas pelo WhatsApp através da Z-API, processá-las utilizando um Agente de IA e responder automaticamente ao usuário.

Também foi implementado o registro automático dos contatos em uma planilha do Google Sheets, garantindo que cada usuário fosse cadastrado apenas uma vez.

Ao final da aula, o fluxo foi publicado utilizando a Production URL do Webhook.

Realizei testes enviando mensagens do meu número corporativo para o número pessoal utilizado na Z-API e o agente respondeu corretamente, validando o funcionamento completo da automação.

---
