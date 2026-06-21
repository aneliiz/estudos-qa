# Plano de Teste

O Plano de Teste é um documento que define como os testes serão conduzidos em um projeto:

- O que será testado  
- Como será testado  
- Quem irá testar  
- Quando os testes ocorrerão  

É o guia principal do processo de QA.

---

## Objetivo

- O processo de testes seja organizado  
- Todos saibam o que será testado  
- Haja alinhamento entre equipe e stakeholders  
- O software atenda aos requisitos de qualidade  

---

Sem um plano de teste:

X Testes ficam desorganizados  
X Cenários podem ser esquecidos  
X Falta de padronização  
X Risco maior de falhas em produção  

---

## Estrutura de um Plano de Teste

### 1. Introdução

Descrição geral do projeto e objetivo dos testes.

**Exemplo:**

> Este plano define a estratégia de testes para o sistema de login de usuários.

---

### 2. Escopo

Define o que será e o que não será testado.

**Incluído:**

- Funcionalidade de login  
- Validação de campos  
- Mensagens de erro  

**Não incluído:**

- Testes de performance  
- Testes de segurança avançados  

---

### 3. Estratégia de Teste

Define como os testes serão realizados.

**Exemplo:**

- Teste de Caixa Preta  
- Teste manual  
- Teste funcional  
- Testes exploratórios  

---

### 4. Ferramentas

Ferramentas que serão utilizadas.

- Jira  
- Postman  
- Cypress  
- Selenium  

---

### 5. Equipe

Define quem é responsável pelos testes.

| Nome | Função |
|-----|-------|
| QA | Execução dos testes |
| Dev | Correção de bugs |
| PO | Validação final |

---

### 6. Cronograma

Define quando os testes serão executados.

| Etapa | Data |
|------|------|
| Planejamento | 01/04 |
| Execução | 02/04 - 05/04 |
| Reteste | 06/04 |

---
 
### 7. Critérios de Entrada e Saída

#### - Critérios de Entrada

- Sistema disponível  
- Requisitos definidos  
- Ambiente configurado  

#### - Critérios de Saída

- Todos os testes executados  
- Bugs críticos corrigidos  
- Taxa mínima de sucesso atingida  

---

### 8. Gestão de Defeitos

Define como os bugs serão tratados.

- Registro no Jira  
- Classificação por prioridade  
- Acompanhamento até correção  

---

### 9. Riscos

Possíveis problemas durante os testes.

| Risco | Impacto |
|------|--------|
| Atraso no sistema | Alto |
| Falta de ambiente | Médio |
| Mudança de requisitos | Alto |

---

### 10. Entregáveis

O que será entregue ao final dos testes.

- Casos de teste  
- Relatórios de execução  
- Bugs registrados  
- Evidências  

---

## Exemplo Resumido

### Projeto: Sistema de Login

- Tipo de teste: Funcional  
- Técnica: Caixa Preta  
- Ferramenta: Postman  
- Resultado esperado: Login funcionando corretamente  

---

O **Plano de Teste** é a base para um processo de QA eficiente.
Ele garante:

- Organização  
- Clareza  
- Qualidade  

Sendo um dos artefatos mais importantes dentro do ciclo de testes.