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


### Próximas melhorias ###
Verificar se o aluno já existe.
Evitar cadastros duplicados.
Retornar informações ao Arthur.
Registrar logs.
Persistir em banco SQL futuramente.

