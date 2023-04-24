---
title: Criação de perfis de atributos condicionais
description: Saiba como criar perfis de atributos condicionais
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# Criação de perfis de atributos condicionais {#id1843I0HN0Y4}

No nível da empresa, é extremamente importante garantir que você tenha um sistema de marcação padrão em vigor. Tags ou atributos condicionais podem ser associados a ativos digitais no repositório, o que ajuda a publicar a saída com base nas condições escolhidas. Por exemplo, você pode criar um atributo condicional para conteúdo do Windows e Mac. Em seguida, adicione esses atributos ao conteúdo relevante em seus tópicos. No momento da publicação do conteúdo, você pode escolher se deseja publicar somente conteúdo do Windows ou Mac.

AEM Guias permitem criar e associar atributos condicionais facilmente usando os atributos DITA relevantes. Você pode definir atributos condicionais no nível global ou de pasta. As condições definidas globalmente são visíveis em todos os projetos e as condições específicas da pasta são visíveis apenas nos projetos criados na pasta especificada. Os autores de conteúdo podem usar esses atributos condicionais para condicionar o conteúdo em seus tópicos DITA ou mapas que criarem ou usarem. Essas condições podem ser usadas pelo editor para criar predefinições condicionais. Usando as predefinições condicionais, o editor pode decidir qual condição incluir e excluir da saída publicada.

>[!NOTE]
>
> Você pode criar ou editar os atributos condicionais em um Perfil de pasta ao qual tem acesso. Se o administrador do sistema não tiver concedido acesso a um perfil de pasta, não será possível criar ou editar os atributos condicionais no Perfil da pasta.

Para definir atributos condicionais, execute as seguintes etapas:

1. Clique no link do Adobe Experience Manager na parte superior e escolha **Ferramentas**.

1. Selecionar **Guias** na lista de ferramentas.

1. Clique no botão **Perfis de pasta** e selecione um Perfil de pasta.

   >[!NOTE]
   >
   > Não é possível editar o perfil global.

1. Clique no botão **Atributos condicionais** e clique em **Editar**.

   A tabela Atributos condicionais é exibida.

1. Clique em **Adicionar**.

1. Insira o **Nome**, **Valor** e um **Rótulo** para o atributo .

   Você pode salvar um perfil somente com o nome do atributo. No entanto, um atributo só pode ser usado quando tiver um valor especificado. Se você especificar - valor e rótulo para um atributo, o Editor da Web ainda mostraria somente o valor do atributo. O rótulo é exibido ao administrador de publicação no momento da criação da predefinição condicional.

   A captura de tela a seguir mostra a definição para a variável `platform` atributo com valor de `unix` e um rótulo de `Red Hat Linux`.

   ![](images/add-profile.png)

1. Se quiser adicionar mais valores para o mesmo atributo, clique no botão **+** e insira valor e rótulo adicionais.

1. Se quiser adicionar mais atributos, clique em **Adicionar**.

1. Clique em **Salvar** para salvar as alterações.


O `platform` é armazenado no sistema. Sempre que um autor decidir usar o `platform` em um tópico DITA em uma pasta, eles verão os valores na guia Propriedades no Editor da Web.

![](images/properties-tab.png)

**Tópico principal:**[ Geração de saída](generate-output.md)

