# Teoria de eletronica digital

## Representação numérica
Analógica -> contínua

Digital -> discreta

## Sistemas
Analógico 
- quantidades físicas

Digital
- quantidades físicas
- informações lógicas

## Conversões

### Decimal
> multiplicar cada digito pelo seu peso

### Binário
> "jogar 21"

> dividir por 2 e armazenar os restos, parte fracionária multiplicar por 2

### Octal

> dividir por 8 e armazenar os restos


| Digito Octal | Equivalente Binario |
|--------------|---------------------|
|      0       |        000          |
|      1       |        001          |
|      2       |        010          |
|      3       |        011          |
|      4       |        100          |
|      5       |        101          |
|      6       |        110          |
|      7       |        111          |

### Hexadecimal
> dividir por 16 e armazenar os restos

| Digito Hexa | Equivalente Binario |
|--------------|---------------------|
|      0       |        0000          |
|      1       |        0001          |
|      2       |        0010          |
|      3       |        0011          |
|      4       |        0100          |
|      5       |        0101          |
|      6       |        0110          |
|      7       |        0111          |
| 8 |1000
| 9 |1001
|A|1010
|B|1011
|C|1100
|D|1101
E|1110
F|1111

## Aritmética

### Binária

Adição
>0+0=0 </br> 0+1=1 </br> 1+1=0 carry 1 </br> 1+1+1=1 carry 1

Subtração
>0-0=0 </br> 0-1=0 carry 1 </br> 1-0=1 </br> 1-1=0

Multiplicação e Divisão
> segue o modelo decimal

#### Complemento de 2
> binário </br> inverte 0s e 1s </br> +1

sinal | bit
---|---
positivo | 0
negativo | 1

- **Overflow** é diferente de estouro de bit
    > (+)+(+)=(-) </br> (-)+(-)=(+)

## Portas lógicas

### AND

x = A . B

| A | B | X |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

<img src="/FGA0073-TED/imagens/portaAND.png" alt="porta lógica AND">

### OR

x = A + B

| A | B | X |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

<img src="/FGA0073-TED/imagens/portaOR.png" alt="porta lógica OR">

### NOT

X = Ā (ou NOT A)

| A | x=Ā |
|---|---|
| 0 | 1 |
| 1 | 0 |

<img src="/FGA0073-TED/imagens/portaNOT.png" alt="porta lógica NOT">

## Simplificação booleana

<img src="/FGA0073-TED/imagens/resumoALGEBRA.png" alt="Resumo boole">

## Mapa de Karnaugh
### 2 variáveis
<img src="/FGA0073-TED/imagens/resumoMAPA2.png" alt="2 variáveis">

### 3 variáveis
<img src="/FGA0073-TED/imagens/resumoMAPA3.png" alt="3 variáveis">

### 4 variáveis
<img src="/FGA0073-TED/imagens/resumoMAPA4.png" alt="4 variáveis">