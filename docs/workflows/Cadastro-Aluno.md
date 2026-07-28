# Workflow - Cadastro de Aluno

## Objetivo

Responsável por cadastrar um novo aluno no banco de dados (Google Sheets).

Este workflow não conversa diretamente com o usuário.
Ele é executado pelo workflow principal (Arthur) sempre que o agente identifica que possui todas as informações necessárias para criar um novo perfil.

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

### Fluxo do Workflow: WF - Cadastro do Aluno

Fluxo

When Executed by Another Workflow: ( Recebe os dados enviados pelo Workflow principal (Arthur).

▼

Edit Fields: ( Organiza todas as informações recebidas.)

▼

Code: (Executa regras que o Edit Fields não consegue fazer sozinho.)

▼

Google Sheets (Append Row): (Insere uma nova linha na aba)

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

### Próximas melhorias
- Verificar se o aluno já existe.
- Evitar cadastros duplicados.
- Retornar informações ao Arthur.
- Registrar logs.
- Persistir em banco SQL futuramente.

