---
title: Criar tópicos
description: Saiba como criar tópicos
exl-id: 336bbbff-f268-40be-ad3a-9c72923be71b
source-git-commit: 8073716bccacbe8d6a158b44d5106b083e3a5dcd
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 0%

---

# Criar tópicos {#id2056AL00O5Z}

O AEM Guides permite criar tópicos DITA do tipo — tópico, tarefa, conceito, referência, glossário, DITAVAL e muito mais. Além de criar tópicos com base nos modelos prontos para uso, também é possível definir seus modelos personalizados. Para obter mais informações sobre o uso de modelos DITA personalizados, consulte *Configurar modelos e tags para criação* em Instalar e configurar o Adobe Experience Manager Guides as a Cloud Service.

Execute as seguintes etapas para criar um tópico:

1. Na interface do usuário do Assets, navegue até o local em que deseja criar o tópico.

1. Para criar um novo tópico, clique em **Criar** \> **Tópico DITA**.

1. Na página Blueprint, selecione o tipo de documento DITA que deseja criar e clique em **Próxima**.

   ![](images/create_dita_topic.png){width="800" align="left"}

   Por padrão, os Guias do AEM fornecem os modelos de tópicos DITA mais usados. É possível configurar mais modelos de tópico de acordo com seus requisitos organizacionais. Consulte *Configurar modelos e tags para criação* em Instalar e configurar o Adobe Experience Manager Guides as a Cloud Service.

   >[!NOTE]
   >
   > Na exibição em lista da interface do usuário do Assets, o tipo de tópico DITA é mostrado na coluna Tipo como Tópico, Tarefa, Conceito, Referência, Glossentry ou DITAVAL. O mapa DITA é exibido como Map.

1. Na página Propriedades, especifique o documento **Título**.

1. \(Opcional\) Especifique o arquivo **Nome**.

   Se o administrador tiver configurado o nome de arquivo automático com base na configuração UUID, você não verá a opção para especificar o nome do arquivo. Um nome de arquivo baseado em UUID é automaticamente atribuído ao arquivo.

   Se a opção de nomenclatura de arquivo estiver disponível, então o nome também será sugerido automaticamente com base no **Título** do seu documento. Se quiser especificar manualmente o nome do documento, verifique se **Nome** não contém nenhum espaço, apóstrofo ou chaves e termina com .xml ou .dita. Por padrão, as Guias do AEM substituem todos os caracteres especiais por hifens. Consulte a seção Nomes de arquivo no Guia de práticas recomendadas para obter as práticas recomendadas sobre a nomeação de arquivos DITA.

1. Clique em **Criar**. A mensagem Topic Created (Tópico criado) é exibida.

   Você pode optar por abrir o tópico para edição no Editor da Web ou salvar o arquivo de tópico no repositório AEM.

   Todos os novos tópicos criados na interface do usuário do Assets **Criar** \> **Tópico DITA** ou o Editor da Web recebe uma ID de tópico exclusiva. O valor dessa ID é o próprio nome do arquivo. Além disso, um novo documento é salvo como a cópia de trabalho mais recente do tópico no DAM. Até salvar uma revisão de um tópico recém-criado, você não verá nenhum número de versão no Histórico de versões. Se você abrir o tópico para edição, as informações da versão serão mostradas no canto superior direito da guia do arquivo de tópico:

   ![](images/topic-version-none_cs.png){width="550" align="left"}

   As informações de versão de um tópico recém-criado são mostradas como *nenhum*. Ao salvar uma nova versão, um número de versão é atribuído como 1.0. Para obter mais informações sobre como salvar uma nova versão, consulte [Salvar como nova versão](web-editor-features.md#save-as-new-version-id209ME400GXA).


>[!NOTE]
>
> Se o administrador tiver configurado o Editor da Web para fazer check-out dos arquivos antes de editar, você não poderá editar um arquivo até fazer check-out. Da mesma forma, se configurado, você será solicitado a fazer check-in de qualquer arquivo com check-out antes de fechá-lo.

>[!IMPORTANT]
>
> Depois de criar o tópico DITA, continue salvando as alterações na sua cópia de trabalho e crie uma nova versão após concluir as atualizações do tópico.

**Tópico pai:**[ Criar e visualizar tópicos](create-preview-topics.md)