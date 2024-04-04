# Aritmética Digital: Operações e Circuitos

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
</br>
- exemplo:
101101 binário</br>
010010 complemento de 1</br>
    +1 adiciona 1 para formar o complemento de 2</br>
______</br>
010011 complemento de 2 do número binário original</br>
</br>
- positivo: é representado na forma binária direta e um bit de sinal 0 é colocado na frente do MSB
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

**** correção representação binaria com complemento 2