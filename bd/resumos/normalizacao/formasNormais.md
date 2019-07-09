# Formas normais

**Normalização** é realizada na prática para que os projetos resultantes sejam de alta qualidade e satisfaçam *propriedades desejáveis*, que podem ser definidas por essas formas normais: 1FN, 2FN, 3FN, BCNF, 4FN e 5FN.

Normalmente, os projetistas vão apenas até BCNF, 4fn e 5fn raramente são utilizadas na prática.


## Conceitos importantes

É preciso ensinar alguns conceitos importantes para explicar as formas normais:

- **Chave candidata**: Se um esquema de uma relação tem mais de uma chave, cada uma é chamada de *chave candidata*. Uma será escolhida para ser a *chave primária*, e as outras serão chamadas de *chave secundária*.
- **Atributo primo**: É o membro de alguma *chave primária*.
- **Atributo não-primo**: Não é membro de nenhuma *chave candidata*.

# Primeira Forma Normal (1FN)

Considerada como sendo parte da própria definição de relação.

**Não permite**:

- Atributos compostos
- Atributos multivalorados
- Relações aninhadas

Os únicos artibutos permitidos na 1FN são os *simples*.


# Segunda Forma Normal (2FN)

## Conceitos importantes

- Dependência funcional total
- Atributo primo

Todo atributo de *R* *não-primo* está funcionalmente dependente da *chave primária*.

# Terceira Forma Normal (3FN)

## Conceitos importantes

- Dependência transitiva: `X -> Z` que pode ser derivada de duas `X -> Y` e `Y -> Z`

Um esquema de relação *R* está na **3FN** se nenhum atributo atributo *A* *não-primo* em *R* é *transitivamente dependente* da chave primária. Ou seja, os atributos não dependem de nada além da *chave primária*.

# Forma Normal de Boyce-Codd (FNBC)

Um esquema de relação R está na Forma Normal de Boyce-Codd (FNBC) se sempre que uma DF `X → A` ocorrer em R, então X é uma superchave de R.

# Quarta Forma Normal (4FN)

