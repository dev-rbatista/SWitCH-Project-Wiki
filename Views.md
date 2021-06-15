## Contents
- [Views](#views)
	- [Introduction](#introduction)
	- [Nível 1](#nível-1)
		- [Vista Lógica](#vista-lógica)
		- [Vista de Processos](#vista-de-processos)
		- [SSD US001](#ssd-us001)
		- [SSD US002](#ssd-us002)

	- [Nível 2](#nível-2)
		- [Vista Lógica](#vista-lógica-1)
		- [Vista de Processos](#vista-de-processos-1)
			- [SSD US13 (Porquê esta US?)](#ssd-us13-porquê-esta-us)
			- [(outros SSD arquiteturalmente relevantes)](#outros-ssd-arquiteturalmente-relevantes-1)
		- [Vista de Implementação](#vista-de-implementação)
		- [Vista Física](#vista-física)
	- [Nível 3 (Front end)](#nível-3-ui)
		- [Vista Lógica](#vista-lógica-3)
		- [Vista de Processos](#vista-de-processos-3)
		- [Vista de Implementação](#vista-de-implementação-2)
		- [Vista Física](#vista-física-2)
	- [Nível 3 (Back end)](#nível-3-mdv)
		- [Vista Lógica](#vista-lógica-4)
		- [Vista de Processos](#vista-de-processos-4)
		- [Vista de Implementação](#vista-de-implementação-3)
		- [Vista Física](#vista-física-3)
	- [Nível 3 (Persistência)](#nível-3-planeamento)
		- [Vista Lógica](#vista-lógica-5)
		- [Vista de Processos](#vista-de-processos-5)
		- [Vista de Implementação](#vista-de-implementação-4)
		- [Vista Física](#vista-física-4)


  ![img](diagramas/nivel1/LogicViewBusinessLogic-Business_Logic_View___SP01.svg)

# Views

## Introduction
Será adotada a combinação de dois modelos de representação arquitetural: C4 e 4+1.

O Modelo de Vistas 4+1 [[Krutchen-1995]](References.md#Kruchten-1995) propõe a descrição do sistema através de vistas complementares permitindo assim analisar separadamente os requisitos dos vários stakeholders do software, tais como utilizadores, administradores de sistemas, project managers, arquitetos e programadores. As vistas são deste modo definidas da seguinte forma:

- Vista lógica: relativa aos aspetos do software visando responder aos desafios do negócio;
- Vista de processos: relativa ao fluxo de processos ou interações no sistema;
- Vista de desenvolvimento: relativa à organização do software no seu ambiente de desenvolvimento;
- Vista física: relativa ao mapeamento dos vários componentes do software em hardware, i.e. onde é executado o software;
- Vista de cenários: relativa à associação de processos de negócio com atores capazes de os despoletar.

O Modelo C4 [[Brown-2020]](References.md#Brown-2020)[[C4-2020]](References.md#C4-2020) defende a descrição do software através de quatro níveis de abstração: sistema, contentor, componente e código. Cada nível adota uma granularidade mais fina que o nível que o antecede, dando assim acesso a mais detalhe de uma parte mais pequena do sistema. Estes níveis podem ser equiparáveis a mapas, e.g. a vista de sistema corresponde ao globo, a vista de contentor corresponde ao mapa de cada continente, a vista de componentes ao mapa de cada país e a vista de código ao mapa de estradas e bairros de cada cidade.
Diferentes níveis permitem contar histórias diferentes a audiências distintas.

Os níveis encontram-se definidos da seguinte forma:
- Nível 1: Descrição (enquadramento) do sistema como um todo;
- Nível 2: Descrição de contentores do sistema;
- Nível 3: Descrição de componentes dos contentores;
- Nível 4: Descrição do código ou partes mais pequenas dos componentes (e como tal, não será abordado neste DAS/SAD).

Pode-se dizer que estes dois modelos se expandem ao longo de eixos distintos, sendo que o Modelo C4 apresenta o sistema com diferentes níveis de detalhe e o Modelo de Vista 4+1 apresenta o sistema de diferentes perspetivas. Ao combinar os dois modelos torna-se possível representar o sistema de diversas perspetivas, cada uma com vários níveis de detalhe.

Para modelar/representar visualmente, tanto o que foi implementado como as ideias e alternativas consideradas, recorre-se à Unified Modeling Language (UML) [[UML-2020]](References.md#UML-2020) [[UMLDiagrams-2020]](References.md#UMLDiagrams-2020).

## Nível 1
### Vista Lógica

![img.png](Images/img.png)

### Vista de Processos
#### Criar Objecto

![L1_ProcessView_CreateObject.png](diagrams/L1_ProcessView_CreateObject.png)

#### Obter Objecto

![L1_ProcessView_GetObject.png](diagrams/L1_ProcessView_GetObject.png)

## Nível 2
### Vista Lógica

![LogicView_Nível2.png](diagrams/LogicView_Nível2.png)

### Vista de Processos

#### SSD US Criar/Adicionar um recurso

![ProcessView_Nível2_AddOrCreate.png](Process%20View_Nível2_AddOrCreate.png)


#### SSD US Obter um recurso

![ProcessView_Nível2_Get.png](diagrams/ProcessView_Nível2_Get.png)

#### SSD US Obter um recurso com API Externa (Standard Categories)

![ProcessView_Nível2_Get_External.png](diagrams/ProcessView_Nível2_Get_External.png)



### Vista de Implementação
![L2_ImplementationView.png](diagrams/L2_ImplementationView.png)!

### Vista Física

Uma proposta muito simplificada.

![L2_Physical-View.png](diagrams/L2_Physical_View.png)

De facto, deve-se ter em consideração os requisitos não funcionais ["Physical Contraints"](Background.md#Physical_Constraints).

## Nível 3 (MDR)
### Vista Lógica
Alternativa baseada numa arquitetura por camadas sobrepostas:
![N3-VL-MDR-alt1](diagramas/nivel3/MDR/N3-VL-MDR-alt1.png)

Alternativa baseada numa arquitetura por camadas concêntricas (Onion):
![N3-VL-MDR-alt2](diagramas/nivel3/MDR/N3-VL-MDR-alt2.png)

A alternativa Onion será a adotada.

### Vista de Processos

#### SD US01
TBD

#### (outros SSD arquiteturalmente relevantes)
[...]

### Vista de Implementação
![N3-VI-MDR-alt2](diagramas/nivel3/MDR/N3-VI-MDR-alt2.png)

Alguns detalhes mais (se existissem pais do que 4 níveis, podia ser considerado nível 4):

![N3.1-VI-MDR-alt2](diagramas/nivel3/MDR/N3.1-VI-MDR-alt2.png)

### Vista Física

Por agora, não existe necessidade de ser representada.

## Nível 3 (UI)

### Vista Lógica
TBD

### Vista de Processos
TBD

### Vista de Implementação
TBD

### Vista Física
TBD


## Nível 3 (Back-end)
### Vista Lógica

No desenvolvimento da aplicação foram aplicados vários padrões de design de software. 
Inicialmente a representação do modelo lógico seguiu a arquitetura **DDD**, domain-driven design, como forma introdutória para a reestruturação e nova aplicação do modelo de domínio.
Foram introduzidos conceitos como os *aggregates* e *value objects* que permitiram iniciar a reengenharia da aplicação e criar as bases para a utilização da arquitetura **Onion**.

A forma final da aplicação utiliza a arquitetura ***Onion*** que é representada por uma divisão em camadas concêntricas cujas dependências têm um sentido interno.
O diagrama de classes apresenta-se dividido em 4 camadas, ***infrastructure***, ***interface adapters***, ***use case services*** e ***domain***, sendo a *infrastructure* a mais exterior e o *domain* a mais interior, representado na seguinte imagem.

![logic-view](diagrams/logic-view-backend.png)

### Vista de Processos

Seguindo a estruturação apresentada na vista lógica é possível construir a **sequência de processos que serão a base de funcionamento para a implementação das user stories**. 

![sd_us001](diagrams/general%20diagram%20SD.png)

Aplicando a estrutura do diagrama de sequência podemos concluir que segue um padrão comum para todas as **user stories** da aplicação.
Desta forma, há um pedido http direccionado ao ***REST controller*** que invoca um ***service***, específico para cada caso de uso, onde a lógica de negócio será aplicada. Daqui será invocado o **repositório** do respetivo agregado envolvido, que será responsável pela comunicação com a persistência, e mediante o tipo de pedido adicionar ou obter a informação pretendida.

Entre cada uma destas etapas serão invocados ***assemblers*** cuja finalidade é mapear os dados com o objectivo de proteger e encapsular a informação proveniente de camadas diferentes. Isto permite-nos respeitar os princípios do encapsulamento e tornar a aplicação escalável.

Esta arquitetura garante que o ***single responsibility principle*** é respeitado.

Na seguinte lista serão descritas as características específicas de cada tipo de diagrama

#### 1) GET HTTP request 

#### US110 - Get Category list

Nos **pedidos http - Get** o repositório comunica com o repositório JPA para obter todos os dados relativos à user story, neste caso às categorias, converte cada objecto de JPA para objecto de domínio e adiciona a uma lista. Posteriormente essa lista é convertida para um DTO da lista e devolvido ao ***controller*** 

![sd_us110](diagrams/SD/SD_US110_GetCategoryList.png)

______

#### 2) POST HTTP request com dois agregados

#### US010 - Create Family and set Administrator

Nos **pedidos http - Post** o ***service*** é responsável pela criação de dois objectos do domínio, ***Admin*** e ***Family***, através dos ***value objects*** provenientes dos respectivos *assemblers*. Em primeiro adiciona um dos objectos (*admin*) ao seu repositório e posteriormente o outro objecto (*family*) ao repositório respectivo. Através da devida anotação no método do *service* (*@transactional*) garantimos que caso haja alguma falha no processo, nenhum dos objectos é adicionado ao seu repositório.

![sd_us010](diagrams/SD/SD_US010_CreateAFamilyAndSetAdministrator.png)


______

#### 3) POST HTTP request com verificação

#### US151 - Add email

No caso de ser necessário verificação da existência de um *value object* (email), o *service* tem o papel de fazer o pedido ao repositório do objecto de domínio (*person*) onde o *value object* vai ser adiconado, fazer a verificação da sua existência. Em caso negativo, adiciona à lista desses *value objects* (*email list*), existente no objecto de domínio *person*. Em caso positivo, rejeita a acção e comunica a excepção *email already registered* para o *controller*.

![sd_us151](diagrams/SD/SD_US151_AddEmail.png)

______

#### 4) Abstração das Account 

Todas as Accounts seguem a mesma forma de criação variando apenas o OwnerID, podendo ser familyID/personID na criação da Cash Account ou personID na criação nos restantes tipos de conta.
Para as Account de person, os diferentes tipos de Accounts são criadas com a selecção do respectivo AccountType, como se encontra presente no diagrama das Factory 1 e 2.


#### US120 - Create **Family** Cash Account

![sd_us120](diagrams/SD/SD_US120_CreateFamilyCashAccount.png)

#### US170,171,172,173 - Create **Person**'s Cash, Bank, BankSavings and Credit Accounts

![sd_us17X](diagrams/SD/SD_US170:171:172:173_CreateAccount.png)

Como é a persistência que cria o ID's para as accounts o **diagrama Factory 1**  é utlizado para obter as account quando ainda não foi atribuido ID pela persistência enquanto que o **diagrama Factory 2** é utilizado para obter as accounts quando já lhes foi atribuido o ID.

#### Account Factory 1 (sem accountID)

![sd_factory_1](diagrams/SD/SD_extra_AccountFactory_1.png)

#### Account Factory 2 (com accountID)

![sd_factory_2](diagrams/SD/SD_extra_AccountFactory_2.png)


### Vista de Implementação

Tal como referido na **vista lógica** a implementação de todas as **user stories** segue uma estrutura concêntrica subdivida em **infrastructure**, **interface adapters**, **use case services** e **domain** com as seguintes dependências.

![class-diagram](diagrams/class-diagram-general.png)



### Vista de Persistência

Para conseguir a persistência de dados na aplicação, foi utilizado um modelo em espelho dos objetos de domínio. 

Cada Objeto de Domínio que se pretende guardar em persistência tem um Objeto de Dados correspondente que utiliza a _programming interface_ Jakarta Persistence API (JPA). Esta simetria de Domínio/Dados é representada na imagem seguinte:


![mirror](https://imgur.com/9Of4KB4.jpg)


Assim que os Objetos de Domínio forem convertidos para Objetos de Dados JPA (usando _Assemblers_ dedicados ao efeito em classes _Repository_ de domínio), serão adicionados à base de dados usando _interfaces_ de Repositórios CRUD adequados ao seu tipo.
O repositório CRUD irá adicionar a informação contida nos Objetos de Dados JPA à base de dados, devolvendo uma cópia do objeto idêntica ou, em alguns casos, com um ID gerado automaticamente aquando da adição. Esta sequencia de processos está representada na imagem seguinte, uma secção do SD da US120 - _Create Family Cash Account_:

![repo](https://i.imgur.com/2fHdjOO.png)

A adição/recolha de informação à base de dados é da inteira responsabilidade dos RepositóriosJPA (_CRUD Repositories_). Os Objetos de Dados JPA apenas são manipulados por estes repositórios, sendo o único envolvimento por outras classes a sua tradução de/para domínio por parte dos DataDomainAssemblers.
Não há nenhum contacto com Objetos JPA e classes na camada de Serviço:

![imp](https://i.imgur.com/mZDVBAV.png)


## Nível 3 (Base de Dados)


### Vista Física
A implementação da aplicação usa duas bases de dados diferentes: POSTGRES para produção e H2 para testes. Esta distinção é obtida através de dois ficheiros de propriedades distintos, que são indicados através duma tag _TestPropertySource_:

```java
@SpringBootApplication
@TestPropertySource(locations = "classpath:application-test.properties")
public class
FFMSpringBootApplication {...}
```

A base de dados POTSGRES está de momento alojada num servidor Amazon Web Service (AWS) 

```java
spring.jpa.database=POSTGRESQL
spring.datasource.platform=postgres
spring.datasource.url=jdbc:postgresql://ffmapp.c5zejpkmwdl8.eu-west-3.rds.amazonaws.com:5432/ffmapp
spring.datasource.username=g3
spring.datasource.password=*********
spring.jpa.show-sql=true
spring.jpa.generate-ddl=true
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.jdbc.lob.non_contextual_creation=true
```