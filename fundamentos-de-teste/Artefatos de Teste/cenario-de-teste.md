# Cenários de Teste

Os cenários de teste descrevem o que deve ser testado em um sistema.
São descrições de alto nível, sem muitos detalhes técnicos.

Eles focam em:

- Fluxos principais do sistema  
- Funcionalidades importantes  
- Comportamentos esperados  

---
-  **Cenário de Teste -> O que testar**
-  **Caso de Teste -> Como testar**

---

## Exemplo (Login)

### Cenários de Teste:

- Usuário realiza login com sucesso  
- Usuário digita senha incorreta  
- Usuário deixa campos em branco  
- Usuário tenta acessar sem cadastro  

 Aqui **não tem passo a passo**, só a ideia do teste.

---

## Comparando com Caso de Teste

### Cenário:
> Usuário realiza login com sucesso

### Caso de Teste:
- Acessar tela de login  
- Inserir usuário válido  
- Inserir senha válida  
- Clicar em "Entrar"  
- Validar redirecionamento  
-  >Cenário = visão geral  
- >Caso de teste = detalhado  

---

## Características de um bom cenário

- Simples  
- Claro  
- Objetivo  
- Baseado no comportamento do usuário  

---

## Exemplo

### Cenários de Teste

#### Compra de Produto

- Usuário adiciona produto ao carrinho  
- Usuário remove produto do carrinho  
- Usuário finaliza compra com sucesso  
- Usuário tenta comprar sem estoque  

---

#### Pagamento

- Pagamento com cartão aprovado  
- Pagamento com cartão recusado  
- Pagamento via PIX  
- Pagamento com dados inválidos  

---

#### Cadastro

- Usuário se cadastra com sucesso  
- Usuário tenta cadastrar email já existente  
- Usuário deixa campos obrigatórios vazios  

---

## Transformando Cenário em Caso de Teste

### Cenário:
> Usuário finaliza compra com sucesso

### Caso de Teste:

1. Acessar produto  
2. Adicionar ao carrinho  
3. Ir para checkout  
4. Inserir dados válidos  
5. Confirmar pagamento  

Resultado esperado:
> Compra concluída com sucesso 

##

### Reutilização de Cenários

- **Reutilizar** cenários entre funcionalidades semelhantes
- **Versionamento** para rastrear mudanças
- **Documentar dependências** entre cenários
- **Automatizar** cenários estima no CI/CD

---

## Resumo
- Cenários = visão macro  
- Casos de teste = visão detalhada  
- Um complementa o outro  