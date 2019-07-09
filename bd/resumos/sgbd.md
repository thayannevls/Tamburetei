# SGBD

## Assertion
Mecanismo para especificar restrições complexas envolvendo mais de uma tabela.

## Trigger
Especificar ações automáticas que o sistema executará quando ocorrer certos eventos e condições.

## Functions e procedures

São úteis para quando temos um BD acessado por várias aplicações, para reduzir o custo de comunicação, para aumentar o poder de modelagem de views e/ou para definir restrições complexas que estão além do poder de assertion/trigger.

## Transações

Uma **transação** é um conjunto de procedimentos que são percebidos com uma única ação. Tem as propriedades de *atomicidade*, *consistência*, *isolamento* e *durabilidade*, podendo ser lembrado por ACID.


### Atomicidade

Todas as ações que compõe a transação devem ocorrer com sucesso, se uma falhar, a transação é desfeita.

### Consistência

Uma transação deve levar o banco de dados de um estado consistente para outro consistente, ou seja, deve respeitar todas as constraints.

### Isolamento

Cada transação funciona de maneira independente de outras transações, sem interferências.

### Durabilidade

Os resultados de uma transação são permanentes e podem ser desfeitos somente por uma transação subsequente.

### Fenômenos a serem evitados

- Dirty read: A transação lê dados escritos por uma transição simultânea não efetivada.
- Nonrepeatable read: Transação lê novamente dados lidos anteriormente, e descobre que os dados foram alterados por outra transição
- Phantom read: a transação executa novamente uma consulta que retorna um conjunto de linhas que satisfazem  uma determinada condição, e descobre que o conjunto é diferente por causa de uma outra transação efetivada recentemente.

## Segurança

**GRANT** e **REVOKE** concede e restringe privilégios.