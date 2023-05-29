---
title: Atualização dos Guias do Adobe Experience Manager
description: Saiba como atualizar os Guias do Adobe Experience Manager
source-git-commit: 414ee8ae3b12bb40054ddbe9e1a008ebc6058f89
workflow-type: tm+mt
source-wordcount: '2750'
ht-degree: 1%

---


# Atualização dos Guias do Adobe Experience Manager {#id224MBE0M0XA}

>[!NOTE]
>
> Siga as instruções de atualização específicas para a versão licenciada do seu produto.

Você pode atualizar sua versão atual dos Guias do AEM para a versão 4.2.1
- Se você estiver usando a versão 4.1, 4.1.x ou 4.2, é possível atualizar diretamente para a versão 4.2.1.
- Se você estiver usando a versão 4.0, será necessário atualizar para a versão 4.2 antes de atualizar para a versão 4.2.1.
- Se você estiver usando a versão 3.8.5, será necessário atualizar para a versão 4.0 antes de atualizar para a versão 4.2.
- Se você estiver em uma versão anterior à 3.8.5, consulte a seção Atualizar guias de AEM no guia de instalação específico do produto.

>[!NOTE]
>
> Você deve instalar o service pack AEM antes de atualizar a versão dos Guias AEM.

Para obter mais detalhes, consulte os seguintes procedimentos:

- [Atualização da versão 3.8.5 para a versão 4.0](#id2256DK003E1)
- [Atualizar para a versão 4.2](#id22A3F500SXA)
- [Atualizar para a versão 4.2.1](#upgrade-version-4-2-1)


>[!IMPORTANT]
>
> Antes de começar a atualização, faça um backup completo do sistema para evitar perda de dados.

## Atualização da versão 3.8.5 para a versão 4.0 {#id2256DK003E1}

Se você estiver usando a versão 3.8.5 dos Guias do AEM, é possível atualizar para a versão 4.0 dos Guias do AEM. Com o recurso de atualização, não é necessário desinstalar a versão anterior dos Guias do AEM.

Antes de executar o processo, há determinadas tarefas que você deve concluir. As subseções a seguir o guiarão pelos pré-requisitos, pela geração de relatórios e pelo processo de migração. Além disso, depois de instalar o AEM Guides versão 4.0, você pode personalizar várias configurações, de acordo com as configurações do cliente.

>[!NOTE]
>
> Este processo de atualização é aplicável somente da versão 3.8.5 para a versão 4.0. Para o processo de atualização da versão 3.4 ou superior para a 3.8.5, consulte o *Atualizar guias do AEM* seção no guia de instalação específico do produto disponível no [Página de arquivamento da ajuda](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).

****Pré-requisitos****

Antes de iniciar o processo de atualização dos Guias AEM, verifique se você tem:

1. Foram importados os comentários de revisão em tópicos abertos para revisão.
1. Todas as análises ativas foram fechadas.
1. Todas as tarefas de tradução foram fechadas.
1. Desinstale quaisquer hot fixes do AEM Guides instalados na parte superior da versão anterior \(versão principal ou patch\) do AEM Guides.

**Antes de instalar a versão 4.0**

Antes de instalar a versão 4.0, execute as seguintes etapas:

1. Certifique-se de que neste ponto o AEM Guides está na versão 3.8.5.
1. Baixe o pacote de script de atualização. Para fazer isso, procure por &quot;Pacote de atualização da solução XML Documentation 4.0&quot; em [Portal de distribuição de software Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html) que baixará um arquivo zip.
1. Faça upload deste pacote para AEM usando o Gerenciador de pacotes e instale este pacote.
1. Quando o pacote de atualização estiver instalado, execute os scripts abaixo na mesma ordem e siga as instruções fornecidas:

**Verificar API de compatibilidade de atualização**

Essa API foi projetada para avaliar o status atual do sistema e relatar se a atualização é possível ou não. Para executar esse script, acione o endpoint fornecido abaixo:

| Ponto final | /bin/dxml/upgrade/3xto4x/report |
| --- | --- |
| Tipo de solicitação | **GET** Você pode usar um navegador da Web no qual esteja conectado à instância AEM como administrador. |
| Resposta esperada | - Caso todos os nós necessários possam ser movidos, você receberá uma verificação aprovada. <br>- Caso um nó esteja presente no local de destino, você receberá um erro relevante. Limpe o repositório \(delete node /var/dxml\) e reinstale o pacote de atualização e acione esse endpoint novamente. <br>**Nota:** Este não é um erro comum, pois o local de destino não é usado anteriormente pelos Guias AEM 3.x. <br> - Se o script não for bem-sucedido, não continue e relate à equipe de sucesso do cliente. |

**API de migração de dados do sistema**

Essa API foi projetada para migrar os dados do sistema, conforme mencionado na **Mapeamento de migração** seção.

1. Não execute este script se a API de verificação de compatibilidade de atualização falhar \(não continuar\).
1. Depois que a API Verificar compatibilidade de atualização retornar sucesso, você poderá executar o script de atualização.

| Ponto final | /bin/dxml/upgrade/3xto4x |
| --- | --- |
| Tipo de solicitação | **POST** Esse script é uma solicitação POST, portanto, deve ser executado por meio de agentes como o Postman. |
| Resposta esperada | - Depois que a migração for bem-sucedida, você poderá instalar a solução XML Documentation versão 4.0.<br>- Em caso de erros, restaure para o último ponto de verificação e compartilhe os logs de erro junto com a saída da API com a equipe de sucesso do cliente. |

**Mapeamento de migração**: a API acima migra todos os dados do local de origem para o local de destino.

| Origem | Destino |
|------|------|
| /content/fmdita | /var/dxml |
| /content/dxml | /var/dxml |
| /etc/fmdita | /libs/fmdita |

## Instalar versão 4.0 {#id23598G006XA}

1. Instale a versão 4.0 somente se as etapas de atualização forem bem-sucedidas.
1. Baixe o pacote da versão 4.0 de [Portal de distribuição de software Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html):

   - Se você estiver usando a versão UUID do software, procure por &quot;Versão 4.0 UUID para solução XML Documentation para AEM 6.5&quot;.
   - Se você estiver usando a versão não UUID do software, procure por &quot;Versão 4.0 não UUID para a solução XML Documentation para AEM 6.5&quot;.
Carregue o pacote na instância do servidor AEM existente\(s\) usando o Gerenciador de pacotes do CRX e instale-o.

   >[!NOTE]
   >
   > Aguarde até que todos os componentes do sistema sejam iniciados.

1. Limpe o cache do navegador após instalar o pacote.
1. Se um dispatcher estiver configurado na instância do autor do AEM, execute as seguintes etapas:
   - Verifique se os seguintes itens são tratados nas regras do dispatcher:
   - O padrão de URL /home/users/\*/references está na lista de permissões.
   - O padrão de URL /libs/cq/security/userinfo.json não é armazenado em cache.
1. Limpar o cache do dispatcher \(para limpar qualquer `clientlibs` em cache\).

## Atualizar para a versão 4.2 {#id22A3F500SXA}

A atualização para a versão 4.2 depende da versão atual dos Guias do AEM.

Se você estiver usando a versão 4.0, 4.1 ou 4.1.x, é possível atualizar diretamente para a versão 4.2.

****Pré-requisitos****

Antes de iniciar o processo de atualização do AEM Guides 4.2, verifique se você tem:

1. Atualizado para a versão 4.0, 4.1 ou 4.1.x dos Guias do AEM.
1. Todas as tarefas de tradução foram fechadas.
1. Alterado o nível de log para **INFORMAÇÕES** para `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` e anexar esses logs em um novo arquivo de log, por exemplo, `logs/translation_upgrade.log.`

>[!NOTE]
>
> Você deve fechar todas as revisões ativas. Se as tarefas de revisão não forem fechadas durante a atualização para a versão 4.2, as tarefas de revisão em andamento mais antigas continuarão levando os usuários para as páginas de revisão mais antigas, e as tarefas de revisão criadas após a atualização exibirão as atualizações mais recentes na funcionalidade.

## Instalar versão 4.2 {#id2245IK0E0EV}

1. Baixe o pacote da versão 4.2 de [Portal de distribuição de software Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html).
1. Instale o pacote da versão 4.2.
1. Após concluir a instalação do pacote, aguarde a seguinte mensagem\(s\) nos logs:

   `Completed the post deployment setup script`

   A mensagem acima indica que todas as etapas da instalação foram concluídas.

   Caso encontre qualquer um dos seguintes prefixos de ERRO, relate-os à equipe de sucesso do cliente:

   - Erro no script de configuração pós-implantação
   - Exceção ao portar o MAP de tradução
   - Não é possível portar o mapa de conversão de v1 para v2 para a propriedade
1. Atualização do plugin do conector Oxygen lançado com a versão 4.2 \(se necessário\).
1. Limpe o cache do navegador após instalar o pacote.
1. Continue atualizando as personalizações conforme detalhado na próxima seção.

## Depois de instalar a versão 4.2 {#id2326F02004K}

>[!IMPORTANT]
>
> O modelo de alta tecnologia não é exibido no servidor atualizado. Para incluir o modelo de alta tecnologia em seu servidor, você pode copiá-lo: Fonte: /libs/fmdita/pdf/Hi-Tech Destino: /content/dam/dita-templates/pdf

Depois de instalar o AEM Guides, você pode mesclar as várias configurações aplicáveis da versão recém-instalada à sua configuração.

>[!NOTE]
>
> O modelo dam-update-asset pode ser personalizado. Se alguma personalização foi feita, precisamos sincronizar as personalizações e os Guias do AEM na cópia de trabalho do modelo.

1. **Fluxo de trabalho do Ativo de atualização do DAM \(Alterações pós-processamento\):**

1. Abrir URL:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Selecionar **Fluxo de trabalho do Ativo de atualização DAM**.
1. Clique em **Editar**.
1. Se a variável **Iniciador de pós-processamento DXML** estiver presente, verifique se as personalizações estão sincronizadas.
1. Se a variável **Iniciador de pós-processamento DXML** estiver ausente, execute as seguintes etapas para inseri-lo:

1. Clique em **Inserir componente** \(Responsável pelo pós-processamento do AEM Guides como a etapa final do processo\).
1. Configure o **Etapa do processo** com os detalhes abaixo:

   **Guia Comum**

   **Título:** Iniciador de pós-processamento DXML

   **Descrição**: etapa do iniciador de pós-processamento DXML que acionará um trabalho sling para pós-processamento DXML do ativo modificado/criado

   **Guia Processo**

   - Selecionar **Iniciador de pós-processamento DXML** do **Processo** lista suspensa

   - Selecionar **Avanço do manipulador**

   - Selecionar **Concluído**

1. Clique em **Sincronizar** na parte superior direita depois de concluir as alterações. Você receberá uma notificação de sucesso.

   >[!NOTE]
   >
   > Atualize e verifique se as alterações personalizadas e a etapa de pós-processamento dos Guias do AEM estão presentes no modelo de fluxo de trabalho final.

1. Uma vez **Fluxo de trabalho do Ativo de atualização DAM** estiver validado, verifique as configurações correspondentes do inicializador. Para fazer isso, vá para a interface de fluxo de trabalho do AEM e abra iniciadores.

   ```http
   http://localhost:4502/libs/cq/workflow/content/console.html
   ```

   Localize e faça alterações \(se necessário\) nos dois inicializadores a seguir \(que devem estar ativos\) correspondentes a **Fluxo de trabalho do Ativo de atualização DAM**:

1. Iniciador para &quot;*Nó criado*&quot; para **Fluxo de trabalho do Ativo de atualização DAM**- para condição `"jcr:content/jcr:mimeType!=video"`, o valor de &quot;Globbing&quot; deve ser:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; deve ter `"event-user-data:changedByWorkflowProcess"`.
   - Iniciador para &quot;*Nó Modificado*&quot; para **Fluxo de trabalho do Ativo de atualização DAM -** para a condição &quot;`jcr:content/jcr:mimeType!=video`&quot;,
   - 
      - o valor de &#39;Globbing&#39; deve ser:

   ```json
   `"/content/dam(/((?!/subassets|/translation_output).)*/)renditions/original"`
   ```

   - &#39;excludeList&#39; deve ter `"event-user-data:changedByWorkflowProcess"`.
1. Quando a atualização for concluída, verifique se todas as personalizações/sobreposições estão validadas e atualizadas para corresponder ao novo código do aplicativo. Alguns exemplos são apresentados abaixo:
   - Quaisquer componentes sobrepostos de/libs/fmditaor/libsdevem ser comparados com o novo código do produto e as atualizações devem ser feitas em arquivos sobrepostos em/apps.
   - Todas as categorias de clientlib usadas do produto devem ser revisadas para alterações. Todas as configurações substituídas \(exemplos abaixo\) devem ser comparadas com as mais recentes para obter os recursos mais recentes:
   - elementmapping.xml
   - ui\_config.json\(pode ter sido definido em perfis de pasta\)
   - alterado `com.adobe.fmdita.config.ConfigManager`
   - Verifique se qualquer um dos códigos personalizados estava usando caminhos antigos \(como mencionado na [Mapeamento de migração](#id2244LE040XA) section\) - deve ser atualizado para os novos caminhos para que as personalizações também funcionem conforme esperado.
1. Leia sobre as novas configurações trazidas na versão atual \(verifique [Notas de versão](../release-info/release-notes-4.2.md)\) e veja se alguma funcionalidade foi afetada, em seguida, tome as medidas apropriadas. Um exemplo pode ser o uso da seção &quot;Manuseio aprimorado de arquivos e versões&quot;, introduzida na versão 4.0, para a qual é necessário ativar uma configuração.

## Etapas para indexar o conteúdo existente para usar a nova localização e substituição:

Execute as seguintes etapas para indexar o conteúdo existente e usar o novo texto de localização e substituição no nível do mapa:

- Executar uma solicitação POST no servidor \(com autenticação correta\) - `http://<server:port\>/bin/guides/map-find/indexing`. \(Opcional: é possível passar caminhos específicos dos mapas para indexá-los; por padrão, todos os mapas serão indexados \|\| Por exemplo: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`\)

- A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com id de trabalho para o mesmo ponto de extremidade - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Por exemplo: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)

- Quando o trabalho for concluído, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados nos logs do servidor.

## Atualizar para a versão 4.2.1 {#upgrade-version-4-2-1}

A atualização para a versão 4.2.1 depende da versão atual dos Guias AEM.

Se você estiver usando a versão 4.1, 4.1.x ou 4.2, é possível atualizar diretamente para a versão 4.2.1.

>[!NOTE]
>
>O pós-processamento e a indexação podem levar algumas horas. Recomendamos que você inicie o processo de atualização fora do horário de pico.

****Pré-requisitos****

Antes de iniciar o processo de atualização do AEM Guides 4.2.1, verifique se você:

1. Atualizado para a versão 4.1, 4.1.x ou 4.2 dos Guias do AEM.
1. Todas as tarefas de tradução foram fechadas.
1. Alterado o nível de log para **INFORMAÇÕES** para `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript` e anexar esses logs em um novo arquivo de log, por exemplo, `logs/translation_upgrade.log.`

>[!NOTE]
>
> Você deve fechar todas as revisões ativas. Se as tarefas de revisão não forem fechadas durante a atualização para a versão 4.2, as tarefas de revisão em andamento mais antigas continuarão levando os usuários para as páginas de revisão mais antigas, e as tarefas de revisão criadas após a atualização exibirão as atualizações mais recentes na funcionalidade.

## Instalar versão 4.2.1

1. Baixe o pacote de versão 4.2.1 de [Portal de distribuição de software Adobe](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html).
1. Instale o pacote da versão 4.2.1.
1. Você pode optar por ACESSAR o acionador para iniciar o trabalho de atualização do mapa de tradução. Para obter detalhes, consulte [Ativar acionador de script por meio de um Servlet](#enable-trigger-serverlet).


1. Após concluir a instalação do pacote, aguarde a seguinte mensagem\(s\) nos logs:

   `Completed the post deployment setup script`

   A mensagem acima indica que todas as etapas da instalação foram concluídas.

   Caso encontre qualquer um dos seguintes prefixos de ERRO, relate-os à equipe de sucesso do cliente:

   - Erro no script de configuração pós-implantação
   - Exceção ao portar o MAP de tradução
   - Não é possível portar o mapa de conversão de v1 para v2 para a propriedade
1. Atualização do plugin do conector Oxygen lançado com a versão 4.2 \(se necessário\).
1. Limpe o cache do navegador após instalar o pacote.
1. Continue atualizando as personalizações conforme detalhado na próxima seção.

### Ativar acionador de script por meio de um Servlet{#enable-trigger-serverlet}

POST:

```
http://localhost:4503/bin/guides/script/start?jobType=translation-map-upgrade
```

Resposta:

```
{
"msg": "Job is successfully submitted and lock node is created for future reference",
"lockNodePath": "/var/dxml/executor-locks/translation-map-upgrade/1683190032886",
"status": "SCHEDULED"
}
```

Na resposta JSON acima, a chave `lockNodePath` mantém o caminho para o nó criado no repositório que aponta para a tarefa enviada. Ela será excluída automaticamente quando o trabalho for concluído. Até lá, é possível consultar esse nó para saber o status atual do trabalho.

Exemplo de log: a seguir está uma amostra de logs que aparecerão no arquivo de log depois que você acionar o script.

```
04.05.2023 14:17:12.876 *INFO* [[0:0:0:0:0:0:0:1] [1683190032736] POST /bin/guides/script/start HTTP/1.1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Acquiring lock for job : translation-map-upgrade
04.05.2023 14:17:12.897 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Starting the thread to upgrade translation map from V1 to V2
04.05.2023 14:17:12.899 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Initiating lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.901 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Starting porting of translation map from V1 to V2
04.05.2023 14:17:12.904 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Memory increase is of : 764 kB
04.05.2023 14:17:12.906 *INFO* [pool-59-thread-1] com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2
04.05.2023 14:17:12.907 *INFO* [pool-59-thread-1] com.adobe.dxml.common.executor.RunnableSynchronizedOTS Releasing lock for node : /var/dxml/executor-locks/translation-map-upgrade/1683190032886
04.05.2023 14:17:12.909 *INFO* [pool-59-thread-1] com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2
```

Procure `com.adobe.fmdita.translationservices.TranslationMapUpgradeScript Completed porting of translation map from V1 to V2` e `com.adobe.fmdita.xmltranslation.ots.TranslationMapUpgradeOTS Completed the thread to upgrade translation map from V1 to V2` antes de prosseguir para as próximas etapas.



## Depois de instalar a versão 4.2.1

>[!IMPORTANT]
>
> O modelo de alta tecnologia não é exibido no servidor atualizado. Para incluir o modelo de alta tecnologia em seu servidor, você pode copiá-lo: Fonte: /libs/fmdita/pdf/Hi-Tech Destino: /content/dam/dita-templates/pdf

Depois de instalar o AEM Guides, você pode mesclar as várias configurações aplicáveis da versão recém-instalada à sua configuração.

>[!NOTE]
>
> O modelo dam-update-asset pode ser personalizado. Se alguma personalização foi feita, precisamos sincronizar as personalizações e os Guias do AEM na cópia de trabalho do modelo.

1. **Fluxo de trabalho do Ativo de atualização do DAM \(Alterações pós-processamento\):**

1. Abrir URL:

   ```http
   http://localhost:4502/libs/cq/workflow/admin/console/content/models.html
   ```

1. Selecionar **Fluxo de trabalho do Ativo de atualização DAM**.
1. Clique em **Editar**.
1. Se a variável **Iniciador de pós-processamento DXML** estiver presente, verifique se as personalizações estão sincronizadas.
1. Se a variável **Iniciador de pós-processamento DXML** estiver ausente, execute as seguintes etapas para inseri-lo:

1. Clique em **Inserir componente** \(Responsável pelo pós-processamento do AEM Guides como a etapa final do processo\).
1. Configure o **Etapa do processo** com os detalhes abaixo:

   **Guia Comum**

   **Título:** Iniciador de pós-processamento DXML

   **Descrição**: etapa do iniciador de pós-processamento DXML que acionará um trabalho sling para pós-processamento DXML do ativo modificado/criado

   **Guia Processo**

   - Selecionar **Iniciador de pós-processamento DXML** do **Processo** lista suspensa

   - Selecionar **Avanço do manipulador**

   - Selecionar **Concluído**

1. Clique em **Sincronizar** na parte superior direita depois de concluir as alterações. Você receberá uma notificação de sucesso.

   >[!NOTE]
   >
   > Atualize e verifique se as alterações personalizadas e a etapa de pós-processamento dos Guias do AEM estão presentes no modelo de fluxo de trabalho final.

1. Uma vez **Fluxo de trabalho do Ativo de atualização DAM** estiver validado, verifique as configurações correspondentes do inicializador. Para fazer isso, vá para a interface de fluxo de trabalho do AEM e abra iniciadores.

   ```http
   http://localhost:4502/libs/cq/workflow/content/console.html
   ```

   Localize e faça alterações \(se necessário\) nos dois inicializadores a seguir \(que devem estar ativos\) correspondentes a **Fluxo de trabalho do Ativo de atualização DAM**:

1. Iniciador para &quot;*Nó criado*&quot; para **Fluxo de trabalho do Ativo de atualização DAM**- para condição `"jcr:content/jcr:mimeType!=video"`, o valor de &quot;Globbing&quot; deve ser:

   ```json
   /content/dam(/((?!/subassets|/translation_output).)*/)renditions/original
   ```

   - &#39;excludeList&#39; deve ter `"event-user-data:changedByWorkflowProcess"`.
   - Iniciador para &quot;*Nó Modificado*&quot; para **Fluxo de trabalho do Ativo de atualização DAM -** para a condição &quot;`jcr:content/jcr:mimeType!=video`&quot;, o valor de &#39;Globbing&#39; deve ser:

   ```json
   `"/content/dam(/((?!/subassets|/translation_output).)*/)renditions/original"`
   ```

   - `excludeList` deve ter `"event-user-data:changedByWorkflowProcess"`.


1. Quando a atualização for concluída, verifique se todas as personalizações/sobreposições estão validadas e atualizadas para corresponder ao novo código do aplicativo. Alguns exemplos são apresentados abaixo:
   - Quaisquer componentes sobrepostos de/libs/fmditaor/libsdevem ser comparados com o novo código do produto e as atualizações devem ser feitas em arquivos sobrepostos em/apps.
   - Todas as categorias de clientlib usadas do produto devem ser revisadas para alterações. Todas as configurações substituídas \(exemplos abaixo\) devem ser comparadas com as mais recentes para obter os recursos mais recentes:
   - elementmapping.xml
   - ui\_config.json\(pode ter sido definido em perfis de pasta\)
   - alterado `com.adobe.fmdita.config.ConfigManager`
   - Verifique se qualquer um dos códigos personalizados estava usando caminhos antigos \(como mencionado na [Mapeamento de migração](#id2244LE040XA) section\) - deve ser atualizado para os novos caminhos para que as personalizações também funcionem conforme esperado.
1. Leia sobre as novas configurações trazidas na versão atual \(verifique [Notas de versão](../release-info/release-notes-4.2.1.md)\) e veja se alguma funcionalidade foi afetada, em seguida, tome as medidas apropriadas. Um exemplo pode ser o uso da seção &quot;Manuseio aprimorado de arquivos e versões&quot;, introduzida na versão 4.0, para a qual é necessário ativar uma configuração.

## Etapas para indexar o conteúdo existente para usar a nova localização e substituição:

Execute as seguintes etapas para indexar o conteúdo existente e usar o novo texto de localização e substituição no nível do mapa:

- Certifique-se de que o `damAssetLucene` a indexação foi concluída. Pode levar algumas horas, dependendo da quantidade de dados presentes no servidor. Você pode confirmar que a reindexação foi concluída verificando se o campo de reindexação está definido como falso em
   `http://<server:port>/oak:index/damAssetLucene`.  Além disso, se você tiver adicionado personalizações no `damAssetLucene`, talvez seja necessário aplicá-los novamente.

- Executar uma solicitação POST no servidor \(com autenticação correta\) - `http://<server:port\>/bin/guides/map-find/indexing`. (Opcional: é possível passar caminhos específicos dos mapas para indexá-los. Por padrão, todos os mapas serão indexados \|\| Por exemplo: `https://<Server:port\>/bin/guides/map-find/indexing?paths=<map\_path\_in\_repository\>`)

- Você também pode passar uma pasta raiz para indexar os mapas DITA de uma pasta específica (e suas subpastas). Por exemplo, `http://<server:port\>/bin/guides/map-find/indexing?root=/content/dam/test`. Observe que se os parâmetros de caminhos e de raiz forem transmitidos, somente o parâmetro de caminhos será considerado.

- A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com id de trabalho para o mesmo ponto de extremidade - `http://<server:port\>/bin/guides/map-find/indexing?jobId=\{jobId\}`\(Por exemplo: `http://localhost:8080/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42`\)


- Quando o trabalho for concluído, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados nos logs do servidor.

**Tópico pai:**[ Baixar e instalar](download-install.md)

