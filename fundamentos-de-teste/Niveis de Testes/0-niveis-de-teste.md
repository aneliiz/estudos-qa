## O que é Níveis de Testes?

Os níveis de teste são etapas no ciclo de desenvolvimento de software, divididos em quatro fases principais: unitário, integração, sistema e aceitação, organizados para garantir qualidade desde o código individual até o produto completo. Eles seguem uma ordem cronológica que identifica erros cedo, economizando custos e tempo. 

---


**Teste de Unidade (Unitário):** A menor parte testável do software (funções, métodos, classes) é testada isoladamente pelos desenvolvedores para garantir funcionamento correto.

**Teste de Integração:** Verifica a interação e comunicação entre diferentes módulos ou componentes que foram testados individualmente.

**Teste de Sistema:** Avalia o comportamento de todo o sistema funcional e não funcionalmente (performance, segurança, usabilidade) como um todo, simulando o ambiente final.

**Teste de Aceitação:** Valida se o sistema atende aos critérios de negócio e requisitos funcionais sob a perspectiva do usuário final. 

--- 

## Pirâmide de Testes

A distribuição ideal segue a pirâmide:

```
                         🔺
                        /  \
                       /    \
                      /  UAT \
                     /        \
                    /----------\
                   /  SISTEMA   \
                  /              \
                 /----------------\
                /    INTEGRAÇÃO    \
               /                    \
              /----------------------\
             /       UNITÁRIOS        \
            /__________________________\
```

**Recomendação:**
- **70%** Testes Unitários (rápidos, baratos)
- **20%** Testes de Integração (moderados)
- **10%** Testes de Sistema/UAT (mais lentos, caros)

> Mais testes nas camadas inferiores = detecção precoce de problemas