# O que é Teste de Segurança

É um tipo de teste não funcional que verifica se o sistema está protegido contra ameaças, ataques e acessos indevidos.

Ele garante que dados sensíveis estejam seguros e que o sistema não tenha vulnerabilidades.

---
Garante que o sistema:

- Proteja dados do usuário
- Evite invasões
- Controle acessos corretamente
- Seja confiável e seguro

> “O sistema pode ser invadido ou explorado de alguma forma?”

---

## Como funciona
### 1. Identificar pontos sensíveis

- Login  
- Cadastro  
- Pagamentos  
- APIs  
- Banco de dados  

---

### 2. Definir possíveis ataques

- Tentativas de login com senha errada  
- Inserção de códigos maliciosos  
- Acesso sem autenticação  

---

### 3. Criar cenários de teste

- Inserir SQL no campo de login  
- Tentar acessar página sem login  
- Fazer múltiplas tentativas de senha  

---

### 4. Executar testes

- Manual (tentando “quebrar” o sistema)  
- Automatizado (ferramentas de segurança)  

---

### 5. Analisar resultados

- O sistema bloqueou o ataque?  
- Os dados ficaram protegidos?  
- Existe alguma brecha?  

---

## Tipos de Testes de Segurança

## 1. Teste de Autenticação

Verifica o processo de login.

E garante que só usuários válidos acessem.

### Exemplo

- Login com senha errada várias vezes  

Esperado:
- Conta bloqueada após tentativas  

---

## 2. Teste de Autorização

Verifica permissões de acesso.

Garante que usuários só acessem o que podem.

### Exemplo

- Usuário comum tentando acessar área admin  

Esperado:
- Acesso negado  

---

## 3. Teste de Injeção

Testa inserção de código malicioso.

Evita ataques como SQL Injection.

### Exemplo

Campo de login:

> ' OR '1'='1 (força a validação a sempre retornar verdadeiro)

Esperado:
- Sistema rejeita entrada  
- Não faz login indevido  

---

## 4. Teste de Sessão

Verifica controle de sessão do usuário.

Evita sequestro de sessão.

### Exemplo

- Usar sessão após logout  

Esperado:
- Sessão inválida  

---

## 5. Teste de Criptografia

Verifica proteção de dados.

Garantir dados seguros.

### Exemplo

- Senha no banco deve estar criptografada  

Esperado:
- Não armazenar senha em texto puro  

---

## 6. Teste de Vulnerabilidades

Busca falhas conhecidas no sistema.

Identificar brechas de segurança.

### Exemplo

- Scanner encontra endpoint inseguro  

Esperado:
- Corrigir vulnerabilidade  

---

## Exemplo na prática

### Sistema: Login


### Cenário 1 - Tentativa de invasão

- Inserir senha errada várias vezes  

Esperado:
- Conta bloqueada  

---

### Cenário 2 - SQL Injection

- Inserir código malicioso  

Esperado:
- Login negado  

---

### Cenário 3 - Acesso indevido

- Acessar URL interna sem login  

Esperado:
- Redirecionar para login  

---

### Cenário 4 - Sessão

- Fazer logout e tentar voltar  

Esperado:
- Sessão encerrada  

---

## Problemas comuns encontrados

- Senhas sem criptografia  
- Falta de validação de entrada 
- Acesso indevido
- Sessões mal gerenciadas  
- APIs expostas  

---

## Top 10 Vulnerabilidades (OWASP)

1. **Injeção** (SQL, NoSQL, OS)
2. **Autenticação quebrada**
3. **Exposição de dados sensíveis**
4. **XXE** (XML External Entity)
5. **Controle de acesso quebrado**
6. **Misconfiguration**
7. **XSS** (Cross-Site Scripting)
8. **Insecure deserialization**
9. **Uso de componentes com vulnerabilidades conhecidas**
10. **Logging e monitoring insuficiente**

---

## Ferramentas de Teste de Segurança

| Ferramenta | Tipo | Uso |
|-----------|------|-----|
| OWASP ZAP | Scanner | Vulnerabilidades web |
| Burp Suite | Proxy | Teste manual e automático |
| Snyk | SCA | Dependências vulneráveis |
| SonarQube | SAST | Análise estática |
| Fortify | SAST | Código seguro |

> Segurança é responsabilidade de todos - dev, QA e infraestrutura
