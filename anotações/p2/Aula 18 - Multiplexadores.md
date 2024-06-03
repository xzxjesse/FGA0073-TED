# Aula 18 - Multiplexadores
> enviam um certo número de informações, contidas em vários canais, a um só canal;

    Converte informações paralelas para serial antes de transmitir para um destino remoto.

Ex.:Tabela de saídas em um circuito com 2 seleções, 4 entradas e 1 saída:

|S1|S0|Z|
|---|---|---|
|0|0|I0|
|0|1|I1|
|1|0|I2|
|1|1|I3|

- **Formato paralelo**
    > Processam todos os bits simultaneamente

    - É mais rápido
    - Se a distância for longa, é necessário muitas linhas para transmissão

- **Formato serial**
    > Cascata

1. **Geração de Produtos Canônicos**
    ![Gerador de produtos canônicos](/imagens/Gerador%20de%20produtos%20canônicos.png)

    - Segue uma tabela verdade

2. **Matriz de Simples Encadeamento**

    Com duas entradas e apenas porta AND
    ![Matriz de simples encademento](/imagens/Matriz%20simples%20encadeamento.png)

3. **Matriz de Duplo Encadeamento**
    ![Matriz de duplo encadeamento](/imagens/Matriz%20de%20duplo%20encadeamento.png)

## Circuito multiplex

-> numero de linhas da tabela verdade vai definir a quantidade de canais de entrada do MUX

-> var de entrada do circuito se tornam as entradas de seleção do MUX

### Projeto:
# ESTUDAR PARA PROVA

1. Circuito gerador de produtos canônicos
    - seletores
2. Conjunto de portas AND
    - número de canais
3. 1 porta OR

![Multiplex 2 variáveis](/imagens/Multiplex%202%20variaveis.png)

> conecta o gerador de produtos canônicos (seletores) com os canais de informação e saí tudo dps de passar por uma OR

## Ampliação da capacidade de um sistema multiplex

![Ampliação MUX 4 entradas](/imagens/Ampliação%20MUX%204%20entradas.png)

## Como implementar esse circuito lógico utilizando um e, apenas um, multiplexador de 8 canais e portas lógicas?

![multiplex 8x1](/imagens/multiplex%208x1.png)