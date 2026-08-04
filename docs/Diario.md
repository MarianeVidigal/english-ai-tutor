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

### Aula 1: Introdução às Ferramentas do n8n e Organização da Base de Automação.

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

### Aula 2: Construindo e finalizando o agente de IA

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

### Aula 03: Agente Integrado ao WhatsApp com registro automático de leads no Google Sheets usando Z-API.

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

- Instalei o Docker Desktop para desenvolvimento do projeto English AI Tutor
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

Aprendi que:

- Docker Desktop utiliza o WSL2 para executar containers Linux.
- O arquivo docker-compose.yml define os serviços que serão executados pelo Docker.
- Containers permitem executar aplicações de forma isolada e organizada.
- O Docker Compose facilita a criação e gerenciamento de ambientes de desenvolvimento.
- Problemas de configuração podem ser diagnosticados através de mensagens de erro e comandos no terminal.

---

## Ferramentas

- Docker Desktop
- WSL2
- n8n
- VS Code
- GitHub

---

## Configuração

### Docker

Instalado localmente.

### WSL2

Utilizado como backend do Docker Desktop.

### n8n

Executado através de Docker Compose.

Porta:

5678

URL Local:

http://localhost:5678

---

## Objetivo futuro

Este ambiente permitirá adicionar novos serviços como:

- PostgreSQL
- Qdrant
- Redis
- Ollama

## Dificuldades encontradas

Durante a instalação do Docker Desktop, o sistema informou que a virtualização não estava disponível.

Após investigar o problema, identifiquei que a virtualização da BIOS estava habilitada, porém o WSL2 ainda não estava configurado corretamente.

Depois de habilitar os componentes necessários do Windows e reiniciar o computador, o Docker iniciou normalmente.

---

# Dia 3

**Data:** 

27/07/2026

**Tempo investido: 4h44**

---

## Objetivo do dia
Construção do primeiro Workflow do Arthur

Hoje foi iniciado o desenvolvimento da primeira ferramenta utilizada pelo Arthur.

Até este momento o Arthur apenas conversava utilizando IA.

A partir deste Sprint começou a separação da arquitetura em múltiplos Workflows especializados.

O primeiro Workflow criado foi:

**WF - Cadastro de Aluno** 

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

**Essa arquitetura facilita:**

- manutenção;
- testes;
- reutilização;
- escalabilidade;
- organização do projeto.

---

## Desenvolvimento no Workflows: *WF - Cadastro do Aluno*

Fluxo

When Executed by Another Workflow

▼

Edit Fields

▼

Code

▼

Google Sheets (Append Row)

## Responsabilidade de cada nó

### 1. When Executed by Another Workflow

É a porta de entrada deste workflow.

Não realiza nenhuma alteração nos dados.

Receber os dados enviados pelo Arthur.

Exemplo:
 - Nome
 - Nível
 - Objetivo
 - Área
 - Método
 - SessionId

### 2. Edit Fields

Organiza todas as informações recebidas.

Também define valores padrão utilizados no cadastro.

Campos adicionados:

status = Ativo

versaoPerfil = 1

### 3. Code

Este foi o primeiro nó utilizando JavaScript.

Inicialmente foi tentado utilizar:

```
crypto.randomUUID()
```

Entretanto o ambiente do n8n não disponibiliza o objeto crypto.

Foi necessário utilizar:

```
crypto.randomUUID()
```

através do módulo disponível no ambiente do n8n.

O código passou a ser responsável por:

- gerar UUID;
- gerar dataCadastro;
- gerar ultimoAcesso.

Exemplo:

fc427eb0-1f61-4ab2-9313-2d135b95a252

### 4. Google Sheets

Insere uma nova linha na aba:

Alunos

Campos gravados:

- IdAluno
- SessionId
- Nome
- Nivel
- Objetivo
- Área
- Método
- DataCadastro
- UltimoAcesso
- Status
- VersaoPerfil
- Resultado

Após a execução existe um novo aluno cadastrado na planilha.

A aba **Alunos** passou a funcionar como o banco de dados inicial do projeto.

No futuro esse banco poderá ser migrado para PostgreSQL sem alterar a arquitetura do Arthur.

---

## Primeiro teste

Foi executado manualmente o Workflow.

Resultado:

✔ UUID gerado corretamente.

✔ Data cadastrada corretamente.

✔ Linha inserida na planilha.

Como o Workflow foi executado isoladamente, os campos recebidos do Arthur permaneceram vazios.

Mesmo assim foi possível validar toda a lógica de cadastro.

---

## Arquitetura Modular

Cada Workflow possui apenas uma responsabilidade.

---

## Workflow como Serviço

O Cadastro de Aluno funciona como um pequeno serviço especializado.

No futuro será chamado pelo Arthur sempre que necessário.

---

## Separação de responsabilidades

Cada nó possui apenas uma função.

Isso torna o Workflow mais organizado.

---

## Persistência de dados

O Google Sheets passa a funcionar como banco de dados da aplicação.

---

## Integração externa

Primeira integração completa utilizando credenciais de API.

---

## Próximo objetivo

Na próxima Sprint o Arthur deixará de ser apenas um chatbot.

Ele será capaz de:

- conversar;
- identificar quando possui todas as informações necessárias;
- executar automaticamente o Workflow Cadastro de Aluno;
- registrar o novo aluno na planilha;
- continuar a conversa normalmente após o cadastro.


Arthur

▼

Conversa com usuário

▼

(em breve)

Call Workflow

▼

WF Cadastro de Aluno

▼

Google Sheets

---

# Dia 4

**Data:** 

28/07/2026

**Tempo investido: 6h20**

---

## Objetivo da Sprint

O objetivo desta Sprint era permitir que o Arthur cadastrasse automaticamente um novo aluno no Google Sheets após coletar todas as informações necessárias durante a conversa.

Durante o desenvolvimento descobri limitações na arquitetura utilizada inicialmente e decidimos refatorar completamente essa parte do projeto para torná-la mais modular, robusta e próxima de uma arquitetura utilizada em sistemas reais de Inteligência Artificial.

---

## O que já estava funcionando antes desta Sprint

Antes de iniciar os trabalhos de hoje, o projeto já possuía:

Workflow de Cadastro de Aluno criado.
Integração funcionando com Google Sheets.
Geração automática de UUID para cada aluno.
Criação automática da Data de Cadastro.
Estrutura inicial do cadastro funcionando.
AI Agent (Arthur) realizando a conversa normalmente.

O problema era apenas a comunicação entre o Arthur e o Workflow de Cadastro.

---

## Dificuldades encontradas

Inicialmente utilizamos o recurso:
```
Call n8n Workflow Tool
```
A ideia era que o Arthur chamasse diretamente o Workflow de Cadastro e enviasse os dados preenchidos durante a conversa.

Entretanto começaram a surgir diversos problemas.

Os principais foram:

parâmetros chegando como null;
erro de validação do schema;
campos sendo considerados inválidos;
dificuldade do modelo em preencher corretamente todos os parâmetros da ferramenta.

Em alguns testes a IA chegou inclusive a montar corretamente todos os dados:
```
{
  "nome": "Rodrigo",
  "nivel": "zero",
  "objetivo": "viajar",
  "area": "T.I",
  "metodo": "pratica",
  "sessionId": "123456"
}
```

Porém o próprio Workflow Tool rejeitava essas informações durante a validação.

---

## Decisão

Ao invés de continuar tentando contornar as limitações do Workflow Tool, foi tomada uma decisão importante.

Toda a arquitetura foi redesenhada.

---

### Novo Workflow criado

Foi criado um novo Workflow chamado:

**WF - Extrair Perfil**

Sua única responsabilidade passou a ser interpretar a conversa realizada pelo Arthur e transformar linguagem natural em dados estruturados.

A arquitetura final ficou da seguinte forma:
```
Arthur
    │
    ▼
WF - Extrair Perfil
    │
    ▼
AI Agent (Extrator)
    │
    ▼
Edit Fields
    │
    ▼
Execute Sub-workflow
    │
    ▼
WF - Cadastro de Aluno
    │
    ▼
Google Sheets
```
Com essa alteração, o Arthur deixou de interpretar e cadastrar diretamente o aluno.

Agora ele apenas conversa normalmente.

Toda a lógica de interpretação e cadastro ficou isolada em workflows especializados.

Essa mudança tornou a arquitetura muito mais organizada, reutilizável e escalável.

---

### AI Agent 

O AI Agent deixou de ser um professor de inglês.

Dentro deste Workflow ele passou a exercer apenas uma função:

Extrator de Dados

Foi criado um novo System Prompt extremamente objetivo.

Seu papel é:

analisar o texto recebido;
identificar as informações do aluno;
entregar apenas dados estruturados.

Ele não deve:

conversar;
responder perguntas;
explicar o que fez;
escrever textos.

Sua única responsabilidade é extrair informações.

---

### Structured Output Parser

Durante o desenvolvimento foi introduzida uma nova ferramenta do n8n:

Structured Output Parser
Finalidade

Forçar o AI Agent a responder obrigatoriamente seguindo um formato pré-definido.

Ao invés de responder livremente:
```
Olá!

Seu nome é Mariane...
```
O AI passa a responder obrigatoriamente:
```
{
  "nome": "...",
  "nivel": "...",
  "objetivo": "...",
  "area": "...",
  "metodo": "..."
}
```
---

### Auto-Fix Format

Também foi ativada a opção:

Sua finalidade é tentar corrigir automaticamente pequenas falhas no formato retornado pelo modelo.

Exemplo:

Se o modelo responder:
```
Claro!

{
...
}
```
ou utilizar Markdown:

```json
{
...
}
```
o Parser tenta remover essas informações antes de entregar o resultado.

--- 

###  Problema encontrado

Ao executar o Workflow surgiu o erro:
```
A Model sub-node must be connected and enabled
```
Após investigação descobrimos que o próprio Structured Output Parser possui uma entrada obrigatória chamada:
```
Model *
```
Essa entrada exige um Chat Model exclusivo para o Parser.

Foi necessário adicionar um segundo nó:

Groq Chat Model

ligado diretamente ao Structured Output Parser.

A estrutura final ficou assim:
```
When Executed by Another Workflow
                │
                ▼
             AI Agent
            │         │
            │         ▼
            │   Groq Chat Model
            │
            ▼
Structured Output Parser
            │
            ▼
      Groq Chat Model
```
Após essa alteração o erro desapareceu.

---

## Estado atual do projeto

Atualmente o Workflow já consegue:

✔ Utilizar Structured Output.

✔ Validar automaticamente o formato da resposta.

✔ Gerar JSON estruturado.

✔ Corrigir automaticamente pequenas falhas de formatação.

Entretanto o Workflow ainda não está recebendo corretamente o conteúdo da conversa durante os testes isolados.

Esse será o próximo passo do desenvolvimento.

---

# Dia 5

**Data:** 

29/07/2026

**Tempo investido: 3h30**

---

**Continuação do objetivo do dia anterior, ocorreram alguns erros e não conseguir chegar ao resultado esperado.**

---

## Desenvolvimento do WF - Extrair Perfil


Inicialmente ele foi desenvolvido utilizando um Manual Trigger, permitindo testar seu funcionamento de forma isolada, sem depender do Workflow principal do Arthur.

Durante esse processo foram utilizados os seguintes componentes:

- Manual Trigger
- Edit Fields (simulação da conversa)
- AI Agent
- Groq Chat Model
- Structured Output Parser
- Edit Fields (organização da saída)

Após diversos testes foi confirmado que o Workflow era capaz de transformar corretamente uma conversa em um objeto JSON estruturado contendo:

- Nome
- Nível
- Objetivo
- Área
- Método

Somente após essa validação o Manual Trigger foi removido e substituído novamente pelo nó When Executed by Another Workflow.

Depois da validação individual do Extrator foi realizada sua integração com o Workflow de Cadastro.

Foi utilizado o nó:

**Execute Sub-workflow**

Esse nó passou a enviar automaticamente os dados extraídos para o Workflow:

**WF - Cadastro de Aluno**

Durante os testes foi confirmado que todos os campos estavam sendo transmitidos corretamente.

A partir dessas informações o Workflow gerou automaticamente:

- idAluno (UUID);
- dataCadastro;
- ultimoAcesso;
- status;
- versão do perfil.

Em seguida realizou o cadastro no Google Sheets com sucesso.

---

Após a integração completa foi identificado um detalhe importante.

Na planilha a data estava correta, mas o horário estava com outro fuso, tive que alterar o código no Workflow WF - Cadastro de Aluno

Antes:
```
const agora = new Date().toISOString();

aluno.dataCadastro = agora;
aluno.ultimoAcesso = agora;
```

Depois: 
```
const agora = new Date();

const dataHoraBrasil = agora
	.toLocaleString("sv-SE", {
		timeZone: "America/Sao_Paulo",
		hour12: false,
	})
	.replace(",", "");

aluno.dataCadastro = dataHoraBrasil;
aluno.ultimoAcesso = dataHoraBrasil;
```
---

## Testes realizados

Foram realizados testes completos simulando novos alunos.

Fluxo validado:

- Usuário conversa normalmente com o Arthur.
- Arthur coleta todas as informações necessárias.
- Arthur chama o Workflow WF - Extrair Perfil.
- O Workflow interpreta toda a conversa utilizando IA.
- Os dados são organizados em formato estruturado.
- O Workflow chama automaticamente o WF - Cadastro de Aluno.
- O Cadastro gera UUID e datas.
- O Cadastro grava todas as informações no Google Sheets.

Todos os testes foram concluídos com sucesso.

---

## Resultado Final da Sprint

Ao término desta etapa o Professor Arthur passou a possuir sua primeira funcionalidade completa.

Agora ele é capaz de:

- conversar naturalmente com um novo aluno;
- identificar automaticamente informações importantes durante a conversa;
- estruturar essas informações utilizando Inteligência Artificial;
- cadastrar automaticamente o aluno;
- gerar identificadores únicos;
- registrar datas padronizadas;
- armazenar permanentemente todas as informações em sua base de dados.

Essa foi a primeira funcionalidade completa do projeto, envolvendo conversa, inteligência artificial, regras de negócio e persistência de dados.

---

# Dia 6

**Data:** 

30/07/2026

**Tempo investido: 6h45**

---

## O que foi desenvolvido

### Mudanças

Durante o desenvolvimento foi decidido abandonar definitivamente a utilização do sessionId como identificador do aluno, ocorreu muitos erros porque não tinha como usar ele como identificador único. 

Novo padrão adotado:

Identificação permanente:

Token
Código de Segurança

O sessionId deixa de representar o aluno e poderá ser utilizado futuramente apenas para identificar sessões temporárias de conversa.

---

### Conclusão do Workflow de Autenticação

Finalizado o WF - Autenticacao.

Implementações:

Busca do aluno pelo Token.
Validação do Código de Segurança.
Retorno padronizado.
Tratamento para Token inexistente.
Tratamento para Código incorreto.

Durante os testes foi necessário:

ativar Convert types where required nos nós IF;
ajustar diferenças entre String e Number;
validar todos os cenários.
Testes realizados

✔ Token válido + Código válido

✔ Token inexistente

✔ Código incorreto

Todos funcionando corretamente.

---

### Alterações na estrutura da planilha

Foi realizada uma reorganização completa da aba Alunos.

Campos atuais:
```
IdAluno
Token
CodigoSeguranca
Nome
Nivel
Objetivo
Area
Metodo
EstadoAtual
Status
DataCadastro
UltimoAcesso
UltimaAula
TotalAulas
Idioma
VersaoPerfil
Observacoes
```
Também foi padronizada a nomenclatura das colunas removendo acentos para facilitar integrações futuras.

---

### Nova Arquitetura Definida

O projeto passa a possuir dois agentes principais.

**Arthur Core**

Responsável por:

controlar todo o fluxo do sistema;
identificar se o aluno possui cadastro;
realizar autenticação;
conduzir o processo de cadastro;
gerar Token e Código;
chamar os workflows necessários;
encaminhar o aluno autenticado ao Professor Arthur.

O Arthur Core NÃO ensinará inglês.

---

**Professor Arthur**

Responsável exclusivamente por:

ensinar inglês;
corrigir exercícios;
realizar conversação;
adaptar as aulas conforme o perfil do aluno.

O Professor Arthur deixa de possuir responsabilidades relacionadas a:

cadastro;
autenticação;
banco de dados;
segurança.

---

### Reaproveitamento dos Workflows

Foi decidido manter e reutilizar os workflows já desenvolvidos.

Os workflows existentes passam a ser utilizados pelo Arthur Core.

Reutilizados:

WF - Extrair Perfil
WF - Cadastro de Aluno
WF - Autenticacao

Nenhum deles será recriado.

Apenas mudarão de responsável (quem faz a chamada).

---

## Próximos objetivos

Sprint seguinte:

concluir o Arthur Core;
mover completamente o fluxo de cadastro para o Arthur Core;
integrar o Professor Arthur apenas após autenticação ou cadastro;
posteriormente realizar integração com Telegram.

---

# Dia 7

**Data:** 

31/07/2026

**Tempo investido: 3h50**

---

## Objetivo do dia

Concluir a arquitetura do Arthur, validar o fluxo completo de autenticação, cadastro e preparar o Arthur para iniciar as aulas.

---

## Arquitetura

A arquitetura do projeto.
```
Gateway
↓
Arthur Core
↓
Autenticação / Cadastro
↓
Professor Arthur
```
Responsabilidades:

### Gateway

- ponto único de entrada para qualquer plataforma.

### Arthur Core

Foi decidido que o Arthur Core será responsável exclusivamente pelo controle da navegação do sistema.

- controla toda a navegação;
- identifica novos alunos;
- identifica alunos cadastrados;
- realiza autenticação;
- realiza cadastro;
- decide quais workflows executar.

### Professor Arthur

- responsável exclusivamente pelo ensino;
utilizará o perfil do aluno para personalizar as aulas.

Essa separação facilita a manutenção e futuras expansões.

---

## Memória

Foi adicionada uma Simple Memory ao AI Agent do Arthur Core.

Configuração:
```
Session Key: {{ $json.sessionId }}
Context Window Length: 10
```
**Objetivo:**

- manter o contexto durante a conversa;
- evitar que o Arthur reinicie o fluxo a cada mensagem.

Foi decidido que essa memória será utilizada apenas para conversas temporárias.

A lógica permanente continuará sendo implementada utilizando o campo EstadoAtual.

---

## Prompt do Arthur Core

O prompt foi completamente reestruturado.

Foram adicionadas regras para:

- interpretar respostas naturais;
- aceitar diversas formas de responder "sim" e "não";
- realizar apenas uma pergunta por vez;
- nunca solicitar Token e Código juntos;
- nunca utilizar ferramentas com informações incompletas;
- utilizar WF - Autenticacao somente quando possuir Token e Código.

Também foram adicionadas restrições para impedir que o Arthur invente informações.

---

## Fluxo de cadastro

Foi validado o fluxo completo para novos alunos.

O Arthur conseguiu:

- solicitar nome;
- solicitar nível;
- solicitar objetivo;
- solicitar área;
- solicitar método de estudo.

Após receber todas as informações:

- executou o WF - Extrair Perfil;
- executou o WF - Cadastro de Aluno;
- salvou corretamente na planilha;
- recebeu o Token e Código de Segurança gerados;
- informou corretamente esses dados ao usuário.

---

## Correções realizadas

Durante os testes foram encontrados e corrigidos diversos problemas.

### Correção 1

O Arthur reiniciava a conversa após receber o Token.

**Causa:**

Ausência de memória.

**Solução:**

Implementação da Simple Memory.

### Correção 2

O Arthur tentava autenticar antes de possuir Token e Código.

**Solução:**

Alteração do prompt obrigando a autenticação somente após possuir ambos os dados.

### Correção 3

O Arthur inventava Token e Código.

**Solução:**

O workflow passou a retornar os valores reais para o AI Agent.

## Correção 4

O Arthur não reconhecia algumas respostas naturais.

Exemplo:

"Já sou aluno"

**Solução:**

Foram adicionadas diversas formas de respostas equivalentes ao prompt.

---

## Testes realizados

### Teste 1 — Aluno já cadastrado

Fluxo testado:

- identificação de aluno existente;
- solicitação do Token;
- solicitação do Código de Segurança;
- autenticação;
- continuação da conversa.

Resultado:

✅ Aprovado.

### Teste 2 — Token inválido

Fluxo testado:

- tentativa de autenticação com dados incorretos.

Resultado:

✅ O Arthur identificou a falha e solicitou novas informações corretamente.

### Teste 3 — Interpretação de respostas naturais

Foram testadas respostas como:

- Já utilizo
- Sou aluno
- Tenho cadastro
- Já utilizei o Arthur

Resultado:

✅ O Arthur conseguiu interpretar corretamente todas as respostas sem exigir apenas "Sim" ou "Não".

### Teste 4 — Cadastro de novo aluno

Fluxo validado:

- perguntas realizadas uma por vez;
- coleta de todas as informações;
- execução do WF - Extrair Perfil;
- execução do WF - Cadastro de Aluno;
- gravação na planilha;
- retorno do Token e Código de Segurança.

Durante o primeiro teste foi identificado um problema onde o modelo inventava o Token e o Código de Segurança.

Após ajustes no retorno do workflow, o problema foi resolvido.

Resultado final:

✅ O Arthur passou a informar exatamente os dados gerados pelo sistema.

---

## Decisão

Foi decidido que:

- Token será o identificador permanente do aluno;
- Código de Segurança será utilizado para autenticação;
- SessionId continuará sendo utilizado apenas para memória temporária da conversa;
- EstadoAtual será responsável futuramente pela continuidade das aulas entre diferentes plataformas.

---

## Situação atual do projeto

Funcionalidades disponíveis:

- cadastro de novos alunos;
- autenticação utilizando Token e Código de Segurança;
- geração automática de Token;
- geração automática de Código de Segurança;
- armazenamento das informações no Google Sheets;
- memória temporária utilizando SessionId;
- arquitetura modular baseada em workflows independentes;
- separação das responsabilidades entre Arthur Core e Professor Arthur.

---

## Conclusão

A partir deste momento, a infraestrutura principal do sistema encontra-se funcional e organizada, permitindo que as próximas etapas sejam focadas na inteligência pedagógica, personalização das aulas e evolução da experiência do aluno.

Hoje o Arthur deixou de ser apenas um agente conversacional e passou a possuir uma arquitetura modular, preparada para crescer, integrar novas plataformas e evoluir de forma organizada ao longo do desenvolvimento.

---

## Próximos objetivos

A próxima etapa do projeto terá foco na experiência de aprendizagem.

Os principais objetivos serão:

- integrar completamente o Professor Arthur;
- iniciar automaticamente a aula após autenticação;
- utilizar os dados do cadastro para personalizar o ensino;
- implementar a continuidade das aulas utilizando o campo EstadoAtual;
- evitar perguntas repetidas para alunos já cadastrados;
- iniciar a implementação da memória permanente do aluno.

---

# Dia 8

**Data:** 

03/08/2026

**Tempo investido: 2h00**

---

## Objetivo

Concluir a integração entre o Arthur Core e o Professor Arthur, finalizar o fluxo de início das aulas, implementar o salvamento do progresso do aluno e corrigir diversos problemas estruturais da arquitetura.

---

## O que foi desenvolvido

### Arquitetura

A arquitetura do projeto foi reorganizada para separar as responsabilidades de cada componente.

Estrutura atual:
```
Arthur Core
|
├── WF - Autenticacao
├── WF - Buscar Perfil
├── WF - Extrair Perfil
└── WF - Iniciar Aula
            │
            ▼
    Professor Arthur
            │
            └── WF - Salvar Progresso
```
Agora cada workflow possui uma única responsabilidade, facilitando manutenção, testes e futuras expansões.

---

### Arthur Core

O prompt do Arthur Core foi completamente reestruturado.

- Separação entre usuários cadastrados e novos alunos.
- Controle completo do fluxo de autenticação.
- Controle completo do fluxo de cadastro.
- Obrigatoriedade de fazer apenas uma pergunta por vez.
- Uso correto da memória da conversa.
- Encaminhamento transparente para o Professor Arthur.
- Correção do problema em que o Core fazia múltiplas perguntas simultaneamente.

O Core passou a atuar exclusivamente como controlador de fluxo.

---

### Professor Arthur

O prompt do Professor Arthur foi completamente reescrito.

Agora ele:

- recebe automaticamente todas as informações do aluno;
- nunca pergunta novamente dados já conhecidos;
- personaliza exemplos conforme área profissional;
- adapta o conteúdo ao nível do aluno;
- continua exatamente do ponto onde a última aula terminou;
- mantém um estilo de aula conversacional;
- corrige erros de forma didática;
- trabalha em pequenos blocos de aprendizagem.

---

### Primeiro Acesso

Foi implementado o comportamento específico para novos alunos.

Quando:

novoAluno = true

o Professor Arthur:

- lembra o aluno para guardar Token e Código de Segurança;
- apresenta essas informações apenas como um lembrete;
- inicia imediatamente a primeira aula.

Quando:

novoAluno = false

o Professor Arthur nunca menciona Token nem Código de Segurança.

---

### Workflow "WF - Iniciar Aula"

Foi criado um novo workflow responsável por preparar os dados antes da primeira aula.

Fluxo:
´´´
Recebe Token
↓
Busca Perfil
↓
Valida aluno
↓
Prepara dados
↓
Chama Professor Arthur
´´´
Este workflow centraliza toda a preparação das informações utilizadas pelo Professor Arthur.

---

### Workflow "WF - Salvar Progresso"

Foi criado o primeiro sistema de persistência do aprendizado.

Estrutura:
´´´
When Executed by Another Workflow
↓
Google Sheets
(Update Row)
↓
Edit Fields
´´´
Campos atualizados:

EstadoAtual
UltimaAula
TotalAulas
UltimoAcesso

Foi validado com sucesso utilizando dados simulados.

Resultado:

- atualização correta da planilha;

retorno:
´´´
{
  "sucesso": true
}
´´´
---

### Integração do Professor Arthur

Foi criada a Tool:
´´´
Call WF - Salvar Progresso
´´´
O Professor Arthur agora está preparado para registrar automaticamente a evolução do aluno ao concluir conteúdos importantes.

Também foi adicionada uma nova seção ao prompt definindo exatamente quando essa ferramenta deve ser utilizada.

---

## Correções Realizadas

Durante esta etapa foram corrigidos diversos problemas:

- repetição de perguntas do cadastro;
- múltiplas perguntas em uma única resposta;
- perda de contexto entre Arthur Core e Professor Arthur;
- erro de Session ID da memória;
- passagem incorreta dos dados do aluno;
- estrutura dos objetos retornados pelos workflows;
- repetição do Token e Código de Segurança;
- integração entre cadastro e início da primeira aula.

---

## Limitações Encontradas

Durante os testes foi atingido o limite de uso da API da Groq.

Foram identificados dois tipos de limite:

- TPD (Tokens Per Day)
- TPM (Tokens Per Minute)

Durante o desenvolvimento será necessário controlar o ritmo dos testes ou futuramente utilizar uma estratégia de modelos diferentes para desenvolvimento e produção.

---

## Situação Atual do Projeto

- Arquitetura modular
- Arthur Core
- Professor Arthur
- Cadastro
- Autenticação
- Busca de Perfil
- Início da Aula
- Persistência do progresso
- Integração entre workflows

## Próximos objetivos

Concluir a integração definitiva entre o Professor Arthur e o workflow WF - Salvar Progresso, validando que o progresso seja salvo automaticamente ao final de cada bloco de aprendizagem, garantindo que o aluno possa continuar exatamente do ponto onde parou na próxima sessão.

Ideia de um super amigo: E :black_heart:
```
Iniciar a implementação em Python para realizar o cadastro e a autenticação dos alunos.
```
---

# Dia 9

**Data:** 

04/08/2026

**Tempo investido: 1h40**

---

## Encerramento da Versão 1

Hoje concluí oficialmente a primeira versão funcional do Arthur.

Todos os objetivos definidos para a arquitetura baseada em n8n foram alcançados.

A implementação conta com:

- Arthur Core
- Professor Arthur
- Cadastro
- Autenticação
- Memória
- Continuação das aulas
- Salvamento de progresso

Toda a arquitetura foi arquivada para futuras consultas.

---

## Início da Versão 2

Após a conclusão da V1, iniciei o planejamento da nova arquitetura.

A principal mudança será a substituição do Arthur Core por uma implementação em Python.

O Professor Arthur continuará responsável pelas aulas.

O objetivo desta nova versão é aprofundar meus conhecimentos em Python, banco de dados, arquitetura de software e integração com Inteligência Artificial.

Hoje foi criado o documento:

Projeto-V2-Python.md
