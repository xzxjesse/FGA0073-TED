# Conceitos Introdutórios

## Sistemas Digitais
Conjunto de dispositivos que manipulam informações lógicas ou quantidades físicas, que estão representadas digitalmente.

## Reprentação Numérica
| Analógica | Contínua   |
|-----------|------------|
| Digital   | Discreta   |

## Sistemas

- Digital
    > Manipulam informação lógica e quantidade física representada no formato digital.
- Analógico
    > Manupulam quantidades físicas representadas no formato analógico.

## Sistemas de numeração digital

### Sistema Decimal
Composto por **10 numerais ou símbolos**. </br>
Tem valor **posicional**.

> MSD-> Most Significant Digit
> LSD-> Least Significant Digit
| MSD |     |     |     |     |     |     | LSD |
| 2   | 7   | 4   | 5   |  ,  | 2   | 1   | 4   |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 10^3| 10^2| 10^1| 10^0|     | 10^-1| 10^-2| 10^-3|

(2 x 10^+3) + (7 x 10^+2) + (4 x 10^+1) + (5 x 10^+0) + (2 x 10^-1) + (1 x 10^-2) + (4 x 10^-3) = 2745,214

### Sistema Binário
Composto por apenas **2 dígitos**, 0 e 1.</br>
Níveis de **tensão** - Alto e baixo</br>
Tem valor **posicional**.

- **BIT**: Binary digit

| MSB |     |     |     |     |     |     | LSB |
| 1   | 0   | 1   | 0   |  ,  | 1   | 0   | 1   |
|-----|-----|-----|-----|-----|-----|-----|-----|
| 2^3 | 2^2 | 2^1 | 2^0 |     | 2^-1| 2^-2| 2^-3|

(1 x 2+3) + (0 x 2+2) + (1 x 2+1) + (1 x 2+0) + (1 x 2-1) + (0 x 2-2) + (1 x 2-3) = 11,625

> Sistemas Digitais -> Informação na forma binária -> 2 Estados de operação

- Em sistemas eletrônicos digitais, a informação binária é representada em termos da tensão (ou correntes) nos diversos circuitos
    - Na prática são representados por uma faixa de valores
    > Bit 1 → 2 a 5 volts
    > Tensões inválidas
    > Bit 0 → 0 a 0,8 volts
