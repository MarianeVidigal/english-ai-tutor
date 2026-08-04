# WF - Cadastro Aluno

## Objetivo

Responsável por persistir o cadastro de novos alunos na base de dados.

Este workflow recebe um perfil já validado e realiza o armazenamento definitivo das informações.

---

## Responsabilidades

- Salvar o novo aluno na base de dados.
- Registrar o Token.
- Registrar o Código de Segurança.
- Inicializar os dados do aluno.
- Retornar a confirmação do cadastro.

---

## Entrada

Recebe:

- IdAluno
- Token
- Código de Segurança
- Nome
- Nível
- Objetivo
- Área
- Método de Estudo
- Idioma
- Versão do Perfil

---

## Processamento

1. Receber os dados do novo aluno.
2. Salvar as informações na base de dados.
3. Inicializar o progresso do aluno.
4. Confirmar o cadastro.

---

## Saída

Retorna:

- Cadastro realizado com sucesso.
- Perfil armazenado.
- Token.
- Código de Segurança.

---

## Banco de Dados

Google Sheets

Tabela:

Alunos

---

## Workflows relacionados

- WF - Extrair Perfil
