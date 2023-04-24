---
title: Usar editor DISAVAL
description: Saiba como usar o editor DISAVAL
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---


# Editor DITAVAL {#id17C5E0U0OQE}

Os arquivos DITAVAL são usados para gerar saída condicional. Em um único tópico, você pode adicionar condições usando atributos de elemento para condicionar o conteúdo. Em seguida, crie um arquivo DITAVAL em que especifique as condições que devem ser selecionadas para gerar conteúdo e qual condição deve ser deixada de fora da saída final.

AEM Guias permitem que você crie e edite facilmente arquivos DITAVAL usando o editor DITAVAL. O editor DISAVAL recupera os atributos \(ou tags\) definidos em seu sistema e você pode usá-los para criar ou editar arquivos DITAVAL. Para obter mais detalhes sobre como criar e gerenciar tags no AEM, consulte [Administração de tags](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/sites/authoring/features/tags.html?lang=en) na documentação AEM.

## Criar arquivo DITAVAL

Execute as seguintes etapas para criar um arquivo DITAVAL:

1. Na interface do usuário do Assets, navegue até o local onde deseja criar o arquivo DISAVAL.

1. Clique em **Criar** \> **Tópico DITA**.

1. Na página Blueprint, selecione o modelo de arquivo DITAVAL e clique em **Próximo**.

1. Na página Propriedades , especifique o **Título** e **Nome** para o ficheiro DITAVAL.

   >[!NOTE]
   >
   > O nome é sugerido automaticamente com base no Título do arquivo. Se você quiser especificar manualmente o nome do arquivo, verifique se o Nome não contém espaços, apóstrofe ou chaves e termina com .ditaval.

1. Clique em **Criar**. A mensagem Tópico criado é exibida.

   Você pode optar por abrir o arquivo DITAVAL para edição no editor DISAVAL ou salvar o arquivo de tópico no repositório AEM.


## Editar arquivo DITAVAL

Execute as seguintes etapas para editar um arquivo DITAVAL:

1. Na interface do usuário do Assets, navegue até o arquivo DISAVAL que deseja editar.

1. Para obter um bloqueio exclusivo no arquivo, selecione o arquivo e clique em **Check-out**.

1. Selecione o arquivo e clique em **Editar** para abrir o arquivo no editor Guides DITAVAL AEM.

   O editor DISAVAL permite executar as seguintes tarefas:

   A: Alternar painel esquerdo : Alternar a exibição do painel esquerdo. Se você tiver aberto o arquivo DISAVAL por meio do mapa DITA, o mapa e o repositório serão mostrados nesse painel. Para obter mais informações sobre como abrir um arquivo por meio do mapa DITA, consulte [Editar tópicos por meio do mapa DITA](map-editor-advanced-map-editor.md#id17ACJ0F0FHS).

   B: Salvar : Salva as alterações feitas no arquivo. Todas as alterações são salvas na versão atual do arquivo.

   C: Adicionar propriedade : Adicione uma única propriedade no arquivo DISAVAL.

       ![](images/ditaval-editor-props.png)
       
       A primeira lista suspensa lista os atributos DITA permitidos que você pode usar no arquivo DITAVAL. Há cinco atributos compatíveis: &quot;público-alvo&quot;, &quot;plataforma&quot;, &quot;produto&quot;, &quot;props&quot; e &quot;outros props&quot;.
   
   : A segunda lista suspensa mostra os valores configurados para o atributo selecionado. Em seguida, a próxima lista suspensa mostra as ações que você pode configurar no atributo selecionado. Os valores permitidos no menu suspenso de ação são - `include`, `exclude`, `passthrough`e `flag`. Para obter mais informações sobre esses valores, consulte a definição de [prop](http://docs.oasis-open.org/dita/dita/v1.3/errata01/os/complete/part3-all-inclusive/langRef/ditaval/ditaval-prop.html#ditaval-prop) elemento na documentação do OASIS DITA

   D: Adicionar todas as propriedades : Se quiser adicionar todas as propriedades condicionais ou atributos definidos no sistema com um único clique, use o recurso Adicionar todas as propriedades.

>[!NOTE]
>
> Se todas as propriedades condicionais definidas já existirem no arquivo DITAVAL, você não poderá adicionar mais propriedades. Você recebe uma mensagem de erro neste cenário.

    ![](images/ditaval-all-props.png)

1. Quando terminar de editar o arquivo DITAVAL, clique em **Salvar**.

   >[!NOTE]
   >
   > Se você fechar o arquivo sem salvar, as alterações serão perdidas. Se você não deseja confirmar as alterações em AEM repositório, clique em **Fechar** e, em seguida, clique em **Fechar sem salvar** no **Alterações não salvas** caixa de diálogo.


## Visualizações do editor DISAVAL

O editor DITAVAL dos Guias AEM suporta a exibição de arquivos DITAVAL em dois modos ou exibições diferentes:

Autor : Esta é uma visualização típica do que você vê é a que você obtém \(WYSISYG\) do editor DITAVAL. É possível adicionar ou remover propriedades usando a interface do usuário simples, que apresenta as propriedades, seus valores e ações na lista suspensa. Na exibição Autor, você tem as opções para inserir uma propriedade individual e inserir todas as propriedades com um único clique.

: Você também pode encontrar a versão do arquivo DITAVAL em que está trabalhando no momento ao passar o ponteiro do mouse sobre o nome do arquivo.

Fonte : A exibição Origem exibe o XML subjacente que compõe o arquivo DITAVAL. Além de fazer edições de texto regulares nesta exibição, um autor também pode adicionar ou editar propriedades usando o Catálogo inteligente.

    Para chamar o Catálogo inteligente, coloque o cursor no final de qualquer definição de propriedade e insira &quot;&lt;&quot;. O editor mostrará uma lista de todos os elementos XML válidos que você pode inserir nesse local.
    
    ![](images/ditaval-source-view.png)

