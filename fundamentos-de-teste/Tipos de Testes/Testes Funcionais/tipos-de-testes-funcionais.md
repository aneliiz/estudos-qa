
# Tipos de Teste Funcional

- ### Teste de Unidade
Testa pequenas partes do código

- ### Teste de Integração
Testa comunicação entre sistemas

- ### Teste de Sistema
Testa o sistema completo

- ### Teste de Aceitação
Valida com base no que o cliente pediu

---

## Exemplo

### Requisito:
Usuário deve conseguir fazer login

---

### Casos de teste:

1. Login com dados válidos  
Deve acessar o sistema  

2. Login com senha errada  
Deve mostrar erro  

3. Campos vazios  
Deve validar obrigatoriedade  

---

## Exemplo Completo: Sistema de Compra

### Fluxo:
1. Usuário cria conta
2. Faz login
3. Adiciona produto ao carrinho
4. Finaliza compra
5. Recebe confirmação

### Testes Funcionais:
- Criar conta com email novo (positivo)
- Criar conta com email duplicado (negativo)
- Login com senha correta (positivo)
- Login com senha errada (negativo)
- Adicionar produto fora de estoque (negativo)
- Finalizar compra com sucesso (positivo)

> Cada teste valida um comportamento específico da funcionalidade