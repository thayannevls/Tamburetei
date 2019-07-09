# Dependência funcional

Uma dependência funcional, `X -> Y`, ocorre se sempre que duas tuplas tem o mesmo valor para X, elas devem ter o memso valor para Y.

Se `t1[x] = t2[x]`, então `t1[y] = t2[y]`, para todas as tuplas de R.

## Fatos

Se **K** é uma chave primária de *R*, então ela determina funcionalmente todos os atributos de *R*, uma vez que nunca há duas tuplas distintas onde `t1[K] = t2[K]`

## Exemplo

**A** | **B** | **C** | **D**
--- | --- | --- | --- 
a1 | b1 | c1 | d1
a1 | b2 | c2 | d2
a2 | b2 | c2 | d3
a3 | b3 | c4 | d3


Dependências funcionais que podem existir:

- `B -> C`
- `C -> B`
- `{A, B} -> C`
- `{A, B} -> D`
- `{C, D} -> B`

## Dependência funcional total

uma DF `X-> Y` onde a remoção de qualquer atributo de *X* faz com que a DF não ocorra mais.

## Dependência funcional parcial

uma DF `X-> Y`, onde que permita a remoção de um atributo de *X*, e a DF continue a ocorrer.
