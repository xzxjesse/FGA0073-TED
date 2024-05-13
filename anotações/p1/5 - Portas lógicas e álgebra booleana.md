# Portas lógicas e álgebra booleana

## parte 1

### Constantes e variáveis booleanas

| Nível Lógico 0 | Nível Lógico 1 |
|---|---|
| falso | verdadeira |
| desligado | ligado |
| baixo | alto |
| não | sim |
| chave aberta | chave fechada |

### Tabelas-verdade

| A | B | C | X |
|---|---|---|---|
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

### Expressões booleanas:

#### AND

x = A . B

| A | B | X |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

![porta lógica AND](/imagens/portaAND.png)

- É a multiplicação ordinária de 0s e 1s;
- A saída é igual a 1 quando todas as entradas forem iguais a 1;
- A saída é 0 para o caso em que uma ou mais entradas são iguais a 0;
- Uma porta AND é um circuito lógico que realiza a operação AND nas entradas do circuito.

#### OR

x = A + B

| A | B | X |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

![porta lógica OR](/imagens/portaOR.png)

- Produz o resultado 1 quando qualquer variável for igual a 1;
- Produz o resultado 0 quando todas as variáveis forem iguais a 0;
- A porta OR é um circuito lógico que realiza a operação OR sobre as entradas lógicas do circuito.

#### NOT

X = Ā (ou NOT A)

| A | x=Ā |
|---|---|
| 0 | 1 |
| 1 | 0 |

![porta lógica NOT](/imagens/portaNOT.png)

> onde o pequeno círculo denota inversão

#### Resumo das operações booleanas:

**OR:**

| Entrada | Saída |
|---|---|
| 0 + 0 | 0 |
| 0 + 1 | 1 |
| 1 + 0 | 1 |
| 1 + 1 | 1 |

**AND:**

| Entrada | Saída |
|---|---|
| 0.0 = 0 | 1 |
| 0.1 = 0 | 0 |
| 1.0 = 0 | 0 |
| 1.1 = 1 | 1 |

**NOT:**

| Entrada | Saída |
|---|---|
| 0 | 1 |
| 1 | 0 |

### Outras portas

#### NAND
Inversão da porta AND

| A | B | X |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

![porta lógica NAND](/imagens/portaNAND.png)

#### NOR
Inversão da porta OR

| A | B | X |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 0 |

![porta lógica NOR](/imagens/portaNOR.png)

### Blocos lógicos 

#### OU exclusivo (XOR)

| A | B | X |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 0 |

![bloco lógico XOR](/imagens/blocoXOR.png)

- tem apenas duas entradas

**Função ou exclusivo:** assume 1 quando as variáveis assumirem valores diferentes entre si.

> X = (!A.!B) + (A.B)

#### NOU exclusivo (XNOR)

| A | B | X |
|---|---|---|
| 0 | 0 | 1 |
| 0 | 1 | 0 |
| 1 | 0 | 0 |
| 1 | 1 | 1 |

![bloco lógico XNOR](/imagens/blocoXNOR.png)

- tem apenas duas entradas

**Função coincidência:** assume 1 quando houver coincidência entre os valores das variáveis.

> X = (!A.B) + (A.!B)

### MOS
Circuitos eletrônicos que utilizam **MOSFETs** (Metal-Oxide-Semiconductor Field-Effect Transistors) como componentes básicos. </br>

MOSFETs são transistores de efeito de campo onde a condução de corrente é controlada pelo campo elétrico aplicado a um terminal chamado gate/porta. </br>

1. Inversor CMOS:

- É o circuito CMOS mais básico.
- Realiza a operação lógica **NOT (NÃO), invertendo o sinal de entrada.**
- Utiliza um único transistor, podendo ser **um NMOS ou PMOS**, dependendo do projeto específico.
- Quando a entrada está em 0 (terra), a saída do inversor fica em 1 (próxima da tensão de alimentação).
- Quando a entrada está em 1 (próxima da tensão de alimentação), a saída do inversor fica em 0 (terra).

2. Porta NAND CMOS:

- Realiza a operação lógica **NAND**.
- A saída da porta NAND é verdadeira (1) somente quando ambas as entradas são falsas (0).
- Utiliza uma **combinação de transistores NMOS e PMOS** ligados em paralelo (para a rede pull-down) e em série (para a rede pull-up).
- Quando pelo menos uma entrada está em 1, o caminho de corrente pull-up é habilitado, forçando a saída a 0.
- Somente quando ambas as entradas estão em 0, o caminho pull-down é ativado, conectando a saída à terra (0).

## parte 2

### Representação de circuitos e expressões booleanas

**Procedimento para projetar um circuito**
1. Problema
2. Análise do problema
3. Tabela verdade
4. Expressão lógica
5. Circuito lógico


### Descrevendo circuitos lógicos algebricamente

**Procedência de operador:** para evitar confusão é necessário entender a prioridade de operações (AND -> OR), ou usar parênteses.

**Tabelas verdade obtidas de expressões booleanas**
- Permite que se analise uma porta ou uma combinação lógica de cada vez;
- Permite que se confira facilmente o trabalho;
- Quando o trabalho se encerra, dispõem de uma tabela que ajuda a verificação de erros do circuito lógico.

**Procedimento:**
1. Montar o quadro de possibilidades
2. Montar colunas para os vários membros da expressão
3. Preenchemos essas colunas com os resultados
4. Montar uma coluna para os resultados finais
5. Preencher essa coluna com oss resultados finais

**Exemplo:** x = ĀB + BC

| A | B | C | Ā | ĀB | BC | ĀB+BC |
|---|---|---|---|----|----|-------|
| 0 | 0 | 0 | 1 |  1 |  0 |   0   |
| 0 | 0 | 1 | 1 |  0 |  0 |   0   |
| 0 | 1 | 0 | 1 |  0 |  0 |   0   |
| 0 | 1 | 1 | 1 |  1 |  1 |   1   |
| 1 | 0 | 0 | 0 |  0 |  0 |   0   |
| 1 | 0 | 1 | 0 |  0 |  0 |   0   |
| 1 | 1 | 0 | 0 |  0 |  0 |   0   |
| 1 | 1 | 1 | 0 |  1 |  1 |   1   |

[Exercícios](https://docs.google.com/spreadsheets/d/1hrmsPwJVw_XwoI_RSojuriU9ucpwFBRE-OfaqmjoqpY/edit?usp=sharing)