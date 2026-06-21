# Massa de Dados

A massa de dados é o conjunto de dados utilizados para executar testes.
São os valores que você insere no sistema para validar comportamentos.


- Cenário -> O que testar  
- Caso de Teste -> Como testar  
- Massa de Dados -> Com o que testar  

---

## Exemplo (Login)

### Cenário:
Usuário faz login

### Massa de Dados:

| Tipo | Usuário | Senha |
|------|--------|------|
| Válido | ane123 | 123456 |
| Inválido | ane123 | 000000 |
| Vazio | "" | "" |

Aqui estão os dados que vão validar diferentes comportamentos.

---
  
## Tipos de Massa de Dados

### Dados Válidos

Dados corretos que devem funcionar.

**Exemplo:**
- Email: ane@email.com  
- Senha: 123456  

---

### Dados Inválidos

Dados incorretos para testar falhas.

**Exemplo:**
- Email sem @  
- Senha errada  

---

### Dados Limite
Valores nos limites do sistema.

**Exemplo:**
- Senha com 6 caracteres (mínimo)  
- Senha com 5 caracteres (inválido)  

---

### Dados Duplicados

Testa repetição de informações.

**Exemplo:**
- Cadastro com email já existente  

---

### Dados Nulos / Vazios

Campos sem preenchimento.

**Exemplo:**
- Campo email vazio  
- Campo senha vazio  

---

## Exemplo

### Campos:

- Nome  
- Email  
- Senha  

---

### Massa de Dados

| Caso | Nome | Email | Senha | Resultado Esperado |
|-----|------|------|------|------------------|
| Válido | Ane | ane@email.com | 123456 | Cadastro realizado |
| Email inválido | Ane | aneemail.com | 123456 | Erro |
| Senha curta | Ane | ane@email.com | 123 | Erro |
| Nome vazio | "" | ane@email.com | 123456 | Erro |
| Email duplicado | Ane | ane@email.com | 123456 | Erro |

---

## Boas Práticas

- **Privacidade**: Nunca usar dados reais de clientes em testes  
- **Automatização**: Gerar massa de dados via scripts  
- **Limpeza**: Deletar dados de teste após execução  
- **Rastreamento**: Marcar dados de teste para fácil identificação  
- **Documentação**: Explicar de onde os dados vieram e quando usados

## Relação com outras técnicas

### Partição de Equivalência

Divide os dados em grupos:

- Válidos  
- Inválidos  

A massa de dados vem desses grupos.

---

### Valor Limite

Foca nos extremos:

- Mínimo  
- Máximo  

A massa de dados inclui esses valores.|

---


## Resumo

- Massa de dados = entradas do teste  
- Fundamental para validar comportamento  
- Deve ser variada e bem planejada  

Sem uma boa massa de dados, o teste perde qualidade.