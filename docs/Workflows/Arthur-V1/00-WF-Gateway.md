# WF - Gateway

## Objetivo

Responsável por receber todas as mensagens enviadas pelo usuário e encaminhá-las para o Arthur Core.

Este workflow é o ponto de entrada da aplicação.

---

## Responsabilidades

- Receber a mensagem do usuário.
- Iniciar a conversa.
- Encaminhar todas as mensagens para o Arthur Core.
- Retornar ao usuário a resposta gerada pelo sistema.

---

## Entrada

Recebe:

- Mensagem do usuário

---

## Processamento

1. Recebe a mensagem.
2. Encaminha para o Arthur Core.
3. Aguarda a resposta.
4. Retorna a resposta ao usuário.

---

## Saída

Resposta final da conversa.

---

## Workflows relacionados

- Arthur Core
