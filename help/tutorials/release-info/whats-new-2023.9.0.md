---
title: Notas de versão | Novidades no Adobe Experience Manager Guides, versão de setembro de 2023
description: Conheça os recursos novos e aprimorados da versão de setembro de 2023 do Adobe Experience Manager Guides as a Cloud Service
source-git-commit: c01c3500b55f3579633ad1a954f9010783365add
workflow-type: tm+mt
source-wordcount: '1361'
ht-degree: 0%

---

# Novidades da versão de setembro de 2023 do Adobe Experience Manager Guides as a Cloud Service

Este artigo aborda os recursos novos e aprimorados da versão de setembro de 2023 do Adobe Experience Manager Guides (mais tarde conhecido como *Guias de AEM as a Cloud Service*).

Para obter mais detalhes sobre as instruções de atualização, a matriz de compatibilidade e os problemas corrigidos nesta versão, consulte [Notas de versão](release-notes-2023.7.0.md).

## Conecte-se a uma fonte de dados e insira dados em seus tópicos

Agora você pode se conectar rapidamente às suas fontes de dados usando conectores prontos para uso do AEM Guides. Conectar-se a uma fonte de dados permite manter suas informações sincronizadas com a fonte, e qualquer atualização dos dados é refletida automaticamente, tornando os Guias AEM um verdadeiro hub de conteúdo. Esse recurso ajuda a economizar tempo e esforço para adicionar ou copiar os dados manualmente.

O AEM Guides permite que o administrador configure os conectores prontos para uso para bancos de dados JIRA e SQL (MySQL, PostgreSQL, SQL Server, SQLite). Eles também podem adicionar outros conectores estendendo as interfaces padrão.
Depois de adicionado, você pode visualizar os conectores configurados listados no painel Fontes de dados no Editor da Web.

<img src="assets/data-sources.png" alt="Lista de fontes de dados no painel" width="300">

*Exibir as fontes de dados conectadas.*

Crie um trecho de conteúdo para buscar os dados de uma fonte de dados conectada. Em seguida, você pode inserir os dados em seus tópicos e editá-los. Depois de criar um gerador de snippet de conteúdo, você pode reutilizá-lo para inserir os dados em qualquer tópico.

Agora você também pode criar um tópico de uma fonte de dados conectada. Um tópico pode conter dados em vários formatos, como tabelas, listas e parágrafos. Também permite criar um mapa DITA para todos os tópicos. Você pode associar metadados ao tópico ao extrair de uma fonte de dados.

Para obter mais detalhes, consulte [Usar dados da sua fonte de dados](../user-guide/web-editor-content-snippet.md).

## Adicionar citações ao seu conteúdo

Citações são referências à fonte de informações adicionada ao conteúdo. Citações ajudam a estabelecer credibilidade e evitar plágios. As citações ajudam os leitores a localizar a fonte e verificar as informações apresentadas no texto.

Nos Guias do AEM, é possível adicionar citações ou importar citações e aplicá-las ao conteúdo. É possível adicionar essas citações de qualquer fonte de livros, sites e diários.

Depois de inserir as citações nos tópicos, você pode visualizá-las no Editor da Web. Você também pode publicar conteúdo com citações usando o PDF nativo.

![Citações listadas em um painel](assets/citation-panel.png){width="300" align="left"}
*Exibir a lista de citações no painel Citações.*

Para obter mais detalhes, consulte [Adicionar e gerenciar citações no seu conteúdo](../user-guide/web-editor-apply-citations.md).


## Publicar em um fragmento de conteúdo

Fragmentos de conteúdo são partes distintas do conteúdo no AEM. São conteúdos estruturados com base em um modelo de conteúdo. Fragmentos de conteúdo são conteúdo puro sem informações de design ou layout. Eles podem ser criados e gerenciados independentemente dos canais compatíveis com o AEM. A modularidade e a reutilização dos fragmentos de conteúdo levam a maior flexibilidade, consistência, eficiência e gerenciamento mais simples.

Agora, os Guias do AEM oferecem uma maneira de publicar um tópico ou os elementos dentro de um tópico em um fragmento de conteúdo. Você pode criar um mapeamento baseado em JSON entre um tópico e um modelo de fragmento de conteúdo. Use esse mapeamento para publicar em um fragmento de conteúdo o conteúdo presente em alguns ou todos os elementos de um tópico.

Aproveite o potencial do AEM Guides e fragmentos de conteúdo e use fragmentos de conteúdo em qualquer site de AEM. Também é possível extrair os detalhes por meio de APIs compatíveis com fragmentos de conteúdo.

![opção para publicar o fragmento de conteúdo](assets/content-fragment-publish.png){width="550" align="left"}
*Publicar um tópico em um fragmento de conteúdo.*

## Revisar melhorias

Os Guias do AEM agora oferecem um recurso aprimorado de revisão com as seguintes funcionalidades:

### Pesquisar tópicos de revisão

Realizar revisões é um recurso essencial dos Guias do AEM. Ajuda os revisores a revisar os documentos atribuídos a eles .
Agora é possível pesquisar um tópico inserindo alguma parte do texto do título ou caminho de arquivo na barra de pesquisa da exibição de tópicos do painel de revisão. Você também pode optar por exibir todos os tópicos ou exibir tópicos com comentários. Por padrão, é possível exibir todos os tópicos presentes na tarefa de revisão. Para obter mais detalhes, consulte [Revisar tópicos](../user-guide/review-topics.md).

![Pesquisar em um painel de tópicos de revisão](assets/review-search-topic.png){width="800" align="left"}
*Pesquisar um tópico de revisão no painel de revisão.*



## Estrutura de extensão do Guides

Crie pacotes personalizados sobre os Guias do AEM para fornecer extensibilidade usando a Estrutura de extensão dos Guias do AEM. Esses pacotes são úteis para desenvolvedores e consultores e fornecem extensibilidade aos componentes no Editor. Eles podem direcionar botões, caixas de diálogo e listas suspensas e adicionar JavaScript personalizado que pode interoperar facilmente com a interface do usuário dos Guias AEM.



## Aprimoramentos de PDF nativo

As seguintes melhorias de PDF nativo foram feitas na versão 4.3.0 para tornar os Guias de AEM um produto mais robusto:



### Ordenar páginas na saída do PDF

Você pode mostrar ou ocultar as seguintes seções no PDF e também organizar a ordem em que elas devem aparecer na saída final do PDF:

* TOC
* Capítulos e tópicos
* Lista de figuras
* Lista de tabelas
* Índice
* Glossário
* Citação
* Layouts de página

Se você não quiser mostrar uma seção específica na saída do PDF, oculte isso desativando o botão de alternância.

Para obter mais detalhes, consulte [Ordem da página](../native-pdf/components-pdf-template.md#page-order).

### Mesclar páginas

Em uma saída de PDF nativo por padrão, todas as seções começam em uma nova página. Agora é possível mesclar uma seção com sua página anterior ou com a próxima página. Isso publica a seção em continuação com a página selecionada na saída do PDF e não há quebra de página entre elas.

Para obter mais detalhes, consulte a descrição do recurso Mesclar páginas em [Ordem da página](../native-pdf/components-pdf-template.md#page-order) seção.

### Páginas estáticas

Você também pode criar layouts de página personalizados e publicá-los como páginas estáticas na saída do PDF. Isso ajuda a adicionar qualquer conteúdo estático, como Notas ou páginas em branco.

Para obter mais detalhes, consulte a descrição do recurso Páginas estáticas em [Ordem da página](../native-pdf/components-pdf-template.md#page-order) seção.


### Variáveis em referências cruzadas

Você pode usar variáveis para definir uma referência cruzada. Quando você usa uma variável, seu valor é extraído das propriedades.

Agora você também pode usar {figure} e {table}.
Uso {figure}para adicionar uma referência cruzada ao número da figura. Ele escolhe o número de figura a partir dos estilos de numeração automática que você definiu para legenda digital.

Uso {table} para adicionar uma referência cruzada ao número da tabela. Ele escolhe o número da tabela a partir dos estilos de numeração automática definidos para a legenda.

Para obter mais detalhes, consulte [Referências cruzadas](../native-pdf/components-pdf-template.md##cross-references).



### Reformulação do editor de CSS

Agora, o editor de CSS foi reprojetado para obter uma melhor experiência do usuário com seletores e propriedades de estilo.

#### Aprimoramento da caixa de diálogo Adicionar estilo

Agora é possível usar seletores personalizados para adicionar estilos complexos. O novo campo Seletor ajuda você a adicionar seletores personalizados além da combinação Classe, Tag e Pseudo Classe. Por exemplo, você pode criar `table a.link` estilo para todos os hiperlinks dentro de uma tabela.

![adição de estilos nos modelos de pdf nativos](assets/add-styles-native-pdf.png){width="300" align="left"}

#### Personalizar propriedades de estilo

Agora, o AEM Guides apresenta a você um novo painel de propriedades na seção de visualização para estilos. É possível editar as propriedades dos estilos de forma mais eficiente e rápida no painel de propriedades.



## Selecionar todas as predefinições em uma coleção de mapas

É possível não apenas selecionar uma predefinição individual, mas também ativar todas as predefinições de um mapa DITA de uma só vez.
![editar uma coleção de mapas](assets/edit-map-collection.png){width="800" align="left"}\
*Selecione todas as predefinições em uma coleção de mapas.*

Para obter mais detalhes, consulte [Usar coleção de mapas para geração de saída](../user-guide/generate-output-use-map-collection-output-generation.md).


## Suporte nativo ao PDF no painel de publicação em massa


Com o recurso de ativação em massa dos Guias do AEM, você pode ativar rápida e facilmente seu conteúdo, desde a criação até a instância de publicação. No mapa de Ativação em massa, é possível incluir a predefinição de saída de PDF nativo, o site AEM, PDF, HTML5, Personalizado e saída JSON.
Para obter mais detalhes, consulte [Ativação em massa de conteúdo publicado](../user-guide/conf-bulk-activation.md).

## Ferramenta de movimentação em massa aprimorada

Agora, como administrador, você pode usar a aprimorada Ferramenta de movimentação em massa para mover pastas com muitos arquivos de um local para outro.
Você pode usar a caixa de diálogo Procurar arquivo para selecionar as pastas de origem que deseja mover. Você também pode procurar e selecionar o local de destino para mover as pastas de origem. Selecionar ![ícone de informações](assets/info-icon.svg) {width="25" align="left"} próximo a um campo para exibir mais informações sobre ele.

Para obter mais detalhes, consulte [Mover arquivos em massa](../user-guide/authoring-file-management.md#move-files-bulk).


