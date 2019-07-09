# Processador

## Nível de microarquitetura

### Single Cycle

Cada instrução é executada em um ciclo de clock. O período de clock deve ter duração suficiente para concluir os seguintes passos:

1. Instruction Fetch
2. Decode and Register Fetch
3. ALU operation
4. Data fetch if required
5. Register write-back setup time

### Multiple Cycle

A execução de cada instrução é dividida em passos menores.

### Pipelined

Assim como a *Multiple Cycle* as instruções são divididas em passos menores, e além disso, múltiplas instruções são executadas ao mesmo tempo.

## Príncipios de projeto para computadores modernos

Listaremos alguns príncipios do padrão RISC são seguidos por arquitetos de processadores de próposito geral seguem.

- Todas as instruções são diretamente executadas por hardware. Para máquina com filosofia CISC, as instruções, em geral menos frequentes, que não existem em hardware, são interpretadas
- Não existe o nível de microinstrução
- As instruções precisam ser facilmente decodificadas
  - decodificação influencia na velocidade de execução das instruções
  - decodificação determina os recursos a serem usados na execução das instruções
  - quanto menor o número de formatos, mais fácil a decodificação 
- Somente as Instruções de Load e Store devem referenciar a Memória
  - Acesso à memória é mais lento
  - Instruções que acessam a memória podem ser intercaladas com outras instruções 
- Projetar uma máquina com muitos registradores (>= 32)
  - Palavras de memória devem permanecer nos registradores o maior tempo possível
  - Falta de registradores pode obrigar a buscar várias vezes a mesma palavra da memória
- Maximizar a Taxa à qual as instruções são executadas
- Uso de **paralelismo**: execução de várias instruções lentasao mesmo tempo
- Execução de instruções não precisa seguir a lógica da programação
- Solução para aumentar a velocidade do processador: Uso de **paralelismo**.
  - **no nível das instruções**: um único processador deve executar mais instruções por segundo. 
  - **no nível do processador**: vários processadores trabalhando juntos na solução do mesmo problema
- **Paralelismo no Nível das Instruções**: Maior gargalo para a velocidade de execução de instruções é o acesso à memória.
  - **Execução em Pipeline**: O processamento em pipeline divide a execução de instruções em várias partes, cada uma das quais tratada por um hardware dedicado exclusivamente a ela.

## Paralelismo no nível de instruções

Teremos a execuçã da instrução em pipeline. O processamento em pipeline divide a execução de instruções em várias partes, cada uma das quais tratada por um hardware dedicado exclusivamente a ela.

## Computadores matriarcais

### Processador matriarcal

Possui uma *única* unidade de controle e um grande número de processadores que executam a mesma sequência de instruções, cada um possuindo sua *ULA* para fazer as operações. Possui um custo elevado e possui o problema de não serem independentes, por terem uma única *unidade de controle*.

### Processador vetorial

Parecido com o matriarcal, porém as operações aritméticas serão executadas em uma única *ULA* que opera em pipeline, invés de cada processador ter a sua.

## Multiprocessadores

Nesse padrão, os processadores são independentes um dos outros, compartilhando apenas de uma memória por meio de barramentos, sendo necessário gerenciar conflitos que possam ocorrer nela.

## Multicomputadores

Sistemas com um grande número de computadores totalmente independentes, sem compartilhar memória, e se comunicando entre eles com uma velocidade alta.

## Conceitos relevantes

- **Multiple Instruction Single Data (MISD) stream**: múltiplas unidades de controle executando instruções distintas que operam sobre o mesmo dado. 
- **Multiple Instruction Multiple Data (MIMD) stream**: esta classe é bastante genérica envolvendo o processamento de múltiplos dados por parte de múltiplas instruções