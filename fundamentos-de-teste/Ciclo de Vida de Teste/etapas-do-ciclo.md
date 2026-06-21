# Ciclo de Vida de Testes

O Ciclo de Vida de Testes (STLC) é o conjunto de etapas que definem como o processo de testes é realizado, desde o planejamento até a finalização.

Ele garante organização, qualidade e controle durante os testes.

1. Entender o sistema  
2. Planejar os testes  
3. Criar testes  
4. Executar testes  
5. Reportar bugs  
6. Finalizar  

---

## Etapas do STLC


## 1. Análise de Requisitos

### O que acontece?

O QA analisa os requisitos do sistema para entender:

- O que será testado  
- O que é esperado  
- Possíveis riscos  

---

### Exemplo:

Sistema de login:

- Deve permitir login com email e senha  
- Deve mostrar erro para dados inválidos  

---

### Saída:

- Lista de cenários de teste  
- Dúvidas para o time  

---

## 2. Planejamento de Teste

### O que acontece?

Definição da estratégia de testes.

---

### Inclui:

- Escopo  
- Tipo de teste  
- Ferramentas  
- Cronograma  
- Equipe  

### Saída:

- Plano de Teste  

---

## 3. Design de Teste

### O que acontece?

Criação dos artefatos de teste:

- Cenários de teste  
- Casos de teste  
- Massa de dados  


### Exemplo:

Caso de teste:

- Inserir login válido  
- Validar acesso  

### Saída:

- Casos de teste documentados  

---

## 4. Preparação do Ambiente

### O que acontece?

Configuração do ambiente necessário para testar.

### Exemplo:

- Sistema disponível  
- Banco de dados  
- Usuários de teste  

### Saída:

- Ambiente pronto para execução  

---

## 5.  Execução dos Testes

### O que acontece?

Execução dos casos de teste.


### Durante essa fase:

- Testes são executados  
- Resultados são registrados  
- Evidências são coletadas  


### Resultado:

| Caso | Resultado |
|------|----------|
| Login válido | Passou |
| Login inválido | Falhou |

---

## 6. Reporte de Bugs

### O que acontece?

Registro de defeitos encontrados.

---

### Inclui:

- Descrição do bug  
- Passos para reproduzir  
- Evidências  
- Severidade  

### Saída:

- Bug report  

---

## 7. Reteste e Regressão

### O que acontece?

- Retestar bugs corrigidos  
- Garantir que nada quebrou  

---

### Tipos:

- Reteste → bug específico  
- Regressão → sistema geral  

---

## 8. Encerramento dos Testes

### O que acontece?

Finalização do ciclo de testes.

---

### Inclui:

- Relatórios finais  
- Métricas  
- Lições aprendidas  


### Saída:

- Test Summary Report  

---

## Fluxo Resumido

>Requisitos -> Planejamento -> Design -> Ambiente -> Execução -> Bugs -> Reteste -> Encerramento

## Exemplo Completo (Login)

| Etapa          | Ação                    |
|----------------|------------------------|
| Análise        | Entender login         |
| Planejamento   | Definir testes         |
| Design         | Criar casos            |
| Execução       | Testar login           |
| Bug            | Senha não valida       |
| Reteste        | Corrigido              |
| Encerramento   | Relatório final        |
