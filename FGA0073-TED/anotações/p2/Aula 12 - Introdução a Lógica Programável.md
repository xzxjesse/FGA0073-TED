# Introdução a Lógica Programável
[Aula](https://www.youtube.com/watch?v=-IMIWvk2w5I)

## Dispositivos Lógicos Programáveis (PLD)
> são circuitos integrados programáveis pelo usuário, que possui um grande número de portas lógicas (AND, OR, NOT), flip-flops e registradores que estão ligados em um mesmo CI.

### Tipos de Dispositivos Lógicos Programáveis (PLDs)

- SPLDs (Simple Programmable Logic Devices)
    - **Programmable Array Logic (PAL)**: geralmente é programável somente uma vez
    
        <img src="/FGA0073-TED/imagens/PAL.png">

    - **Generic Array Logic (GAL)**: pode ser reprogramável
    
        <img src="/FGA0073-TED/imagens/GAL.png">

    > **Macrocélulas:** lógica de saída adicional em um arranjo

- CPLDs (Complex Programmable Logic Devices)
    > formado por vários SPLDs com interconexões programáveis chamadas de PIA (Programmable Interconnect Array) / IAM (Advanced Interconnect Matrix)

    - Cada SPLD vai ser chamado de LAB (Logic Array Block), bloco de função, bloco lógico ou bloco genérico.

    - Entradas conectadas ao LAB e saídas interconectadas a qualquer outro LAB pela PIA

    <img src="/FGA0073-TED/imagens/CPLD.jpg">

### Field Programmable Gate Array (FPGAs)

- CLB - bloco lógico configurável
    - é formado de múltiplos módulos lógicos menores e uma interconexão programável local que é usada para interconectar módulos dentro de uma CLB
- Interconexões
- Blocos de entrada/saída (Ao longo do perímetro)

> não usa estruturas PAL, GAL ou PLA.

    O módulo lógico pode ser configurado para lógica combinacional, lógica sequencial, ou ambos e utiliza o look-up table.

- LTU - look-up table
    - é um tipo de memória programável que gera funções lógicas combinacionais de soma de produtos.

- CL - célula lógica
    - é baseada na lógica LUT de quatro entradas tradicionais mais uma lógica adicional e um flip-flop

> Usam tecnologia volátil SRAM mas incluem memória de configuração não volátil que reconfigura o aparelho.

<img src="/FGA0073-TED/imagens/FGPA.jpg">

## Processo de programação

<img src="/FGA0073-TED/imagens/processo_de_programação.jpg">

<img src="/FGA0073-TED/imagens/processo_de_programação_2.jpg">

1. Entrada do projeto
2. Simulação funcional
3. Síntese
4. Implementação
5. Simulação de temporização
6. Download