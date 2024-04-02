# Sistemas de numeração e códigos

## Sistema de numeração decimal
460,13₇ 
- b=7 (é a base)
- q-1=2 (é a posição máxima a esquerda)
- p=-2 (é a posição máxima a direita)

460,13₇ = 238,14285714₁₀

### Exemplos de conversão para decimal
1110,1₂ = </br>
1x2^3 + 1x2^2 + 1x2^1 + 0x2^0 + 1x2^-1 </br>
8 + 4 + 2 + 0 + 0,5 = 14,5₁₀ </br>
</br>
321₄ </br>
3x4^2 + 2x4^1 + 1x4^0 </br>
48 + 8 + 1 = 57₍₁₀₎</br>
</br>
88,101₉ </br>
8x9^1 + 8x9^0 + 1x9^-1 + 0x9^-2 + 1x9^-3 </br>
72 + 8 + 1/9 + 0 + 3/9 = 80.4444444444₍₁₀₎ </br>
</br>
51₅ </br>
Não é possível converter pq o 5 não esta incluso nos números da base 5, apenas de 0 a 4, para que sejam 5 digitos.

## Sistema de numeração binário

### Conversão decimal-binario
#### método 1
soma de pesos dos bits nas posições(jogar 21)</br>
45₍₁₀₎ =  1   0   1   1   0   1</br>
         2^5 2^4 2^3 2^2 2^1 2^0</br>
          32  16  8   4   2   1</br>
</br>
32 + 8 = 40 + 4 = 44 + 1 = 45</br>

#### método 2
inicio -> dividir por 2 -> gravar o quociente (Q) e o resto (R) -> Q=0?:
- sim: agrupe os Rs no número binário desejado, o primeiro R como LSB e o último como MSB (de baixo pra cima)
- não: volte a dividir por 2 e refazer o ciclo

### Exemplo com as 2 metodologias
m1:</br>
83₍₁₀₎ = </br>
      1  0   1   0   0   1   1</br>
2^7 2^6 2^5 2^4 2^3 2^2 2^1 2^0</br>
128 64  32  16  8   4   2   1</br>
</br>
m2:</br>
83/2 = 41 r=1</br>
41/2 = 20 r=1</br>
20/2 = 10 r=0</br>
10/2 = 5 r=0</br>
5/2= 2 r=1</br>
2/2 = 1 r=0</br>
1010011</br>

### números decimais fracionários em binário
parte inteira: divisões sucessivas por 2 </br>
parte fracionaria: multiplicação sucessiva por 2 </br>
</br>
33,2₍₁₀₎</br>
</br>
33/2 = 16 r=1</br>
16/2 = 8 r=0</br>
8/2 = 4 r=0</br>
4/2 = 2 r=0</br>
2/2= 1 r=0</br>
33₍₁₀₎=100001</br>
</br>
0,2x2=0,4</br>
0,4x2=0,8</br>
0,8x2=1,6</br>
0,6x2=1,2</br>
0,2x2=0,4</br>
          _____</br>
0,2₍₁₀₎=0,0011</br>
                  ____</br>
33,2₍₁₀₎ = 100001,001</br>

## Sistema de numeração hexadecimal
0 - 9 : igual o sistema decimal</br>
10 - 15 : A, B, C, D, E, F</br>

### Conversão hexadecimal-decimal
2AF = 15x16^0 + 10x16^1 +2x16^2 </br>

### Conversão decimal-hexadecimal
divisões sucessivas por 16</br>
para descobrir o resto com a calculadora devemos multiplicar a parte fracionaria por 16</br>
</br>
423/16 = 26 r=7</br>
26/16 = 1 r=10</br>
=1A7</br>

### Conversão hexadecimal-binario
cada digito do hexa vai ser convertido em 4 bits de binario, podendo adicionar 0 na frente para completar os 4 digitos</br>
9F2 = 1001 1111 0010</br>
</br>
9 = 1001</br>
9/2 = 4 r=1</br>
4/2 = 2 r=0</br>
2/2 = 1 r=0</br>
</br>
F = 1111</br>
15/2 = 7 r=1</br>
7/2 = 3 r=1</br>
3/2 = 1 r=1</br>
</br>
2 = 0010</br>
2/2 = 1 r = 0</br>
</br>

### Conversão binario-hexadecimal
busca o bit menos significativo, caso sobrem bits deve-se adicionar 0, e converter usando o peso de cada casa</br>
1110100110</br>
</br>
0 0 1 1</br>
8 4 2 1</br>
0x8 + 0x4 + 1x2 + 1x1</br>
= 3</br>
</br>
1 0 1 0</br>
8 4 2 1</br>
1x8 + 1x2 = A</br>
0 1 1 0 </br>
8 4 2 1</br>
1x4 + 1x2</br>
= 6</br>
</br>
=3A6

## Sistema de numeração octal

### Conversão octal-decimal
372₈ = 3x8^2 + 7x8^1 + 2x8^0</br>
= 3x64 + 7x8 + 2x1</br>
=250</br>
</br>
24,6₈ = 2x8^1 + 4x8^0 + 6x8^-1</br>
= 2x8 + 4x1 + 3/4</br>
= 20,75</br>

### Conversão decimal-octal
divisões sucessivas por 8</br>
</br>
266₁₀</br>
266/8 = 33 r=2</br>
33/8 = 4 r=1</br>
4/8 = 0 r=4</br>
412₈</br>

### Conversão octal-binario
cada digito do octal vai ser convertido em 3 bits de binário</br>
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
</br>
165₈ = 001110101₂</br>
1 = 001</br>
6 = 110</br>
5 = 101</br>

### Conversão binario-octal
100111010₂ = 472₈</br>
010 = 2</br>
111 = 7</br>
100 = 4</br>