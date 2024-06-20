# Aula 21 - Dispositivos Correlatos do FF

## Funcionamento de sistemas

### Assíncronos
    as saídas de circuitos lógicos podem mudar de estado a qualquer momento em que uma ou mais entradas mudem de estado

### Síncronos
    os momentos exatos em que uma saída qualquer pode mudar de estado são determinados por um sinal denominado clock

### Ciclo de clock
    é medido de uma borda de subida até a próxima borda de subida ou de uma borda de descida até a próxima borda de descida

- **Período (T):** tempo que ele leva para completar um ciclo (em segundos / ciclos)

- **Frequência do clock (Hz):** velocidade de um sistema digital, é normalmente representada pelo número de ciclos de clock que ocorrem em um segundo (ciclos / segundo)

- Entrada de clock: denominada **CLK, CK, CP**, é disparada por borda
(**é ativada pela transição do sinal de clock**) e indicada por um triângulo nessa entrada.

- **Entradas de controle**: uma ou mais e podem ter vários nomes, a depender do funcionamento. **Não terão efeito na saída Q até que uma transição ativa do clock ocorra.**

## FF S-R com clock
### Circuito Interno
![circuito interno](/imagens/Circuito%20interno%20FF%20SR.png)

### Disparado com borda positiva do CLK
![FF SR](/imagens/FF%20SR.png)

- Seta: borda de subida necessária na entrada CLK
- Q0: nível de saída Q antes da borda de subida do CLK

### Disparado com borda negativa no CLK
![FF SR negativo](/imagens/FF%20SR%20negativo.png)

## FF J-K com clock

![FF JK](/imagens/FF%20JK.png)

    Modo de comutação: J=K=1 não resulta em uma saída ambígua, o FF irá mudar para o estado lógico oposto no instante da transição positiva do sinal de CLK

### Circuito interno
![circuito interno](/imagens/Circuito%20interno%20FF%20JK.png)