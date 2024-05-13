# Resumão

## Software Architecture Partterns
![Padrão de arquitetura de software](/FGA0138-MDS/dojo/img/padrão%20de%20arquitetura%20de%20software.gif)
[Fonte](https://www.linkedin.com/posts/brijpandeyji_%3F%3F%3F%3F%3F%3F%3F%3F-%3F%3F%3F%3F%3F%3F%3F%3F%3F%3F%3F%3F-activity-7139576994286952448-kYXD?utm_source=share&utm_medium=member_desktop)

### MVC (Model-View-Controller):
Padrão clássico separando o código em três camadas:
 - **Modelo**: Dados e lógica de negócios
 - **Visualização**: Apresentação dos dados ao usuário
 - **Controlador**: Manipula a entrada do usuário e atualiza o modelo/visualização

### MVP (Model-View-Presenter):

- Introduz um **apresentador** para mediar entre a visualização e o modelo.

### MVI (Model-View-Intent):

Construído para programação reativa.
- View emite **intenções**, manipuladas pelo modelo, atualizando estado e view.
- Promove o fluxo de dados unidirecional e simplifica a lógica da interface do usuário.

### MVVM (Model-View-ViewModel):

Adequado para frameworks reativos e interfaces de usuário complexas.
- View se liga a um **ViewModel** que contém dados e lógica de exibição.
- ViewModel atualiza pelo modelo, em seguida, atualiza a exibição.

### VIPER (Visualização, Ator, Apresentador, Entidade, Roteador):

Projetado para aplicações grandes e complexas.
- Cinco camadas: **View, Interactor (lógica de negócio), Presenter (preparação de dados), Entity (modelos de dados), Router (coordenação do fluxo de dados)**.
- Aumenta a modularidade e a capacidade de manutenção para projetos massivos.

## Data Base

### Banco de Dados Relacional:

#### Estrutura tabular
dados organizados em tabelas com linhas e colunas, cada tabela tem um esquema definido com tipos de dados específicos para cada coluna.
![Estrutura Banco Relacional](/FGA0138-MDS/dojo/img/estrutura%20banco%20relacional.png)

#### Esquema fixo
esquema rígido e fixo, o que significa que a estrutura das tabelas (número de colunas, tipos de dados, relacionamentos) deve ser definida antecipadamente e mantida ao longo do tempo.

#### Consistência
enfatizam a consistência dos dados e seguem o ACID (Atomicidade, Consistência, Isolamento, Durabilidade) para garantir a integridade dos dados.

#### Transações
suportam transações complexas, permitindo que várias operações sejam agrupadas em uma única transação que é executada de forma atômica.

### Banco de Dados Não Relacional

#### Estrutura flexível
não possuem uma estrutura tabular rígida e podem armazenar dados de forma flexível, muitas vezes usando formatos como documentos, pares chave-valor, grafos ou colunas.

#### Esquema dinâmico
permitem um esquema dinâmico, o que significa que você pode adicionar campos aos seus documentos (ou equivalentes) sem a necessidade de alterar um esquema central.

#### Escalabilidade
podem ser facilmente dimensionados horizontalmente.

#### Consistência flexível
Em geral, eles não seguem o modelo ACID estrito, priorizando a disponibilidade e a partição, o que pode resultar em diferentes níveis de consistência, dependendo da configuração.

### SQL (Structured Query Language)
é usada para consultar e manipular dados em bancos de dados relacionais. 

|COMANDO| FUNÇÃO|
|---|---|
|SELECT| retoma registros no banco de dados|
|CREATE TABLE|cria novas tabelas em uma base de dados|
|CREATE DATABASE|cria um banco de dados do zero|
|USE e SHOW DATABASES|serve para fazer a visualização mais rápida de diferentes bases de dados|
|INSERT|insere dados no banco de dados|
|UPDATE|atualiza os dados nas tabelas|
|DELETE|exclui um ou mais registros de uma base de dados|
|DROP|remove uma tabela ou uma base de dados|

### NoSQL (Not Only SQL)
Existem várias categorias, incluindo bancos de dados de documentos, bancos de dados de colunas, bancos de dados de grafos e muito mais, cada um projetado para tipos específicos de dados e casos de uso.

### PostgreSQL
é um sistema de gerenciamento de banco de dados relacional de código aberto.

[Material complementar](https://rockcontent.com/br/blog/postgresql/)

## API(Application Programming Interface) 
[Fonte](https://aws.amazon.com/pt/what-is/api/#:~:text=API%20significa%20Application%20Programming%20Interface,de%20serviço%20entre%20duas%20aplicações.)

são mecanismos que permitem que dois componentes de software se comuniquem usando um conjunto de definições e protocolos. 

- SOAP - Simple Object Access Protocol (Protocolo de Acesso a Objetos Simples)
    - Cliente e servidor trocam mensagens usando XML
- RPC - Remote Procedure Calls (Chamadas de Procedimento Remoto)
    - O cliente conclui uma função (ou um procedimento) no servidor e o servidor envia a saída de volta ao cliente
- WebSocket 
    - Usa objetos JSON para transmitir dados
    - O servidor pode enviar mensagens de retorno de chamada a clientes conectados
- **REST - Transferência Representacional de Estado**
    - O cliente envia solicitações ao servidor como dados. O servidor usa essa entrada do cliente para iniciar funções internas e retorna os dados de saída ao cliente.
    - Ausência de estado: os servidores não salvam dados do cliente entre as solicitações
    - Funções: **GET, PUT, DELETE, PATCH...** 
    - HTTP: usado para troca de dados entre clientes e servidores 

- Privadas, públicas, de parceiros ou compostas.

- **EndPoint:** são pontos de contato finais no sistema de comunicação da API.

- **teste de API:** [dojo backend](https://www.youtube.com/watch?v=6Emem3E0qqo)

### FastAPI
é um framework web para construção de APIs com Python.

### Integração
![exemplo de integração](/FGA0138-MDS/dojo/img/exemplo%20integração.png)
![arquitetura integração](/FGA0138-MDS/dojo/img/arquitetura%20integração.png)
