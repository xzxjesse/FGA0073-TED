# Aula 23 - Contadores Síncronos ou Paralelos
sinal de clock é comum nos FF e eles são disparados simultaneamente (em paralelo) pelos pulsos de clock de entrada.

- atraso existe e é fixo, mas não é propagado.
    - **atraso total** = tempo do propagação do ff + tempo de propagação de uma and

![sincronos](/imagens/sincronos.jpg)

- b muda quando a=1
- c muda quando b=a=1
- d muda quando c=b=a=1

- indesejado: os de nível alto de binário conecta na nand, a saída da nand joga nos clear e monta a configuração do circuito sincrono

### Procedimento geral
1. Determine o menor número de FF tal que 2^n >=X, e conecte-os como um contador. Se 2^n=X não faça os passos 2 e 3.
2. Conecte uma porta NAND nas entradas assíncronas de CLEAR de todos os FFs.
3. Determine quais FFs estarão no estado ALTO na contagem X; então conecte as saídas normais destes FFs nas entradas da porta NAND.

### Questão 5
![Q5](/imagens/Q5.png)
![resposta Q5](/imagens/resposta%20Q5.png)

#### tabela de estado ATUAL / PRÓXIMO estado

1. O primeiro passo é escrever a expressão lógica para a entrada de controle de cada FF.
2. Em seguida, estabeleça um estado ATUAL para o contador e aplique essa combinação de bits às expressões lógicas do controle.
3. As saídas das expressões de controle nos permitirão prever os comandos para cada FF e o PRÓXIMO estado resultante para o contador depois da aplicação do sinal de clock.
4. Repita esse processo até que toda a sequência de contagem seja determinada.

### Contador autocorretor
    é um contador em que estados normalmente não usados retornam à seqüência de contagem normal.

### Circuito com FF D e JK

![FF D e JK](/questões/p2/FF%20D%20e%20JK.png)

1. síncrono ou assíncrono? (sinal de clk pra todos = síncronos)

2. Requisitos
    1. clk pra todos
    2. j e k = 1 no primeiro ff
    3. j e k a partir do segundo só quando o ff anterior for 1

3. analisar a NAND

    o que não limpar nos ff com a nand vai gerar um num binário que é o modulo do circuito

    ![analise](/questões/p2/D%20e%20JK%20analise.png)

    ![modulo](/questões/p2/D%20e%20JK%20modulo.png)

### Projetar contador síncrono

1. Determine o número de bits necessários (número de flip-flops) e a seqüência de contagem desejada.

2. Desenhe o diagrama de transição de estados, mostrando todos os estados possíveis, inclusive aqueles que não fazem parte da sequência de contagem desejada.

3. Use o diagrama de transição de estados para construir uma tabela que relacione todos os estados ATUAIS e seus PRÓXIMOS estados.

4. Acrescente uma coluna a esta tabela para cada entrada Je K. Para cada estado ATUAL, indique os níveis necessários em cada entrada Je K para produzir a transição para o PRÓXIMO estado.

5. Projete os circuitos lógicos que forneçam os níveis necessários para cada entrada J e K.

6. Implemente as expressões finais.