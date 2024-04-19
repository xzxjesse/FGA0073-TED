# Exercícios de Fixação
[Questões](https://engsoftmoderna.info/cap2.html#exercícios-de-fixação)

1. Como XP preconiza que devem ser os contratos de desenvolvimento de software?

    > Os contratos devem ser de **escopo aberto**, uma vez que ao iniciar o projeto os requisitos não estão bem definidos para nenhuma das partes.

2. Quais as diferenças entre XP e Scrum?

    > Há muitas diferenças, a começar com o **objetivo e objeto de trabalho** de cada metodologia, por exemplo, o XP é uma metodologia para desenvolvimento de software, enquanto o Scrum é uma metodologia de gerenciamento de projetos, além disso, **os papeis, eventos e artefatos** não são definidos no XP e sim apenas no Scrum.

3. Times Scrum são ditos cross-funcionais e auto-organizáveis. Por quê? Defina esses termos.

    > Os times Scrum são apontados como tal porque a metodologia propõe independência e autonomia para execução do projeto, de modo que quem defina as tarefas, quem realiza e quando sejam membros da equipe. O termo **cross-funcionais** se refere a independência dos membros com relação a pessoas externas, a equipe deve ter todas as especializações necessárias para desenvolver o projeto; Enquanto **auto-organizáveis** se refere a independência dos membros quanto a gerenciamento de tarefas, eles devem ter autonomia para definir quem, como e quando as histórias serão implementadas.

4. Em Scrum, qual a diferença entre as histórias do topo e do fundo do Backlog do Produto?

    > **O Backlog do produto é como uma lista de prioridades**, as histórias mais a cima são mais importantes e desenvolvidas, enquanto a baixo ficam as menos estruturadas e com menor relevência.

5. O que são e para que servem story points?

    > É uma **escala de classificação para o tempo de trabalho por complexidade**, as mais simples recebem o tamanho de 1 story ponint e de acordo com isso mensuram as seguintes tarefas. 

6. Em Scrum, qual a diferença entre uma sprint review e uma retrospectiva?

    > A **sprint review tem como objetivo mostrar os resultados** da sprint, enquanto a **retrospectiva foca em analisar as possíveis melhorias** e é a última atividade da sprint.

7. Um sprint pode ser cancelado? Se sim, por quem e por qual motivo? Para responder a essa questão, consulte antes o Scrum Guide (link), que é o guia que documenta a versão oficial de Scrum.

    > Sim, apenas pelo Product Owner e somente se a Meta da Sprint se tornar obsoleta.

8. Procure pensar em um sistema de uma área da qual tenha algum conhecimento.
    1. Escreva então uma história para esse sistema (veja que histórias são especificações resumidas de funcionalidades, com 2-3 sentenças). 
    2. Em seguida, quebre a história que definiu em algumas tarefas (de forma semelhante ao que fizemos no sistema similar ao Stack Overflow, usado como exemplo na seção sobre XP). 
    3. Existem dependências entre essas tarefas? Ou elas podem ser implementadas em qualquer ordem?

9. Suponha dois times, A e B, atuando em projetos diferentes, contratados por empresas distintas, sem conexões entre eles. Porém, ambos os times adotam sprints de 15 dias e ambos possuem 5 desenvolvedores. Nos seus projetos, o time A considera que sua velocidade é de 24 pontos. Já o time B assume uma velocidade de 16 pontos. Pode-se afirmar que A é 50% mais produtivo que B? Justifique sua resposta.

10. Quais são as principais diferenças entre Scrum e Kanban?
    
    > O **Kanban é mais simples**, não tem os eventos, papeis nem artefatos do Scrum, mantendo somente o quadro de tarefas, chamado no Kanban de **Quadro Kanban** que contém o Backlog do produto, também.

11. Quais são as diferenças entre um Quadro Scrum e um Quadro Kanban?

12. Qual o erro existe no seguinte Quadro Kanban?

| Backlog | Especificação (2) | Implementação (5) | Validação (3) |
|---------|-------------------|-------------------|---------------|
| XXXXXX  | X - XXXX          | XXX - XXX         | XXX -        |

13. Suponha o seguinte quadro Kanban. Neste momento, o time não consegue trabalhar na especificação de novas histórias, pois o WIP do passo Especificação está sendo totalmente preenchido por itens esperando movimentação para o passo seguinte (Implementação). O que seria mais recomendado neste momento: (a) desrespeitar o WIP e já puxar uma nova história do Backlog para Especificação; ou (b) ajudar o time nas três tarefas em Validação, de forma a desbloquear o fluxo do processo.

| Backlog | Especificação (2) | Implementação (5) | Validação (3) |
|---------|-------------------|-------------------|---------------|
| XXXX  |  - XXXXXX          | XXXX - X         | XXX -        |

14. Por que se recomenda que os limites WIP calculados usando a Lei de Little sejam incrementados, por exemplo em 50%, de forma a admitir uma margem de erro? Em outros palavras, quais eventos podem originar esses erros na estimativa dos WIPs?

15. Descreva os principais recursos oferecidos por Waterfall, Scrum e Kanban para controlar riscos e garantir um fluxo de trabalho sustentável e que propicie o desenvolvimento de software com qualidade.

16. Seja um processo Kanban, dividido em quatro passos. A tabela a seguir informa o lead time de cada um deles e o throughout do passo C, que é o passo mais lento. Com base nesses valores, calcule o WIP de cada passo (última coluna da tabela).

| Passo | Lead Time (médio, dias) | Throughput (tarefas/dia) | WIP |
|:---:|:---:|:---:|:---:|
| A | 4 | - | |
| B | 3 | - | |
| C | 10 | 0.5 | |
| D | 5 | - | |

17. Seja o seguinte gráfico, que mostra — para um determinado sistema — como os custos de mudanças variam conforme a fase do desenvolvimento em que elas são realizadas. (a) Qual método de desenvolvimento você recomendaria para esse sistema? Justifique sua resposta. (b) Sistemas de quais domínios podem ter uma curva de custos de mudanças semelhante a essa?

<img src="/FGA0138-MDS/imagens/grafico_q17.png" alt="Gráfico">

18. O artigo Development and Deployment at Facebook (link) apresenta os métodos e práticas de desenvolvimento de software usados no Facebook. Na sua primeira seção (páginas 2-3; figura 2), os autores fazem uma distinção entre alguns métodos de desenvolvimento, baseando-se na frequência com que versões de um sistema são liberadas para uso quando se adota cada um deles. Complete a seguinte tabela informando a frequência de releases mencionada no artigo para alguns métodos e políticas de liberação de software.

| Método | Frequência de novas releases |
|:---:|:---:|
|Waterfall| |
|Evolucionário| |
|Ágil| |
|Facebook| |
|Deployment Contínuo| |

19. Por que métodos como o Processo Unificado (UP) e Espiral não são considerados ágeis? E qual a diferença deles para o Modelo Waterfall?