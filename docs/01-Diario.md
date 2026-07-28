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

- Configurei meu primeiro AI Agent utilizando Groq.
- Entendi o papel do System Prompt.
- Aprendi que o comportamento do agente pode ser completamente alterado apenas modificando as instruções.

### Memória
- Aprendi a adicionar memória ao agente.
- Configurei o Context Window Length em 5.
- Entendi que a memória permite ao agente lembrar mensagens anteriores.

### Tools
- Adicionei uma calculadora.
- Adicionei a Wikipedia.
- Compreendi que o agente pode utilizar ferramentas externas.

### Deploy
- Aprendi a disponibilizar uma URL pública.
- Descobri como ativar o Workflow na versão mais recente do n8n.

## O que foi desenvolvido

Nesta aula foi concluída a construção do primeiro Agente de IA funcional utilizando o n8n.

- Configurei um agente funcional.
- Adicionei memória.
- Integrei ferramentas.
- Publiquei o agente na Web.
- Realizei testes alterando o comportamento do agente.

Para ampliar suas capacidades, foram integradas duas ferramentas (**Tools**):

- Calculadora, permitindo realizar operações matemáticas.
- Wikipedia, possibilitando consultar informações durante a conversa.

Durante os testes, foram realizadas diferentes configurações no System Prompt para observar como as instruções influenciam o comportamento do agente. Entre os experimentos, o agente foi configurado para responder de forma sedutora e, em outro momento, para responder de forma mais ríspida quando recebesse mensagens grosseiras. Esses testes demonstraram, na prática, como o comportamento de um Agente de IA pode ser alterado apenas modificando o prompt, sem necessidade de alterar o fluxo da automação.

---

## Aula 03: Agente Integrado ao WhatsApp com registro automático de leads no Google Sheets utilizando a Z-API.

## O que aprendi

- Compreendi a diferença entre APIs e Webhooks.
- Aprendi a diferença entre os nodes **Filter**, **If** e **Switch**.
- Tive meu primeiro contato com o node **HTTP Request**.
- Também compreendi a diferença entre a **Test URL** e a **Production URL** do Webhook.

## O que foi desenvolvido

Durante esta aula foi desenvolvido um fluxo completo de atendimento automático via WhatsApp.

O fluxo passou a receber mensagens enviadas pelo WhatsApp através da Z-API, processá-las utilizando um Agente de IA e responder automaticamente ao usuário.

Também foi implementado o registro automático dos contatos em uma planilha do Google Sheets, garantindo que cada usuário fosse cadastrado apenas uma vez.

Ao final da aula, o fluxo foi publicado e testado.

## Encerramento do Dia

Além de aprender os conceitos fundamentais da ferramenta, consegui desenvolver dois projetos completos utilizando Agentes de IA.

- Um agente semelhante ao ChatGPT, acessado por uma interface de chat.
- Um agente capaz de responder automaticamente mensagens recebidas pelo WhatsApp.

A partir deste ponto, o objetivo deixa de ser apenas aprender o n8n e passa a ser aplicar esse conhecimento na construção de um projeto próprio, documentando toda a evolução desde sua concepção até uma versão funcional.

---

# Dia 1

**Data:**

09/07/2026

**Tempo investido: 4 horas**

---

## Objetivo do dia

Planejar a arquitetura do projeto English AI Tutor e definir os primeiros passos para o desenvolvimento do MVP.

---

## O que foi desenvolvido

### Documentação da Arquitetura

Foram criados os seguintes documentos:

- 03-Plano-de-Aprendizagem.md
- 04-Perfil-do-Aluno.md
- 05-Sistema-de-Memória.md
- 06-Modos-de-Funcionamento.md
- 07-Arquitetura-do-Sistema.md

Cada documento define uma parte específica da inteligência do Professor Arthur.

---

### Definição da primeira interação do Arthur

Foi projetada a primeira conversa entre o Professor Arthur e um novo aluno.

Nessa interação Arthur deverá:

- apresentar-se;
- explicar como pode ajudar;
- identificar o nome do aluno;
- descobrir se o aluno já estudou inglês;
- identificar o objetivo do aprendizado;
- identificar a forma preferida de estudo;
- realizar uma breve avaliação para estimar o nível de inglês;
- montar um plano de estudos personalizado.

---

### Organização do projeto

Foi criada a estrutura da primeira Sprint de desenvolvimento.

Sprint 01:

Objetivo:

Construir a primeira versão funcional do Professor Arthur.

Também foi definida a estratégia de desenvolvimento baseada em Sprints, aproximando o projeto do fluxo de trabalho utilizado em equipes de desenvolvimento de software.

---

### Modelagem inicial do sistema

Foi definida a primeira estrutura de armazenamento de dados.

Inicialmente será utilizado o Google Sheets como banco de dados temporário.

A estrutura planejada será composta por abas independentes para:

- Alunos
- Histórico de Aulas
- Sessões
- Plano de Estudos
- Conteúdos Concluídos

Essa organização facilitará uma futura migração para um banco de dados relacional.

---

## Aprendizados

Hoje compreendi melhor como um projeto de software é planejado antes do início da implementação.

Percebi a importância de definir arquitetura, responsabilidades dos componentes e organização dos dados antes de construir os fluxos no n8n.

Também comecei a entender conceitos de Engenharia de Software que vão além da criação de automações.

---

## Dificuldades

Durante o planejamento surgiram diversas ideias novas para o projeto.

O principal desafio foi manter o foco no MVP e evitar adicionar funcionalidades que podem ser implementadas apenas em versões futuras.

---

# Dia 2

**Data:**

24/07/2026

**Tempo investido: 3 horas**

## O que foi desenvolvido

Hoje preparei o ambiente de desenvolvimento local que será utilizado durante a construção do projeto.

Principais atividades realizadas:

- Instalei o Docker Desktop.
- Identifiquei e resolvi um problema na inicialização do Docker relacionado ao WSL2.
- Habilitei os componentes necessários do Windows para utilização do WSL2.
- Validei o funcionamento do Docker e do WSL2 através do terminal.
- Criei o primeiro arquivo docker-compose.yml.
- Estruturei o ambiente para execução local do n8n.
- Executei meu primeiro container Docker.
- Iniciei o n8n local com sucesso.
- Organizei a estrutura da documentação no GitHub.
- Criei o documento 11-Ambiente-de-Desenvolvimento.md para registrar a configuração do ambiente do projeto.

---

## O que aprendi

Hoje tive meu primeiro contato prático com Docker.

Aprendi que:

- Docker Desktop utiliza o WSL2 para executar containers Linux.
- O arquivo docker-compose.yml define os serviços que serão executados pelo Docker.
- Containers permitem executar aplicações de forma isolada e organizada.
- O Docker Compose facilita a criação e gerenciamento de ambientes de desenvolvimento.
- Problemas de configuração podem ser diagnosticados através de mensagens de erro e comandos no terminal.

Também compreendi melhor a relação entre:

- Docker
- WSL2
- Docker Compose
- n8n

e como essas tecnologias trabalham juntas.

---

## Dificuldades encontradas

Durante a instalação do Docker Desktop, o sistema informou que a virtualização não estava disponível.

Após investigar o problema, identifiquei que a virtualização da BIOS estava habilitada, porém o WSL2 ainda não estava configurado corretamente.

Depois de habilitar os componentes necessários do Windows e reiniciar o computador, o Docker iniciou normalmente.

---

**Data:** 

28/07/2026

**Tempo investido: 4h44**

---

## Objetivo do dia
Construção do primeiro Workflow do Arthur

Hoje foi iniciado o desenvolvimento da primeira ferramenta utilizada pelo Arthur.

Até este momento o Arthur apenas conversava utilizando IA.

A partir deste Sprint começou a separação da arquitetura em múltiplos Workflows especializados.

O primeiro Workflow criado foi:

**WF - Cadastro de Aluno** (Detalhes do fluxo na pasta *Workflows*, arquivo *Cadastro de Aluno.md*)

Sua responsabilidade é registrar um novo aluno na base de dados.

---

## Decisão de Arquitetura

Foi decidido não criar um Workflow gigantesco contendo todas as regras.

Em vez disso, cada funcionalidade será construída como um Workflow independente.

Arquitetura planejada:

Arthur
 - Cadastro de Aluno
 - Buscar Perfil
 - Registrar Aula
 - Registrar Vocabulário
 - Plano de Estudos
 - Dashboard
 - Outros módulos
