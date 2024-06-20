# Aula 20 - Flip-Flops
dispositivos com memória volátil

informação armazenada enquanto o circuito estier energizado

## Cicuitos lógicos sequenciais
![circuitos sequenciais](/imagens/circuitos%20sequenciais.png)

## Flip-Flops (FF)
> O **FF** é diferente do **latch** pela forma de mudança de estados, os FF são pela mudança de estados e nos latch são por pulsos em entradas

    A maioria das entradas dos FFs precisa ser apenas momentaneamente ativada (pulsada) para provocar a mudança de estado na saída do FF, sendo que a saída permanece no novo estado após o pulso de entrada terminar.

- Entradas (sinal de clock, síncronas, assíncronas...)

- Q -> saída normal
    - 0: **clear ou reset**
    - 1: **set**

- !Q -> saída invertida

## Latch
1. entradas de repouso mantem o sinal anterior ate intervenção

2. basta colocar a entrada de repouso em 0 na entrada de set para ativar a saida normal Q

3. se retirar o pulso e mandar de volta para a saida de repouso, vai manter a saida normal Q no sinal anterior (1)

4. mesmo se mandar pulsos na entrada de set, vai manter Q no nivel anterior, alto

|SET|RESET|Q||
|:---:|:---:|:---:|---|
|0|0|inválida|
|0|1|1|
|1|0|Q|
|1|1|Qa |nível anterior|

## Latch com portas NAND

### Realimentação:
![Latch com portas NAND](/imagens/Latch%20com%20portas%20NAND.png)

|SET|RESET|Qa|Saída Normal - Q|
|:---:|:---:|:---:|:---:|
|0|0|0|inválido Q=Qa=1|
|0|0|1|inválido Q=Qa=1|
|0|1|0|1|
|0|1|1|1|
|1|0|0|0|
|1|0|1|0|
|1|1|0|0|
|1|1|1|1|

### Estado inicial

- carga externa
- tempo de propagação
- capacitância parasita

50% de chance de iniciar em 0 e 50% de iniciar em 1

-> ligar na entrada que precisa no circuito

### Sinal de ativação no Latch
-> **bolinha na entrada** do circuito representa que deve ser **ativada com nível baixo**

## Latch com portas NOR

![Latch com portas NOR](/imagens/Latch%20com%20portas%20NOR.png)

muda a ativação com relação a nand

# FAZER A ANALISE

## Resumo
![resumo latch](/imagens/resumo%20latch.png)