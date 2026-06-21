# Teste Baseado em Estado


O Teste Baseado em Estado é uma técnica de teste que valida o comportamento do sistema com base nos estados em que ele pode estar e nas transições entre esses estados.

> O sistema muda de estado conforme ações/eventos, e cada mudança precisa ser testada.

---

## Objetivo

Garantir que:

- O sistema transite corretamente entre estados  
- Estados inválidos não sejam acessados  
- Regras de transição sejam respeitadas  
- O comportamento em cada estado esteja correto  

---

## O que é um "estado"?

Um estado representa uma situação em que o sistema pode estar.

Exemplo:

- Pedido: Criado, Pago, Enviado, Entregue  
- Usuário: Logado, Deslogado, Bloqueado  
- Sistema: Ativo, Inativo, Em manutenção  

---

## Estrutura Básica

Um teste baseado em estado envolve:

- **Estados** → Situações possíveis  
- **Eventos** → Ações que causam mudanças  
- **Transições** → Mudanças de um estado para outro  

---

## Exemplo 1 - Pedido em E-commerce

### Estados:

- Criado  
- Pago  
- Enviado  
- Entregue  

---

### Transições:

| Estado Atual | Evento | Próximo Estado |
|-------------|--------|---------------|
| Criado | Pagamento aprovado | Pago |
| Pago | Pedido enviado | Enviado |
| Enviado | Entrega realizada | Entregue |

---

### Fluxo:

Criado -> Pago -> Enviado -> Entregue

### Casos de Teste:

| Cenário | Estado Atual | Ação | Resultado Esperado |
|--------|-------------|------|------------------|
| Pagamento válido | Criado | Pagar | Vai para Pago |
| Enviar pedido | Pago | Enviar | Vai para Enviado |
| Entregar pedido | Enviado | Entregar | Vai para Entregue |

---

## Exemplo 2 - Login de Usuário

### Estados:

- Deslogado  
- Logado  
- Bloqueado  

---

### Transições:

| Estado Atual | Evento | Próximo Estado |
|-------------|--------|---------------|
| Deslogado | Login correto | Logado |
| Deslogado | 3 tentativas erradas | Bloqueado |
| Bloqueado | Reset senha | Deslogado |

---

### Casos de Teste:

| Cenário | Estado | Ação | Resultado |
|--------|--------|------|----------|
| Login correto | Deslogado | Inserir credenciais | Logado |
| Tentativas erradas | Deslogado | Errar 3x | Bloqueado |
| Reset senha | Bloqueado | Redefinir | Deslogado |

---

## Passo a Passo

1. Identificar todos os estados do sistema  
2. Identificar eventos que causam mudanças  
3. Definir transições válidas  
4. Criar fluxos possíveis  
5. Criar testes para cada transição  

---


## Quando usar?

- Sistemas com workflow (fluxos)  
- E-commerce (pedidos)  
- Sistemas bancários  
- Controle de usuários  
- Aplicações com status  

---

## Comparação com Outras Técnicas

| Técnica | Foco |
|--------|------|
| Partição de Equivalência | Dados |
| Valor Limite | Bordas |
| Tabela de Decisão | Regras |
| Baseado em Estado | Fluxos |

---

O Teste Baseado em Estado é essencial para validar sistemas que possuem fluxos e mudanças de status.

Ele garante que:

- O sistema siga o fluxo correto  
- Não ocorra comportamento inesperado  
- Estados inválidos sejam evitados  

É muito utilizado no mercado e extremamente importante para QA.