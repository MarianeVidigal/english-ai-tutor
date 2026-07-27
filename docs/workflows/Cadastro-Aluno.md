# Workflow - Cadastro de Aluno

## Objetivo

Cadastrar um novo aluno no English AI Tutor.

---

## Entrada

- SessionId
- Nome
- Nível
- Objetivo
- Área
- Método de aprendizagem

---

## Processamento

1. Verificar se o SessionId já existe.
2. Se existir, retornar o cadastro existente.
3. Se não existir:
   - Gerar UUID.
   - Registrar DataCadastro.
   - Registrar UltimoAcesso.
   - Definir Status = Ativo.
   - Definir VersaoPerfil = 1.
   - Salvar no Google Sheets.

---

## Saída

```json
{
  "sucesso": true,
  "idAluno": "UUID",
  "novoCadastro": true
}
```

---

## Dependências

- Google Sheets
- UUID Generator

---

## Futuras melhorias

- Cadastro via Google Login.
- Cadastro via GitHub.
- Cadastro via Microsoft.
- Migração para PostgreSQL.
