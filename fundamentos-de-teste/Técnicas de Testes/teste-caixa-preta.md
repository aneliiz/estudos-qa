# Teste de Caixa Preta

O Teste de Caixa Preta é uma técnica de teste onde o testador não possui acesso ao código-fonte nem conhecimento da estrutura interna do sistema.

O sistema é tratado como uma "caixa fechada", onde:

- São fornecidas entradas
- E analisadas as saídas

O objetivo é verificar se o sistema funciona corretamente de acordo com os requisitos.

---

## Objetivo

- Atender aos requisitos funcionais
- Responder corretamente as entradas do usuário
- Se comporte conforme o esperado
- Não apresente falhas visíveis ao usuário

---

## Características

- Não exige conhecimento de programação  
- Baseado em requisitos e especificações  
- Foco no comportamento externo  
- Simula o uso real do sistema  
- Pode ser executado por QA ou usuários  

---

## Exemplo

### Sistema: Login

**Entrada:**

Usuário: ana123
Senha: 123456


**Resultado esperado:**

Acesso permitido ao sistema



O testador não precisa saber como o sistema valida o login internamente — apenas verifica se o comportamento está correto.

---

## Casos de Teste

| Usuário | Senha | Resultado Esperado |
|--------|------|------------------|
| ana123 | 123456 | Login realizado |
| ana123 | 000000 | Senha incorreta |
| errado | 123456 | Usuário inválido |
| vazio | vazio | Campos obrigatórios |

---

## Vantagens vs Desvantagens

| Vantagem | Desvantagem |
|----------|------------|
| Simula uso real | Não detecta erros lógicos ocultos |
| Qualquer um pode fazer | Menos eficiente (cobre menos caminho) |
| Não requer programação | Requer bom conhecimento de requisitos |
| Rápido para entender | Dados limitados para debug |

**Ideal para:** QAs e testadores manuais  
**Combinar com:** Caixa Branca para cobertura total

---

## Técnicas de Teste

### Particionamento de Equivalência

Divide os dados em grupos (classes) para reduzir a quantidade de testes.

**Exemplo: Campo idade**

- 0–120 -> válido  
- < 0 -> inválido  
- > 120 -> inválido  

Em vez de testar todos os valores, testamos representantes de cada grupo.

---

### Análise de Valor Limite

Foca nos valores próximos aos limites, onde erros são mais comuns.

**Exemplo: idade entre 18 e 60**

- 17 X
- 18 ok
- 19 ok
- 59 ok
- 60 ok 
- 61 X

---

### Tabela de Decisão

Usada quando há várias combinações de regras.

| Usuário Correto | Senha Correta | Resultado |
|----------------|--------------|-----------|
| Sim | Sim | Acesso permitido |
| Sim | Não | Acesso negado |
| Não | Sim | Acesso negado |
| Não | Não | Acesso negado |

---

### Teste de Estado

Valida mudanças de estado do sistema.

**Exemplo: Pedido**

Criado -> Pago -> Enviado -> Entregue


Testa se as transições ocorrem corretamente.

---

### Teste de Casos de Uso

Baseado nos fluxos reais do usuário.

**Exemplo:**

1. Usuário acessa a tela de login  
2. Digita usuário e senha  
3. Clica em "Entrar"  
4. Sistema valida e retorna resposta  

---

## Vantagens

- Não exige conhecimento técnico  
- Representa o comportamento do usuário  
- Fácil de implementar  
- Valida requisitos do sistema  
- Pode ser aplicado em qualquer nível de teste  

---

## Desvantagens

- Não testa a lógica interna do código  
- Pode deixar caminhos não testados  
- Dependência da qualidade dos requisitos  
- Dificuldade em identificar a causa dos erros  

---

## Quando usar?

- Testes funcionais  
- Testes de sistema  
- Testes de aceitação  
- Validação de requisitos  

---

## Comparação com Outros Tipos

| Tipo | Foco | Acesso ao Código |
|------|------|----------------|
| Caixa Preta | Comportamento | Não |
| Caixa Branca | Estrutura interna | Total |
| Caixa Cinza | Integração | Parcial |

---