# Particionamento de Equivalência

O Particionamento de Equivalência é uma técnica de teste que divide os dados de entrada em grupos (classes de equivalência) onde os valores se comportam de forma semelhante.

> Testar um valor de cada grupo é suficiente para representar todos os outros valores daquela classe.

--- 
Imagine um campo que aceita números de **1 a 1.000.000**.

- Testar todos -> impossível  
- Testar por classes -> eficiente e inteligente  
###

1 - Quais entradas são válidas?
2 - Quais entradas são inválidas?
3 - Existem tipos diferentes de erro?
4 - O sistema trata cada tipo corretamente?

---

## Exemplo 1 - Idade

### Regra:
Aceita idade entre **18 e 60**

### Classes:

| Classe | Tipo | Intervalo |
|-------|------|----------|
| 1 | Válida | 18–60 |
| 2 | Inválida | < 18 |
| 3 | Inválida | > 60 |

### Casos de Teste:

| Entrada | Classe | Resultado |
|--------|--------|----------|
| 25 | Válida | Aceito |
| 17 | Inválida | Erro |
| 70 | Inválida | Erro |

---

## Exemplo 2 - Campo de Senha

### Regras:
- Mínimo 8 caracteres  
- Deve conter número  
- Deve conter letra  

### Classes:

| Classe | Tipo | Exemplo | Motivo |
|-------|------|--------|-------|
| Senha válida | Válida | abc12345 | Atende todas regras |
| Muito curta | Inválida | abc12 | < 8 caracteres |
| Sem número | Inválida | abcdefgh | Falta número |
| Sem letra | Inválida | 12345678 | Falta letra |

### Casos de Teste:

| Entrada | Resultado Esperado |
|--------|------------------|
| abc12345 | Aceito |
| abc12 | Rejeitado |
| abcdefgh | Rejeitado |
| 12345678 | Rejeitado |

---

## Exemplo 3 - Campo de e-mail

### Regras:
- Deve conter "@"
- Deve conter domínio (.com, .com.br, etc)

### Classes:

| Classe | Tipo | Exemplo |
|-------|------|--------|
| Email válido | Válida | ane@email.com |
| Sem @ | Inválida | aneemail.com |
| Sem domínio | Inválida | ane@email |
| Vazio | Inválida | "" |

---

## Vantagens e Quando Usar

**Vantagens:**
- Reduz drasticamente número de testes
- Eficiente e prático
- Cobre todos os tipos de entrada
- Fácil de documentar

**Quando usar:**
- Campos com múltiplos padrões
- Dados de intervalo (0-100)
- Validação de formato (email, telefone)

> Combinar com Análise de Valor Limite para cobertura completa

---

## Exemplo 4 - Valor de Compra (E-commerce)

### Regra:
- Frete grátis acima de R$100

### Classes:

| Classe | Tipo | Intervalo |
|-------|------|----------|
| Frete grátis | Válida | > 100 |
| Frete pago | Válida | ≤ 100 |

### Casos:

| Valor | Resultado |
|------|----------|
| 150 | Frete grátis |
| 80 | Frete pago |

---

O Particionamento de Equivalência permite:

- Reduzir testes
- Aumentar cobertura
- Testar de forma estratégica
