---
title: Como adicionar [!DNL AEM Guides] para [!DNL AEM as a Cloud Service] ambiente
description: Saiba como adicionar [!DNL AEM Guides] para [!DNL AEM as a Cloud Service] ambiente
exl-id: a1e020c2-360c-4d71-b5fd-8179d9ceacda
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# [!DNL AEM Guides] implantação as a Cloud Service

Saiba como adicionar [!DNL Guides] para [!DNL AEM as a Cloud Service] ambiente.

## Implantação manual por meio do pipeline de git do Cloud Manager

Se você comprou [!DNL AEM Guides] as a Cloud Service antes de 29 de março de 2022, siga estas instruções de implantação:

* Se estiver começando no novo, você poderá substituir o código gerado automaticamente por [!UICONTROL Cloud Manager] com o código do acordo de recompra abaixo que tem o plug-in XML já integrado: https://github.com/Adobe-TCS/XML-documentation-for-AEMaaCS

* Se você já tiver feito check-in nas personalizações [!UICONTROL Cloud Manager] git repo, consulte o acordo de recompra abaixo para obter instruções sobre como adicionar plug-in XML ao seu código existente: https://github.com/Adobe-TCS/DoX-Installer-for-AEMaaCS

## Implantação Via Cloud Manager

Se você for um cliente que comprou [!DNL AEM Guides] as a Cloud Service em ou após 29/03/2022, siga estas instruções para adicionar [!DNL Guides] para [!DNL AEM as a Cloud Service] ambiente:

1. Faça logon em [!UICONTROL Cloud Manager].

1. Edite o programa para o qual deseja configurar [!DNL AEM Guides].

1. Mudar para **[!UICONTROL Soluções e complementos]** guia .

1. No **[!UICONTROL Soluções e complementos]** tabela, clique em **[!UICONTROL Ativos]**.

1. Selecionar **[!UICONTROL Guias]** e selecione **[!UICONTROL Salvar]**.

O programa foi configurado com êxito para o provisionamento automático da solução Guias AEM.

![Configuração AEM solução Guias](assets/addon-configuration.png)

>[!NOTE]
>
>Para instalar [!DNL AEM Guides] em qualquer ambiente do programa integrado, você deve executar o pipeline associado ao ambiente . Nenhuma configuração adicional é necessária na base de código Git do CM para instalar [!DNL AEM Guides].
