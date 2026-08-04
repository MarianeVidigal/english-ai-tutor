# Projeto - Arthur V2 (Python)

A primeira versão provou que a arquitetura funcionava.

A segunda versão tem como objetivo construir uma implementação mais robusta, desacoplada e escalável utilizando Python.

---

## Objetivo

A Versão 2 do Arthur tem como principal objetivo substituir o Arthur Core desenvolvido em n8n por uma implementação própria em Python.

A arquitetura pedagógica construída durante a Versão 1 será preservada.

O Professor Arthur continuará sendo responsável pelo ensino de inglês.

A principal mudança será a forma como o sistema realiza:

- Cadastro de alunos
- Autenticação
- Recuperação de perfil
- Gerenciamento de sessões
- Persistência dos dados

---

## Motivação

Durante o desenvolvimento da Versão 1 foi possível validar toda a lógica de funcionamento do sistema utilizando exclusivamente o n8n.

Com essa experiência, tornou-se possível evoluir a arquitetura para uma solução híbrida, utilizando Python para toda a camada de negócio e mantendo a Inteligência Artificial apenas como responsável pelo ensino.

Essa mudança permitirá maior controle sobre o sistema, melhor organização do código e maior facilidade para futuras integrações.

---

## Objetivos da Versão 2

### Cadastro

O cadastro será desenvolvido em Python.

Será responsável por:

- validar dados;
- gerar Token;
- gerar Código de Segurança;
- criar o perfil do aluno.

---

### Autenticação

A autenticação será realizada em Python.

Receberá:

- Token
- Código de Segurança

Retornará:

- Perfil completo do aluno.

---

### Banco de Dados

Substituir a persistência baseada em Google Sheets por um banco de dados.

Inicialmente será utilizado:

SQLite

Posteriormente será possível migrar para:

- PostgreSQL
- MySQL
- SQL Server

sem alterar a arquitetura principal.

---

### Professor Arthur

O Professor Arthur continuará existindo.

Seu funcionamento permanecerá praticamente inalterado.

Ele continuará responsável por:

- ensinar inglês;
- adaptar as aulas;
- corrigir exercícios;
- acompanhar a evolução do aluno.

O Professor Arthur deixará de depender do Arthur Core em n8n e passará a receber os dados diretamente da camada Python.

---

## Nova Arquitetura
```
Usuário
↓
Python
↓
Cadastro
↓
Banco de Dados
↓
Autenticação
↓
Professor Arthur
```
---

## Tecnologias previstas

- Python
- SQLite
- SQLAlchemy (caso necessário)
- FastAPI (futuramente)
- n8n
- Inteligência Artificial
- GitHub

---

## Objetivos pessoais

Além da evolução do Arthur, esta versão também representa uma nova etapa da minha formação profissional.

Durante esta implementação pretendo desenvolver conhecimentos em:

- Python
- Arquitetura de Software
- Banco de Dados
- APIs
- Backend
- Integração entre aplicações
- Engenharia de Software

---

## Meta da Versão 2

Ao final desta versão, o Arthur deverá ser capaz de:

- cadastrar novos alunos;
- autenticar alunos existentes;
- gerenciar os dados do aluno em banco de dados;
- iniciar automaticamente o Professor Arthur;
- manter a continuidade das aulas.

Toda essa lógica será controlada pelo código Python, tornando a arquitetura mais modular e independente.
