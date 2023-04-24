---
title: Site AEM
description: Saiba como AEM Site
source-git-commit: 23d6c87b525f0763990166e46f4bd4ac2d6e7cd5
workflow-type: tm+mt
source-wordcount: '2545'
ht-degree: 0%

---


# Site AEM {#id205BE3008SW}

As opções a seguir estão disponíveis para a saída do Site de AEM:

Você pode criar a predefinição de site AEM de duas maneiras:

**No Editor da Web:** No painel Repositório, abra o arquivo de mapa DITA na Visualização de mapa e, na guia Saída, selecione o ícone + para criar uma predefinição de saída e, em seguida, selecione AEM Site no menu suspenso do tipo na caixa de diálogo Adicionar predefinição.No editor da Web, as configurações foram organizadas em guias Geral e Avançado:

**Geral**

O **Geral** contém as seguintes configurações:

- Nome do site
- Caminho de saída
- Páginas de saída existentes
- Excluir páginas do site órfão
- Aplicar condições usando \(se as condições forem definidas para um mapa\)
- Usar Linha de Base \(Se uma linha de base for criada para um mapa\)
- Fluxo de trabalho de pós-geração

**Avançado**

A guia Advanced contém as seguintes configurações:

- Limpar arquivos temporários DITA-OT
- Gerar PDF separado para cada tópico
- Usar propriedades de mapa como padrão

Para obter detalhes, consulte [Configuração do site AEM](#id231KIM004X1).

**No painel de mapa**

Para abrir predefinições de saída para AEM Site, clique em um arquivo de mapa DITA na interface do usuário do Assets, em seguida, clique em Predefinições de Saída e na opção de saída AEM Site. No painel de mapa, clique em **Editar** na parte superior para atualizar as várias configurações e, em seguida, clique em **Salvar**.

>[!TIP]
>
> Consulte a *Publicação AEM Site* no guia de práticas recomendadas para obter as práticas recomendadas relacionadas à criação AEM saída do Site.

## Configuração do site AEM {#id_aem_site_config}

As opções a seguir estão disponíveis para a saída do Site de AEM:

| Opções do AEM Site | Descrição |
| --- | --- |
| Tipo de saída | O tipo de saída que você deseja gerar. Para gerar saída responsiva AEM Site , escolha a opção AEM Site . |
| Nome da configuração | Dê um nome descritivo para as configurações do site de AEM que você está criando. Por exemplo, você pode especificar *Saída de clientes internos* ou *saída de usuários finais*. |
| Nome do site | Um nome de site onde a saída é armazenada em seu repositório AEM.<br><br>Um nó no repositório de AEM é criado com o nome especificado aqui. Se você não especificar o Nome do site, o nó do site será criado com o nome do arquivo do mapa DITA.<br><br>O Nome do site especificado aqui também é usado como o título na guia do navegador.<br><br>Você também pode usar variáveis ao definir o Nome do site. Para obter mais detalhes sobre o uso de variáveis, consulte [Use variáveis para definir as opções Caminho de destino, Nome do site ou Nome do arquivo](generate-output-use-variables.md#id18BUG70K05Z). |
| Design | Selecione o template de design que deseja usar para gerar a saída.<br><br>Para obter detalhes sobre como usar modelos de design personalizados para gerar saída, entre em contato com o administrador de publicação. |
| Caminho de destino | O caminho no repositório de AEM, onde a saída é armazenada. Ao gerar a saída final, o Nome do site e o Caminho de destino são combinados. Por exemplo, se você especificar o Nome do site como `user-guide` e o Caminho de destino como `/content/output/aem-guides`, então a saída final é gerada sob a variável `/content/output/aem-guides/user-guide` nó .<br><br>Você também pode usar variáveis ao definir o Caminho de destino. Para obter mais detalhes sobre o uso de variáveis, consulte [Use variáveis para definir as opções Caminho de destino, Nome do site ou Nome do arquivo](generate-output-use-variables.md#id18BUG70K05Z). |
| Aplicar condições usando | Selecione uma das seguintes opções:<br><br>**Nenhum Aplicado**: Selecione essa opção se não quiser aplicar nenhuma condição na saída publicada.<br>**Arquivo DITAVal**: Selecione DITAVall file(s) para gerar conteúdo condicional. Você pode selecionar vários arquivos DITAVal usando a caixa de diálogo Procurar ou digitando o caminho do arquivo. Use o ícone de cruz próximo ao nome do arquivo para removê-lo. Os arquivos DITAVal são avaliados na ordem especificada, de modo que as condições especificadas no primeiro arquivo têm prioridade sobre as condições correspondentes especificadas nos arquivos posteriores. Você pode manter a ordem dos arquivos adicionando ou excluindo arquivos. Se o arquivo DITAVal for movido para outro local ou excluído, ele não será excluído automaticamente do painel de mapa. Você precisa atualizar o local caso os arquivos sejam movidos ou excluídos. Você pode passar o mouse sobre o nome do arquivo para ver o caminho no repositório AEM onde o arquivo está armazenado. Você só poderá selecionar arquivos DITAVal e um erro será exibido se você selecionar qualquer outro tipo de arquivo.<br>**Predefinição de condição**: Selecione uma predefinição de condição no menu suspenso para aplicar uma condição enquanto publica a saída. Essa opção estará visível se você tiver adicionado uma condição para o arquivo de mapa DITA. As configurações condicionais estão disponíveis na guia Predefinições de condição do console de mapa DITA. Para saber mais sobre a predefinição de condição, consulte [Usar predefinições de condição](generate-output-use-condition-presets.md#id1825FL004PN). |
| Páginas de saída existentes | Selecione o **Substituir conteúdo** opção para substituir conteúdo nas páginas existentes. Essa opção substitui apenas o conteúdo presente nos nós de conteúdo e cabeçalho da página. Essa opção permite a publicação combinada de conteúdo. Selecionar essa opção fornece uma opção para selecionar a exclusão de páginas órfãs da saída publicada. Isso também é o *default* para criar a saída AEM Site .<br><br>Selecione o **Excluir e criar** para forçar a exclusão de quaisquer páginas existentes durante a publicação. Essa opção exclui o nó da página, juntamente com o conteúdo e todas as páginas filhas. Use essa opção se tiver alterado o modelo de design da predefinição de saída ou se desejar que outras páginas já presentes no destino sejam removidas. |
| Excluir páginas do site órfão | Selecionar o **Substituir conteúdo** no **Páginas de saída existentes** apresenta essa opção. Se você selecionar essa opção, então todas as páginas órfãs serão excluídas do AEM Site publicado. Para que esse recurso seja executado com êxito, você deve publicar o mapa DITA inteiro e não usar a publicação incremental.<br><br>Digamos que você publicou um mapa DITA, que contém os tópicos a.dita, b.dita e c.dita. Antes de publicar o mapa novamente, você removeu o tópico b.dita do mapa. Agora, se você selecionou essa opção, todo o conteúdo relacionado a b.dita será removido da saída do Site AEM e apenas a.dita e c.dita serão publicadas.<br><br>Este recurso não remove nenhum mapa filho publicado. Por exemplo, se o mapa pai contiver um mapa filho e você remover todo o mapa filho, o conteúdo do mapa filho não será excluído da saída publicada. No entanto, se você remover qualquer tópico de um mapa filho e republicar, o conteúdo do tópico removido será excluído da saída do site.<br><br>Além disso, se houver algum conteúdo referenciado e esse conteúdo for removido antes da republicação, os dados do conteúdo referenciado não serão removidos.<br><br>**Observação**: As informações sobre páginas órfãs excluídas também são capturadas nos logs de geração de saída. Para obter mais informações sobre como acessar os arquivos de log, consulte [Visualizar e verificar o arquivo de log](generate-output-basic-troubleshooting.md#id1821I0Y0G0A__id1822G0P0CHS). |
| Limpar arquivos temporários DITA-OT | Selecione essa opção para limpar os arquivos temporários gerados pelo DITA-OT. O local onde o DITA-OT armazena arquivos temporários pode ser encontrado no log de geração de saída.<br><br>Se você estiver apresentando erros ao gerar saída por meio do DITA-OT, é possível desmarcar essa opção para reter os arquivos temporários. Em seguida, você pode usar esses arquivos para solucionar erros de geração de saída. |
| Gerar PDF separado para cada tópico | Se selecionada, um PDF também é criado para cada tópico no mapa DITA. Ao escolher essa opção, uma nova opção Dividir caminho do PDF é exibida.<br><br>No campo Dividir caminho do PDF, especifique o caminho para armazenar os PDF gerados para cada tópico.<br><br>**Observação**: AEM Guias usa o plug-in DITA-OT chamado pdfx para gerar PDF para cada tópico. Esse plug-in é fornecido com o pacote DITA-OT fornecido pronto para uso. Você pode personalizar esse plug-in para gerar o PDF de acordo com suas necessidades. Se você usar um plug-in DITA-OT personalizado, integre o plug-in pdfx para ter capacidade de geração de PDF no nível do tópico. |
| Executar fluxo de trabalho de pós-geração | Ao escolher essa opção, uma nova lista suspensa Fluxo de trabalho de pós-geração é exibida contendo todos os fluxos de trabalho configurados no AEM. Você deve selecionar um workflow que deseja executar após a conclusão do workflow de geração de saída. |
| Usar linha de base | Se tiver criado uma Linha de base para o mapa DITA selecionado, selecione essa opção para especificar a versão que deseja publicar.<br><br>**Importante**: Quando você está gerando saída incremental para o Site de AEM, a saída é criada usando a versão atual dos arquivos e não a Linha de Base anexada.<br><br>Consulte [Trabalhar com linha de base](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) para obter mais detalhes. |
| Propriedades | Selecione as propriedades que deseja processar como metadados. Essas propriedades são definidas na página Propriedades do mapa DITA ou do arquivo de mapa de favoritos. As propriedades selecionadas na lista suspensa são listadas abaixo do campo Propriedades e são removidas da lista suspensa.<br><br>**Observação**: As propriedades de metadados fazem distinção entre maiúsculas e minúsculas.<br><br>*Se você selecionou uma Linha de base, os valores das propriedades serão baseados na versão da Linha de base selecionada.<br>* Se você não tiver selecionado uma Linha de base, os valores das propriedades serão baseados na versão mais recente.<br><br>Você também pode transmitir os metadados para a saída usando a publicação DITA-OT. Para obter mais detalhes, consulte [Transmita os metadados para a saída usando DITA-OT](pass-metadata-dita-ot.md#id21BJ00QD0XA).<br><br>**Observação**: Se você não tiver definido a variável `cq:tags` na opção Propriedades , em seguida, os valores para `cq:tags` são selecionadas da cópia de trabalho atual mesmo que tenha selecionado uma linha de base para publicação. |
| Usar Propriedades Do Mapa Se Estiver Ausente No Tópico | Se selecionada, as propriedades definidas para o arquivo de mapa também são copiadas para os tópicos em que essas propriedades não estão definidas. Considere os seguintes pontos ao usar essa opção:<br><br>*Somente as propriedades String, Date ou Long (singe com vários valores) podem ser passadas para as páginas do Site AEM.<br>* Os valores de metadados para uma propriedade do tipo String não suportam caracteres especiais (como `@, #, " "`).<br>* Essa opção deve ser usada juntamente com o `Properties` opção. |

## Nota adicional sobre AEM Site

### Gerar saída baseada em artigos no Editor da Web

Você pode gerar a saída do Site de AEM para um ou mais tópicos, ou o mapa DITA inteiro no Editor da Web. É necessário criar predefinições de saída para o mapa DITA e gerar facilmente a saída do Site de AEM para o mapa. Se você atualizou alguns tópicos em seu mapa, também poderá gerar a saída do Site de AEM somente para esses tópicos do Editor da Web. Para obter mais detalhes, consulte [Publicação baseada em artigo no Editor da Web](web-editor-article-publishing.md#id218CK0U019I).

### Gerar tópicos de vinculação de saída de outros mapas

É um cenário muito comum ter um grande conjunto de documentação distribuída por várias pastas e mapas DITA. Torna-se extremamente complexo publicar conteúdo vinculado a vários locais. Por padrão, todos os links `<xref>` são criados com `local` `@scope`. A publicação desses tópicos não envolve nenhum desafio, pois usa um link direto para o tópico. Caso o tópico esteja fora do mapa DITA atual, o link não mostrará o conteúdo vinculado.

Outra maneira de vincular conteúdo é criar um link usando o `peer` `@scope`. Para tal conteúdo, o link é resolvido em tempo de execução, escolhendo o contexto configurado para o tópico vinculado do contexto de publicação do mapa DITA. A captura de tela a seguir mostra o painel Propriedades de um link que tem o `peer` `@scope`:

![](images/peer-link-scope-link.png){width="800" align="left"}

Para simplificar a publicação de mapas complexos e tópicos que se vinculam a outros tópicos em outros mapas, os Guias de AEM permitem que você defina o contexto de publicação para cada predefinição de saída.

O contexto de publicação permite especificar qual tópico deve ser usado a partir de qual mapa para publicar uma saída específica. Vamos entender isso com a ajuda de um exemplo — digamos que você tenha quatro pastas: amostra a, amostra b, amostra c e amostra d. Cada pasta contém um mapa DITA — mapa DITA A, mapa DITA B, mapa DITA C e mapa DITA D. A vinculação entre mapas acontece quando um tópico no mapa DITA A é vinculado a um tópico no mapa DITA B, C ou D. Na captura de tela a seguir, um tópico de conceito de amostra contém links \(ou referências\) para arquivos que fazem parte de outros mapas DITA.

![](images/sample-concept-link-to-other.png){width="450" align="left"}

Agora, ao definir as configurações de publicação do AEM Site para o arquivo de mapa que contém este tópico, você pode selecionar qual contexto de publicação para o conteúdo vinculado é usado durante a publicação. Um contexto de publicação é uma combinação do mapa DITA e de sua predefinição de saída. A predefinição de saída, por sua vez, contém uma versão específica do conteúdo e predefinições condicionais. Toda essa combinação do mapa DITA, predefinição de saída, versão \(arquivos\) e condições definem o contexto de publicação para um mapa vinculado.

Execute as etapas a seguir para especificar o contexto de publicação para arquivos intervinculados:

1. Abra o **Predefinições de saída** guia do mapa DITA que deseja publicar.

1. Selecione o **Site AEM** predefinição de saída.

   Você obtém as guias Configurações de predefinições AEM e Publicar contexto .

   ![](images/aem-site-publish-settings.png){width="800" align="left"}

1. Abra o **Publicar contexto** guia .

   É exibida uma lista de tópicos dependentes. Esses são os tópicos que são vinculados a partir de algum tópico no mapa atual, mas estão disponíveis em outros mapas DITA.

   >[!NOTE]
   >
   > A guia Publicar contexto mostra tópicos que estão vinculados usando o `peer` `@scope` somente. Para links com `local` `@scope`, não é necessário especificar o contexto de publicação.

   Por padrão, todos os tópicos vinculados têm a predefinição de saída mais recente e o mapa selecionado.

   ![](images/default-publish-context.png){width="800" align="left"}

1. Para alterar a seleção padrão do mapa e da predefinição do DITA, clique em **Editar** \(na barra de ferramentas principal\).

1. Se quiser usar a saída publicada mais recentemente de cada arquivo dependente no mapa, selecione **Usar o contexto de publicação gerado mais recentemente para todos os tópicos dependentes**.

1. No **Mapa principal** na lista suspensa, selecione o arquivo de mapa com cuja saída você deseja vincular a saída do mapa atual.

   Ao selecionar um arquivo de mapa, a UUID do mapa é mostrada na coluna UUID do mapa pai. As Predefinições de saída associadas ao mapa selecionado são listadas na lista Predefinição do mapa pai.

1. No **Predefinição do mapa pai** na lista suspensa, selecione a predefinição de saída com a qual deseja vincular a saída do mapa atual.

1. Selecione o mapa necessário e sua predefinição de saída para todos os tópicos dependentes e clique em **Concluído**.

   O contexto dos tópicos dependentes agora está definido. Você pode gerar a saída do mapa atual. Para obter mais informações sobre a geração de output, consulte [Gerar saída para um mapa DITA a partir do console de mapa](generate-output-for-a-dita-map.md#).

### Publicação combinada

Os Guias AEM são compatíveis com a publicação de conteúdo DITA no site de AEM existente. Por exemplo, se você tiver um site existente, poderá usar a saída AEM Site para publicar somente o conteúdo DITA nesse site. Nesse processo, o conteúdo não DITA existente não é modificado pelo processo de publicação. Para obter mais informações sobre como configurar seu site para publicar somente conteúdo DITA, entre em contato com o administrador da publicação.

### Publicação `conref`

Se estiver usando `conref` no seu conteúdo, ele é publicado como conteúdo normal ou incorporado junto com o conteúdo no tópico de origem \(ou referência\). O `conref` o conteúdo é renderizado junto com o conteúdo principal e nenhuma página de site separada é criada para o mesmo. Quando você pesquisa o conteúdo referenciado na variável `conref`, em seguida, somente o tópico principal ou a página que contém a variável `conref` o conteúdo é mostrado nos resultados da pesquisa.

>[!NOTE]
>
>Se você gerou páginas separadas para a variável `conref` conteúdo usando os Guias AEM versão 3.5 ou anterior, é recomendável limpar/excluir essas páginas usando a variável [Excluir páginas do site órfão](#delete-orphan-page-aem-site) opção.


### Pesquisar uma string dentro do conteúdo

Você pode procurar por uma string na saída do Site de AEM. Por padrão, você pode pesquisar a string somente nos títulos. Para procurar a string no conteúdo ou no corpo da saída do site AEM, entre em contato com o administrador do sistema para ativar a propriedade flating.enabled .


<img src="images/aem-output-search.png" alt="Pesquisar AEM saída do Site" width="800">

Para obter mais detalhes, consulte *Configurar o nivelamento AEM estrutura do nó do Site* no guia Instalar e configurar os guias do Adobe Experience Manager.

**Tópico principal:**[ Noções básicas das predefinições de saída](generate-output-understand-presets.md)