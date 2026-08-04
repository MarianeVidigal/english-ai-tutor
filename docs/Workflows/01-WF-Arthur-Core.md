# Arthur Core

## Objetivo

Controlar todo o fluxo de navegação do sistema Arthur.

Sua função é decidir qual workflow deverá ser executado em cada etapa da conversa.

---

## Responsabilidades

- Identificar se o usuário possui cadastro.
- Solicitar Token e Código de Segurança.
- Coletar informações para cadastro.
- Executar autenticação.
- Executar cadastro.
- Iniciar aulas.
- Controlar o fluxo completo da conversa.

---

## Entrada

Recebe:

- Mensagem do usuário.

---

## Processamento

Decide qual workflow deverá ser executado:

- WF - Autenticação
- WF - Extrair Perfil
- WF - Iniciar Aula

---

## Saída

Retorna a resposta produzida pelos workflows chamados.

---

## Workflows relacionados

- WF - Autenticação
- WF - Extrair Perfil
- WF - Iniciar Aula
