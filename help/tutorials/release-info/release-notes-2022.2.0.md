---
title: Notas de versão para [!DNL AEM Guides], versão de fevereiro de 2022
description: Versão de fevereiro [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: eb7ff475-bb5b-4d32-b291-024147fbfed1
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 3%

---

# Versão de fevereiro [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Atualize para a versão de fevereiro

Atualize seu [!DNL Adobe Experience Manager Guides] as a Cloud Service (mais tarde conhecido como [!DNL AEM Guides] as a Cloud Service) ao executar as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação do Cloud Services configurada no pipeline correspondente ao ambiente que você deseja atualizar.
1. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.2.114.
1. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de fevereiro de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software suportados por [!DNL AEM Guides] Versão as a Cloud Service de fevereiro de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |


### Conector de oxigênio

| [!DNL AEM Guides] Versão da nuvem | Janelas do conector de oxigênio | Conector de oxigênio Mac |
| --- | --- | --- |
| 2022.2.0 | 2.4.0 | 2.4.0 |
|  |  |  |


## Novos recursos e melhorias

### Publicação PDF nativa

O suporte para a criação de um PDF nativo também foi adicionado na versão de fevereiro do [!DNL AEM Guides] as a Cloud Service. Um novo mecanismo de publicação foi introduzido com os seguintes recursos:
* Criar um modelo de CSS
* Criar modelos de página diferentes
* Modelos de PDF de design que incluem CSS e modelos de página
* Publicar mapa e conteúdo de tópico no formato PDF

### Suporte para caminho do site da base de conhecimento na publicação baseada em artigo

[!DNL AEM Guides] O as a Cloud Service oferece o recurso de publicação baseado em artigos para gerar de forma incremental uma saída de um ou mais tópicos ou publicar seu conteúdo em uma plataforma de base de conhecimento. Com a versão de fevereiro, você tem uma opção adicional para escolher o caminho do site da Base de conhecimento para o qual o tópico/mapa precisa ser publicado. Depois que você selecionar o caminho, a saída será gerada no caminho especificado.

### Aprimoramentos no editor da Web

Muitos aprimoramentos e novos recursos foram adicionados ao Editor da Web:

* **Caixa de diálogo melhorada ao fechar o arquivo**

[!DNL AEM Guides] O as a Cloud Service solicita que você salve suas alterações e desbloqueie seus arquivos bloqueados quando tentar fechar um arquivo aberto no Editor da Web. Os prompts são exibidos com base na variável **Solicitar check-in ao fechar** e **Solicitar nova versão ao fechar** configurações definidas pelo administrador.

Com base na configuração, você obtém a opção de salvar as alterações e criar uma nova versão do documento. Ou também é possível fazer check-in do arquivo e salvar as alterações na versão atual.

![Fechar arquivo](assets/file-close-save-changes-unlock.png)

Para obter mais detalhes, consulte *Fechar e salvar cenários* no Guia do usuário.

* Um espaço sem quebra foi adicionado ao palete de caracteres.  A **sem quebra** impede uma quebra automática de linha em um ponto específico de um documento HTML. O Editor da Web oferece suporte a um espaço sem quebra para saída AEM Site e HTML5.

* Quando você carrega uma imagem do Editor da Web, uma caixa de diálogo de confirmação é exibida se uma imagem com o mesmo nome já existir. Você pode manter ambos os arquivos - existentes e o novo arquivo, ou substituir o arquivo existente e salvar somente o novo arquivo.

* Se algum usuário tiver bloqueado qualquer arquivo para edições, um administrador poderá liberar o bloqueio e verificar o arquivo. Esse recurso será útil quando alguns arquivos precisarem ser editados, mas tiverem sido bloqueados por usuários que não estão disponíveis para fazer check-in no arquivo

### Painel de mapa

Ao optar por baixar o mapa DITA, a solicitação é colocada em fila e você recebe uma notificação quando o mapa estiver pronto para download. Você pode optar por baixar o arquivo de mapa imediatamente ou baixá-lo posteriormente no link fornecido na Caixa de entrada de notificação AEM.

![Download do mapa](assets/download-map-prompt.png)

### Análise

Você pode mencionar os detalhes no campo de descrição da tarefa de revisão e ele é exibido no email enviado ao revisor.

## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

### Publicação baseada em artigo

* A publicação baseada em artigo não publica artigos com base na linha de base selecionada. (8771)
* Os arquivos DITAVAL não são honrados na publicação baseada em artigos. (8770)
* Não é possível fazer a publicação baseada em artigos para o perfil Salesforce quando o tipo de registro é Perguntas frequentes e o conteúdo do campo de artigo é Pergunta. (8448)
* Não é possível fazer a publicação baseada em artigos para o perfil do Salesforce quando o tipo de registro é Manual. (8447)

### Editor da Web

* Arrastar e soltar uma condição não funciona em tópicos DITA. (8761)
* Os atributos estão ausentes ao adicionar um capítulo ao mapa de favoritos usando a opção Arrastar e soltar da exibição Favoritos. (8746)
* Editar as propriedades de uma imagem (altura, largura) resulta em um erro de aplicativo. (8722)
* Os links quebrados não aparecem no painel Contorno na exibição de origem. (8590)
* O Editor XML remove a tag de nova linha no codeblock. (8522)
* Os glossários são mostrados como uma Nota quando um Glossentry é criado. (8384)
* xref não pode ser inserido mesmo em locais válidos. (8354)
* A lista de elementos (Alt+Enter) aparece esmaecida no tema Escuro/Mais Escuro. (7913)
* A lista de modelos de mapa em **Criar** opção (menu reticências) do painel Repositório não é conforme o **Perfil da pasta** em Preferências do usuário. (5918)
* As IDs de elemento não são geradas automaticamente para elementos adicionados pelo recurso Reutilizar conteúdo da barra de ferramentas principal. (5826)

### Interface do usuário do Assets

* A edição de imagem não está funcionando como esperado no servidor de nuvem. (8768)
* No painel Histórico de versões, a seção da versão atual mostra um carimbo de data e hora incorreto e foi modificado por informações. (8765)
* O upload do arquivo DITAVAL no servidor da nuvem falha quando AEM ferramenta de desktop é usada. (8707)
* O segundo usuário administrador não pode ser adicionado como o primeiro usuário administrador a uma pasta. (8430)
* Propriedades não exclusivas de um ativo não são copiadas quando ele é copiado e colado. (8241)

### Alterações de usabilidade

* No painel Revisão do Editor da Web, se um nome de usuário for longo, os ícones para aceitar/rejeitar não serão exibidos claramente. (8793)
* No **Localizar e substituir** , um ícone indesejado é exibido no mouse, na seção de resultados. (8775)
* O ícone personalizado não é extraído da propriedade e, em vez disso, o ícone padrão é exibido para os relatórios gerados usando o botão Gerar relatório . (8573)
