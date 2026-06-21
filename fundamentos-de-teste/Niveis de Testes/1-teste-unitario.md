### ***Teste Unitário***

Exemplo de função JS:
```javascript
// Função simples: soma dois números
function somar(a, b) {
	if (typeof a !== 'number' || typeof b !== 'number') throw new TypeError('a e b devem ser números');
	return a + b;
}

module.exports = { somar };
```

Exemplo de teste unitário JS:
```javascript
// Exemplos de testes com Jest para `somar(a,b)`
const { somar } = require('./math');

test('Fluxo feliz: soma dois números positivos', () => {
	expect(somar(2, 3)).toBe(5);
});

test('Fluxo negativo: lança erro se argumento não numérico', () => {
	expect(() => somar(2, '3')).toThrow(TypeError);
});

test('Fluxo alternativo: soma com zero retorna o outro número', () => {
	expect(somar(0, 5)).toBe(5);
});
```

---

### Boas Práticas

- **Isolamento**: Testar apenas a unidade, usar mocks para dependências
- **Nomeação**: Nome descritivo do que está sendo testado
- **Simplicidade**: Um teste = uma coisa
- **Velocidade**: Devem rodar em milissegundos
- **Cobertura**: Aim ar por 80%+ de cobertura de código

> Testes unitários são a base - quanto mais tiver, mais seguro refatorar