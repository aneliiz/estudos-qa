# O que é Testes Funcionais

É o tipo de teste que verifica se o sistema está funcionando exatamente como deveria, de acordo com os requisitos.

Ele valida **funções do sistema**.

---

O objetivo é garantir que cada funcionalidade:

- Está funcionando corretamente
- Segue os requisitos definidos
- Entrega o resultado esperado para o usuário

> “O sistema faz o que deveria fazer?”

---

## Como funciona na prática

### 1. Receber o requisito

- História de usuário  
- Requisito funcional  
- Demanda do cliente  

Exemplo:

> Como usuário,

> Quero fazer login,

> Para acessar minha conta


---

### 2. Entender a regra de negócio

- O que deve acontecer?
- O que não deve acontecer?
- Quais são os cenários possíveis?

---

### 3. Criar casos de teste

Transformar o requisito em testes práticos.

Exemplo:

**Caso de teste: Login válido**

- Inserir email válido
- Inserir senha válida
- Clicar em login

Resultado esperado:
- Usuário entra no sistema

---

### 4. Criar cenários (por exemplo o BDD)

**Cenário: Login com sucesso**

>Dado que o usuário está na tela de login

>Quando ele insere dados válidos

>Então ele deve acessar sua conta

---


### 5. Executar os testes

- Manual (clicando na aplicação)
- Automatizado (com código)

---

### 6. Validar o resultado

 Resultado esperado X resultado real

Se for igual -> PASSOU  
 Se for diferente -> BUG  

---

## Exemplos de Testes Funcionais

### Login
- Validar login com dados corretos
- Validar erro com dados inválidos

### Cadastro
- Criar conta com dados válidos
- Bloquear campos obrigatórios vazios

---

## Ferramentas Recomendadas

| Ferramenta | Tipo | Linguagem |
|-----------|------|-----------|
| Selenium | Autom Web | Múltiplas |
| Cypress | Autom Web | JavaScript |
| Postman | Autom API | N/A |
| Robot Framework | Autom | Python |
| Jira | Rastreamento | Web |

> Para começar: Usar testes manuais, depois evoluir para automação

### Carrinho de compras
- Adicionar produto
- Remover produto
- Calcular total corretamente

---
