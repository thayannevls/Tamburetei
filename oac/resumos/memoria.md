# Memória

## Composição

### Memória de acesso aleatório

- **RAM (Random Access Memory)**
  - Acesso aleatória
  - Qualquer posição da memória é acessado no mesmo intervalo de tempo
- **RAM estática(SRAM)**
  - Uso de flip-flops
  - Conteúdo persiste enquanto circuito é alimentado
  - Mais rápida
- **RAM dinâmica(DRAM)**
  - Baseada em capacitores
  - Carga deve ser restaurada periodicamente
  - Menor, mais econômica

### Memória somente de leitura

- **ROM (Read-Only Memory)**
  - Simples: Decodificador, linhas de saída e portas lógicas
  - Aplicações de grande volume
- **PROM (Programmable ROM)**
  - Baixo volume e protótipos
  - Conteúdo escritor com queimador de PROM
- **EPROM(Erasable PROM)**
  - Apagada por luz violeta
- **EEPROM(Eletricaly Erasable ROM)**
- **ROM Flash**

## Memória cache

O acesso a memória é um dos principais motivos para menor de velocidade do processamento, o processamento é muito mais rápido que a transferência de dados. Uma das soluções para esse problema é o uso de uma **memória menor** e e **mais rápida** que a *memória principal*


### Príncipio de localidade

- **Localidade temporal**: Uma posição de memória referenciada recentemente tem boas chances de ser referenciada novamente. Iterações e recursividade
- **Localidade espacial**: Uma posição vizinha de uma posição referenciada recentemente tem boas chances de ser referenciada. Dados tendem a ser armazenados em posições contíguas
  
