# Utilizando a ferramenta PowerDesigner na modelagem de aplicações

## Este artigo aborda o uso da ferramenta PowerDesigner, desenvolvida pela Sybase, voltada para a modelagem, possibilitando a combinação de modelagem de aplicações como modelagem de dados, diagramas UML, e técnicas de modelagem de processo de negócios.



<iframe class="ad-medium" src="https://www.devmedia.com.br/marketing/banners/banner_160x600/" frameborder="0" style="outline: none; -webkit-tap-highlight-color: transparent; max-width: 100%; margin: auto; display: block; height: 600px;"></iframe>



[Artigos](https://www.devmedia.com.br/artigos/)[Banco de Dados](https://www.devmedia.com.br/artigos/banco-de-dados)Utilizando a ferramenta PowerDesigner na modelagem de aplicações

Para otimizar recursos no desenvolvimento de uma aplicação, aumentando sua qualidade e confiabilidade, é importante utilizar ferramentas CASE (Computer-Aided Software Engineering).

Este artigo aborda o uso da ferramenta PowerDesigner, desenvolvida pela [Sybase](https://en.wikipedia.org/wiki/Sybase), voltada para a modelagem, possibilitando a combinação de modelagem de aplicações como [modelagem de dados](https://www.devmedia.com.br/modelagem-de-dados-tutorial/20398), [diagramas UML](https://www.devmedia.com.br/uml/), e técnicas de modelagem de processos de negócios. Aqui abordaremos a construção de um destes modelos, através da construção de um diagrama de classes a partir de um estudo de caso.

**A Sybase PowerDesigner gera modelos de dados de vários tipos e estilos, e exporta o código gerado por seus modelos para diversas linguagens de programação**.

### Descrição do cenário

Para demonstrar parte das funcionalidades desta ferramenta é utilizado um diagrama de classes apresentando um fragmento do modelo de um sistema de livraria, conforme mostra a **Figura 1**. As classes Cliente e Livro representam os cadastros básicos. A classe Pessoa representa uma generalização da classe Cliente, incluindo seu Endereço. A classe Pedido registra as compras realizadas pelos clientes. A classe ItemPedido representa os pedidos de Livros realizados por um cliente em um pedido.

![Modelo de Classes do estudo de caso](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image1.jpg)**Figura 1**. Modelo de Classes do estudo de caso

### Criando o diagrama de classes

A ferramenta possui uma janela inicial (ver **Figura 2**) dividida em duas partes, onde é possível navegar nas suas funcionalidades. Do lado esquerdo, é possível navegar pelos diagramas que já foram gerados, ou ainda, por componentes e atributos já incluídos no diagrama. Do lado direito, se encontra a área de construção do diagrama, onde este será projetado, e suas classes e respectivos relacionamentos inseridos.

![Janela Inicial](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image2.jpg)**Figura 2.** Janela Inicial

Para se construir o diagrama de classes anteriormente proposto, deve-se acessar a barra de menu File à New. Um assistente de criação de diagramas é exibido, conforme a **Figura 3**. Muitos são os tipos de diagramas possíveis de serem desenvolvidos com a ferramenta PowerDesigner. Selecionaremos o modelo orientado a objetos, ou ObjectOrientedModel. Algumas definições podem ser efetuadas para o diagrama a ser criado. Neste caso, as configurações se manterão. A opção New model foi escolhida por ser um novo diagrama a ser criado. Em Model Name, o nome do novo modelo será preenchido com modeloLivraria. A opção Object Language é a linguagem base que o **PowerDesigner** trabalhará na criação do diagrama. Em caso de futuras exportações de dados, é possível exportar para uma linguagem de desenvolvimento definida nesta opção. Utilizaremos a [linguagem Java](https://www.devmedia.com.br/guias/java). Esta não é uma escolha definitiva, já que está linguagem pode ser alterada no projeto a qualquer momento. A opção First diagram ficará com o valor Class Diagram, por ser um diagrama de classes o projeto que será desenvolvido.

![Assistente de criação de diagramas](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image3.jpg)**Figura 3.** Assistente de criação de diagramas

Em seguida, a janela de construção de diagramas é disponibilizada, com o documento em branco e uma caixa de ferramentas com os componentes necessários para a construção deste. Esta paleta de ferramentas contém componentes de inserção de classes e relacionamentos entre elas.

### Inserindo as classes no diagrama

Para inserir cada classe no novo diagrama, será utilizado o componente Class, representado pelo ícone ![icon](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image01.jpg) da caixa de ferramentas, clicando então na área reservada para a construção do modelo. A opção de pop-up das classes possibilita ter acesso a todas as suas propriedades. Para abrir uma janela com todas estas propriedades dividias em abas, deve-se clicar com o botão direito do mouse na classe criada e selecionar a opção Properties, ou simplesmente dar um clique duplo sobre a classe. A aba General, exibida na **Figura 4**, possibilita a definição do nome da classe criada (no nosso exemplo, Cliente), bem como do tipo (Type = Class) e se a classe é pública, privada ou protegida (Visibility = public).

![Janela com propriedades da Classe](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image4.jpg)**Figura 4.** Janela com propriedades da Classe – Aba General

A aba Attributes permite criar os atributos da classe e seus tipos. Para a classe Cliente devem ser definidos os atributos codigo e limiteCredito (ver **Figura 5**).

![Janela com propriedades da Classe, Aba Attributes](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image5.jpg)**Figura 5**. Janela com propriedades da Classe – Aba Attributes

Existem outras abas com informações referentes à linguagem selecionada, como a aba Java, que possibilita inserir informações específicas à linguagem.

Através da aba Preview, é possível observar a criação da classe criada na linguagem Java (ver **Figura 6**).

![Resultado em Java da classe Cliente](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image6.jpg)**Figura 6**. Resultado em Java da classe Cliente

O mesmo procedimento deve ser efetuado para as demais classes e atributos. A criação dos atributos pode ser observada através das **Tabelas 1 a 5** representando respectivamente as classes Pessoa, Endereco, Pedido, ItemPedido e Livro.

| **Pessoa**  |                  |
| ----------- | ---------------- |
| ***Name\*** | ***Data Type\*** |
| Nome        | String           |
| Telefone    | String           |
| Email       | String           |

**Tabela 1**. Atributos da classe Pessoa

| **Endereco** |                  |
| ------------ | ---------------- |
| ***Name\***  | ***Data Type\*** |
| Rua          | String           |
| Número       | Int              |
| Cidade       | String           |

**Tabela 2**. Atributos da classe Endereço

| **Pedido** |               |
| ---------- | ------------- |
| **Name**   | **Data Type** |
| Número     | Int           |
| Data       | String        |
| Status     | String        |

**Tabela 3**. Atributos da classe Pedido

| **ItemPedido** |               |
| -------------- | ------------- |
| **Name**       | **Data Type** |
| PrecoUnitario  | String        |
| Quantidade     | Int           |

**Tabela 4**. Atributos da classe ItemPedido

| **Livro** |               |
| --------- | ------------- |
| **Name**  | **Data Type** |
| ISBN      | String        |
| Titulo    | String        |
| Autor     | String        |
| Preço     | String        |

**Tabela 5**. Atributos da classe Livro

### Criação dos relacionamentos

Para criar os relacionamentos é necessário localizar o componente adequado na caixa de ferramentas![caixa de ferramentas](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image02.jpg)(Generalização, Associação, Agregação, Composição e Dependência, respectivamente). O relacionamento entre as classes Cliente e Pedido é uma associação, pois permite navegar de um objeto de uma classe até um objeto da outra e deve ser definido através do componente Association ![Association](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image03.jpg). Ao clicar com o botão direito do mouse no relacionamento é possível escolher a opção Properties, que possibilita definir a multiplicidade do relacionamento, conforme mostra a **Figura 7**. Este relacionamento possui multiplicidade 1:N, pois permite que um Cliente faça vários Pedidos e que um Pedido seja obrigatoriamente de um único Cliente.

![Associação](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image7.jpg)**Figura 7**. Associação

O relacionamento entre as classes Endereco e Pessoa é do tipo composição, que permite que um objeto da classe pessoa contenha um objeto da classe Endereco. Mas se o objeto da classe Pessoa é removido, o objeto da classe Endereco referente a este objeto também o será. Para criar este relacionamento deve ser utilizado o componente Composition ![Composition](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image04.jpg), onde se define qual classe compõe a outra através da opção Container, de acordo com a **Figura 8**.

![Composição](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image8.jpg)**Figura 8.** Composição

O relacionamento entre as classes Cliente e Pessoa é do tipo Generalização e permite que uma classe herde todas as características de outra. Através do componente Generalization ![Generalization](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image05.jpg)(**Figura 9**) pode-se definir este relacionamento entre as classes.

![Herança](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image9.jpg)**Figura 9**. Herança

O relacionamento entre as classes Pedido e ItemPedido é uma agregação. Este relacionamento permite que um objeto contenha uma lista de outros objetos, informando que a classe ItemPedido está contida na classe Pedido. O relacionamento é criado através do componente Aggregation ![Aggregation](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image06.jpg) e devem ser definidas suas multiplicidades, conforme pode ser observado na **Figura 10**.

![Agregação](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image10.jpg)**Figura 10.** Agregação

O relacionamento entre as classes ItemPedido e Livro é definido através do componente Association ![Association](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image03.jpg). Para esse relacionamento, na área referente à Classe Livro, deve-se ativar a opção Navigable, pois se trata de um relacionamento unidirecional (ver **Figura 11**).

![Relacionamento Unidirecional](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image11.jpg)**Figura 11**. Relacionamento Unidirecional

### Conversão de diagramas

**A ferramenta PowerDesigner permite se trabalhar com várias formas de saída de dados a partir dos diagramas criados**. No menu Tools encontram-se várias destas opções de exportação e manipulação dos dados. É possível, assim, gerar outros diagramas com os dados já incluídos neste diagrama de classes. Como exemplo, será gerado um modelo físico, isto é, um DTR (Diagrama de Tabelas Relacionais). Para isso, basta acessar o menu Tools à Generate Physical Data Model. Uma janela com um assistente será exibida, como mostrado na **Figura 12**, onde algumas configurações devem ser feitas. A opção Generate new Physical Data Model deve ser mantida selecionada, já que estamos gerando um novo modelo, e não alterando um existente. A opção de banco de dados que será escolhida é o banco de dados InterBase 6.x. Na aba Selection, deve-se selecionar todas as classes que se tornarão tabelas no modelo físico.

![Janela de configuração de conversão de diagramas](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image12.jpg)**Figura 12.** Janela de configuração de conversão de diagramas

Ao clicar no botão OK, o novo diagrama é gerado, se tornando mais um item da lista de projetos abertos, mais à esquerda da janela da ferramenta, conforme a **Figura 13**.

![Resultado da conversão para o modelo físico de banco de dados](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image13.jpg)**Figura 13.** Resultado da conversão para o modelo físico de banco de dados

### Gerando relatórios

Uma funcionalidade bastante interessante da ferramenta é a possibilidade de gerar relatórios e documentação referente aos modelos construídos. Para este exemplo, será utilizado o assistente de criação de relatórios. Para acessar este assistente, basta clicar em Report à Report Wizard. Cinco passos compõem este assistente. Inicia-se no passo Welcome. Nesta primeira fase, devem ser definidos o nome do relatório que está sendo gerado e o idioma de saída deste. O idioma padrão é o inglês. Uma opção interessante deste assistente é a importação de idiomas. O download destes arquivos externos pode ser feito através do site da Sybase, no formato xrl, e ser inserido na lista de idiomas de saída. O formato xrl é um formato particular da Sybase para idiomas, e significa eXchangeable Report Language.

Ao clicar em next, o foco se transfere para o passo Presentation Options. Nesta opção, é possível determinar o formato de saída do relatório, como o formato HTML. Outro formato de saída é o formato rtf – formato aberto por editores de texto. Existem ainda templates, ou modelos que podem ser utilizados para criação de relatórios. Os templates se resumem a cores de objetos e formatações de texto. Ainda nesta janela, é possível importar templates externos e visualizar o relatório com o template selecionado pelo usuário. Será mantido neste exemplo o formato de saída como HTML e o template Light Blue.

Ao clicar em next, o foco é alterado para a guia Report Structure, com botões de check onde podem ser definidos os itens que serão ou não exibidos no relatório. Todos os objetos, relacionamentos e descrições podem ser marcados ou desmarcados para exportação para relatório. Há ainda nesta tela um botão, com o nome de Define. Esta opção abre uma nova janela com um espaço aberto para digitação, onde é possível inserir textos de comentários no relatório final.

Feita a seleção dos componentes a serem exportados para o relatório, passa-se para a guia Report Layout. É possível nela definir quais componentes serão emitidos no relatório. Esta funcionalidade deixa o usuário livre para definir como será realmente o layout final deste relatório.

Ao clicar novamente em next, o foco atinge a guia End. Esta é a fase final de criação de relatório através do assistente. Nela, é possível antes de gerar o relatório, ter uma previsão de como ele ficará exatamente, clicando no botão Preview. Basta clicar em finish para que o relatório seja gerado, em formato HTML, como previamente definido. O relatório final gerado é mostrado pela **Figura 14.**

![Relatório gerado em HTML executado por um navegador](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image14.jpg)**Figura 14.** Relatório gerado em HTML executado por um navegador

### Importação/Exportação

**A PowerDesigner faz a geração do modelo para arquivos na linguagem previamente determinada como linguagem alvo** – no caso deste artigo, [Java](https://www.devmedia.com.br/guia/linguagem-java/38169). A ferramenta disponibiliza recursos que possibilitam importação e exportação de arquivos através de formato XML (eXtensible Markup Language), facilitando assim o relacionamento do PowerDesigner com outras ferramentas.

É possível fazer a exportação para código em Java, criando as classes a partir do diagrama, e também efetuar a engenharia reversa deste processo, gerando classes no diagrama a partir de classes externas em Java. Para se exportar dados deste projeto, basta acessar a opção Language à Generate Java Code. Deve-se informar o caminho onde os arquivos serão salvos, como pode ser visto na **Figura 15.** A opção Check Model garante que uma revisão será feita no projeto antes da operação ser iniciada, para garantir a consistência do diagrama. Cada uma das classes dará origem a arquivos separados com a extensão .java.

![Janela de geração de classes em Java](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image15.jpg)**Figura 15.** Janela de geração de classes em Java

A importação de classes externas em Java é feita de forma semelhante ao processo de exportação. Ao clicar em Language à Reverse Engineer Java, uma janela é exibida, onde os arquivos serão importados. O campo Reverse Engineer permite selecionar o tipo de dado que será importado. A opção Java Files será mantida, pois é a mais abrangente, possibilitando a importação de qualquer arquivo relacionado à linguagem Java, incluindo as suas classes. Para adicionar arquivos a serem importados, basta clicar no botão Add. Finalizado este processo, ao clicar em OK, as classes externas serão interpretadas, importadas e inseridas no diagrama.

### Comparando modelos

A ferramenta também dispõe de uma facilidade que pode ser muito útil em caso de divergência de modelos, através da opção Compare Models, do menu Tools. Esta comparação só pode ser feita sobre diagramas do mesmo tipo. Na **Figura 16**, é possível verificar que o diagrama utilizado neste artigo está sendo comparado a um novo diagrama qualquer, também de classes. Na janela exibida, há uma divisão onde o lado esquerdo é representado pelo diagrama da livraria, e o lado direito, pelo novo diagrama. É possível analisar item por item de cada diagrama, verificando o que um possui e o outro não. Na parte inferior da janela existe uma lista comparativa entre os dois modelos, onde cada linha apresenta uma diferença encontrada.

![Janela de comparação de modelos](https://www.devmedia.com.br/Imagens/gold/SQL/53/artigo8/image16.jpg)**Figura 16**. Janela de comparação de modelos

### Outras funcionalidades

**A interface da PowerDesigner** dispõe de um menu, denominado Model, que possibilita a visualização de tudo o que já foi inserido e trabalhado no diagrama. Através deste menu, é possível ter acesso, por exemplo, aos planos de negócio empregados no projeto, às classes já inseridas e suas propriedades, todos os tipos de relacionamento utilizados, dentre outros dados. Todos os componentes que compõem a paleta de ferramentas do diagrama e que foram utilizados, podem ser listadas através deste menu, de forma a se ter um controle de tudo o que foi utilizado no diagrama, como cada componente está funcionando e como estes estão interagindo entre si.

### Conclusão

A PowerDesigner é uma ferramenta que tem como vantagem a integração de diferentes modelos utilizados na construção de aplicações, diferenciando-se de outras ferramentas que precisam ser adquiridas separadamente, com poucas funcionalidades referentes à integração dos modelos.

Além do tipo de diagrama aqui descrito, a ferramenta possibilita a construção de diversos outros modelos. Mesmo não sendo uma ferramenta gratuita, sua aquisição pode ser vantajosa, levando em consideração que suas funcionalidades podem auxiliar em diversos tipos de projeto.

Este artigo apresentou a ferramenta PowerDesigner e mostrou a construção de um dos modelos oferecidos pela ferramenta, o diagrama de classes.

**Links**:

- Site oficial do [PowerDesigner](https://www.sap.com/index.html)