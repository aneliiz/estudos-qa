### ***Teste de Integração***

### Exemplo:

**Contexto do Sistema:** 

*Sistema de e-commerce com os seguintes módulos:*

1 - Frontend (tela de compra)

2 - Backend (processamento de pedido)

3 - Banco de dados (armazenamento)

4 - API de pagamento (externa)

---

### Fluxo Feliz

Cenário: Usuário finaliza compra com sucesso

Passos:
1. Usuário adiciona produto ao carrinho
2. Sistema envia dados para o backend
3. Backend consulta o banco (produto disponível)
4. Backend envia pagamento para API
5. API retorna sucesso
6. Pedido é salvo no banco
7. Usuário recebe confirmação

Resultado esperado:
- Compra finalizada com sucesso
- Pedido registrado corretamente

---
### Fluxo Negativo

Cenário: Falha no pagamento

Passos:
1. Usuário tenta finalizar compra
2. Backend envia pagamento para API
3. API retorna erro (cartão recusado)

Resultado esperado:
- Exibir mensagem de erro
- Pedido não deve ser salvo
- Usuário pode tentar novamente

---

### Fluxo Alternativo

Cenário: Produto fora de estoque

Passos:
1. Usuário adiciona produto ao carrinho
2. Backend consulta o banco
3. Produto está indisponível

Resultado esperado:
- Exibir mensagem "Produto indisponível"
- Impedir finalização da compra

---

## ***Tipos de Integração no Cenário***
- **Big Bang:**

Todos os módulos testados juntos:
Frontend + Backend + Banco + API

- **Top-Down:**

Frontend -> Backend -> Banco/API

 *Comunicação da interface com o sistema* 

- **Bottom-Up:**

Banco/API -> Backend -> Frontend

*Dados e integrações internas funcionando*

- **Incremental:**

1. Backend + Banco
2. Backend + API
3. Frontend + Backend

*Testar integrações aos poucos*

---

## Seleção da Estratégia

| Estratégia | Quando usar |
|-----------|------------|
| **Big Bang** | Projeto pequeno, poucos módulos |
| **Top-Down** | Começar pela interface |
| **Bottom-Up** | Começar pelos dados/API |
| **Incremental** | Método mais comum e recomendado |

> A estratégia Incremental reduz riscos e facilita debug