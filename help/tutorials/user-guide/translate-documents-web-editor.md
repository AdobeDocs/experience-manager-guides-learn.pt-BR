---
title: Traduzir documentos do Editor da Web
description: Saiba como traduzir documentos do Editor da Web
source-git-commit: 331871308035441f047b1ed588215b586daf3d28
workflow-type: tm+mt
source-wordcount: '1517'
ht-degree: 0%

---


# Traduzir documentos do Editor da Web {#id21BKF0Z0YZF}

>[!TIP]
>
> É recomendável usar esse recurso de Tradução no Editor da Web se tiver atualizado para AEM Guias as a Cloud Service versão de fevereiro de 2022 ou posterior.

AEM Guias vem com um recurso poderoso no Editor da Web que permite traduzir o conteúdo em vários idiomas. Você pode criar um novo projeto de tradução e adicionar posteriormente os trabalhos de tradução ao projeto de tradução existente. Você também pode criar um projeto de tradução em vários idiomas que inclua trabalhos de tradução para todos os idiomas selecionados.

>[!NOTE]
>
> O administrador pode configurar a guia Gerenciar \(usada para tradução\) no Editor da Web. Para obter mais detalhes, consulte *Configurar o recurso de tradução no Editor da Web* na seção Instalar e configurar os guias do Adobe Experience Manager as a Cloud Service.

## Antes de começar

Antes de executar as etapas neste procedimento, verifique se você criou as pastas de direcionamento e raiz de idioma necessárias

1. Crie uma pasta raiz para armazenar o conteúdo de origem. A pasta raiz deve ser criada com o nome de idioma \(como inglês\) ou código de idioma \(en\).
1. Crie as pastas de destino para as quais deseja traduzir o conteúdo. Por exemplo, se você quiser traduzir o conteúdo para alemão ou francês, crie uma pasta chamada -de \(para alemão\) ou -fr \(para francês\).

>[!NOTE]
>
> A pasta raiz e as pastas de destino devem ser criadas no mesmo nível.

## Criar um novo projeto de tradução

1. No painel Repositório, abra o arquivo de mapa DITA na exibição de mapa.
1. Clique no botão **Gerenciar** guia . O painel Tradução exibe o título hipervinculado do mapa DITA junto com o **Languages** lista.
1. No **Languages** selecione a localidade para a qual deseja traduzir o projeto. Você pode selecionar **Todos** para traduzir o projeto para todos os idiomas disponíveis.

   >[!NOTE]
   >
   > A lista contém as pastas de idioma, juntamente com seus códigos de idioma. Por exemplo, francês \(fr\) e alemão \(de\).

   >[!IMPORTANT]
   >
   > Idioma mostra apenas os idiomas para os quais uma pasta de idioma é criada paralelamente ao idioma de origem. Uma pasta de idioma criada em qualquer outro nível, como um nível abaixo da pasta de idioma de origem também não é exibida. Certifique-se de criar todas as pastas de idioma de destino no mesmo nível da pasta de idioma de origem.

   ![](images/translation-languages.png)

1. Você também pode usar as seguintes opções:

   **Usar linha de base:** Você pode selecionar uma linha de base para traduzir o projeto. Clique em Usar linha de base e escolha uma linha de base criada no mapa. Todos os arquivos que fazem parte da Linha de base selecionada são mostrados na página Tradução . Após a tradução do conteúdo, é possível exportar a Linha de base traduzida. Para obter mais detalhes sobre como exportar a linha de base traduzida, consulte [Exportar linha de base traduzida](generate-output-use-baseline-for-publishing.md#id196SE600GHS).

   **Usar a versão mais recente como em**: Escolha filtrar a versão dos tópicos com base na data e hora de criação. Ao selecionar uma data e hora, somente a versão mais recente dos arquivos criados na ou antes da data e hora selecionadas são mostradas.

1. Clique em **Aplicar**. Uma lista com detalhes dos tópicos e ativos associados é exibida.
1. Selecione os tópicos que deseja enviar para tradução.

   Também é possível usar as seguintes opções de filtragem de tópicos:

   - **Título**: Título do arquivo de origem
   - **Nome do arquivo**: Nome do arquivo de origem
   - **Tipo de arquivo**: Tipo do arquivo de origem. As opções disponíveis são Mapa, Tópico e Imagem.
   - **Tipo de referência**: Referências diretas ou indiretas
   - **Versão**: Número da versão do arquivo de origem
   - **Rótulo da versão**: Rótulo para a versão selecionada do arquivo de origem
   - **Versão de destino**: Número da versão do arquivo de destino
   - **Estado do documento**: Estado do arquivo de origem. As opções disponíveis são Rascunho, Em revisão e Revisado.
   - **Idioma de destino**: O idioma para o qual você deseja traduzir o arquivo de origem
   - **Status da tradução**: As opções disponíveis são: Sincronizado, Cópia ausente, Em andamento e Sincronizado.
   - **Rótulo de destino**: Rótulo para a versão selecionada do arquivo de destino
1. Clique em **Enviar para tradução** no canto superior direito.

   ![](images/translation-send.png)

1. Na lista suspensa , selecione **Criar um novo projeto de tradução**.

   ![](images/translation-project-types.png)

   Além de um novo projeto de tradução, você também pode selecionar entre as seguintes opções:

   - Você pode optar por **Criar uma estrutura** apenas para o projeto de tradução.
   - Você pode selecionar **Criar um novo projeto de tradução em vários idiomas** que incluirá tarefas de tradução para todos os idiomas selecionados para tradução. Por exemplo, se você selecionou francês, alemão e espanhol, ele criará um projeto que contém trabalhos de tradução para os três idiomas.
   - Se você já tiver um projeto de tradução, poderá adicionar tópicos a esse projeto. Selecione Adicionar a **Projeto de tradução existente** na lista Projeto e escolha um projeto na lista Projeto de tradução existente. Você pode classificar esses projetos por ordem mais recente, crescente ou decrescente.

      >[!NOTE]
      >
      > Se o projeto existente for um projeto de escopo, ele terá &#39;\(Escopo\)&#39; anexado em seu nome.

   - Se você precisar criar o escopo de um projeto a ser traduzido, poderá selecionar **Criar um novo projeto de tradução de escopo**. Isso não enviará as cópias para tradução e o status de tradução original dos arquivos será mantido. Não há impacto na cópia do idioma de destino dos tópicos referenciados que são enviados para escopo.
1. No campo **Título do projeto**, informe um título para o projeto.
1. Clique em **Criar** para criar um novo projeto de tradução.

   Um novo projeto de tradução é criado com a versão selecionada dos tópicos. No momento, uma mensagem pop-up é exibida confirmando que o projeto de tradução foi criado. Quando todas as cópias de idioma de destino estiverem disponíveis no projeto de tradução, você receberá uma notificação na Caixa de entrada. Depois que as cópias de idioma de destino estiverem disponíveis no projeto de tradução, você poderá prosseguir e iniciar o trabalho de tradução. Para obter detalhes, consulte [Iniciar o trabalho de tradução](translation-first-time.md#id225IK030OE8).

   >[!NOTE]
   >
   > Se você rejeitar a tradução de um ou mais tópicos em um trabalho de tradução, a variável **Em Andamento** o status de tradução de todos os tópicos rejeitados é revertido para o status original. O status dos tópicos referenciados é verificado e revertido de acordo com o estado de tradução mais recente. Além disso, os arquivos de tradução criados no projeto de destino não são excluídos, mesmo se a tradução for rejeitada para eles.


## Passe o rótulo da versão para a versão de destino

AEM Guias permite que você passe o rótulo do arquivo de origem para o arquivo de destino. Isso ajudará você a identificar facilmente a versão de origem do arquivo traduzido.

Para adicionar o rótulo da versão de origem à cópia de destino, o administrador do sistema deve selecionar a opção **Propagar rótulos de versão de origem para a versão de destino** nos termos do **Tradução** em **Configurações do editor**.

Por exemplo, se você tiver alguns arquivos de origem com o rótulo da versão `Release 1.0` aplicado a eles, você também pode passar no rótulo de origem \(`Release 1.0`\) ao arquivo traduzido.

![](images/translation-pass-source-label.png)

>[!NOTE]
>
> O rótulo de origem é anexado somente a uma versão de destino. Se você mover o rótulo de origem para outra versão, ele será refletido automaticamente no rótulo de destino mais recente.

## Exibir diferença de versão para arquivos fora de sincronia 

AEM Guias fornece o recurso para verificar as diferenças entre a versão selecionada e a última versão de origem traduzida dos tópicos. Você pode optar por traduzir a variável **Fora de Sincronização** arquivos com base nas alterações feitas.

![](images/translation-version-diff.png)

Selecione o **Mostrar diferença**&#x200B;ícone \(![](images/show-difference-icon.svg)\) para um tópico para ver as diferenças entre a última versão traduzida e a versão atual do arquivo selecionado.

>[!NOTE]
>
> **Mostrar diferença** ícone \(![](images/show-difference-icon.svg)\) aparece somente para arquivos DITA que têm o status de tradução como **Fora de Sincronização**.

O **Diferença de versão** será exibida. Mostra o **Última versão traduzida** e **Versão selecionada** à esquerda. A janela de pré-visualização exibe as diferenças entre a última versão traduzida e a versão selecionada do tópico.

![](images/version-diff.png)

## Ignorar ativos fora de sincronia

Se você fizer alterações em alguns dos ativos, esses ativos ficarão Fora de Sincronização. Você pode traduzir novamente os ativos modificados ou optar por descartar o status Fora de Sincronização. Por exemplo, se você fez algumas alterações muito menores que realmente não precisam de uma tradução, você pode marcar o status como Em sincronia.

Para descartar o status Fora de Sincronização, execute as seguintes etapas:

1. Selecione os ativos fora de sincronia para os quais deseja alterar o status.
1. Selecione o **Marcar Sincronizado** botão \(![](images/translation-mark-in-sync-icon.svg)\) no topo. O **Marcar Sincronizado** será exibida.

   ![](images/translation-mark-in-sync.png)

1. Clique em **Forçar Sincronização**. Ele define o status como Em sincronia para os ativos Fora de sincronização selecionados.

>[!NOTE]
>
> **Marcar Sincronizado** botão \(![](images/translation-mark-in-sync-icon.svg)\) aparece somente para ativos que têm o status de tradução como Fora de Sincronização.

## Exibir projetos de tradução em andamento para um mapa ou tópico

Algumas das referências no painel de tradução podem estar em andamento. Essas referências têm um **Em Andamento** link em **Status da tradução** coluna. Ao clicar no link, a variável **Projetos em andamento** será aberta. Na caixa de diálogo, é possível ver a lista de todos os projetos de tradução em andamento \(junto com o idioma de destino\) que contêm a referência selecionada.

>[!NOTE]
>
> Você pode ver o link Em andamento dos projetos traduzidos criados na versão dos Guias AEM as a Cloud Service de fevereiro de 2023 ou posterior.

Clique no nome da referência na caixa de diálogo para abri-la no modo de visualização. Você também pode clicar no projeto de tradução para iniciar a tradução.

![](images/translation-in-progress.png)

**Tópico principal:**[ Trabalhar com o editor da Web](web-editor.md)

