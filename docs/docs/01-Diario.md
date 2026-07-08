# Diário de Desenvolvimento

---

# Dia 0

Data: 07/07/2026

Tempo investido: 55 minutos

Tema: 
Introdução às Ferramentas do n8n e Organização da Base de Automação.

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

---

## O que foi desenvolvido

Durante esta aula foi construída a base inicial da automação.

Foi criado:

- um Chat utilizando o node **On Chat Message**;
- um fluxo para registrar automaticamente todas as mensagens em uma planilha do Google Sheets;
- a estrutura inicial para utilização de um Agente de IA.

O agente foi adicionado ao fluxo, porém sua configuração será realizada nas próximas aulas.

---

## O que aconteceu hoje

- Criei o repositório no GitHub.
- Defini o nome do projeto.
- Estruturei a documentação inicial.
- Iniciei a Imersão de n8n da NoCode StartUp.

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

## Expectativas

Meu objetivo é desenvolver um professor particular de inglês utilizando Inteligência Artificial.
Também desejo evoluir profissionalmente na área de Tecnologia da Informação e utilizar este projeto como portfólio.

---

## Observações

Este é o primeiro dia do projeto.
