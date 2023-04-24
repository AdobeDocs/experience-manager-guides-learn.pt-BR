---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de abril de 2023
description: Versão mais recente dos Guias do Adobe Experience Manager as a Cloud Service
source-git-commit: 77b118655ad8e37e00b0371497e4a2578ddd276e
workflow-type: tm+mt
source-wordcount: '852'
ht-degree: 2%

---

# Versão de abril dos Guias do Adobe Experience Manager as a Cloud Service

## Atualizar para a versão mais recente

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:

1. Verifique o código GKS do Cloud Services e alterne para a ramificação configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2023.4.249.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão mais recente dos Guias AEM as a Cloud Service.

## Etapas para indexar o conteúdo existente (somente se você estiver em uma versão anterior à versão de setembro AEM Guias as a Cloud Service)

Execute as seguintes etapas para indexar o conteúdo existente e usar o novo texto localizar e substituir no nível de mapa:

* Execute uma solicitação de POST para o servidor (com autenticação correta) - `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: Você pode passar caminhos específicos dos mapas para indexá-los, por padrão, todos os mapas serão indexados || Exemplo : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com ID do trabalho para o mesmo ponto final - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por exemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Quando a tarefa for concluída, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados dos logs do servidor.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software suportados pelos Guias AEM as a Cloud Service versão de abril de 2023.

### Servidor de publicação do FrameMaker e do FrameMaker

| AEM Guias das a Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.04.0 | Não compatível | 2022 ou superior |
|  |  |  |


### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac | Editar no Windows Oxygen | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.04.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service fornecem aprimoramentos e novos recursos na versão mais recente:

### Suporte avançado a metadados na publicação de PDF

Os Guias de AEM agora fornecem suporte avançado para os metadados que são mapeados para os metadados na saída do PDF. As opções de metadados incluem informações sobre o documento e seu conteúdo, como nome do autor, título do documento, palavras-chave, informações de direitos autorais e outros campos de dados.

<img src="assets/pdf-metadata.png" alt=" metadados pdf nativos">

É possível importar um arquivo XMP e os Guias AEM podem escolher as informações do arquivo. Você também tem a opção de fornecer os nomes e valores dos metadados usando a lista suspensa. Você também pode adicionar metadados personalizados digitando diretamente no campo de nome.


### Painel de Exibição de Estrutura de Tópicos Avançada

Os Guias AEM fornecem um painel de Exibição de Contorno improvisado no qual você obtém a exibição hierárquica dos elementos usados no documento.

<img src="assets/select-element-content-outline-view_cs.png" alt=" metadados pdf nativos">

A Exibição da estrutura de tópicos oferece as seguintes melhorias:

* A lista suspensa Opções de exibição é exibida na parte superior do painel Exibição em linha. Se um elemento tiver uma ID, um atributo e um texto, você poderá selecioná-los na lista suspensa para exibi-los junto com o elemento . Os atributos que podem ser exibidos no painel Exibição da estrutura de tópicos são determinados pelas configurações dos Atributos de exibição que foram configuradas pelo administrador no **Configurações do editor**.

* Usando o recurso de pesquisa, é possível pesquisar um elemento pelo nome, id, texto ou valor do atributo.


### Publicação com base em microsserviços para guias de AEM as a Cloud Service

AEM Guias as a Cloud Service fornecem o recurso para executar grandes cargas de trabalho de publicação simultaneamente com publicação baseada em microsserviços e aproveitar a plataforma sem servidor Adobe I/O Runtime líder do setor.

Agora, na versão de abril, você pode executar várias solicitações de publicação simultaneamente e gerar saídas de PDF em massa com eficiência usando a publicação Native PDF com base em microsserviço.
Para obter mais detalhes, consulte [Configurar a nova publicação baseada em microsserviços para guias de AEM as a Cloud Service](../knowledge-base/publishing/configure-microservices.md).


## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* PDF nativo | A publicação de conteúdo com uma classe de saída com colchetes() leva a um congelamento da publicação. (11596)
* Ocorre um problema ao mover (arrastar e soltar) o lugar de um item de lista existente com Rastrear alterações em. (11570)
* Ocorre um problema ao mover (arrastar e soltar) como um novo item de lista com Rastrear alterações em. (11569)
* Os itens da lista de recuo ou recuo não funcionam como esperado com Rastrear alterações em. (11568)
* Adicionar conteúdo em uma linha com Rastrear alterações ativado e desativar Rastrear alterações não a desativa. (11567)
* Dificuldade em arrastar e soltar um item de lista, o texto é movido no lugar do item de lista. (11566)
* A revisão concluída não abre no modo somente leitura. (11387)
* Ocorre um problema AEM pesquisa no Site (não funciona além de 2 a 3 nós de nível). (11352)
* Ao criar o elemento exibido em verde (Rastrear alterações), o novo conteúdo é exibido como uma mudança de rastreamento, mesmo que a alteração de rastreamento esteja desativada. (7021)

### Problema conhecido com solução alternativa

O Adobe identificou o seguinte problema conhecido para a versão dos Guias AEM as a Cloud Service abril de 2023.

* PDF nativo | Os metadados antigos não são preenchidos até que a predefinição de saída seja explicitamente aberta.

