---
title: Notas de versão | Adobe Experience Manager Guides as a Cloud Service, versão de abril de 2023
description: Versão mais recente do Adobe Experience Manager Guides as a Cloud Service
exl-id: 3b09f0b3-cfa4-422d-91b7-733ab1c1896c
source-git-commit: cf612da41f79b0bf9da4c4d7454a0e3c86af7a4c
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 2%

---

# Versão de abril do Adobe Experience Manager Guides as a Cloud Service

## Atualizar para a versão mais recente

Atualize seus Guias do Adobe Experience Manager atuais as a Cloud Service (mais tarde chamados de *Guias de AEM as a Cloud Service*), executando as seguintes etapas:

1. Confira o código Git do Cloud Services e alterne para a ramificação configurada no pipeline Cloud Services correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade no `/dox/dox.installer/pom.xml` arquivo do seu código Git Cloud Services para 2023.4.249.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão mais recente dos Guias do AEM as a Cloud Service.

## Etapas para indexar o conteúdo existente (somente se você estiver em uma versão anterior à versão de setembro do AEM Guides as a Cloud Service)

Execute as seguintes etapas para indexar o conteúdo existente e usar o novo texto de localização e substituição no nível do mapa:

* Execute uma solicitação POST no servidor (com a autenticação correta) - `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: é possível passar caminhos específicos dos mapas para indexá-los; por padrão, todos os mapas serão indexados || Exemplo: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com id de trabalho para o mesmo ponto de extremidade - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por exemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Quando o trabalho for concluído, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados nos logs do servidor.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade dos aplicativos de software compatíveis com os Guias do AEM as a Cloud Service na versão de abril de 2023.

### FrameMaker e FrameMaker Publishing Server

| Versão do AEM Guides as a Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.04.0 | Não compatível | 2022 ou superior |
|  |  |  |


### Conector de oxigênio

| Versão do AEM Guides as a Cloud | Janelas do conector Oxygen | Conector Oxygen Mac | Editar no Oxygen Windows | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.04.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Novos recursos e melhorias

O AEM Guides as a Cloud Service oferece aprimoramentos e novos recursos na versão mais recente:

### Suporte a metadados avançados na publicação do PDF

Agora, os Guias do AEM fornecem suporte avançado para os metadados que são mapeados para os metadados na saída do PDF. As opções de metadados incluem informações sobre o documento e seu conteúdo, como nome do autor, título do documento, palavras-chave, informações de direitos autorais e outros campos de dados.

<img src="assets/pdf-metadata.png" alt=" metadados pdf nativos">

Você pode importar um arquivo XMP e os Guias AEM podem coletar as informações do arquivo. Também há a opção de fornecer os nomes e valores dos metadados usando a lista suspensa. Você também pode adicionar metadados personalizados digitando diretamente no campo de nome.


### Painel Modo de Exibição de Estrutura de Tópicos Avançado

As Guias do AEM fornecem um painel Exibição de contorno aprimorado no qual você obtém a exibição hierárquica dos elementos usados no documento.

<img src="assets/select-element-content-outline-view_cs.png" alt=" metadados pdf nativos">

A Exibição de estrutura de tópicos fornece as seguintes melhorias:

* A lista suspensa Opções de exibição é exibida na parte superior do painel Exibição de estrutura de tópicos. Se um elemento tiver uma ID, um atributo e um texto, você poderá selecioná-los na lista suspensa para exibi-los junto com o elemento. Os atributos que podem ser exibidos no painel Modo de Exibição de Estrutura de Tópicos são determinados pelas configurações de Atributos de Exibição definidas pelo administrador no **Configurações do editor**.

* Usando o recurso de pesquisa, você pode pesquisar um elemento por seu nome, id, texto ou valor de atributo.


### Publicação baseada em microsserviços para guias do AEM as a Cloud Service

O AEM Guides as a Cloud Service oferece o recurso para executar grandes cargas de trabalho de publicação simultaneamente com publicações baseadas em microsserviços e aproveitar a plataforma Adobe I/O Runtime sem servidor, líder do setor.

Agora, na versão de abril, você pode executar várias solicitações de publicação simultaneamente e gerar saídas de PDF em massa de maneira muito eficiente, usando a publicação de PDF nativo baseada em microsserviços.
Para obter mais detalhes, consulte [Configure a nova publicação baseada em microsserviços para os Guias do AEM as a Cloud Service](../knowledge-base/publishing/configure-microservices.md).


## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* PDF nativo | A publicação de conteúdo que tem uma classe de saída com colchetes() resulta em um congelamento da publicação. (11596)
* Ocorre um problema ao mover (arrastar e soltar) no lugar de um item de lista existente com o Controle de alterações ativado. (11570)
* Ocorre um problema ao mover (arrastar e soltar) como um novo item de lista com a opção Controlar alterações ativada. (11569)
* O recuo ou o recuo de itens de lista não funciona como esperado quando a opção Controlar alterações está ativada. (11568)
* Adicionar conteúdo em uma linha com a opção Controlar alterações ativada e desativar Controlar alterações não o desativa realmente. (11567)
* Dificuldade em arrastar e soltar um item de lista, o texto é movido no lugar do item de lista. (11566)
* A revisão concluída não abre no modo somente leitura. (11387)
* Problema ocorre na pesquisa do site AEM (não funciona além de 2-3 nós de nível). (11352)
* Ao criar no elemento exibido em verde (Controlar alterações), o novo conteúdo é exibido como rastrear alteração mesmo que a opção rastrear alteração esteja desativada. (7021)

### Problema conhecido com a solução alternativa

A Adobe identificou o seguinte problema conhecido para os Guias AEM as a Cloud Service na versão de abril de 2023.

* PDF nativo | Os metadados antigos não são preenchidos até que a predefinição de saída seja aberta explicitamente.
