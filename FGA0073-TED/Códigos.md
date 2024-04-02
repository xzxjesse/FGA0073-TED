# Códigos
Podem ser numéricos ou alfanuméricos

## BCD
> Decimal codificado em binário - binary coded decimal

O código BCD representa cada dígito de um número decimal por um número binário de 4 bits.

- apenas os números de 4 bits de 0000 a 1001 são usados
- o BCD não usa os números: 1010, 1011, 1100, 1101, 1110 e 1111

### Tabela

Decimal | BCD
------- | --------
0 | 0000
1 | 0001
2 | 0010
3 | 0011
4 | 0100
5 | 0101
6 | 0110
7 | 0111
8 | 1000
9 | 1001
10 | 0001 0000
11 | 0001 0001
12 | 0001 0010
13 | 0001 0011
14 | 0001 0100
15 | 0001 0101
16 | 0001 0110
17 | 0001 0111
18 | 0001 1000
19 | 0001 1001
20 | 0010 0000

### Exemplo
137 = 10001001 BINÁRIO
137 = 0001 0011 0111 BCD

## Excesso de 3
É a transformação do número decimal no binário correspondente, somando-se três unidades

## Decimal | Excesso de 3
------- | --------
  | ABCD
0 | 0011
1 | 0100
2 | 0101
3 | 0110
4 | 0111
5 | 1000
6 | 1001
7 | 1010
8 | 1011
9 | 1100
10 | 1101
11 | 1110
12 | 1111
13 | 0000
14 | 0001
15 | 0010
16 | 0011
17 | 0100
18 | 0101
19 | 0110
20 | 0111

* Esse código é obtido somando-se 3 ao valor binário natural do dígito decimal.
* Para converter um número decimal maior que 20, basta converter cada dígito decimal individualmente e concatenar os resultados.

### Exemplo

Converter o número decimal 123 para o código Excesso de 3:

1. Converte 1 para 0100 (binário natural) + 3 = 0111.
2. Converte 2 para 0101 (binário natural) + 3 = 0110.
3. Converte 3 para 0110 (binário natural) + 3 = 0111.
4. Concatena os resultados: 0111 0110 0111.

O número decimal 123 no código Excesso de 3 é 0111 0110 0111.

## Gray
É usado para evitar erros na representação de uma sequência de numeros em um circuito digital, ele muda apenas um bit entre dois números sucessivos na sequência.

Decimal | Binário | Código Gray
------- | -------- | --------
0 | 000 | 000
1 | 001 | 001
2 | 010 | 011
3 | 011 | 010
4 | 100 | 110
5 | 101 | 111
6 | 110 | 101
7 | 111 | 100

* Para converter um número decimal maior que 7, basta converter cada dígito decimal individualmente e concatenar os resultados.

### Exemplo

Converter o número decimal 5 para binário e código Gray de 3 bits:

1. Converte 5 para 101 em binário.
2. O código Gray de 101 é 111.

O número decimal 5 em binário de 3 bits é 101, e em código Gray de 3 bits é 111.

## Byte
Sequência de oito bits

## ASCII
É um código de 7 bits, 2^7 = 128 representações codificadas.</br>
Usado para transferir informações entre computadores e dispositivos de entrada e saída.

### Alfabeto ASCII de 7 bits

| Caractere | Código ASCII |
|---|---|
| A | 01000001 |
| B | 01000010 |
| C | 01000011 |
| D | 01000100 |
| E | 01000101 |
| F | 01000110 |
| G | 01000111 |
| H | 01001000 |
| I | 01001001 |
| J | 01001010 |
| K | 01001011 |
| L | 01001100 |
| M | 01001101 |
| N | 01001110 |
| O | 01001111 |
| P | 01010000 |
| Q | 01010001 |
| R | 01010010 |
| S | 01010011 |
| T | 01010100 |
| U | 01010101 |
| V | 01010110 |
| W | 01010111 |
| X | 01011000 |
| Y | 01011001 |
| Z | 01011010 |

**Observações:**

* Os caracteres em minúsculas são representados com o mesmo código ASCII, mas com o bit 6 definido como 1.
* Os códigos ASCII de 0 a 31 e de 127 a 255 são reservados para caracteres de controle e não são representados como caracteres visíveis.

## Detecção de erros

### Bit de paridade
É um bit extra anexado ao conjunto de bits de código a ser transferido de uma localidade para outra

- Paridade par: o valor do bit de paridade é determinado para qe o número total de 1s conconjunto, incluindo o bit de paridade, seja um número par;
- Paridade impar: é usado da mesma forma, mas para que o conjunto de bits incluindo o de paridade de um número impar.

Quando se usa o método de paridade deve haver uma concordância entre o transmissor e o receptor entre o tipo de paridade, par ou ímpar.