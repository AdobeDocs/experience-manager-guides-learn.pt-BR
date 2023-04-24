---
title: Gerenciar predefinições de saída do Perfil global e de pasta
description: Saiba como gerenciar predefinições de saída globais e de perfil de pasta
source-git-commit: 3b33b27e4acb8d0b185427725e23b8beac0c2a46
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---


# Gerenciar predefinições de saída do Perfil global e de pasta {#id22BLJ0D0V1U}

As predefinições de Perfil Global e de Pasta só estão disponíveis para usuários administrativos de nível de pasta.

Como administrador, os Guias AEM permitem criar e gerenciar predefinições de saída para os Perfis Global e de Pasta. Em seguida, você pode usar facilmente essas predefinições de saída para gerar saída para todos os mapas relacionados a esse Perfil Global ou de Pasta.

Execute as etapas a seguir para criar uma predefinição de saída para os Perfis global e de pasta:

1. Selecione o mapa DITA para o qual deseja criar uma predefinição de saída.
1. Selecione o **Editar tópicos** da **Opções** do arquivo de mapa. O arquivo de mapa é aberto para edição no Editor da Web.
1. No **Saída** selecione o ícone + para criar uma predefinição de saída para o mapa DITA.

   ![](images/add-global-output-preset.png){width="350" align="left"}

1. Insira os seguintes detalhes na **Adicionar predefinição** caixa de diálogo:
   - Tipo
   - Nome
   - Destino \(para predefinição da Base de conhecimento\)
1. Selecione o **Adicionar ao perfil da pasta** caixa de seleção para criar uma predefinição de saída para o perfil de pasta relacionado e clique em **Adicionar**. A predefinição é criada e aparece sob a variável **Saída** de todos os mapas relacionados. \( ![](images/global-preset-icon.svg)\) indica uma predefinição de nível de perfil de pasta.
1. Insira os detalhes de configuração.

   >[!NOTE]
   >
   > Essas predefinições adicionadas ao perfil da pasta são independentes dos mapas, portanto, as configurações específicas do mapa não estão presentes para essas predefinições.

1. Você pode selecionar a variável **Gerar predefinição** ícone na parte superior para gerar a saída dos mapas relacionados à predefinição de saída criada. Você verá o status do processo de geração de saída. Para exibir a saída, passe o ponteiro do mouse sobre o tópico e clique em **Exibir saída**.

>[!NOTE]
>
> Os Guias de AEM também fornecem uma predefinição de saída PDF pronta para gerar a saída para seus mapas DITA.

**Outras operações do menu Opções**

Também é possível executar as seguintes operações na predefinição do menu Opções:

- Selecione a predefinição como predefinição padrão de pdf. Em seguida, a predefinição selecionada seria usada como a predefinição padrão para gerar a saída do PDF usando o **Baixar como PDF** para um mapa.
- **Editar**, **Renomear**, **Duplicar** ou **Excluir** uma predefinição de saída existente do **Opções** menu.

>[!NOTE]
>
> Quando uma predefinição de saída em Perfis globais e de pastas é excluída, ela refletirá em todos os mapas relacionados e não aparecerá sob a variável **Saída** guia .

**Tópico principal:**[ Trabalhar com o editor da Web](web-editor.md)

