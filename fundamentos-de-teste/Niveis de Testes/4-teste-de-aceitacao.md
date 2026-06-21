#  O que é Teste de Aceitação?
É a etapa onde se valida se o sistema atende as necessidades do usuário e do negócio e está pronto para ser entregue (produção).
Em outras palavras: *Isso aqui resolve o problema do cliente de verdade?*


##  Como Funciona?

O processo inicia com uma necessidade do negócio.

Requisito:

- História de usuário
- Requisito funcional
- Solicitação direta do cliente
- Demanda estratégica da empresa

### Ex. de História de Usuário:

*Como usuário,  
Quero fazer login,  
Para acessar minha conta.*

Essa história define:
- Quem é o usuário
- O que ele quer fazer
- Por que ele quer fazer

---

## Definição dos Critérios de Aceite

Os critérios de aceite definem quando a funcionalidade pode ser considerada pronta.

Sem critérios claros, não é possível validar corretamente.

### Exemplo:

Critérios de aceite:

- Deve permitir login com email e senha válidos
- Deve exibir mensagem de erro com dados inválidos
- Deve redirecionar para a página inicial após login bem-sucedido
- Deve bloquear acesso após múltiplas tentativas inválidas

Os critérios funcionam como uma checklist obrigatória.

---

## Criação dos Cenários de Teste

Os critérios são transformados em cenários executáveis.

Muito comum usar o formato BDD (Behavior Driven Development):

> Dado / Quando / Então

### Exemplo – Fluxo Feliz

Cenário: Login válido

**Dado** que o usuário está na tela de login  
**Quando** ele insere email e senha válidos  
**Então** ele deve acessar o sistema com sucesso  

---

### Exemplo – Fluxo Negativo

Cenário: Login inválido

**Dado** que o usuário está na tela de login  
**Quando** ele insere senha incorreta  
**Então** o sistema deve exibir mensagem de erro  

---

### Exemplo – Fluxo Alternativo

Cenário: Usuário esqueceu a senha

**Dado** que o usuário está na tela de login  
**Quando** ele clicar em "Esqueci minha senha"  
**Então** o sistema deve permitir redefinição de senha  

---

## Execução dos Testes

A execução pode ser feita por:

- Usuário final (UAT)
- Cliente
- Product Owner
- QA (em alguns casos)

Durante essa etapa, verifica-se se todos os critérios de aceite são atendidos.

---

## Validação dos Resultados

Após a execução, se todos os critérios foram atendidos é APROVADO  
Se algum critério falhou é REPROVADO

Se reprovado:
- O bug é registrado
- A funcionalidade volta para o time de desenvolvimento
- Após correção, é reavaliada


---

# Tipos de Teste de Aceitação

| Tipo                  | Descrição                                      |
|-----------------------|-----------------------------------------------|
| UAT (Usuário Final)   | Validação pelo usuário ou cliente              |
| Alfa                  | Teste interno antes de liberar                 |
| Beta                  | Teste com usuários reais                      |
| Contrato              | Verifica regras definidas em contrato          |
| Regulatório           | Valida conformidade com leis e normas          |

---

# 1. Teste de Aceitação do Usuário (UAT)

### Fluxo Feliz
Cenário: Usuário realiza compra com sucesso

Passos:
1. Criar conta
2. Fazer login
3. Adicionar produto ao carrinho
4. Finalizar compra

Resultado esperado:
- Compra realizada com sucesso
- Usuário satisfeito com o processo


### Fluxo Negativo
Cenário: Erro ao finalizar compra

Passos:
1. Tentar finalizar compra
2. Sistema apresenta erro inesperado

Resultado esperado:
- Usuário não consegue concluir a compra
- Experiência negativa

---

## Aprovação e Liberação

Após UAT bem-sucedido:

✓ Todos critérios de aceite atendidos  
✓ Usuário final aprova a funcionalidade  
✓ Sign-off de stakeholders obtido  

**Próximo passo:** Deploy para produção

> UAT é a última gate antes do lançamento ao público


### Fluxo Alternativo
Cenário: Usuário desiste da compra

Passos:
1. Adicionar produto ao carrinho
2. Abandonar antes de finalizar

Resultado esperado:
- Sistema mantém itens no carrinho
- Usuário pode retornar depois

---

# 2. Teste Alfa

### Fluxo Feliz
Cenário: Sistema validado internamente

Resultado esperado:
- Funcionalidades principais aprovadas


###  Fluxo Negativo
Cenário: Problemas encontrados antes do lançamento

Resultado esperado:
- Bugs identificados e corrigidos


### Fluxo Alternativo
Cenário: Ajustes de última hora

Resultado esperado:
- Pequenas melhorias aplicadas

---

# 3. Teste Beta

### Fluxo Feliz
Cenário: Usuários reais aprovam o sistema

Resultado esperado:
- Feedback positivo


### Fluxo Negativo
Cenário: Usuários encontram erros

Resultado esperado:
- Problemas reportados


### Fluxo Alternativo
Cenário: Feedback de melhorias

Resultado esperado:
- Sugestões de UX e funcionalidades

---

# 4. Teste de Contrato

### Fluxo Feliz
Cenário: Requisitos atendidos

Resultado esperado:
- Sistema cumpre tudo que foi acordado


### Fluxo Negativo
Cenário: Requisito não atendido

Resultado esperado:
- Reprovação do sistema


### Fluxo Alternativo
Cenário: Ajustes negociados

Resultado esperado:
- Alterações acordadas entre as partes

---

# 5. Teste Regulatório

### Fluxo Feliz
Cenário: Sistema conforme leis (ex: LGPD)

Resultado esperado:
- Dados protegidos corretamente


### Fluxo Negativo
Cenário: Falha de segurança de dados

Resultado esperado:
- Sistema não aprovado


### Fluxo Alternativo
Cenário: Ajustes de conformidade

Resultado esperado:
- Correções implementadas

---

# Conclusão

O teste de aceitação garante que o sistema realmente resolve o problema do usuário e atende aos objetivos do negócio, sendo a última validação antes da entrega em produção.
