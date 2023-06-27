---
title: Verificar a instalação dos Guias do AEM
description: Saiba como verificar a instalação dos Guias do AEM
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 5%

---


# Verificar a instalação dos Guias do AEM {#id213BD030FBE}

Depois de instalar os Guias do AEM, é necessário verificar se a instalação foi bem-sucedida ou não. Execute as seguintes etapas para verificar a instalação:

1. Acesse o Developer Console do seu Cloud Service.

   Para obter detalhes sobre como acessar o Console do desenvolvedor, consulte [Acesso ao Developer Console](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=pt-BR) na documentação do AEM.

1. Acesse a lista de pacotes OSGi no AEM.

   Para obter detalhes sobre o acesso a pacotes, consulte [Pacotes](https://experienceleague.adobe.com/docs/experience-manager-learn/cloud-service/debugging/debugging-aem-as-a-cloud-service/developer-console.html?lang=en#bundles) na documentação do AEM.

1. Procure por fmdita na lista de pacotes e verifique seu status.

   O status deve mostrar *Ativo* para pacotes implantados com êxito. Se algum dos pacotes não tiver um status Ativo, verifique os registros de AEM para solucionar o problema de instalação.


**Tópico pai:**[ Baixar e instalar](download-install.md)

