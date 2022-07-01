---
title: Configurar DITA-OT personalizado em [!DNL AEM Guides]
description: Saiba como configurar o DITA-OT personalizado em [!DNL Adobe Experience Manager Guides]
role: Admin
exl-id: f479c2cf-5b8b-4517-be97-81303468007a
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# Configurar DITA-OT personalizado em [!DNL AEM Guides] para AEM

As etapas para adicionar um DITA-OT personalizado estão documentadas na seção . _Usar plug-ins personalizados DITA-OT_ do _Guia de Instalação e Configuração_.

Em um alto nível, as etapas são:

+ Obtenha o DITA-OT básico
   + Se quiser obter uma cópia do DITA-OT pronto para uso do [!DNL AEM Guides], baixe-o do caminho `/etc/fmdita/dita_resources/DITA-OT.zip`
   + Se quiser obter uma versão diferente, baixe o de [dita-ot repo](https://www.dita-ot.org/download)
+ Faça alterações no DITA-OT como [adição de novo plug-in](https://www.dita-ot.org/dev/topics/plugins-installing.html)ou personalizar plug-ins existentes (consulte o exemplo na seção links relacionados abaixo)
+ Upload `DITA-OT.zip` recebido para `/apps/<project-folder>/dita_resources` (criar uma pasta de projeto personalizada é uma abordagem recomendada)
+ Adicionar perfil DITA por meio de **[!UICONTROL Ferramentas]** > **[!UICONTROL Guias]** > **[!UICONTROL Perfis DITA]** (use o caminho DITA-OT onde o DITA-OT personalizado é carregado, consulte a captura de tela abaixo)
   ![Perfis DITA](assets/dita-profile.png)

>[!MORELIKETHIS]
>
>+ [Personalização de amostras de plug-in DITA-OT](https://www.dita-ot.org/dev/topics/pdf-customization.html)

