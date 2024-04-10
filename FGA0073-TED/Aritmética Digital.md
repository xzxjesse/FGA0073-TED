# Aritmética Digital: Operações e Circuitos

# parte 1

## Adição binária
0+0=0</br>
1+0=1</br>
1+1=10 (0 + carry 1)</br>
1+1+1=11 (1 + carry 1)</br>

## Subtração binária
0-0=0</br>
0-1=1</br>
1-0=1</br>
1-1=0</br>

## Multiplicação binária
0x0=0</br>
0x1=0</br>
1x0=0</br>
1x1=0</br>

## Divisão binária
Segue o modelo da operação decimal, entretanto, só resulta em 0s e 1s

## Representação de números com sinal
**Sinal - módulo**</br>
Bit de sinal:</br>
positivo - </br>
negativo - 1</br>
</br>

**Complemento de 1**</br>
Substituindo cada bit do número pelo seu complemento, 0 por 1 e 1 por 0</br>
</br>

**Complemento de 2**</br>
É a soma de 1 ao complemento de 1 do número binário na posição do bit menos significativo</br>

- exemplo:
101101 binário</br>
010010 complemento de 1</br>
    +1 adiciona 1 para formar o complemento de 2</br>
______</br>
010011 complemento de 2 do número binário original</br>
</br>
- positivo: é representado na forma binária direta e um bit de sinal 0 é colocado na frente do MSB
</br>
- negativo: é representado na forma de complemento de 2 e um bit de sinal 1 é colocado na frente do MSB
</br>
exemplo:</br>
 0  101101</br>
(+) binário direto</br>
</br>
 1  010011</br>
(-) complemento a 2</br>
</br>

**Extensão de sinal** </br>
sistemas tem registradores múltiplos de pres de 4 bits</br>
em 8 bits:</br>
1 bit representa o sinal</br>
7 bits representam o número</br>
</br>
no caso de um número menor que o registrador:</br>
número positivo: adicione 0s</br>
número negativo: adicione 1s</br>

- exemplo
9 com 5 bits em um registrador de 8 bits</br>
+9 = 00001001</br>
-9 = 11110111</br>

**Negação**
conversão de sinais</br>

- exemplo:
+9 = 01001 binário original com o sinal</br>
-9 = 10111 complemento a 2 (negar)</br>
+9 = 01001 negar novamente</br>

# parte 2

## Adição e subtração no sistema de complemento de 2

1. determinar o complemento de 2 do número negativo
2. realizar a soma

- desconsiderar possíveis estouros de bits

### formas de realizar:
1. notação com bit de sinal
- representar número em binário puro
- verificar quantidade de bits
- tratar números negativos (complemento de 2)
- realizar soma binária
- desconsiderar estouro de bits
- verificar bit de sinal do resultado
    resultado negativo: determinar o complemento de 2

exemplo, considerando 8 bits: </br>
+ 32 = 00100000 </br>
- 45 = 01010011 </br>
________________ </br>
       01110011 </br>
       10001100 </br>
             +1 </br>
________________ </br>
        1001101

2. notação sem bit de sinal
- representar os números em binário puro
- verificar a quantidade de bits
- tratar números negativos (complemento de 2)
- realizar soma binária
- desconsiderar estouro de bits
- verificar sinal do resultado
    resultado negativo: determinar o complemento de 2

**->COMPLEMENTAR 2 NESSE CASO SERIA ADICIONAR 1 AO INVERSO OU TIRAR 1 DO INVERSO?** 

## Overflow aritmético
acontece apenas quando dois números negativos ou dois positivos são somados, e sempre vão resultar em sinal e magnitude incorretas

- Como identificar: Examinando o bit de sinal do resultado e comparando com o do resultado

## Representação em ponto flutuante
representa números muito grandes ou muito pequenos sem aumento de bits

- mantissa: magnitude do número
- expoente: número de casas decimais que a virgula é movida

| precisão | sinal | expoente(+/-) | significando |
|----------|-------|---------------|--------------|
| simples  |   1   |       8       |      23      |
| 32 bits  | bit31 |   bit30-23    |  bit22-00    |
|----------|-------|---------------|--------------|
| dupla    |   1   |      11       |      52      |
| 64 bits  | bit63 |   bit62-52    |  bit51-00    |

## Adição em BCD

1. Usando a adição binária comum, come os grupos de código BCD para cada posição de dígito
2. Para as posições onde a soma é menor ou igual a 9, nenhuma correção é necessária. O resultado está na forma BCD apropriada
3. Quando a soma dos dois dígitos é maior que 9, o fator de correção 0110 deve ser adicionado para obter o resultado na forma BCD correta. Este caso sempre produz um carry para a próxima posição, seja da adição original, seja da adição de correção

## Representação de hexa com sinal
**-> ?** 

### Adição em hexa

1. some os dois dígitos hexa em decimal, inserindo mentalmente o decimal equivalente para os dígitos maiores do que 9
2. se a soma é menor ou igual a 13, ele pode ser expresso por um dígito hexadecimal
3. se a soma é maior ou igual a 16, subtrais 16 e coloque um carry na próxima posição

### Subtração em hexa

1. 
- numero hexadecimal
- converte para binário
- toma o complemento a 2
- converte de volta para hexadecimal

2. 
- subtrais cada dígito de F
- soma 1
- você terá o equivalente hexadecimal do complemento a 2