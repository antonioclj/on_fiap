# Capítulo 5 - Azure DevOps e Ferramentas

## Preparação de ambiente

### 1.1 Pré-requisitos

- [X] Criar conta GitHub em https://GitHub.com/.
- [X] Ter acesso ao seu e-mail __@fiap.com.br__.
- [X] Criar conta Azure em https://portal.azure.com/ a partir de seu e-mail @fiap.com.br.

### 1.2 Conta Azure

#### Instruções:

a. Navegar para https://portal.azure.com/

b. Efetuar login com seu e-mail @fiap.com.br ou sua conta Microsoft. Apos o login você será direcionado para janela _Welcome to Azure!_

![](/capitulo5-azure-devops/imagens/preparacao/welcome-azure.png)
   
c. Clicar no botão _Explorar_.
   
![](/capitulo5-azure-devops/imagens/preparacao/botao-explore.png )
  
d. Clicar no botão _Increva-se agora mesmo_. Nesta opção você terá acesso no perfil estudante com US$ 100 de crédito.

![](/capitulo5-azure-devops/imagens/preparacao/inscreva-se.png)

e. Clicar no botão _Experimente Gratuitamente_ e seguir os procedimento de autenticação com seu e-mail @fiap.com.br. 

![](/capitulo5-azure-devops/imagens/preparacao/experimente-gratuitamente.png)

Após a conclusão você será redirecionado para tela de _Visão Geral_.

![](/capitulo5-azure-devops/imagens/preparacao/visao-geral.png)

https://portal.azure.com/#home

### 1.3 Fork (cópia) do Repositório _simple-api-java_

> https://GitHub.com/acnaweb/simple-api-java/

O objetivo do Fork é permitir que você tenha o repositório em sua conta GitHub e pratique as atividades.

#### Instruções:

a. Efetuar login no https://GitHub.com/.

b. Navegar para o repositório _simple-api-java_ - https://GitHub.com/acnaweb/simple-api-java/.

c. Clicar no botão _Fork_.

![](/capitulo5-azure-devops/imagens/preparacao/botao-fork.png)

d. Na tela _Create a new Fork_ será criado um novo repositório _simple-api-java_ em sua conta. Clicar em _Create Fork_.

![](/capitulo5-azure-devops/imagens/preparacao/create-fork.png)

e. Verificar o repositório recém criado.

![](/capitulo5-azure-devops/imagens/preparacao/simple-api-java.png)

## Azure DevOps

### 2.1 Visão geral do Azure DevOps

Azure DevOps é Plataforma de DevOps da Microsoft que oferece uma série de ferramentas integradas projetadas para suportar o desenvolvimento, o teste, a implantação e a monitoração de aplicações em qualquer ambiente, seja na nuvem ou em sistemas locais. O Azure DevOps dá suporte a uma cultura colaborativa e um conjunto de processos que reúnem desenvolvedores, gerentes de projetos e colaboradores para desenvolver software. Ele permite que as organizações criem e melhorem produtos em ritmos mais acelerados do que o fariam com abordagens tradicionais de desenvolvimento de software. 

O Azure DevOps fornece recursos integrados que você pode acessar por meio do seu navegador web ou do cliente de IDE. Você pode usar todos os serviços incluídos no Azure DevOps ou escolher apenas o que precisa para complementar seus fluxos de trabalho existentes. O quadro abaixo lista alguns dos serviços do Azure DevOps, veja:

![](/capitulo5-azure-devops/imagens/topico6/tabela-servicos.png)

Quadro 14 – Quadro de serviços da Azure DevOps

Fonte: https://learn.microsoft.com/pt-br/azure/devops/user-guide/what-is-azure-devops?view=azure-devops, 03/08/2024.

> *__Dica:__* Para maiores informações sobre o [Manifesto para Desenvolvimento Ágil de Software](https://agilemanifesto.org/iso/ptbr/manifesto.html)

#### Azure Boards

O _Azure Board_ é o serviço responsável pela parte de gerenciamento e planejamento de projetos.

O _Azure Board_  permite adotar 4 modelos de processos:

1. Basic
2. Scrum
3. Ágil
4. CMMI

No Azure Boards são criadas User Stories, Task e Bugs.

> *__Dica:__* Para maiores informações acesse https://azure.microsoft.com/pt-br/products/devops/boards/

#### Azure Repos

O Azure Repos é um conjunto de ferramentas de controle de versão que você pode usar para gerenciar seu código. Se o projeto de software for grande ou pequeno, o uso do controle de versão assim que possível será uma boa ideia.

O Azure Repos fornece dois tipos de controle de versão:

- Git: controle de versão distribuído
- TFVC (Controle de Versão do Team Foundation): controle de versão centralizado

> __Git__ é o sistema de controle de versão mais usado atualmente e está se tornando rapidamente o padrão para controle de versão. Git é um sistema de controle de versão distribuído, ou seja, sua cópia local do código é um repositório de controle da versão completa.

> *__Dica:__* Para maiores informações acesse https://azure.microsoft.com/pt-br/products/devops/repos/

#### Azure Pipelines

O Azure Pipelines é a parte do Azure DevOps que cria, testa e implanta projetos de código automaticamente. O Azure Pipelines combina integração contínua, testes contínuos e entrega contínua para criar, testar e entregar seu código para qualquer destino. O Azure Pipelines dá suporte a todos os principais idiomas e tipos de projeto.

> *__Dica:__* https://azure.microsoft.com/pt-br/products/devops/pipelines/

### Azure Test Plans

Azure Test Plans fornece ferramentas avançadas e avançadas que todos na equipe podem usar para impulsionar a qualidade e a colaboração em todo o processo de desenvolvimento. A solução de gerenciamento de teste fácil de usar e baseada em navegador fornece todos os recursos necessários para testes manuais planejados, testes de aceitação do usuário, testes exploratórios e coleta de comentários dos stakeholders.

> *__Dica:__* https://azure.microsoft.com/pt-br/products/devops/test-plans/

### Azure Artifacts

O Azure Artifacts permite que os desenvolvedores publiquem e consumam vários tipos de pacotes de feeds e registros públicos, como PyPI, Maven Central e NuGet.org. Você pode combinar o Azure Artifacts com o Azure Pipelines para publicar artefatos de pipeline e de compilação, implantar pacotes ou integrar arquivos em diferentes estágios do pipeline para criar, testar ou implantar seu aplicativo.

> *__Dica:__* https://azure.microsoft.com/products/devops/artifacts/

### 2.2 Gerenciamento de projetos e equipes

O _Azure Board_ é o serviço responsável pela parte de gerenciamento e planejamento de projetos e equipes.

No Azure DevOps, o gerenciamento de projetos e equipes é estruturado de forma a promover a colaboração eficiente e o controle rigoroso dos processos de desenvolvimento. A plataforma é dividida em três segmentos principais que facilitam a organização e a gestão de recursos, tarefas e equipes dentro de qualquer ambiente empresarial. Seguem os segmentos:

* Organização: Uma organização no Azure DevOps é um mecanismo para organizar e conectar grupos de projetos relacionados. Exemplos incluem divisões de negócios, divisões regionais ou outras estruturas empresariais. Você pode escolher uma organização para toda a empresa, uma organização para si mesmo ou organizações separadas para unidades de negócios específicas. Isso facilita o gerenciamento de permissões, políticas e a visibilidade dos processos em diferentes níveis da empresa, promovendo uma governança de TI eficiente e centralizada.

* Projeto: Um projeto no Azure DevOps contém o seguinte conjunto de recursos:

  * Quadros e backlogs para planejamento ágil.
  * Pipelines para integração e implantação contínuas.
  * Repositórios para controle de versão e gerenciamento de código-fonte e artefatos.
  * Integração contínua de testes em todo o ciclo de vida do projeto.

O projeto permite uma configuração detalhada de segurança e controle de acesso, garantindo que somente usuários autorizados possam fazer alterações ou visualizar informações sensíveis. Cada organização contém um ou mais projetos.

* Equipe: Uma equipe é uma unidade que suporta muitas ferramentas configuráveis pela equipe. Essas ferramentas ajudam você a planejar e gerenciar o trabalho e facilitam a colaboração. Cada equipe possui seu próprio backlog. Além disso, as equipes podem configurar suas próprias sprints, estabelecer metas específicas e utilizar dashboards customizados para monitorar progressos e métricas chave.

#### Organizações

Nesta prática vamos compreender a navegação e acesso a Organização no Azure DevOps.

a. Na barra de pesquisa digitar "Azure DevOps" e clicar na opção _Azure DevOps Organizations_

![](/capitulo5-azure-devops/imagens/topico6/pesquisar-azure-devops.png)

b. Na janela _Azure DevOps_ clicar no link _My Azure DevOps Organizations_. Você será direcionado para tela de login com sua conta @fiap.com.br.

![](/capitulo5-azure-devops/imagens/topico6/my_organizations.png)

c. Na janela seguinte atualizar o nome e clicar em _Continue_.

![](/capitulo5-azure-devops/imagens/topico6/more-details.png)

d. A seguir clicar no botão _Create New Organization_.

![](/capitulo5-azure-devops/imagens/topico6/create-new-organization.png)

e. Clicar em _Continue_.

![](/capitulo5-azure-devops/imagens/topico6/get-started-continue.png)

f. Na janela, informe o nome da organização (no exemplo, useu o alias de meu e-mail). Clicar em _Continue_.

> *__Atenção:__* Use o alias de seu e-mail (sem a parte @fiap.com.br). 

> *__Dica:__* Usar o nome da empresa é boa prática para nome de organização.

![](/capitulo5-azure-devops/imagens/topico6/organization-name.png)

Após a criação da organização você será direcionado para tela de criação de projeto. Note no canto superior esquerdo o nome da organização recém criada.

![](/capitulo5-azure-devops/imagens/topico6/post-create-organization.png)

> *__Importante:__* Para acessar a url da organização diretamente pelo browser use o padrão https://dev.azure.com/<Nome da Organização>. No exemplo, a url de acesso é https://dev.azure.com/pf1524.

#### Projetos

Nesta prática vamos criar o primerio projeto com nome "fiap-on".

a. Informar os dados abaixo e clicar em _Create Project_.
    
    - Project name: fiap-on
    - Description: Projeto de software demonstração
    - Clicar na opção: Private
    - Expandir o item _Advanced_
    - Clicar em _Work item process_ e selecionar a opção _Scrum_

![](/capitulo5-azure-devops/imagens/topico6/create-project.png)

O projeto será criado e a janela "Welcome to the project" será exibida.

![](/capitulo5-azure-devops/imagens/topico6/welcome-project.png)

> *__Importante:__* Para acessar a url do projeto diretamente pelo browser use o padrão https://dev.azure.com/<Nome da Organização>/<Nome do Projeto>. No exemplo, a url de acesso é https://dev.azure.com/pf1524/fiap-on.

> *__Dica:__* Você repetir o processo e criar novos projetos.

#### Usuários

Todo projeto possue 1 usuário: o proprietário do projeto. No entanto, espera-se que a equipe de pessoas desenvolvedores, analistas de qualidade e outras partes interessadas, tenham acesso ao projeto. 

A seguir vamos adicionar usuários na organização.

a. Saia do projeto atual e acesse a organização clicando no ícone "Azure DevOps" no canto superior esquerdo.

![](/capitulo5-azure-devops/imagens/topico6/home-azure-devops.png)

b. Na tela seguinte vamos acessar o menu _Organization settings_ que encontra-se no canto inferior esquerdo.

![](/capitulo5-azure-devops/imagens/topico6/organization-settings.png)

c. No menu lateral esquerdo clicar no item _Users_. 

![](/capitulo5-azure-devops/imagens/topico6/menu-users.png)

Na próxima tela será exibida a lista de usuários que foram adicionados na organização. Note que apenas o seu usuário (proprietário) foi adicionado.

Nesta tela são adicionados os novos usuários que farão parte da organização.

a. Clicar em _Add users_.

![](/capitulo5-azure-devops/imagens/topico6/add-users.png)

b. Na janela _Add new users_ acesse a caixa de texto "Users or Service Prncipals" e digite os e-mails das pessoas que farão parte do projeto. 

> *__Alerta:__* Como você está acessando com seu e-mail @fiap.com.br, não será possível adicionar usuários fora do domínio @fiap.com.br. Para avançar na prática desta aula, utiliza um e-mail de uma pessoa colega de sua turma.

Clicar em _Add to projects_ e selecione o(s) projeto(s) ao qual o usuário terá acesso.

Clicar em _Add_ para confirmar.

![](/capitulo5-azure-devops/imagens/topico6/add-user.png)

Clicar em _Add_ para confirmar.

> *__Atenção__* Os usuários adicionados receberão email de convite para o Azure DevOps. Cada usuário deverá clicar em "Acesse agora" para aceitar o convite e fazer parte da organização.

![](/capitulo5-azure-devops/imagens/topico6/email-invite.png)

#### Processos

O Azure Boards oferece vários processos para você escolher para gerenciar os itens de trabalho. Selecionar o processo certo é essencial para otimizar um fluxo de trabalho de projeto e garantir seu sucesso. Um processo significa criar objetos do sistema de controle de item de trabalho (work item), que pode ser o modelo de processo de herança para o Azure DevOps.

- Modelos de processo

Um modelo de processo é uma estrutura que define como as tarefas e atividades são gerenciadas em um projeto de desenvolvimento de software usando a plataforma Azure Boards.

Existem 4 modelos de Processo disponíveis no Azure Devops.

1. Basic (Padrão) - é o modelo de processo mais simples.
2. Scrum - é um nível acima do "Basic".
3. Agile - suporta muitos termos do método Agile.
4. CMMI - fornece o máximo de suporte para processos formais e gerenciamento de alterações.

- Principais diferenças entre os processos padrão

O quadro a seguir resume as principais distinções entre os tipos de item de trabalho e os estados usados pelos quatro processos padrão.

![](/capitulo5-azure-devops/imagens/topico6/comparacao-modelos-processo.png)

Fonte: https://learn.microsoft.com/pt-br/azure/devops/boards/work-items/guidance/choose-process?view=azure-devops, 02/08/2024.

- Estados, transições e motivos do fluxo de trabalho

Os estados do fluxo de trabalho dão suporte ao acompanhamento do status do trabalho à medida que ele passa de um estado _New_ para um estado _Closed_ ou _Done_. Cada fluxo de trabalho consiste em um conjunto de estados, as transições válidas entre estados e os motivos para fazer a transição do item de trabalho para o estado selecionado.

Os diagramas a seguir mostram a progressão típica dos tipos de item de trabalho usados para rastrear defeitos de trabalho e código nos três processos padrão. Eles também mostram algumas das regressões para estados anteriores e transições para estados removidos. Cada imagem mostra apenas o motivo padrão associado à transição.

1. Basic 

![](/capitulo5-azure-devops/imagens/topico6/state-basic.png)

2. Scrum 

![](/capitulo5-azure-devops/imagens/topico6/state-scrum.png)

3. Agile 

![](/capitulo5-azure-devops/imagens/topico6/state-agile.png)

4. CMMI 

![](/capitulo5-azure-devops/imagens/topico6/state-cmmi.png)

- Critérios para escolha de modelos de processo

A escolha de um modelo de processo deve respeitar os critérios a seguir:

1. Basic - Escolha Básico quando sua equipe quiser o modelo mais simples que usa os tipos de item de trabalho Problema, Tarefa e Épico para acompanhar o trabalho.

2. Scrum - Escolha Scrum quando sua equipe praticar o Scrum. Esse processo funciona muito bem para acompanhar itens da lista de pendências (backlog) do produto e bugs no quadro Kanban. 

3. Agile - Escolha Agile quando sua equipe usar métodos de planejamento Agile, incluindo Scrum, e acompanhe as atividades de desenvolvimento e teste separadamente. Esse processo funciona muito bem para rastrear Histórias de Usuários e (opcionalmente) bugs no quadro Kanban.

4. CMMI - Escolha CMMI quando a equipe seguir métodos mais formais do projeto que exigem uma estrutura para aperfeiçoamento de processos e um registro auditável das decisões.

> *__Importante__* Para este curso estamos utilizando o modelo de processo _Scrum_. Esta escolha é realizada na criação do projeto.

#### Backlog (Lista de Pendências)

Com o _backlog_ (lista de pendências), você pode planejar rapidamente seu projeto adicionando _user stories_ (histórias de usuário) ou requisitos à sua lista de pendências do produto. Assim que o plano estiver em vigor, você poderá começar a impulsionar os esforços de desenvolvimento do código.

Uma lista de pendências do Azure Boards é uma lista priorizada de itens de trabalho que orienta o esforço da equipe de desenvolvimento, ajuda a gerenciar o escopo do projeto e facilita a comunicação e a colaboração eficazes por meio do ciclo de vida de desenvolvimento de software.

Use listas de pendências para realizar as seguintes tarefas:

- Definir histórias de usuários, itens do backlog da lista de pendências ou requisitos
- Reordenar a lista de pendências
- Adicionar detalhes e estimativas a itens da lista de pendências
- Atualização em massa
- Arrastar itens até um sprint
- Mapear itens da lista de pendências dentro de uma hierarquia
- Examinar a hierarquia ou o portfólio de trabalho atribuído a várias equipes
- Prever trabalho
- Exibir progresso de acumulação, contagens ou totais

No Azure Board o _backlog_ está fica disponível no projeto. Nos passos seguintes criaremos itens de backlog.

a. Acesse o projeto clicando no ícone _Azure DevOps_ e a seguir clicar no projeto _fiap-on_.

![](/capitulo5-azure-devops/imagens/topico6/acessando-fiap-on.png)

b. No menu lateral esquerdo selecionar o menu _Boards_. Clicar em _Backlogs_ para acessar a lista de pendencias.

![](/capitulo5-azure-devops/imagens/topico6/menu-backlogs.png)

#### Work Items (Itens da Lista de Pendências)

No modelo de procesos _Scrum_ existem 2 tipos de _work itens_: 

  - Product Backlog Item
  - Bug

Na sequencia vamos adicionar alguns _Product Backlog Item_ no _backlog_. Os passos a e b deverão ser repetidos para cada itens na tabela abaixo.

 Item de backlog| 
|--|
|Tela inicial|
|Cadastro Usuário|
|Cadastro Perfil|
|Tela Dashboard|
|Aplicativo Mobile iOS|
|Aplicativo Mobile Android|

a. Clicar no botão _New Work Item_.

![](/capitulo5-azure-devops/imagens/topico6/botao-new-workitem.png)

b. Digitar o nome e clicar em "Add to top"

![](/capitulo5-azure-devops/imagens/topico6/item-tela-inicial.png)

 Item de backlog| 
|--|
|Tela inicial|
|Cadastro Usuário|
|Cadastro Perfil|
|Tela Dashboard|
|Aplicativo Mobile iOS|
|Aplicativo Mobile Android|

Ao final o _backlog_ terá uma configuração com 6 itens

![](/capitulo5-azure-devops/imagens/topico6/6-itens.png)

c. Vamos alterar o modo de visualização para _Board_, clicar no menu lateral _Boards_.

![](/capitulo5-azure-devops/imagens/topico6/modo-boards.png)

A tela no modo Boards será apresentada conforme a imagem.

![](/capitulo5-azure-devops/imagens/topico6/tela-modo-boards.png)

- Navegação no board

Você pode reordenar os cards (itens no board) arrastando e soltando.

> *__Prática__* Reorganize a sequencia de cards de modo que fiquem na ordem crescente de prioridade.

- Nomes de colunas no board

Você pode renomear os nomes de colunas no board. Vamos realizar alterações conforme os nomes na sequencia.

a. Clicar no ícone do menu _board settings_.

![](/capitulo5-azure-devops/imagens/topico6/menu-board-settings.png)

b. Clicar no menu _Columns_.

![](/capitulo5-azure-devops/imagens/topico6/menu-columns.png)

c. Clicar em cada coluna nas "tabs" e alterar o nome conforme a tabela abaixo.

| De | Para |
|--|--|
| New | Novo |
| Approved | Aprovado |
| Committed | Comitado |
| Done | Concluído |

![](/capitulo5-azure-devops/imagens/topico6/renomear-colunas.png)

d. Clicar em _Save_.

Verifique que as colunas agora têm novos nomes no _board_.

![](/capitulo5-azure-devops/imagens/topico6/novos-nomes-no-board.png)

- Atribuição de atividades

Cada card no board representa uma atividade que deverá ser executada.

Os cards na coluna _Novo_ indicam que não foram iniciados.

Vamos mover o card _Tela Inicial_ para coluna _Aprovado_ e atribuir um usuário responsável por sua execução.

a. Mover o card _Tela Inicial_ para coluna _Aprovado_ .

b. Clicar no card e informar um usuário responsável pela execução. 

![](/capitulo5-azure-devops/imagens/topico6/tela-inicial-flavio.png)

c. Clicar em _Save and Close_.

Observe que no board existem 5 cards não iniciados em _Novo_ e um card _Aprovado_

![](/capitulo5-azure-devops/imagens/topico6/bord-aprovado.png)

> *__Prática__* Mova outros cards para _Aprovado_ e atribua a um usuário.

- Integração com repositórios de código

Os cards no Azure Board pode ser integrados com _branches_ no repositório do GitHub ou Azure Repos.

Vamos integrar o Azure Board no repositório do GitHub e associar os cards a novas branches.

> *__Dica__* Saiba mais em https://learn.microsoft.com/pt-br/azure/devops/boards/github/connect-to-github?view=azure-devops

a. Estando com o projeto selecionado, clicar no menu _Project settings_ na parte inferior do menu esquerdo.

![](/capitulo5-azure-devops/imagens/topico6/project-settings.png)

b. Clicar no menu _GitHub Connections_.

![](/capitulo5-azure-devops/imagens/topico6/menu-github-connections.png)

c. Clicar em _Connect your GitHub account_.

![](/capitulo5-azure-devops/imagens/topico6/connect-your-github-account.png)

Você será direcionado para uma janela no GitHub para  autorização do Azure Boards.

d. Clicar em _Authorize AzureBoards_

![](/capitulo5-azure-devops/imagens/topico6/authorize-azureboards.png)

e. Selecionar o repositório criado no _Fork_ e clicar em _Save_.

![](/capitulo5-azure-devops/imagens/topico6/add-github-repositories.png)

f. Na tela seguinte clicar em _Approve, Install & Authorize_

![](/capitulo5-azure-devops/imagens/topico6/approve.png)

Agora vamos vincular um card a uma branch nova no repositório.

a. Vá para o board e atribua a si mesmo um card que esteja na coluna _Aprovado_ - anote o número do id do card.

No exemplo, o id do card é 3.

![](/capitulo5-azure-devops/imagens/topico6/id-card-3.png)

b. Faça o clone de seu repositório e acesse a pasta do repositório. A seguir configure dados de usuário e email no git.

```sh
git clone https://github.com/antonioclj/simple-api-java.git
```

```sh
cd simple-api-java
```

```sh
git config user.email "antonioclj.ac@gmail.com"
git config user.name "Prof. AC"
git config credential.username "antonioclj"
```

c. Com um editor de texto ou sua IDE favorita, faça qualquer alteração no arquivo README.md e salve.

d. Adicionar as alteração para "stage" no git.

```sh
git add README.md
```

> *__Atenção:__* Na mensagem do commit você deve fazer referencia ao id do card (no exemplo: 3). Para tanto use o formato **AB#3** onde o número 3 refere-se ao id do card. No seu caso qual é o número?

d. Criar um commit que integrará no Azure Board pelo id do card.

```sh
git commit -m "Adicionado comentário para AB#3"
```

e. Envia as alterações para o repositório remoto

```sh
git push
```

f. Volte ao board e verifique que o card possui um novo ícone indicando um commit realizado no card.

![](/capitulo5-azure-devops/imagens/topico6/card-com-commit.png)


## Azure Developer CLI

### 3.1 Uso de linha de comando do Azure Developer

### 3.2 Automação de tarefas na nuvem

### 3.3 Scripting com a Azure CLI


