# Aula 22 - Contadores Assíncronos

## Contadores assíncronos
![Contadores assincronos](/imagens/contadores%20assincronos.png)

### Frequência
n: quantidade de FF
#### no último FF
1/2^n
#### padrão
Fclock/2^n
#### quando NAND força o clear
Fclock/modulo
#### máxima
1/n.t

### Procedimento geral
1. Determine o menor número de FF tal que 2^n >=X, e conecte-os como um contador. Se 2^n=X não faça os passos 2 e 3.
2. Conecte uma porta NAND nas entradas assíncronas de CLEAR de todos os FFs.
3. Determine quais FFs estarão no estado ALTO na contagem X; então conecte as saídas normais destes FFs nas entradas da porta NAND.

![Modulo e sequência](/questões/p2/modulo%20e%20sequencia.jpg)


### Diagrama de transição de estados
![Diagrama de estados](/imagens/diagrama%20de%20estados.jpg)

#### Módulo:
    quantidade de estados ESTÁVEIS diferentes na sequência de contagem

- para determinar a quantidade de FF, N, é necessário considerar 2N=>quantidade de estados/contagens, que vai ser o módulo do circuito

![contador de modulo <2^n](/imagens/contador%20de%20modulo%202^n.png)

#### Estado básico
1. J=K=1
2. Pulso de CLK só no primeiro FF
3. Saída Q do FF conectado ao CLK do FF seguinte

#### Spike ou glitch
    só é um problema em circuitos que controlam circuitos

# PROVA
- circuito pronto, tem que desenhar o diagrama de transição de estado e dizer o modulo

## NAND não limpando o FF C
![Questão de FF prova](/questões/p2/FF.png)

- cai no 5, e a nand limpa os 2 primeiros FF e manda pro 4; tem modulo 1, o loop é só no 4, 1 estado estavel no 4

![Diagrama do FF](/questões/p2/diagrama%20FF.png)

## NAND limpando só o FF C
![Questão de FF prova](/questões/p2/FF2.png)

![Diagrama do FF](/questões/p2/Diagrama%20FF2.png)

## Análise da NAND
    pega o estado, converte pra binario, vê os que estão sendo mudados e coloca na nand, se der 1 ele é estável, se der 0 (acionar a nand) é temporario

## Contadores assíncronos decrescente

### Na prática:
pegar só as saídas invertidas, mas conceitualmente não pode

### Forma correta:
inserir as saídas invertidas nos clocks

## Atraso de propagação em contadores assíncronos

![Atraso de propagação em contadores assíncronos](/questões/p2/Atraso%20de%20propagação%20em%20contadores%20assíncronos.jpg)