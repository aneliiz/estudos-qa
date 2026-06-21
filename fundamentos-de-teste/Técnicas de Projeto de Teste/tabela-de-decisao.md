# Tabela de Decisão

A Tabela de Decisão é uma técnica de teste usada para validar sistemas que possuem múltiplas condições e regras de negócio.

Ela organiza:

- Condições (entradas)
- Ações (saídas)

> Testar todas as combinações possíveis de regras de forma organizada.

---

## Objetivo

Garantir que:

- Todas as combinações de condições sejam testadas  
- As regras de negócio estejam corretas  
- Nenhum cenário seja esquecido  

---

## Quando usar?

Use tabela de decisão quando:

- Existem várias regras combinadas  
- Há muitas condições (if/else)  
- O comportamento depende de múltiplas variáveis  

---

## Exemplo 1 - Sistema de Login

### Condições:

- Usuário correto?
- Senha correta?

---

### Tabela de Decisão:

| Regra | Usuário válido | Senha válida | Resultado |
|------|---------------|-------------|----------|
| 1 | Sim | Sim | Acesso permitido |
| 2 | Sim | Não | Acesso negado |
| 3 | Não | Sim | Acesso negado |
| 4 | Não | Não | Acesso negado |

---

### Casos de Teste:

| Usuário | Senha | Resultado Esperado |
|--------|------|------------------|
| correto | correto | Login realizado |
| correto | errado | Erro |
| errado | correto | Erro |
| errado | errado | Erro |

---

## Exemplo 2 - Frete em E-commerce

### Regras:

- Compra acima de R$100 → frete grátis  
- Cliente VIP → frete grátis  

---

### Condições:

- Valor > 100?
- Cliente VIP?

---

### Tabela:

| Regra | Valor > 100 | Cliente VIP | Resultado |
|------|-------------|------------|----------|
| 1 | Sim | Sim | Frete grátis |
| 2 | Sim | Não | Frete grátis |
| 3 | Não | Sim | Frete grátis |
| 4 | Não | Não | Frete pago |

---

## Exemplo 3 - Aprovação de Empréstimo

### Regras:

- Renda alta  
- Nome limpo  

---

### Tabela:

| Regra | Renda alta | Nome limpo | Resultado |
|------|------------|------------|----------|
| 1 | Sim | Sim | Aprovado |
| 2 | Sim | Não | Negado |
| 3 | Não | Sim | Negado |
| 4 | Não | Não | Negado |

---

## Passo a Passo

1. Identificar todas as condições  
2. Identificar possíveis ações  
3. Criar todas as combinações  
4. Montar a tabela  
5. Criar casos de teste  

---

## Comparação com Outras Técnicas

| Técnica | Foco |
|--------|------|
| Partição de Equivalência | Grupos de dados |
| Valor Limite | Bordas |
| Tabela de Decisão | Combinação de regras |

---
A **Tabela de Decisão** é essencial para testar sistemas com múltiplas regras porque

- Garante cobertura total  
- Evita falhas em combinações  
- Organiza cenários complexos  

É muito usada em sistemas financeiros, e-commerce e validações de negócio.