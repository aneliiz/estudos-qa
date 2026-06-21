# Teste de Caixa Branca

O Teste de Caixa Branca é uma técnica de teste de software baseada na análise da estrutura interna do sistema.

Nesse tipo de teste, o testador possui acesso total ao código-fonte, permitindo validar:

- Lógica de programação  
- Fluxos de execução  
- Estruturas condicionais  
- Laços de repetição  
- Tratamento de exceções  

O objetivo principal é garantir que o código foi implementado corretamente e que todos os caminhos possíveis foram testados.

---

## Objetivos

- Verificar a corretude da lógica interna  
- Garantir cobertura de código  
- Identificar falhas ocultas  
- Validar estruturas de decisão  
- Detectar erros de implementação  

---

## Características

- Requer conhecimento em programação  
- Baseado na estrutura do código  
- Foco em testes estruturais  
- Pode ser automatizado  
- Executado por desenvolvedores ou QAs técnicos  

---

## O que é testado?

### Estruturas condicionais
```js
if (idade >= 18)
```

### Laços de Repetição
```js
for (int i = 0; i < 10; i++)
```

### Fluxos de decisão

```js
if (x > 0) {
   // caminho 1
} else {
   // caminho 2
}
```

### Tratamento de erros
```js
try {
   // código
} catch (Exception e) {
   // tratamento
}
```
-----

## Exemplo:

```js
int calcularDesconto(int valor) {
    if (valor > 100) {
        return valor - 10;
    } else {
        return valor;
    }
}
```
### Caso de teste
| Entrada | Resultado Esperado | Caminho       |
| ------- | ------------------ | ------------- |
| 150     | 140                | if verdadeiro |
| 100     | 100                | if falso      |

----

O Teste de Caixa Branca é essencial para garantir a qualidade do software em nível estrutural. 

Ele permite:

- Validar a lógica do sistema

- Garantir cobertura completa

- Reduzir falhas em produção

---

## Métricas de Cobertura de Código

Mede quanto do código foi testado:

| Métrica | Descrição | Ideal |
|---------|-----------|-------|
| Cobertura de Linha | % de linhas executadas | 80%+ |
| Cobertura de Ramo | % de if/else testados | 75%+ |
| Cobertura de Caminho | % de fluxos completos | 60%+ |

**Ferramentas:**
- Jest, Istanbul (JavaScript)
- JaCoCo (Java)
- Coverage.py (Python)

> Alta cobertura = maior confiança no código