# Caso de Teste 
O Caso de Teste é um documento que descreve exatamente como validar uma funcionalidade do sistema:

- O que testar?  
- Como testar?  
- Qual resultado esperar?  

---

## Objetivo

- O sistema funcione conforme esperado  
- Os testes sejam reproduzíveis  
- Outros testadores possam executar o mesmo teste  
- Haja padronização no processo  

---

## Estrutura de um Caso de Teste

Um caso de teste geralmente contém:

| Campo | Descrição |
|------|----------|
| ID | Identificador único |
| Título | Nome do teste |
| Descrição | O que será testado |
| Pré-condição | O que precisa antes do teste |
| Passos | Ações a serem executadas |
| Dados de Entrada | Informações usadas |
| Resultado Esperado | Comportamento esperado |
| Resultado Obtido | Resultado real |
| Status | Passou / Falhou   |

---

## Exemplo

### Caso de Teste: Login válido

| Campo | Valor |
|------|------|
| ID | CT-001 |
| Título | Login com dados válidos |
| Pré-condição | Usuário cadastrado |
| Passos | 1. Acessar login<br>2. Inserir usuário<br>3. Inserir senha<br>4. Clicar em entrar |
| Dados | Usuário: ane123 / Senha: 123456 |
| Resultado esperado | Acesso ao sistema |
| Resultado obtido | Acesso ao sistema |
| Status | Passou |

---

## Exemplo 2 - Login inválido

| Campo | Valor |
|------|------|
| ID | CT-002 |
| Título | Login com senha incorreta |
| Pré-condição | Usuário cadastrado |
| Passos | Inserir usuário correto e senha errada |
| Dados | ane123 / 000000 |
| Resultado esperado | Mensagem de erro |
| Status | Falhou (exemplo) |

---

## Diferença entre Cenário e Caso de Teste

| Tipo | Descrição |
|------|----------|
| Cenário de Teste | O que testar (alto nível) |
| Caso de Teste | Como testar (detalhado) |

---

## Boas Práticas

- Escrever passos claros e objetivos  
- Evitar ambiguidade  
- Criar casos independentes  
- Reutilizar quando possível  
- Manter padronização  

---
>O **caso de teste**, em especial, é um dos Artefatos de Teste mais importantes, porque:

- Define exatamente como testar  
- Garante qualidade e padronização  
- Facilita execução e manutenção  

##

### Manutenção de Casos de Teste

- **Rever periodicamente** quando requisitos mudam
- **Remover casos obsoletos** para evitar confuão
- **Rastrear** qual requisito cada caso valida
- **Versionar** para controlar histórico de mudanças