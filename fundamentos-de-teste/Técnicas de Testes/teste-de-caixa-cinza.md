# Teste de Caixa Cinza


O Teste de Caixa Cinza é uma abordagem intermediária entre:

- Caixa Preta (sem acesso ao código)
- Caixa Branca (acesso total ao código)

Nesse tipo de teste, o testador possui conhecimento parcial da estrutura interna do sistema, mas executa os testes pela interface externa, como um usuário.
Ele não vê todo o código, mas entende como o sistema funciona por dentro

---

## Objetivo

Garantir que o sistema:

- Funcione corretamente do ponto de vista do usuário
- Esteja bem integrado entre seus componentes
- Não apresente falhas de comunicação entre camadas
- Seja seguro contra acessos indevidos

---

## Características

- Conhecimento parcial da arquitetura do sistema  
- Combina técnicas de caixa preta e branca  
- Foco em integração e segurança  
- Testes baseados em lógica + comportamento  
- Muito usado em APIs, bancos de dados e sistemas web  

---

## Exemplo

### Sistema: Login com Banco de Dados

- O sistema usa um banco de dados
- Existe validação de usuário e senha
- Há proteção contra ataques

**Entrada:**


Usuário: ana123
Senha: 123456


**Resultado esperado:**

Acesso permitido


---

### Teste de Segurança (SQL Injection)

**Entrada maliciosa:**
Usuário: ' OR '1'='1
Senha: qualquer


**Resultado esperado:**
Acesso negado


Aqui o testador usa conhecimento interno (banco de dados) para criar testes mais inteligentes.

---

## Casos de Teste

| Cenário | Entrada | Resultado Esperado |
|--------|--------|------------------|
| Login válido | Usuário e senha corretos | Acesso permitido |
| Login inválido | Dados incorretos | Acesso negado |
| SQL Injection | `' OR '1'='1` | Bloqueado |
| Integração com banco | Dados persistidos | Salvo corretamente |
| API resposta | Requisição válida | Status 200 |

---

## Técnicas de Teste

### Teste de Integração

Verifica a comunicação entre componentes.

**Exemplo:**

- Frontend -> Backend  
- Backend -> Banco de dados  

---

### Teste de Segurança

Focado em vulnerabilidades.

**Exemplos:**

- SQL Injection  
- XSS (Cross-Site Scripting)  
- Acesso não autorizado  

---

### Teste baseado em ados

Valida como os dados são processados e armazenados.

**Exemplo:**

- Inserção de dados no banco  
- Recuperação de informações  
- Validação de consistência  

---

### Teste de API

Verifica endpoints e respostas do sistema.

**Exemplo:**

GET /usuarios
POST /login


Valida:

- Status HTTP  
- Estrutura da resposta  
- Dados retornados  

---

### Teste de Fluxo Parcial

Analisa partes internas do sistema com base no conhecimento disponível.

---

## Métricas Importantes

- Taxa de sucesso dos testes  
- Cobertura de integração  
- Número de falhas encontradas  
- Tempo de resposta da API  
- Taxa de erros  

---


## Vantagens

- Testes mais inteligentes e estratégicos  
- Combina visão interna e externa  
- Melhor detecção de falhas de integração  
- Identifica vulnerabilidades de segurança  
- Maior cobertura que caixa preta  

---

## Desvantagens

- Requer conhecimento técnico  
- Pode ser mais complexo de planejar  
- Nem sempre há acesso suficiente à arquitetura  
- Depende da qualidade das informações internas  

---

## Quando usar?

- Testes de integração  
- Testes de API  
- Testes de segurança  
- Sistemas web complexos  
- Aplicações com banco de dados  

---

## Comparação com outros tipos

| Tipo | Foco | Acesso ao Código |
|------|------|----------------|
| Caixa Preta | Comportamento | Não |
| Caixa Branca | Estrutura interna | Total |
| Caixa Cinza | Integração e segurança | Parcial |

---
