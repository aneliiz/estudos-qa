# O que é Testes de Performance

É um tipo de teste não funcional que avalia a velocidade, estabilidade e capacidade de resposta do sistema.

Ele mede como o sistema se comporta em diferentes níveis de uso.

---
O teste garante que o sistema:

- Responda rápido 
- Aguente muitos usuários
- Não trave ou caia
- Use bem os recursos (CPU, memória)

> “O sistema continua rápido e estável mesmo com muitos usuários?”

---

## Como funciona

### 1. Definir cenário real
Simular como usuários usam o sistema:

- 100 pessoas fazendo login ao mesmo tempo  
- 50 pessoas adicionando itens ao carrinho  

---

### 2. Definir métricas

- Tempo de resposta
- Taxa de erro
- Usuários simultâneos  
- Uso de CPU e memória  

---

### 3. Executar testes com ferramentas

Ex de ferramentas:

- Apache JMeter  
- k6  
- Gatling  

---

### 4. Analisar resultados

- O sistema ficou lento?  
- Deu erro?  
- Caiu?  

---

## Tipos de Testes de Performance


## 1. Teste de Carga (Load Test)

Testa o sistema com uma quantidade esperada de usuários.

Ver se o sistema aguenta o uso normal.

### Exemplo

Sistema de e-commerce:

- 200 usuários simultâneos  
- Todos navegando e comprando  

Esperado:
- Sistema continua rápido  
- Sem erros  

---

## 2. Teste de Stress

Testa o sistema além do limite.

Descobre o ponto de quebra.

### Exemplo

- 10.000 usuários simultâneos  

Esperado:
- Sistema pode ficar lento, mas não deve travar completamente ou perder dados  

---

## 3. Teste de Pico

Testa aumento repentino de usuários.

Ver como o sistema reage a picos.

### Exemplo

- De 50 -> 1.000 usuários em segundos  

Esperado:
- Sistema se adapta  
- Pode ficar mais lento, mas não cair  

---

## 4. Teste de Resistência

Testa o sistema por longos períodos.

Ver estabilidade ao longo do tempo.

### Exemplo

- 200 usuários por 8 horas  

Esperado:
- Sistema continua estável  
- Sem vazamento de memória  

---

## Exemplo na prática

### Sistema: Login

### Cenário 1 - Carga normal

- 100 usuários logando ao mesmo tempo  

Resultado esperado:
- Login em até 2 segundos  

---

### Cenário 2 - Stress

- 5.000 usuários simultâneos  

Resultado esperado:
- Sistema lento, mas funcional  

---

### Cenário 3 - Pico

- 50 → 1.000 usuários rapidamente  

Resultado esperado:
- Sistema se adapta sem cair  

---

### Cenário 4 - Longa duração

- 200 usuários por 6 horas  

Resultado esperado:
- Sistema estável  

---

## Problemas comuns encontrados

- Lentidão   
- Queda do sistema  
- Erros de servidor
- Alto uso de CPU/memória  

---

## Métricas e Benchmarks

| Métrica | Excelente | Bom | Aceitável |
|---------|-----------|-----|-----------|
| Tempo resposta | < 1s | < 2s | < 5s |
| Taxa erro 5xx | 0% | < 0.1% | < 1% |
| Disponibilidade | > 99.99% | > 99.9% | > 99% |
| CPU idle | > 30% | > 20% | > 10% |

---

## Ferramentas Populares

- **Apache JMeter**: Código aberto, multilíngue, completo
- **k6**: Moderno, baseado em Go, ótimo para CI/CD
- **Gatling**: Scala, alta throughput, relatórios bonitos
- **LoadRunner**: Corporativo, caro, muito poderoso
- **New Relic**: Monitoramento contínuo em produção

> Testes de performance devem ser integrados ao CI/CD para detecção contínua