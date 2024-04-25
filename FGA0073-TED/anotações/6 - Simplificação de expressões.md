# Simplificação de expressões booleanas

## Álgebra de Boole

### Postulados

#### Postulado da complementação

O bloco lógico que executa o postulado da complementação é o **inversor**.

> A=0->!A=1

> A=1->!A=0

> **!A=A**

#### Postulado da adição

> 0+0=0

> 0+1=1

> 1+0=1

> 1+1=1

#### Postulado da multiplicação

> 0.0=0

> 0.1=0

> 1.0=0

> 1.1=1

### Propriedades

#### Propriedade comutativa

- Adição:
> A+B=B+A

- Multiplicação:
> A.B=B.A

#### Propriedade associativa

- Adição:
> A+(B+C)=(A+B)+C=A+B+C

- Multiplicação:
> A.(B.C)=(A.B).C=A.B.C

#### Propriedade distributiva

> A.(B+C)=A.B+A.C

### Teoremas de Morgan

1. O complemento do produto é igual à soma dos complementos

    > (!(A.B))=!A+!B

2. O complemento da soma é igual ao produto dos complementos

    > !A.!B=(!(A+B))

### Identidades auxiliares

> A+A.B=A

> (A+B).(A+C)=A+B.C

> A+!A.B=A+B

### Resumo

<img src="/FGA0073-TED/imagens/resumoALGEBRA.png" alt="Resumo">

## Mapa de Karnaugh

### Construção

Diagrama:

|  | !B | B |
|---|---| --- |
| **!A** |  |  |
| **A** |  |  |

Possibilidades:

1. A=1

|  | !B | B |
|---|---| --- |
| **!A** |  |  |
| **A** | **-** | **-** |

2. A=0(!A=1)

|  | !B | B |
|---|---| --- |
| **!A** | **-** | **-** |
| **A** |  |  |

3. B=1

|  | !B | B |
|---|---| --- |
| **!A** |  | **-** |
| **A** |  | **-** |

4. B=0(!B=1)

|  | !B | B |
|---|---| --- |
| **!A** | **-** |  |
| **A** | **-** |  |

Tabela verdade

| A | B || S
|---|---|---|---|
| 0 | 0 | caso 0 | 0 |
| 0 | 1 | caso 1 | 1 |
| 1 | 0 | caso 2 | 1 |
| 1 | 1 | caso 3 | 1 |

caso 0: A=0 e B=0, no diagrama é a intersecção entre A=0 e B=0, também chamada de !A.!B

|  | !B | B |
|---|---| --- |
| **!A** | **-** |  |
| **A** |  |  |

Representação completa:

|  | !B | B |
|---|:---:| :---: |
| **!A** | caso 0 | caso 1  |
| | !A !B | !A B |
| | 0 0 | 0 1 |
| **A** | caso 2 | caso 3  |
| | A !B | A B |
| | 1 0 | 1 1 |

|  | !B | B |
|---|---| --- |
| **!A** | 0 | 1 |
| **A** | 1 | 1 |

> Os 0s e 1s são colocados de acordo com a sua posição na tabela verdade;

### Simplificação

- Formar somente agrupamentos multiplos de 2^n;
- Formar o menor número de agrupamentos possíveis;
- Cada agrupamento deve conter o maior número de elementos possíveis;

#### Análise de agrupamentos

- Variáveis nas formas complementada e não complementada m um agrupamento é elimidada;
- Variáveis que não se alteram para todos os quadros devem ser mantidas;
- A expressão final é obtida da soma de todos os termos de cada agrupamento;

### 2 variáveis:

**Quadra:** 

S=1
|  | !B | B |
|---|---| --- |
| **!A** | 1 | 1 |
| **A** | 1 | 1 |

**Pares:** 

Par A
|  | !B | B |
|---|---| --- |
| **!A** | 0 | 0 |
| **A** | 1 | 1 |

Par !B
|  | !B | B |
|---|---| --- |
| **!A** | 1 | 0 |
| **A** | 1 | 0 |

**Termos isolados:**

|  | !B | B |  |
|---|---| --- | --- |
| **!A** | 0 | 1 | Termo !AB
| **A** | 1 | 0 | Termo A!B


#### Exemplo:

| A | B | S |
|---|---|---|
| 0 | 0 | 0 |
| 0 | 1 | 1 |
| 1 | 0 | 1 |
| 1 | 1 | 1 |

S= !AB + A!B +AB

|  | !B | B |
|---|---| --- |
| **!A** | 0 | 1 |
| **A** | 1 | 1 |

Par 1: A=1

Par 2: B=1

S= Par 1 + Par 2

S= A + B

### 3 variáveis:

**Oitava:**

S=1
|  | !B | !B | B | B |
|---|---|---|---|---|
| **!A** | 1 | 1 | 1 | 1 |
| **A** | 1 | 1 | 1 | 1 |
| | **!C** | **C** | **C** | **!C** |

**Quadras:**

!A
|  | !B | !B | B | B |
|---|---|---|---|---|
| **!A** | 1 | 1 | 1 | 1 |
| **A** | 0 | 0 | 0 | 0 |
| | **!C** | **C** | **C** | **!C** |

!B
|  | !B | !B | B | B |
|---|---|---|---|---|
| **!A** | 1 | 1 | 0 | 0 |
| **A** | 1 | 1 | 0 | 0 |
| | **!C** | **C** | **C** | **!C** |

C!
|  | !B | !B | B | B |
|---|---|---|---|---|
| **!A** | 1 | 0 | 0 | 1 |
| **A** | 1 | 0 | 0 | 1 |
| | **!C** | **C** | **C** | **!C** |

**Pares:**

!A!C
|  | !B | !B | B | B |
|---|---|---|---|---|
| **!A** | 1 | 0 | 0 | 1 |
| **A** | 0 | 0 | 0 | 0 |
| | **!C** | **C** | **C** | **!C** |

AC
|  | !B | !B | B | B |
|---|---|---|---|---|
| **!A** | 0 | 0 | 0 | 0 |
| **A** | 0 | 1 | 1 | 0 |
| | **!C** | **C** | **C** | **!C** |

**Termos isolados:**

|  | !B | !B | B | B | |
|---|---|---|---|---|---|
| **!A** | 0 | 1 | 0 | 1 |  |
| **A** | 0 | 0 | 1 | 0 |
| | **!C** | **C** | **C** | **!C** |
|||!A!BC|ABC|!AB!C|

#### Exemplo:

<img src="/FGA0073-TED/imagens/exemploMAPA3.jpg" alt="Exemplo">

### 4 variáveis:

<img src="/FGA0073-TED/imagens/exemploMAPA4.jpg" alt="Exemplo">
