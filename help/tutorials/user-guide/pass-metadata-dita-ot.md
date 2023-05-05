---
title: Transmita os metadados para a saída usando DITA-OT
description: Saiba como transmitir os metadados para a saída usando DITA-OT
exl-id: 637895e5-aece-4827-a32e-f2ae3e3704ef
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Transmita os metadados para a saída usando DITA-OT {#id21BJ00QD0XA}

Os metadados são informações adicionais sobre a saída. Nos Guias AEM você pode transmitir os metadados existentes ou criar tags de metadados personalizadas. Você pode transmitir metadados para saídas de AEM, PDF, HTML5, EPUB e formato Personalizado usando a publicação DITA-OT.

Execute as seguintes etapas para transmitir os metadados para a saída usando a publicação DITA-OT:

1. No **Interface do usuário do Assets**, navegue e clique no arquivo de mapa DITA para o qual deseja passar os metadados para o DITA-OT.
1. Selecione e edite uma predefinição de saída para a qual deseja passar os campos de metadados. Por exemplo, selecione PDF output preet.
1. Selecionar **DITA-OT** em Gerar &lt;output> Uso da opção na predefinição de saída selecionada.

   ![](images/custom-meta-data-output-preset.png){width="800" align="left"}

1. No menu suspenso Propriedades , selecione os metadados que você deseja passar para a publicação de DITA-OT.

   A lista suspensa Propriedades lista as propriedades personalizadas e padrão. Por exemplo, na captura de tela acima, o autor é a propriedade personalizada enquanto `dc:description`, `dc:language`, `dc:title`e `docstate` são as propriedades padrão.

   >[!NOTE]
   >
   > Essas propriedades são selecionadas do arquivo metadataList disponível no seguinte local:`/libs/fmdita/config/metadataList`. Por padrão, há quatro propriedades listadas neste arquivo `dc:description`, `dc:language`, `dc:title`e `docstate`.

   Esse arquivo pode ser sobreposto em: `/apps/fmdita/config/metadataList`.

   Para transmitir uma propriedade personalizada para a qual você já definiu os valores, consulte [Usar metadados de AEM na saída do PDF DITA-OT](https://experienceleaguecommunities.adobe.com/t5/xml-documentation-discussions/use-aem-metadata-in-dita-ot-pdf-output/td-p/411880).

1. No **Propriedades** selecione as propriedades padrão e personalizadas necessárias. Por exemplo, selecione `author`, `dc:title`e `dc:description`. Estes são os padrões `metadata/properties` que é criado assim que criamos um arquivo. As propriedades selecionadas são listadas abaixo da caixa de depósito.

   ![](images/selected-metadata-properties.png){width="300" align="left"}

1. Clique em **Concluído** no canto superior esquerdo para salvar as alterações.
1. Gere a saída.

As propriedades de metadados selecionadas serão passadas para a saída gerada usando DITA-OT.

**Tópico principal:**[ Geração de saída](generate-output.md)
