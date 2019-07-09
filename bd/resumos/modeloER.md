# Modelo ER

Modelo **E**ntidade-**R**elacionamento.

## Entidades

Representações de coisas/objetos pertecentes ao mini mundo.

## Atributos de entidade

Propriedades usadas para descrever uma entidade.

Cada atributo tem um *value set* associado a ele. Exemplos: Integer, String, data e etc.

### Simples

### Compostos

### Multivalorados


## Tipos de entidade

Correspondem a um mesmo tipo de objeto/coisa que possuem o mesmo conjunto de atributos.

## Chaves

Atributos com a propriedade de unicidade. Uma chave pode ser composta, e uma entidade pode ter uma chave.

No modelo ER cada chave é sublinhada, diferente do esquema relacional que só a chave primária é sublinhada.

## Conjunto de entidades

Cada tipo de entidade terá uma coleção de entidades armazenada no banco de dados. Conjunto de entidades representam o estado atual do banco de dados.

## Relacionamentos

Um relacionamento, relaciona duas ou mais entidades.

### Tipo de relacionamento

Mesma coisa que tipo de entidades, só que pra relacionamentos.

### Grau

Número de entidades participantes.

### Restrições

- Razões de cardinalidade: (1:1), (N:1) e (M:N). Participação máxima.
- Dependência de existência: Participação mínima. Representado por linha dupla para dependência total, e simples para dependência parcial.

### Relacionamento recursivo

Um tipo de relacionamento entre o mesmo tipo de entidade com papéis distintos.

## Entidades Fracas

Um tipo de entidade que não tem um atributo de chave e é “dependente de identificação” por outro tipo de entidade.

