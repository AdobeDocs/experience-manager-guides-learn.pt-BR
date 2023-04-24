---
title: Trabalhar com o editor básico de mapa
description: Saiba como trabalhar com o Editor de mapa básico
source-git-commit: af5c64312a608affe95fd552b3dd1b2e05ea2b8e
workflow-type: tm+mt
source-wordcount: '1394'
ht-degree: 0%

---


# Trabalhar com o editor básico de mapa {#id1942CM005Y4}

O Editor de mapa básico fornece um recurso fácil de arrastar e soltar para adicionar tópicos do repositório de AEM a fim de criar o mapa DITA ou o mapa de favoritos. Você pode adicionar tópicos aninhados, tabelas de relacionamento \(reltable\), atributos e informações de metadados, além de validar o mapa para corrigir.

>[!NOTE]
>
> Se o administrador ativou a opção Editor de mapa avançado , você não terá acesso ao Editor de mapa básico. Por padrão, todos os arquivos de mapa serão abertos no Editor de mapa avançado.

As seções a seguir descrevem as várias funções disponíveis no Editor de mapa básico.

## Adicionar tópicos a um arquivo de mapa {#id193CBL0505Z}

Depois que um arquivo de mapa é criado, é necessário adicionar tópicos ao arquivo de mapa. Com o Editor de mapa básico, é possível adicionar tópicos, tabelas de relacionamento ou outros arquivos de mapa.

Execute as seguintes etapas para criar o arquivo de mapa:

1. Na interface do usuário do Assets, navegue até o arquivo de mapa que deseja editar.

1. Para obter um bloqueio exclusivo no arquivo de mapa, selecione o arquivo de mapa e clique em **Check-out**.

   >[!NOTE]
   >
   > Depois que você tiver um bloqueio exclusivo em um arquivo de mapa, outros usuários não poderão editar o mapa. No entanto, eles poderiam trabalhar nos tópicos do arquivo de mapa.

1. Com o arquivo de mapa selecionado, clique em **Editar**.

   O arquivo de mapa é aberto para edição no Editor de mapa. Usando o Editor de mapa, você cria um mapa usando os tópicos disponíveis no momento que são exibidos no painel Referências .

   ![](images/dita-map-01.png)

1. Usar o **Referências** , navegue até a pasta que contém os tópicos ou os submapas que deseja adicionar.

   >[!NOTE]
   >
   > Você pode adicionar tópicos ou submapas de qualquer pasta no painel Referências .

1. Para adicionar o primeiro tópico ao mapa, arraste e solte o tópico no Editor de mapa básico.

   >[!NOTE]
   >
   > Após adicionar o primeiro link, o link Adicionar nova referência estará disponível quando você passar o mouse sobre um tópico existente no mapa.

1. Para adicionar tópicos subsequentes ou um submapa, arraste e solte o tópico ou submapa no local desejado no mapa.

   Se você adicionar um submapa ao mapa DITA, o submapa será mostrado como um link no mapa DITA. Para exibir todos os tópicos do submapa, clique no link do submapa. O conteúdo do submapa é mostrado em uma nova guia.

   >[!NOTE]
   >
   > Se você soltar um novo tópico em um tópico existente no mapa, você receberá uma mensagem sobre a substituição do tópico. Clique em Sim se quiser substituir o tópico, clique em Não se não quiser substituir o tópico. Você pode usar CTRL+Z e CTRL+Y para desfazer ou refazer qualquer alteração no mapa.

1. Clique em **Salvar**.


## Recursos disponíveis na barra de ferramentas do Editor de mapa básico

A barra de ferramentas principal no Editor de mapa básico permite executar as seguintes tarefas:

![](images/ditamap-toolbar-actions.png)

**A: Pesquisar**

Você pode pesquisar e incluir os tópicos necessários do DAM. Clicar nesse ícone exibe a caixa de diálogo Pesquisar :

![](images/search-dita-map.png)

Insira as palavras-chave que deseja pesquisar, essas palavras-chave são correspondidas no nome de arquivo, conteúdo e até mesmo valores de atributo do tópico. Quando os resultados da pesquisa estiverem disponíveis, selecione o tópico desejado\(s\) e clique no botão Verificar para adicionar os arquivos selecionados ao final da estrutura do mapa. Você pode filtrar os resultados da pesquisa especificando os parâmetros Modificar Data .

**B: Grupo**

Clique na caixa de seleção à esquerda dos tópicos e clique em Grupo na barra de ferramentas para agrupar os tópicos selecionados. Para obter mais informações sobre tópicos de agrupamento, consulte o [topicgroup](https://docs.oasis-open.org/dita/v1.0/langspec/topicgroup.html) documentação na Especificação de idioma OASIS DITA.

**C: Excluir**

Clique na caixa de seleção à esquerda de um tópico e clique em Excluir na barra de ferramentas para remover os tópicos selecionados do mapa.

**D: Mostrar números/Ocultar números**

Exibir a numeração de \(ou ocultar\) para os tópicos no mapa.

**E: Validar**

Verifique se o mapa é válido ou tem erros.

**F: Modo Padrão/Modo XML**

No **Modo padrão**, clicar em um link de tópico mostra a visualização do tópico em uma nova guia. Clicar no **Modo padrão** ícone altera seu modo para **Modo XML**. Em **Modo XML**, clicar em qualquer parte de uma linha de tópico mostra o XML subjacente das referências de tópico dentro do tópico. Na exibição XML de origem, há um **Recuo Automático** que reorganiza o código XML em formato apresentável e facilmente legível. Caso esteja editando um mapa manualmente, a exibição de origem também executa verificações de validação. Caso seu XML contenha erros, o mesmo é realçado no **Modo XML** e você não tem permissão para salvar o arquivo de mapa DITA. Se quiser exibir o XML para o mapa inteiro, clique em qualquer lugar fora do limite do tópico.


**Observação:** No modo Padrão, é possível usar os atalhos do teclado para desfazer \(`Ctrl+z`\) ou refazer \(`Ctrl+y`\) a última ação.


![](images/dita-map-invalid-source.png)

**G: Propriedades do mapa**

Exibe a caixa de diálogo Propriedades do mapa, onde é possível definir os atributos e as informações de metadados para o mapa. Para adicionar um atributo, clique no botão **Adicionar** no canto inferior esquerdo da caixa de diálogo para obter o botão **Atributo** lista suspensa. Na lista , selecione o atributo que deseja adicionar. Se o atributo selecionado tiver valores predefinidos especificados no DTD, esses valores serão apresentados em uma nova lista suspensa. Você pode selecionar o valor desejado na lista suspensa. Se não houver um valor predefinido, você receberá uma caixa de texto para inserir um valor para o atributo selecionado.

![](images/map-properties.png)

## Recursos disponíveis no nível do tópico no Editor de mapa básico

Ao passar o mouse sobre um tópico ou um arquivo de submapa no Editor de mapa básico, você pode executar as seguintes tarefas:

![](images/ditamap-actions.png)

**A: Mover para a esquerda ou Mover para a direita**

Clique nos ícones de seta para a esquerda ou para a direita para mover o tópico para a esquerda ou para a direita. Mover um tópico de uma maneira que o torne um filho \(nest\) ou irmão \(remove aninhamento\) em relação ao tópico acima dele.

**B: Propriedades**

Clique no ícone Propriedades para abrir a caixa de diálogo Propriedades de Topicref. Com essa caixa de diálogo, é possível definir os atributos do tópico e as informações de metadados. Para obter mais informações sobre atributos e metadados de tópicos padrão, consulte o [topicref](https://docs.oasis-open.org/dita/v1.2/os/spec/langref/topicref.html) documentação na Especificação de idioma OASIS DITA.


![](images/map-properties-metadata.png)

**C: Adicionar nova referência**

Clique no ícone Adicionar nova referência para adicionar uma nova referência como um irmão do tópico atual.

**D: Adicionar nova definição de chave**

Clique no ícone Key para adicionar uma nova definição de chave. Qualquer chave substituída ou chave que já tenha sido definida no mapa será exibida em vermelho. Se clicar no ícone Propriedades em uma definição de chave, a caixa de diálogo Propriedades do teclado será exibida.

## Trabalhar com tabelas de relacionamento no Editor de mapa básico {#id1944B0I0COB}

Os editores de mapa dos Guias AEM vêm com um recurso poderoso que permite criar e editar tabelas de relacionamento no mapa DITA.

Execute as seguintes etapas para trabalhar com tabelas de relacionamento no Editor de mapa básico:

1. Na interface do usuário do Assets, navegue até o mapa DITA no qual deseja criar a tabela de relacionamento.

1. Clique no mapa DITA para abri-lo no console do mapa DITA.

1. Selecione o **Tópicos** para ver uma lista de tópicos disponíveis no mapa DITA.

   >[!TIP]
   >
   > A guia Tópicos oferece uma opção para baixar o arquivo de mapa com seus dependentes. Para obter mais detalhes, consulte [Exportar um arquivo de mapa DITA](authoring-download-assets.md#id218UBA00IXA).

1. Na barra de ferramentas principal, clique em **Editar**.

   O arquivo de mapa é aberto no Editor de mapa básico.

1. Selecionar **Relacionável** na barra de ferramentas.

   ![](images/reltable.png)

1. Arraste e solte tópicos da lista de tópicos para o editor Reltable.

   >[!NOTE]
   >
   > Você pode adicionar tópicos de qualquer pasta no painel Referências .

   ![](images/create-reltable.png)

1. Para adicionar um cabeçalho à tabela de relacionamento, clique em **Adicionar Relheader**.

1. Para adicionar uma coluna à tabela de relacionamento, clique em **Adicionar uma coluna**.

   ![](images/complete-reltable.png)

1. Clique em **Salvar**.


Também é possível executar as seguintes ações no editor de tabela de relacionamento:

**Excluir linhas ou colunas**

Para excluir uma coluna da tabela, marque a caixa de seleção no cabeçalho da coluna e clique em Excluir. Para remover uma linha da tabela, marque a caixa de seleção na primeira coluna da respectiva linha e clique em Excluir.

**Excluir um tópico**

Se quiser excluir um tópico da tabela, clique no ícone de cruz ao lado do tópico.

**Excluir a tabela de relacionamento**

Se quiser excluir a tabela de relacionamento, clique em qualquer lugar fora da tabela de relacionamento e clique em Excluir.

**Tópico principal:**[ Trabalhar com o Editor de Mapa](map-editor.md)

