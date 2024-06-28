# Resumo

## Implementação de função em Multiplex
**1 - Construir a tabela verdade os valores da expressão e F como saída**

**2 - Descobrir quando vai ser 1 na saída**

1. analisar cada and e a letra não inclusa é "tanto faz", ou seja, assume 1 e assume 0 como valor
2. vai ser 1 na tabela em todos os valores tirados da expressão

ex.:

|!A| - |!C|D|
|---|---|---|---|
|0|**0**|0|1|
|0|**1**|0|1|

esses 2 casos vão receber F=1

**3 - Desenhar o Multiplex com a quantidade de canais solicitados**

1. Se a quantidade de canais for igual a quantidade de linhas da tabela:
    - entradas viram "chaves" embaixo
    - linhas da tabela viram canais, onde:
        - F=1 -> conecta no 5V
        - F=0 -> conecta no terra
    - Saida é Z

2. Se a quantidade de canais for a metade da quantidade de linhas da tabela:
    - entradas mais significativas viram as "chaves" embaixo
    - entrada menos significativa vai ser analisada de acordo com F para definir os canais
        - se D=F -> i=D
        - se independente de D, F=0 -> i=0
        - se independente de D, F=1 -> i=1
        - se D=!F -> i=!D
    - Saida é Z

## Analise e desenho de FF 

### Síncrono
- **Configuração básica**
    1. clock comum a todos os ff 
    2. j e k do primeiro ff em 1 
    3. a partir do 2°FF todas as entradas j e k serão a saída de uma AND das saídas dos FF anteriores

#### Se básico
Modulo = 2^numFF

0-15
#### Se não básica
1. Identificar as operações que fazem a entrada de cada FF
2. Tabela de estado atual e próximo

|Estado atual|Controladores|Próximo estado|
|:---:|:---:|:---:|
|CBA|Jc-Kc-Jb-Kb-Ja-Ka|CBA|
|000|0--0--0--0--1--1|001|
|001|0--0--1--1--1--1|010|
|010|
|011|
|100|
|101|
|110|
|111|

**Tabela verdade dos FF:**

*Qa é o estado anterior -> atual*

![FF SR negativo](/imagens/FF%20SR%20negativo.png)

![FF JK](/imagens/FF%20JK.png)

x = A . B

| A | B | X |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

x = A + B

| A | B | X |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

3. Desenhar a tabela, pode ser em bin ou dec

### Assíncrono
#### Configuração básica
1. todos os J=K=1
2. Pulso de CLK só no primeiro FF
3. Saída Q do FF conectado ao CLK do FF seguinte

#### Se básico
1. Descobrir número que aciona a NAND
    1. entradas da NAND = 1
    2. FF restantes = 0
    3. **bin formado aciona a NAND e é o Módulo e tem transição pontilhada pra ele**
    4. os seguintes tambem ficam fora
2. Desenhar

#### Se não básica
##### Se tirar a NAND, é básica
1. Descobrir número que aciona a NAND
    1. entradas da NAND = 1
    2. FF restantes = 0
    3. **bin formado aciona a NAND e é o Módulo e tem transição pontilhada pra ele**
2. Avaliar cada possibilidade

## Escolha de FF para circuito
***Se o tempo de hold e de propagação forem muito próximo podemos ter problemas***
1. Síncrono
    1. Frequência minima que deve funcionar
    2. Analisar propagação

        Fmax = 1/TpropFF+TpropAND

    3. Tempo de CLK
    
        Tclk >= N*TpropFF+TpropAND
2. Assíncrono
    1. Frequência minima que deve funcionar
    2. Analisar propagação

        Fmax = 1/N*TpropFF

    3. Tempo de CLK
    
        Tclk >= N*TpropFF

## Projetar circuito

1. **Quantos FF são necessários?**
    1. Qual é o maior num que aparece no diagrama?
    2. Converte o num pra binário.
    3. Quantidade de digitos vai ser a quantidade de FF.
2. **Tabela de estado atual e próximo estado**
3. **Tabela com a excitação dos FF**

|caso|estado atual|estado atual|proximo estado|Jc|Kc|Dd
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
||Chave_A - Chave_B|FF_C - FF_D|FF_C - FF_D|
|a|0 - 0|0 - 0|0 - 1|0|x|1
|a|0 - 0|0 - 1|1 - 0|1|x|0
|a|0 - 0|1 - 0|1 - 1|x|0|1
|a|0 - 0|1 - 1|0 - 0|x|1|0
|b|0 - 1|0 - 0|0 - 1|0|x|1
|b|0 - 1|0 - 1|1 - 0|1|x|0
|b|0 - 1|1 - 0|0 - 0|x|1|0
|b|0 - 1|1 - 1|0 - 0|x|1|0
|c|1 - 0|0 - 0|1 - 1|1|x|1
|c|1 - 0|0 - 1|0 - 0|0|x|0
|c|1 - 0|1 - 0|1 - 1|x|0|1
|c|1 - 0|1 - 1|0 - 0|x|1|0
|d|1 - 1|0 - 0|1 - 1|1|x|1
|d|1 - 1|0 - 1|1 - 1|1|x|1
|d|1 - 1|1 - 0|0 - 1|x|1|1
|d|1 - 1|1 - 1|1 - 0|x|0|0


***Tabela de excitação JK***
|Qa|Q|J|K|
|---|---|---|---|
|0|0|0|x|
|0|1|1|x|
|1|0|x|1|
|1|1|x|0|

***Tabela de excitação D***
|Qa|Q|D|
|---|---|---|
|0|0|0|
|0|1|1|
|1|0|0|
|1|1|1|

***Tabela de excitação T***
|Qa|Q|T|
|---|---|---|
|0|0|0|
|0|1|1|
|1|0|1|
|1|1|0|

4. **Mapa de Karnaugh para cada entrada do FF**

### Mapa de Karnaugh
#### 2 variáveis

![2 variáveis](/imagens/resumoMAPA2.png)

#### 3 variáveis
![3 variáveis](/imagens/resumoMAPA3.png)

#### 4 variáveis
![4 variáveis](/imagens/resumoMAPA4.png)

5. **Desenhar FFs**
6. **Conectar expressões dos Mapas de Karnaugh**