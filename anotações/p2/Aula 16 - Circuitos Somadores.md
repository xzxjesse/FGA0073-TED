# Aula 16 - Circuitos Somadores

## Computador Digital

![Computador Digital](/imagens/computador%20digital.png)
1. Unidade de entrada
2. Unidade de memória
3. Unidade de controle
4. Unidade lógica/aritmética
5. Unidade de saída

## Circuitos Aritméticos

### Unidade Lógica e Aritmética (ULA)
    combina portas lógicas e flip-flops para adicionar, subtrair, multiplicar e dividir números binários

![ULA](/imagens/ULA.png)

### Meio somador

![Meio somador](/imagens/meio%20somador.png)

> é um somador que não vai aceitar carry de entrada

Cout = carry de saída

### Somador Completo

![Somador completo](/imagens/somador%20completo.png)

> recebe um carry de entrada e pode ter um carry de saída também

Cin = carry de entrada

    O circuito somador completo vai ter diversos somadores completos e um meio somador, ou não, em cascata.

### Somador paralelo em CI

![Somador paralelo](/imagens/somador%20paralelo.png)

### Somador completo a partir de meio somadores

![Meio somadores para formar somador completo](/imagens/meios%20pra%20completo.png)

### Subtrator completo
> vai seguir a mesma logica, mas é **a-carry=r-b=resultado**

![Subtrator completo](/imagens/subtrator%20completo.png)

### Complemento de 2

A - B = A + (-B) = A + (!B + 1)

#### Multiplexador

> adição e subtração combinadas

![Multiplexador](/imagens/adição%20e%20subtração%20combinadas.png)