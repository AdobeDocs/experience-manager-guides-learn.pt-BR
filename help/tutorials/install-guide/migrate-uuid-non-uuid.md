---
title: Migração de conteúdo não UUID para UUID
description: Saiba como migrar conteúdo não UUID para UUID
exl-id: 093b380e-9a8b-4e60-aeaa-3458e8c257f2
source-git-commit: 21edbb2f8a49213ea95fac8a957056711219e7e4
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Migração de conteúdo não UUID para UUID {#id226TI0U20XA}

>[!IMPORTANT]
>
> Você pode migrar seu conteúdo não UUID para o servidor UUID. Para migrar para o servidor UUID, você deve ter um servidor não UUID com guias AEM versão 4.0 instalados.

Execute as seguintes etapas para migrar seu conteúdo não UUID:

>[!NOTE]
>
> Cada etapa é essencial e a ausência de qualquer uma delas pode causar falha ou dados corrompidos do servidor. Conclua todas as etapas.

1. Assegure que **Ativar iniciadores do fluxo de trabalho de pós-processamento** in *com.adobe.fmdita.config.ConfigManager* e **Ativar pós-processamento da versão** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation* são ativados.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Instale a versão UUID da próxima versão principal sobre a versão não UUID. Por exemplo, se você estiver usando a build 4.0 não UUID, será necessário instalar a versão 4.1 do UUID.

1. Na guia Iniciador, desative os seguintes fluxos de trabalho e qualquer outro fluxo de trabalho executado em /content/dam usando iniciadores em `http://localhost:4502/libs/cq/workflow/content/console.html`:

   - **Ativo de atualização DAM** fluxo de trabalho
   - **Writeback de metadados DAM** fluxo de trabalho

1. Desativar **Ativar iniciadores do fluxo de trabalho de pós-processamento** in *com.adobe.fmdita.config.ConfigManager* e desativar **Ativar pós-processamento da versão** in *com.adobe.fmdita.postprocess.version.PostProcessVersionObservation*.

   ```http
   http://<server name>:<port>/system/console/configMgr/com.adobe.fmdita.config.ConfigManager
   ```

1. Adicionar um agente de log separado para `com.adobe.fmdita.uuid.upgrade.UuidUpgrade.`

   A resposta do navegador também está disponível em /content/uuid-upgrade/logs.

1. Executar a consulta fornecida em uma pasta com dados menores com `doReviews=false` antes de executá-lo em / content/dam: `http://localhost:4502/bin/dxml/uuid_upgrade?root=/content/dam/test&doReviews=false`

   >[!TIP]
   >
   >  Você pode verificar se todos os arquivos na pasta foram atualizados corretamente e se todos os recursos estão funcionando somente para essa pasta.

**Parâmetros da consulta:**

    - &quot;root&quot;: pasta raiz onde a atualização deve ocorrer \(Use /content/dam para todos os repositórios.\)
    - `doReviews`: true/false \(Se as revisões precisarem ser atualizadas ou não. O valor padrão é falso.\)
    - `doBaselines`: true/false \(Se as linhas de base tiverem que ser atualizadas ou não. O valor padrão é verdadeiro.\)
    - `processLevel`: -1\(falha sem restauração\), 0\(falha com restauração\), 1\(falha com erros\), 2\(atualização bem-sucedida\) \(Ao tentar novamente o script após a falha, somente os arquivos com &quot;fmUpgradeStatus&quot; &lt;= processLevel serão processados novamente, caso contrário, será ignorado. O valor padrão é 1.\)
    - `ignoreImageVersions`: true/false \(Ignora o processamento de versões de imagem. O valor padrão é falso.\)
    
    >[!NOTE]
    >
    > Podemos executar a migração de conteúdo no nível da pasta ou no conteúdo/dam completo ou na mesma pasta \(executar a migração novamente\).

1. Depois que o servidor for migrado com êxito, habilite os seguintes fluxos de trabalho e pós-processamento para continuar trabalhando no servidor:

   - **Ativo de atualização DAM** fluxo de trabalho
   - **Metadados DAM** fluxo de trabalho

>[!NOTE]
>
> Se alguns arquivos não forem processados ou forem corrompidos antes da migração, eles permanecerão corrompidos mesmo após a migração.
