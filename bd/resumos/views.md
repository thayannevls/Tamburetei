# Views

Uma **View** é uma tabela derivada de outras tabelas, essas outras tabelas são chamadas de *tabelas de definição* e também podem ser outras *views*. Uma tabela *view* não existe necessariamente no modo físico do banco de dados, sendo assim considera uma **tabela virtual**, diferente de tabelas base do banco de dados, que são armazenadas fisicamente no banco de dados.

Por ser virtual tem limitações quanto a operações de atualizações que possa ser aplicadas nas *views*, mas em contraste não trás nenhuma limitação em fazer a query de uma *view*.

## Sintaxe

```
CREATE VIEW ALUNO5 AS
SELECT *
FROM ALUNO
WHERE matricula = 5
```

Após criar uma *view* você pode referenciá-la em qualquer lugar, do mesmo jeito que outras tabelas.

## Utilização

*Views* podem ser pensadas como um jeito de especificar uma tabela que usamos frequentemente, mas que não precisamos armazenar. Então quando temos, por exemplo, uma consulta que usamos constantemente, *views* se torna extremamente útil.

Outra exemplo de utilização de *view* é para esconder certos atributos ou tuplas de usuários, onde você cria uma *view* com a consulta restrita para esse usuário.


## Atualização

Uma *view* deve estar sempre atualizada, sendo essa responsabilidade do SGBD e não do usuário.

O problema de implementa eficientemente *views* para querying é complexo, existindo diversas abordagens


### Modificação da consulta

Modificamos a query da *view* em outra query nas tabelas base. Ou computamos a query quando necessário. Essa abordagem tem a desvantagem de ser ineficiente para quando temos queries complexas nas *views*.


### Materialização da View

Consiste em criar uma *view* temporária fisicamente quando é acessada pela primeira vez, essa estratégia assume que outras queries continuaram a seguir o padrão salvo.

Para esse caso, precisa ser desenvolvida estratégias para atualizar as *views* quando as *tabelas base* são atualizadas.

**Estratégias de atualização**

- *IMMEDIATE UPDATE*: Atualiza as *views* sempre que as *tabela base* forem alteradas.

- *LAZY UPDATE*: Atualiza a *view* apenas quando precisar ser usada por uma consulta.

- *PERIODIC UPDATE*: Atualiza periodicamente. Pode ocasinar leituras desatualizadas.

## Restrições

- *Views* definidas com funções de agregação e/ou agrupamento não podem ser atualizadas.
- Os atributos a serem atualizadas não podem ser derivados/calculados a partir de outras tabelas.
