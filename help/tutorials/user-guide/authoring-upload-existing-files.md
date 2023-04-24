---
title: Upload de arquivos
description: Saiba como fazer upload de arquivos
source-git-commit: cc0fbca257d82cc82db5b5da8d263309fd71de55
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 0%

---


# Upload de arquivos {#id176FF000JUI}

Provavelmente, você teria um repositório de conteúdo DITA existente que gostaria de usar com os Guias AEM. Para esse conteúdo existente, você pode usar qualquer uma das seguintes abordagens para fazer upload em massa do seu conteúdo em AEM repositório:

>[!IMPORTANT]
>
> Consulte [Adicionar ativos digitais ao Adobe Experience Manager as a Cloud Service Assets](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html) para obter informações detalhadas sobre os métodos de upload de conteúdo compatíveis no AEM.

## Interface do usuário do console Assets

Você pode selecionar conteúdo em sua área de trabalho e arrastar a interface de usuário AEM \(navegador da Web\) para a pasta de destino. Para obter mais detalhes, consulte [Fazer upload de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html#upload-assets) na documentação AEM.

## AEM aplicativo de desktop

Use AEM aplicativo de desktop se você for um profissional criativo e quiser gerenciar os ativos no desktop local. Você pode abrir e editar esses ativos com seus aplicativos de desktop. Você também pode manter versões e compartilhar seus arquivos com outros usuários. Para obter mais detalhes, consulte [AEM aplicativo de desktop](https://experienceleague.adobe.com/docs/experience-manager-desktop-app/using/using.html).

## Gestor em massa de ativos

Se você tiver migrações em grande escala e ingestões em massa ocasionais, use o Gestor de ativos em massa para carregar seu conteúdo. Com essa ferramenta, você pode fazer upload de conteúdo em massa de armazenamentos de dados compatíveis, como o Azure ou o S3. Para obter mais detalhes, consulte [Gestor em massa de ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/assets/manage/add-assets.html?lang=en#asset-bulk-ingestor).

## Usar o FrameMaker para upload em massa

O Adobe FrameMaker vem com um conector de AEM poderoso que permite carregar facilmente seu DITA existente e outros documentos do FrameMaker \(`.book` e `.fm`\) em AEM. Você pode usar várias funcionalidades de upload de arquivo, como carregar um único arquivo, carregar uma pasta completa com ou sem dependências \(como referências de conteúdo, referências cruzadas e gráficos\).

Para obter mais detalhes sobre o uso do recurso de upload em massa no FrameMaker, consulte a seção *Crie uma pasta CRX e faça upload de arquivos* no Guia do usuário do FrameMaker.

## Erro ao manusear o conteúdo durante o upload {#id201MI0I04Y4}

Em caso de falha ao carregar um ou mais arquivos, um prompt é exibido no final do processo de upload com uma lista de arquivos que falharam no upload:

![](images/uuid-files-failed-to-upload_cs.png){width="650" align="center"}

Para obter mais detalhes sobre como os vários cenários de upload de arquivos, consulte [Upload de conteúdo DITA](authoring-file-management.md#).

Caso você use uma ferramenta como AEM aplicativo de desktop ou o Asset bulk ingestor, a ação a ser executada em um arquivo duplicado será controlada por uma configuração no servidor AEM. Entre em contato com o administrador do sistema para saber mais sobre essa configuração.

**Tópico principal:**[ Gerenciar conteúdo](authoring.md)

