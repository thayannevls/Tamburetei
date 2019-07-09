# Guidelines informal de design para esquemas relacionais

Antes de discutir sobre a teoria formal de design de esquemas de bandos de dados relacionais, vamos discutir quatro conceitos informais para medir a qualidade do seu esquema:

1. Semântica dos atributos
2. Redução de informações redudantes
3. Redução de valores NULL
4. Evitar tuplas espúrias

## Semântica dos atributos

A **semântica** de uma relação se refere a interpretação dos valores de atributos de uma tupal. Em geral, quanto mais fácil explicar a **semântica** de uma relação, melhor será o design do esquema do banco de dados. Para garantir isto, o guideline sugere que:

- Cada *tupla* de uma *relação* deve representar uma *instância* da entidade ou relacionamento.
- Atributos de entidades diferentes não devem ser misturados.
- Apenas as *chaves estrangeiras* devem ser usadas para referenciar outras entidades.
- Atributos de entidades e relacionamentos devem ser mantidos afastados o máximo possível.

## Redução de informações redudantes

Um dos principais do design do esquema é minimizar o desperdício de armazenamento, para isso devemos evitar algumas anamolias.

### Anamolia de inserção

Geralmente ocorre quando não podemos fazer uma inserção de uma entidade A, ao menos que exista uma entidade B associada a ela.

### Anamolia de modificação

Geralmente ocorre quando em uma entidade, caso queiramos modificar um atributo, temos que atualizar muitas tuplas que a referenciam. 

### Anamolia de remoção

Quando ao deletar uma entidade A, muitas dependam dela e precisam ser deletadas também.

## Redução de valores NULL

Relações devem ser projetas de maneira a minimizar valores NULL, sendo assim algumas atitudes podem ser tomadas:

- Atributos que frequentemente assumem valor NULL, podem ser colocar em relações *separadas*
- Ter em mente o significado para valores NULL:
  - Atributos não aplicáveis
  - Atributos que não sabe se existe
  - Atributos que sabemos que existe, mas não está disponível

## Evitar tuplas espúrias

Tuplas espúrias acontece quando duas ou mais relações em uma operação de junção produzem resultados não válidos e ruins. Tuplas espúrias podem ser evitadas se fizermos operações de join com condições de igualdades entre chaves primárias e estrangeiras.

Ao fazer o design do esquema, as relações devem ser projetadas de maneiras a evitar estas tuplas espúrias, seguindo a condição que nenhuma tupla espúria deve ser gerada em operações de junção natural.