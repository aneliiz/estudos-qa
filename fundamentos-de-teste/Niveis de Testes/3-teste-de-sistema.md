# Teste de Sistema
Sistema de e-commerce onde o usuário pode:

1- Criar conta

2- Fazer login

3- Adicionar produtos ao carrinho

4 - Finalizar compra

*O teste de sistema valida o sistema completo de ponta a ponta (end-to-end)*

### **Tipos de Teste de Sistema**
| Tipo de Teste        | Descrição                                  |
|----------------------|--------------------------------------------|
| Funcional            | Valida funcionalidades do sistema          |
| Usabilidade          | Avalia experiência do usuário              |
| Performance          | Mede tempo de resposta                     |
| Segurança            | Verifica proteção de dados                 |
| Compatibilidade      | Testa em diferentes dispositivos/navegadores|

---

## Tipo de teste: ***Funcional***

### Cenário 1 -  Fluxo Feliz
 Cenário: Compra realizada com sucesso

Passos:
1. Acessar o sistema
2. Realizar login com credenciais válidas
3. Adicionar produto ao carrinho
4. Acessar o carrinho
5. Finalizar compra

Resultado esperado:
- Compra finalizada com sucesso
- Mensagem de confirmação exibida
- Pedido registrado no sistema

### Cenário 2 - Fluxo Negativo
Cenário: Falha no login

Passos:
1. Acessar tela de login
2. Inserir usuário inválido
3. Inserir senha incorreta
4. Clicar em "Entrar"

Resultado esperado:
- Sistema exibe mensagem de erro
- Usuário não é autenticado
- Permite nova tentativa

### Cenário 3 - Fluxo Alternativo
Cenário: Finalizar compra com carrinho vazio

Passos:
1. Acessar sistema
2. Realizar login
3. Ir para o carrinho
4. Tentar finalizar compra sem produtos

Resultado esperado:
- Sistema impede a ação
- Exibe mensagem "Carrinho vazio"

---
## Tipo de teste: ***Performace***

### Cenário 1 - Fluxo Feliz
Cenário: Sistema responde rapidamente

Passos:
1. Acessar página inicial
2. Navegar entre páginas

Resultado esperado:
- Tempo de resposta menor que 3 segundos


### Cenário 2 - Fluxo Negativo
Cenário: Sistema lento

Passos:
1. Simular múltiplos acessos simultâneos

Resultado esperado:
- Sistema apresenta lentidão ou falha


### Cenário 3 - Fluxo Alternativo
Cenário: Pico moderado de usuários

Passos:
1. Simular carga média

Resultado esperado:
- Sistema ainda funcional, com leve degradação

---
## Tipo de teste: ***Segurança***

### Cenário 1 - Fluxo Feliz
Cenário: Acesso seguro

Passos:
1. Login válido
2. Acessar área restrita

Resultado esperado:
- Acesso permitido corretamente

### Cenário 2 - Fluxo Negativo
Cenário: Tentativa de acesso indevido

Passos:
1. Acessar URL restrita sem login

Resultado esperado:
- Acesso negado
- Redirecionamento para login

### Cenário 3 - Fluxo Alternativo
Cenário: Sessão expirada

Passos:
1. Fazer login
2. Ficar inativo por tempo prolongado

Resultado esperado:
- Sessão expirada
- Solicitação de novo login

---

## Tipo de teste: ***Usabilidade***

### Cenário 1 - Fluxo Feliz
Cenário: Navegação simples

Passos:
1. Usuário navega pelo sistema
2. Encontra facilmente produtos

Resultado esperado:
- Experiência fluida e intuitiva


### Cenário 2 - Fluxo Negativo
Cenário: Interface confusa

Passos:
1. Usuário tenta encontrar produto

Resultado esperado:
- Dificuldade de navegação
- Possível abandono


### Cenário 3 - Fluxo Alternativo
Cenário: Usuário iniciante

Passos:
1. Primeiro acesso ao sistema 

Resultado esperado:
- Usuário consegue usar com pequena dificuldade

---

## Tipo de teste: ***Compatibilidade***

### Cenário 1 - Fluxo Feliz
Cenário: Sistema funciona em diferentes navegadores

Passos:
1. Acessar no Chrome
2. Acessar no Firefox

Resultado esperado:
- Funcionamento correto em ambos


### Cenário 2 - Fluxo Negativo
Cenário: Incompatibilidade

Passos:
1. Acessar em navegador antigo

Resultado esperado:
- Layout quebrado ou erro


### Cenário 3 - Fluxo Alternativo
Cenário: Dispositivo diferente

Passos:
1. Acessar via mobile

Resultado esperado:
- Interface adaptada (responsiva)

---