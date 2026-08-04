# WF - Autenticação

## Objetivo

Validar o Token e o Código de Segurança do aluno.

Após autenticar, iniciar automaticamente a aula correspondente.

---

## Responsabilidades

- Validar credenciais.
- Buscar perfil.
- Encaminhar para o início da aula.

---

## Entrada

Recebe:

- Token
- Código de Segurança

---

## Processamento

1. Buscar Perfil.
2. Validar credenciais.
3. Chamar WF - Iniciar Aula.

---

## Saída

Resposta produzida pelo Professor Arthur.

---

## Workflows relacionados

- WF - Buscar Perfil
- WF - Iniciar Aula
