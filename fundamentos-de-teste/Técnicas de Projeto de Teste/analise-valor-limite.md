# Análise de Valor Limite

A Análise de Valor Limite é uma técnica de teste (geralmente usada com Caixa Preta) que foca em testar os valores nas bordas (limites) de uma entrada.

> A maioria dos erros acontece nos limites, não no meio dos valores.

---

## Objetivo

- Funciona corretamente nos limites mínimos e máximos
- Trate corretamente valores logo abaixo e acima desses limites
- Não apresente falhas em condições extremas

---

- Qual é o valor mínimo permitido?
- Qual é o valor máximo permitido?
- O que acontece um valor antes e um valor depois?

Regra prática:

Testar sempre **5 pontos principais**:

- Limite inferior - 1  
- Limite inferior  
- Limite inferior + 1  
- Limite superior - 1  
- Limite superior  
- Limite superior + 1  

---

## Exemplo 1 - Idade

### Regra:
Aceita idade entre **18 e 60**

### Valores de Teste:

| Entrada | Tipo | Resultado Esperado |
|--------|------|------------------|
| 17 | Inválido (abaixo) | Erro |
| 18 | Limite mínimo | Aceito |
| 19 | Próximo ao mínimo | Aceito |
| 59 | Próximo ao máximo | Aceito |
| 60 | Limite máximo | Aceito |
| 61 | Inválido (acima) | Erro |

---

## Exemplo 2 - Senha (mínimo 8 caracteres)

### Regra:
Senha deve ter pelo menos **8 caracteres**

### Testes:

| Entrada | Tamanho | Resultado |
|--------|--------|----------|
| 7 caracteres | Abaixo do limite | Rejeitado |
| 8 caracteres | Limite | Aceito |
| 9 caracteres | Acima do limite | Aceito |

---

## Exemplo 3 - Carrinho de Compras

### Regra:
Frete grátis acima de **R$100**

### Testes:

| Valor | Tipo | Resultado |
|------|------|----------|
| 99 | Abaixo | Frete pago |
| 100 | Limite | Frete pago |
| 101 | Acima | Frete grátis |

---

## Exemplo 4 - Campo de Quantidade

### Regra:
Quantidade permitida: **1 a 10**

### Testes:

| Entrada | Tipo | Resultado |
|--------|------|----------|
| 0 | Inválido | Erro |
| 1 | Limite mínimo | Aceito |
| 2 | Próximo | Aceito |
| 9 | Próximo | Aceito |
| 10 | Limite máximo | Aceito |
| 11 | Inválido | Erro |

---

## Passo a Passo

1. Identificar os limites do campo  
2. Definir mínimo e máximo  
3. Criar testes nos pontos críticos  
4. Validar comportamento do sistema  

---

## Relação com Particionamento de Equivalência

| Técnica | Foco |
|--------|------|
| Partição de Equivalência | Grupos de dados |
| Valor Limite | Bordas desses grupos |

 Elas devem ser usadas juntas.

---

> A Análise de Valor Limite é essencial para garantir qualidade, pois:

- Detecta erros críticos  
- Foca nos pontos mais sensíveis  
- Aumenta a confiabilidade do sistema  