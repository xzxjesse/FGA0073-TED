# Aula 17 - Circuitos Lógicos MSI
MSI - Medium Scale Integrtion

> ativo significa 0

> representado por uma bolinha na saída do desenho esquemático

## Codificadores e Decodificadores
**Codificadores** são circuitos combinacionais que tornam possível a passagem de um código conhecido para um desconhecido, os **decodificadores** fazem o caminho inverso.

**Calculadora:**

    decimal - inserção pelo teclado
    |
    codificador
    |
    binário - processamento aritmético
    |
    decodificador
    |
    decimal - resultado no visor

### Decodificador Binário Básico

x = A3 . !A2 . !A1 . A0 = "1"

x = 1001

### Decodificador BCD / Decimal

4 entradas e 10 saídas

### Decodificador 4 Bits

4 entradas e 16 saídas

### Codificador Decimal / Binário

10 entradas e 4 saídas

## Decodificadores/Drivers BCD para 7 segmentos

**Display de sete segmentos**: é um invólucro com sete LEDs (diodos emissores de luz) com formato de segmento, posicionados de modo a possibilitar a formação de números decimais e algumas letras utilizadas no código hexadecimal.

**LED – Diodo Emissor de Luz**: 
- **Display catodo comum**: possui os catodos dos leds interligados, sendo necessário aplicar nível ALTO no anodo para acender cada segmento;
- **Display anodo comum**: possui os anodos dos leds interligados, sendo necessário aplicar nível BAIXO no catodo para acender cada segmento;

# ESTUDAR PARA PROVA

![Display de 7 segmentos](/questões/p2/BCD%207segmentos.png)

- **Montar mapas de Karnaugh**

![Display de 7 segmentos](/questões/p2/BCD%207%20segmentos.png)

![Display bcd 1](/questões/p2/display%20bcd%201.png)

![Display bcd 2](/questões/p2/display%20bcd%202.png)
## Comparadores de Magnitude
# ESTUDAR PARA PROVA