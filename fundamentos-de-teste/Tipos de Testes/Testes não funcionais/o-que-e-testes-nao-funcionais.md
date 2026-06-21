# O que é Testes Não Funcionais?

É o tipo de teste que valida como o sistema se comporta, e não o que ele faz.

Ele avalia **qualidade**, **desempenho**, **segurança**, **usabilidade** e outros aspectos.

---
Garante que o sistema

- Seja rápido
- Seja seguro
- Aguente muitos usuários
- Seja fácil de usar
- Seja estável

> “O sistema funciona bem sob diferentes condições?”

---

## Diferença para teste funcional

| Tipo | O que testa |
|------|------------|
| Funcional | O que o sistema faz |
| Não Funcional | Como o sistema se comporta |

---

## Como funciona

### 1. Entender o contexto

- Quantos usuários o sistema terá?
- Qual o nível de segurança esperado?
- O sistema precisa ser rápido?

---

### 2. Definir critérios

- Página deve carregar em até 2 segundos  
- Sistema deve suportar 1.000 usuários simultâneos  
- Login deve ser protegido contra invasões  

---

### 3. Criar cenários de teste

Exemplo (Performance):

- Simular 100 usuários acessando ao mesmo tempo  
- Medir tempo de resposta  

Exemplo (Segurança):

- Testar login com senha incorreta várias vezes  
- Verificar bloqueio de acesso  

---

### 4. Executar testes
Exemplos de ferramentas:
- JMeter (performance)
- Selenium (automatização)
- OWASP ZAP (segurança)

---

### 5. Analisar resultados

Você avalia:

- Tempo de resposta
- Consumo de recursos
- Comportamento sob carga

---

## Tipos Principais (Resumo)

| Tipo | O que testa | Pergunta |
|------|-----------|----------|
| Performance | Velocidade | O sistema é rápido? |
| Segurança | Proteção | O sistema é seguro? |
| Usabilidade | Facilidade | O sistema é fácil de usar? |
| Compatibilidade | Ambientes | Funciona em todos os dispositivos? |
| Confiabilidade | Disponibilidade | O sistema é estável? |

> Testes não funcionais garantem qualidade além da funcionalidade

