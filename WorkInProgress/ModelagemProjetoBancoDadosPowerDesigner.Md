# Modelagem e Projeto de Banco de Dados com PowerDesigner

## Confira a fazer modelagem e um projeto de banco de dados com o PowerDesigner. Artigo da Revista SQL Magazine - Edição 12.

<iframe class="ad-medium" src="https://www.devmedia.com.br/marketing/banners/banner_160x600/" frameborder="0" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; display: block; height: 600px;"></iframe>

Suporte ao alunoAnotarMarcar como concluído

[Artigos](https://www.devmedia.com.br/artigos/)[Banco de Dados](https://www.devmedia.com.br/artigos/banco-de-dados)Modelagem e Projeto de Banco de Dados com PowerDesigner

Atualmente existem várias ferramentas que auxiliam na documentação e automatização da [modelagem e projeto de banco de dados](https://www.devmedia.com.br/curso/curso-modelagem-de-bancos-de-dados-relacionais/409), dentre as quais podemos destacar o [ErWin](https://www.devmedia.com.br/ca-erwin-data-modeler-modelagem-de-dados-com-erwin/32092) e o [PowerDesigner](https://www.devmedia.com.br/utilizando-a-ferramenta-powerdesigner-na-modelagem-de-aplicacoes/9372). Na primeira edição dessa revista vimos o artigo *'Modelagem de dados com ErWin'*. O objetivo deste artigo é apresentar o **PowerDesigner** mostrando suas características voltadas para projetos de [banco de dados](https://www.devmedia.com.br/cursos/banco-de-dados) e utilizando um estudo de caso bastante semelhante ao apresentado no **artigo sobre ErWin**.

### O PowerDesigner

O PowerDesigner é uma ferramenta da [Sybase para modelagem e soluções](https://www.devmedia.com.br/trabalhando-com-o-sybase-ase-in-memory-database-revista-sql-magazine-93/22801) de projeto para empresas que necessitam construir ou refazer aplicações de forma rápida e consistente. Para isto, o PowerDesigner possui componentes para diversas atividades: [modelagem de processos de negócios](https://www.devmedia.com.br/guia/modelagem-de-processos-de-negocio/35696), [modelagem de dados](https://www.devmedia.com.br/introducao-a-modelagem-de-dados/24953), modelagem de [sistemas orientados a objetos](https://www.devmedia.com.br/principais-conceitos-da-programacao-orientada-a-objetos/32285), armazenamento e controle dos modelos desenvolvidos. Para cada um desses componentes, existe ainda uma série de funcionalidades agregadas. Entretanto, nos restringiremos a discutir as características envolvidas com a modelagem e projeto de bancos de dados.

Sabe-se que um projeto de banco de dados é composto de três fases: modelo conceitual, modelo físico e a criação do script (código com os comandos DDL) responsável por criar toda a estrutura necessária no [sistema gerenciador de banco de dados](https://www.devmedia.com.br/arquitetura-de-um-sgbd/25007) (SGBD). Agora apresentaremos como o PowerDesigner pode auxiliar o DBA durante estas etapas.

### Criando o Modelo Conceitual

Ao iniciar um novo projeto no PowerDesigner, será apresentada uma caixa de diálogo. Esta possibilita a escolha de vários tipos de modelos a serem criados dentre eles: o modelo conceitual (ver **Figura 1**), modelo físico, modelo orientado a objetos utilizando a [linguagem UML](https://www.devmedia.com.br/uml/8579), relatórios e modelos livres (não padronizados). Como neste exemplo estamos projetando um banco de dados e estamos na etapa de criação do modelo conceitual, escolhemos a opção Conceptual Data Model. A partir daí será elaborado o [MER (Modelo Entidade-Relacionamento)](https://www.devmedia.com.br/modelo-entidade-relacionamento-mer/19821). Este é formado por um conjunto de entidades que se relacionam. O MER é representado graficamente através do [DER (Diagrama de Entidade e Relacionamento)](https://www.devmedia.com.br/modelo-entidade-relacionamento-mer-e-diagrama-entidade-relacionamento-der/14332). Para a construção do DER existe uma barra de ferramentas (palette) contendo todos os objetos necessários (ver Figura 2). Caso a palette não esteja visível na sua área de trabalho, abra o menu Tools -> Customize Toolbars... -> e selecione Palette.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image002.jpg)**Figura 1**. Área de trabalho do PowerDesigner

### Criando Entidades

Para criar uma entidade clique no objeto entidade na barra de ferramenta (palette) e dê um outro clique na área de trabalho. Um objeto entidade aparecerá com o nome default “Entity_1”. Para alterar o seu nome para Cliente vá à propriedade da entidade conforme a **Figura 3**. Para isso, clique com o botão direto do mouse sobre a entidade e escolha a opção properties.

Nas propriedades da entidade é possível configurar, dentre outras coisas: o seu nome, o nome que será gerado fisicamente (code) e se a entidade será gerada fisicamente (Generate). Na pasta de atributes da **Figura 4** é possível atualizar os atributos (incluir, alterar ou excluir). Todos os objetos da palette têm propriedades e seguem o mesmo padrão.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image004.gif) **Figura 2**. Barra de ferramentas (palette)

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image006.jpg)**Figura 3**. Propriedades da entidade.

### Criando Atributo

O usuário possui algumas possibilidades para criar atributos. Em propriedade da entidade (Entity properties), existe uma pasta chamada Attributes onde se encontra uma barra de ferramentas que possibilita inserir, excluir ou alterar os atributos. Outra opção é um clique no botão direito do mouse sobre a entidade. Não há necessidade de colocar o tipo de dado do atributo ao projetar o modelo conceitual, mas caso o projetista já tenha essa informação ele pode estar inserindo através de uma tabela padrão apresentada na **Figura 4**. Para que essa tabela apareça é só clicar na coluna Data Type do atributo e depois no botão de reticências.

### Criando Relacionamento

Para criar o relacionamento entre entidades vá à barra de ferramentas, selecione o ícone de relacionamento, clique na entidade pai (entidade origem) e com o botão do mouse ainda pressionado solte-o na entidade filha (entidade destino). A janela da **Figura 5** irá aparecer. Nela é possível especificar as configurações necessárias no relacionamento, tal como a cardinalidade.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image008.jpg)**Figura 4**. Domínio de um atributo

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image010.jpg)**Figura 5**. Propriedades do relacionamento entre as entidades

### Criando Cardinalidade

Através da cardinalidade é possível detalhar o relacionamento, indicando a quantidade de ocorrências mínima e máxima de cada entidade em relação à outra. As possíveis cardinalidades entre entidades são: um para um, um para muitos, muitos para um ou muitos para muitos. Abaixo serão apresentadas duas delas e como elas são importantes no modelo conceitual para que o PowerDesigner gere corretamente o modelo físico.

**1. 1** : (1..N) (um para muitos)
Quando o relacionamento possui esta cardinalidade, além da chave estrangeira ser obrigatória ela também compõe a chave primária da tabela de cardinalidade N, entidade dependente. No nosso exemplo (ver **Figura 6**), não existe produto sem fornecedor. Assim, se o fornecedor for excluído seus produtos correspondentes também serão excluídos. Para implementar o conceito de dependência no PowerDesigner, vá em propriedades do relacionamento, marque a opção Dependent em Produto to Fornecedor, e em Fornecedor to Produto marque a opção Mandatory. Desta forma, configuramos as opções que guiarão o PowerDesigner na geração do modelo físico. Neste caso temos que, como o relacionamento entre fornecedor para produto foi especificado Mandatory, será gerado no modelo físico uma chave estrangeira com restrição NOT NULL.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image013.jpg) ![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image013.jpg)

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image015.jpg)**Figura 6**. Modelo Conceitual de um relacionamento 1:N mapeado para o modelo físico.

**2.** N : N
Como no banco de dados relacional não é possível implementar [diretamente o relacionamento N:N, faz-se necessário explodi-lo em dois relacionamentos 1:N e N:1](https://www.devmedia.com.br/modelagem-1-n-ou-n-n/38894). O PowerDesigner gera automaticamente essa explosão criando uma tabela de relaci onamento que receberá as chaves das tabelas que a originou (ver **Figura 7**). A tabela de relacionamento recebe o nome do relacionamento entre as entidades pedido e produto.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image018.gif)      ![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image018.gif)    ![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image018.gif)**Figura 7**.Modelo Conceitual de um relacionamento N:N mapeado para o modelo físico.

### Criando Herança

Herança é um conceito de orientação a objetos que foi adicionado aos bancos relacionais para dar melhor suporte a relacionamentos cuja semântica diz respeito à criação de tabelas mais genéricas (pai) e mais específicas (filhas). Na Figura 8, a entidade cliente é pai das entidades PessoaJuridica e PessoaFisica. Para criar um relacionamento de herança no PowerDesigner, primeiramente crie a entidade pai e as entidades filhas, conforme o nosso exemplo as entidades: Cliente, PessoaJuridica e PessoaFisica. Logo após, escolha na palette (ver **figura 2**) o ícone de herança (inheritance) dê um clique na entidade filha (PessoaJuridica), um outro clique na entidade pai (Cliente), nos próximos filhos clique na entidade filha (PessoaFisica) e um no conector de herança (veja na figura 8 que o relacionamento de herança é representado por um meio circulo).

Como no modelo físico não existe o conceito de herança, o projetista deve analisar a melhor forma da geração (ler o artigo sobre mapeamento objeto-relacional publicado na edição 5 da SQL Magazine). O PowerDesigner permite várias combinações de geração do modelo de herança (conceitual) para tabelas (físico). Para ter acesso a estas opções, o projetista deve selecionar as propriedades da herança (Inheritance Properties) dando duplo clique no relacionamento de herança (conector). Feito isto, uma janela de diálogo irá aparecer permitindo a configuração de como deve ser a geração automática do modelo físico. Dentre as opções têm-se:

- Gerar apenas a entidade pai (parent) acrescentando todos atributos das entidades filhas (Inherit all attributes).
- Gerar apenas as entidades filhas (children) acrescentando todos os atributos da entidade pai nas filhas.
- Gerar as entidades filhas e entidade pai onde apenas a chave primária é copiada da entidade pai para as filhas ou vice versa.

Neste caso, foi escolhida a opção 1. Veja na **Figura 13** que apenas a tabela cliente foi gerada, contendo as colunas das entidades PessoaJuridica e PessoaFisica. Terminado estes passos, temos o nosso modelo conceitual elaborado (ver **Figura 10**).

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image022.jpg)
**Figura 8**. Configurando Herança



### Criando Associação

Além da herança que faz parte do Modelo Entidade Relacionamento Estendido (MER-E), o PowerDesigner implementa também a associação, que para alguns autores é um tipo de agregação. Para exemplificar, na Figura 9 a associação Entrevista é composta do Candidato a uma certa Oferta de emprego oferecida por uma determinada Empresa.

Este exemplo é classificado como associação ternária uma vez que a entidade associativa Entrevista está associada a 3 (três) outras entidades. Para exemplificar a associação na Figura 9 foi utilizado um exemplo contendo um contexto diferente do estudo de caso deste artigo representado pela **Figura 10.** A criação de relacionamentos de associação segue o mesmo princípio dos demais. Inicialmente é posto no diagrama uma entidade associativa e em seguida são realizadas as conexões necessárias.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image027.gif)

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image025.gif)            ![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image025.gif)**Figura 9**. Associação entre as entidades

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image029.jpg)**Figura 10**. Modelo Conceitual

### Criando o Modelo Físico

Nesta fase o SGBD (Sistema Gerenciador de Banco de Dados) já foi escolhido, e o projeto deve ser direcionado às suas características para uma melhor utilização dos seus recursos. O modelo físico é representado pelo DED (Diagrama de Estrutura de dados). É de responsabilidade do projetista de banco de dados fazer o mapeamento das entidades e atributos para tabelas e colunas respectivamente. Esse mapeamento não é direto e deve ser analisado. Outras atividades como a definição do domínio de cada coluna (baseado no SGBD escolhido) e das chaves estrangeiras também é feita nesta etapa.
No PowerDesigner, o projeto físico é criado automaticamente a partir do projeto conceitual. Assim, temos por exemplo, a geração de tabelas e chaves estrangeiras de forma automatizada. Para gerar o modelo físico a partir do modelo conceitual escolha na barra de menu a opção: Tools-> Generate Physical Data Model. Logo após será apresentado uma janela de diálogo que irá permitir algumas configurações para o mapeamento. Algumas possíveis são: definição do SGBD, prefixo da tabela e nome dos índices (ver **Figuras 11 e 12**). Neste exemplo, escolhemos o SGBD SQL Server 2000.
Ao gerar pela primeira vez o modelo físico o layout parecerá confuso; o projetista deverá arrumar o layout e fazer alguns ajustes no modelo físico gerado.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image031.jpg)**Figura 11**. Escolhendo o SGBD

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image033.jpg)**Figura 12**. Configurando nome das tabelas, índices e regras de Update e Delete

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image035.jpg)**Figura 13.** Modelo Físico

### Geração do Script a partir do Modelo Físico

Para gerar o script do banco de dados escolha na barra de menu a opção Database -> Generation Database... Será aberta a janela de diálogo apresentada na **Figura 14**. Esta janela permite efetuar algumas configurações antes da geração do script. Algumas opções disponíveis são: criação de tabelas (create table), apagar fisicamente as tabelas (drop table) antes de criar, criar chaves primárias e estrangeiras, índices e outros. É possível escolher também como as chaves serão geradas no script: dentro do comando de criação da tabela (inside table) ou fora (outside table - através do comando alter table) - ver **Listagens 1 e 2**.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image037.jpg)**Figura 14**. Geração do Banco de Dados

```
/*===================================================*/
/* Table: tbpedido                                              */
/*===================================================*/
create table tbpedido (
   numpedido            char(8)              not null,
   datpedido            datetime             not null,
   codvendedor          char(4)              null,
   matricula            char(4)              null,
   datvencimento        datetime             null,
   constraint pk_tbpedido primary key  (numpedido, datpedido),
   constraint fk_tbpedido_relations_tbclient foreign key (matricula)
      references tbcliente (matricula),
   constraint fk_tbpedido_relations_tbvended foreign key (codvendedor)
      references tbvendedor (codvendedor)
)
go
```

Listagem 1. Chaves Dentro da Tabela

```
/*=====================================*/
/* Table: tbpedido                                              */
/*=====================================*/
create table tbpedido (
   numpedido            char(8)              not null,
   datpedido            datetime             not null,
   codvendedor          char(4)              null,
   matricula            char(4)              null,
   datvencimento        datetime             null,
   constraint pk_tbpedido primary key  (numpedido, datpedido)
)
go

alter table tbpedido
   add constraint fk_tbpedido_relations_tbclient foreign key (matricula)
      references tbcliente (matricula)
go

alter table tbpedido
   add constraint fk_tbpedido_relations_tbvended foreign key (codvendedor)
      references tbvendedor (codvendedor)
go
```

#### Listagem 2: Chaves Fora da tabela

### Customizando a apresentação dos modelos no PowerDesigner

É possível personalizar algumas tarefas feitas automaticamente pelo PowerDesigner, como o visual do modelo apresentado em tela. Para isto, temos duas opções:



• Tools -> Display Preferences: Disponibiliza várias opções para personalizar o modelo, entre elas: apresentar apenas os atributos chaves das entidades e alterar o formato da entidade (cores de linhas, fontes, etc). O modelo conceitual da Figura 10 foi personalizado para que, por exemplo, não mostrasse os tipos de dados dos atributos nem sua obrigatoriedade (mandatory).
• Tools -> Model Options: Permite, por exemplo, a configuração dos nomes que serão utilizados: (1) na conversão do modelo conceitual para o modelo físico e (2) na geração do script para o BD e deste para o modelo físico. Este último ponto ganha importância uma vez que é interessante deixar a ferramenta customizada para o padrão da empresa.
Outras funcionalidades
O PowerDesigner possui algumas outras funcionalidades importantes ligadas ao projeto de banco de dados, tais como importar arquivos das ferramentas CASE Rational Rose, ErWin e modelos no formato XMI. Isto possibilita que as equipes trabalhem com outras ferramentas e compartilhem seus modelos.
Podemos destacar também o fato do PowerDesigner suportar a geração bi-direcional dos modelos gerados durante o projeto de banco de dados. Ou seja, o mecanismo de engenharia reversa possibilita a criação de modelos através de um banco de dados já existente.

Nota
O XMI (XML Metadata Interchange) é um formato padrão recomendado pela [OMG (Object Management Group)](https://www.devmedia.com.br/revista-engenharia-de-software-magazine-56/27278) desde 1999, que têm como objetivo padronizar o intercâmbio de modelos entre diferentes ferramentas de modelagem.

### Engenharia Reversa

O mecanismo de engenharia reversa possibilita a criação de modelos através de um banco de dados existente. Para efetuar a engenharia reversa devemos seguir os passos:

• File -> Reverse Engineer -> Database...: aparecerá a caixa de diálogo da **Figura 15**, onde podemos informar em qual SGBD as informações serão recuperadas e se a definição será compartilhada ou será feita uma cópia da definição do modelo. Ao confirmar, uma nova caixa de diálogo será apresentada (**Figura 16**) onde o usuário deve informar se a base de origem a ser revertida vem de um script (.sql) ou via ODBC. Após a confirmação o PowerDesigner efetuará a engenharia reversa gerando o modelo conceitual.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image039.jpg)**Figura 15**. Engenharia Reversa.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image041.jpg)**Figura 16**. Engenharia Reversa.

### Relatórios com PowerDesigner

A documentação gerada pelo PowerDesigner, quando utilizada pela primeira vez, não é muito simples. É necessário que o usuário utilize templates ou personalize-os. Para utilizar um template o usuário deve escolher um template em Models -> Reports...
Após escolher um template, será apresentado a **Figura 17**, onde a parte da esquerda (Available items) apresenta as opções de customização do template que o PowerDesigner disponibiliza para o usuário. Ao dar dois cliques no item apresentado à esquerda, automaticamente ele será copiado para o lado direito da figura (Report items) que representa os itens que estarão contidos no relatório final a ser gerado. Por fim, na barra de ferramentas o usuário tem a opção de visualizar o relatório, imprimir, gerar um arquivo .RTF ou .HTML.

![Modelagem e Projeto de Banco de Dados com PowerDesigner](https://www.devmedia.com.br/imagens/SQL/SQL12/ModelagemPowerDesigner4_arquivos/image043.jpg)**Figura 17**. Janela de configuração de relatório.

#### Conclusão

Foram apresentadas neste artigo algumas funcionalidades do PowerDesigner através da elaboração de um projeto de banco de dados.

##### Referências bibliográficas

- ELSMARI, Navathe. Sistemas de Banco de Dados - Fundamentos e Aplicações. Ed. LTC. Terceira Edição. Rio de Janeiro.
- KORTH, Henry F. ; SILBERSCHATZ, Abraham, SUDARSHAN, S. Sistema de Banco de Dados. Ed. Makron Books, Terceira Edição. São Paulo.

Esse artigo foi escrito por **Claudete Moscardini** e **Rosalva Moscardini**

#### Este artigo faz parte da Revista SQL Magazine Edição 12

- [![Revista SQL Magazine Edição 12](https://www.devmedia.com.br/imagens/SQL/SQL12/capaSQL12.JPG)](https://www.devmedia.com.br/modelagem-e-projeto-de-banco-de-dados-com-powerdesigner/link)

AnotarMarcar como concluído