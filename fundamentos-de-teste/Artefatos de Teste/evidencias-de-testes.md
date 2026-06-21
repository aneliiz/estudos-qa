# Evidências de Teste

As evidências de teste são os registros que comprovam que um teste foi executado.

Elas mostram:

- O que foi testado  
- Como foi testado  
- Qual foi o resultado  
---
- Cenário -> O que testar  
- Caso de Teste -> Como testar  
- Massa de Dados -> Com o que testar  
- Evidência -> Prova do teste  

---
Sem evidência:

- Não dá pra provar que o teste foi feito  
- Fica difícil reproduzir bugs  
- Falta de confiabilidade no processo  

Com evidência:

- Transparência  
- Rastreabilidade  
- Credibilidade do QA  

---

## Tipos de Evidência

### 1. Screenshot (Print de Tela)

Captura da tela mostrando o resultado.

**Exemplo:**
- Tela de erro exibida  
- Mensagem de sucesso  
- Campo inválido destacado  

---

### 2. Gravação de Vídeo

Mostra o fluxo completo do teste.

**Exemplo:**
- Processo de login  
- Bug acontecendo em tempo real  

---

### 3. Logs

Registros técnicos do sistema.

**Exemplo:**
- Erros no console  
- Logs de backend  

---

### 4. Relatórios de Teste

Documentos com resultados dos testes.

**Exemplo:**
- Teste passou ou falhou  
- Tempo de execução  

---

### 5. Evidência em Ferramentas

Registros em ferramentas de QA.

**Exemplo:**
- Jira  
- TestRail  
- Azure DevOps  

---

## Exemplo

### Caso de Teste:
Login com senha inválida

---

### Massa de Dados:

- Usuário: ane@email.com  
- Senha: 000000  

---

### Evidência:

---

## Ferramentas Recomendadas

| Ferramenta | Tipo de Evidência | Uso |
|-----------|------------------|-----|
| Jira | Relatório | Acompanhamento de bugs |
| TestRail | Dados estruturados | Execução e resultados |
| Azure DevOps | Integrado | Pipelines e artefatos |
| Allure | Relatório visual | Dashboards de testes |
| Screenshots | Visual | Print de erros |
| Screenrecorder | Vídeo | Reproduzir fluxos |

> Combinar múltiplas evidências para rastreabilidade completa.

- Screenshot da mensagem: "Senha incorreta"  
- Vídeo mostrando tentativa de login  
- Log registrando erro de autenticação  

---

## Exemplo Estruturado

| Item | Descrição |
|------|----------|
| Caso de Teste | Login inválido |
| Resultado | Falhou |
| Evidência | Screenshot + vídeo |
| Observação | Mensagem exibida corretamente |

---

## Boas Práticas

- Capturar evidência sempre  
- Nomear arquivos corretamente  
- Organizar por caso de teste  
- Garantir que a evidência seja clara  
