## Diferença entre Erro, Defeito e Falha

Esses termos representam etapas diferentes de um problema no software, desde a origem até o impacto no usuário.  

##

### *Erro (Error)*

É Um equívoco humano durante o desenvolvimento.

* Desenvolvedor escreve uma lógica incorreta  
* Requisito mal interpretado

> Erro é a causa inicial do problema 



### *Defeito (Bug)*

É Um problema no código ou sistema causado por um erro.

* Cálculo incorreto no sistema  
* Campo aceita valor inválido  


> Defeito é o erro materializado no sistema

### *Falha (Failure)*

É o comportamento incorreto do sistema durante a execução.

* Sistema trava  
* Login não funciona  
* Informação exibida errada  
 
> Falha é o defeito em execução

##


## Relação entre os conceitos

Erro -> Defeito -> Falha

1. Um erro humano acontece  
2. Gera um defeito no sistema  
3. Quando executado, vira uma falha

##

## Importância Prática

A **detecção precoce** é fundamental:

- **Teste de Unidade** descobre Erros rapidamente (menor custo)
- **Teste de Integração** identifica Defeitos antes da produção
- **Teste de Sistema** previne Falhas nos usuários
- **Produção** = maior impacto financeiro e reputacional

> Quanto mais tarde o erro é descoberto, maior o custo de correção.

## *Resumo*

| Conceito | O que é | Onde acontece | Exemplo |
|----------|--------|--------------|---------|
| Erro     | Falha humana | Desenvolvimento | Lógica implementada incorretamente |
| Defeito  | Problema no sistema | Código | Cálculo errado no sistema |
| Falha    | Comportamento incorreto | Execução | Sistema exibe valor errado   |
##


