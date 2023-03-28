---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de fevereiro de 2023
description: Versão de fevereiro do Adobe Experience Manager Guias as a Cloud Service
exl-id: c639b136-11ed-4a8b-a595-4bb5da879747
source-git-commit: ee520ab86ea41df7556a1f40d7bfc5e3617b34ae
workflow-type: tm+mt
source-wordcount: '2178'
ht-degree: 2%

---

# Versão de fevereiro do Adobe Experience Manager Guias as a Cloud Service

## Atualize para a versão de fevereiro

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2023.2.235.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de fevereiro AEM Guias as a Cloud Service.

## Etapas para indexar o conteúdo existente (somente se você estiver em uma versão anterior à versão de setembro AEM Guias as a Cloud Service)

Execute as seguintes etapas para indexar o conteúdo existente e use o novo texto localizar e substituir no nível de mapa:

* Execute uma solicitação de POST para o servidor (com autenticação correta) - `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: Você pode passar caminhos específicos dos mapas para indexá-los, por padrão, todos os mapas serão indexados || Exemplo : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com ID do trabalho para o mesmo ponto final - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por exemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Quando a tarefa for concluída, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados dos logs do servidor.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software compatíveis com AEM Guias as a Cloud Service versão de fevereiro de 2023.

### Servidor de publicação do FrameMaker e do FrameMaker

| AEM Guias das a Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.02.0 | Não compatível | 2022 ou superior |
|  |  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac | Editar no Windows Oxygen | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.02.0 | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service oferecem aprimoramentos e novos recursos na versão de fevereiro:

### Gerar relatórios pelo Editor da Web

AEM Guias vem com um recurso no Editor da Web que permite verificar a integridade geral de seus documentos técnicos e gerar relatórios para eles.
Você pode exibir a lista de tópicos, gerenciar os metadados e ver a multimídia usada em todas as referências do mapa atual do
**Relatórios** no Editor da Web.

**Gerar a exibição de Lista de tópicos**

Você pode gerar a Lista de tópicos que fornece informações detalhadas sobre seus tópicos, como tipo de referência, estado do documento e autor. Você também pode gerar o CSV para baixar o instantâneo atual dos tópicos no mapa DITA.

**Gerenciar metadados e alterar o estado do documento**

Você pode aplicar tags em um tópico individual ou usar o recurso de marcação em massa para aplicar várias tags em vários tópicos, um mapa DITA ou um submapa. Também é possível alterar o estado do documento de todos os tópicos selecionados para o próximo estado comum possível do documento.

<img src="assets/web-editor-metadata-panel.png" alt="gerenciar metadados" width="600">

**Gerar o relatório Multimídia**

Você pode gerar o relatório multimídia, que contém informações detalhadas sobre a multimídia usada em suas referências no mapa atual. Você tem a flexibilidade de filtrar e classificar os arquivos de multimídia listados no relatório.
Você também pode gerar o CSV para baixar o instantâneo atual da multimídia usada no mapa DITA.

<img src="assets/web-editor-reports-multimedia.png" alt="relatório multimídia" width="600">

### UX remodelado para a funcionalidade de revisão

Agora, os guias de AEM fornecem um UX aprimorado que ajuda a revisar os tópicos compartilhados para revisão. Na experiência mais recente, a funcionalidade de revisão tem os seguintes aprimoramentos:

* Interface do usuário atualizada
* Painel Condições , que permite realçar o conteúdo de acordo com as condições disponíveis no tópico
* Cada comentário no painel de comentário está vinculado ao texto correspondente no tópico atual. Ajuda a identificar o texto comentado.
* Os comentários são exibidos na ordem do texto comentado no documento.
* O nome da tarefa de revisão é exibido no workflow de revisão.
* Selecione o rootmap para a tarefa de revisão que é usada para resolver todas as referências principais e termos de glossário usados no conteúdo de revisão.
* Barra de ferramentas contextual que ajuda você a destacar ou tachar rapidamente o texto
* Menu Opções para editar ou excluir seus próprios comentários
* Para comentários desatualizados, você tem acesso à visualização lado a lado, o que ajuda a comparar a versão anterior do tópico com a versão de revisão atual.
* Ao usar os filtros, os comentários no painel direito são filtrados de acordo com a seleção, e o número de comentários no painel esquerdo é atualizado adequadamente.


   <img alt="revisar tarefa" src="assets/comment-pop-up-panel.png" width="600">



### Aprimoramentos de tradução

Agora você tem melhorias mais fáceis de usar no painel Tradução , que ajudam a traduzir facilmente seus documentos do Editor da Web.

**Passe o rótulo da versão para a versão de destino**

AEM Guias permite que você passe o rótulo do arquivo de origem para o arquivo de destino. Isso ajuda você a identificar facilmente a versão de origem do arquivo traduzido.

<img alt="rótulos de tradução" src="assets/translation-pass-source-label.png" width="600">

Por exemplo, se você tiver alguns arquivos de origem com o rótulo da versão Versão 1.0 aplicado a eles, também poderá passar o rótulo da origem (Versão 1.0) para o arquivo traduzido.

**Forçar sincronização para ativos fora de sincronia**

Se você fizer alterações em alguns dos ativos, AEM Guias os marcará como Fora de Sincronização. Você pode traduzir novamente os ativos modificados ou optar por descartar o status Fora de Sincronização. Por exemplo, se você fez algumas pequenas alterações que realmente não precisam de uma tradução, é possível marcar o status como Em sincronia.

<img src="assets/translation-version-diff.png" alt="quadro de tradução" width="600">

**Exibir projetos de tradução em andamento para um tópico ou mapa**

Algumas das referências no painel de tradução podem estar em andamento. Agora os Guias AEM fornecem um recurso para ajudá-lo a visualizar a lista de todos os projetos de tradução Em andamento (junto com o idioma de destino) que contêm a referência selecionada.


### Gerar saída em vários formatos no Editor da Web

Agora é possível gerar facilmente a saída dos tópicos ou do mapa DITA pelo Editor da Web. Você pode configurar várias predefinições de saída, como AEM Site, PDF, HTML5, JSON (um formato de saída sem cabeçalho) e saída personalizada. Em seguida, você pode usá-los para gerar as respectivas saídas.

Você pode definir atributos nos tópicos do DITA e usar a predefinição de condição para aplicar uma condição enquanto publica a saída. Você também pode usar o recurso de publicação da linha de base para publicar seletivamente uma versão específica do seu mapa ou tópico do DITA.


### Localizar e substituir o texto no nível de mapa

AEM Guias permite procurar arquivos em um mapa que contém texto específico. O texto pesquisado é realçado nos arquivos. Agora você também pode substituir a palavra ou frase pesquisada por outra palavra ou frase em todos os arquivos. Você pode selecionar **Substituir tudo** ícone à direita na parte superior da lista para substituir todas as ocorrências do termo pesquisado em todos os arquivos.

<img src="assets/map-find-replace.png" alt="localizar mapa substituir" width="600">

### Excluir e duplicar arquivos do painel de repositório

Agora é possível criar facilmente uma duplicata ou uma cópia de um arquivo da **Opções** do arquivo selecionado no painel de repositório. Por padrão, o arquivo é criado com um sufixo (como `filename_1.extension`).

<img src="assets/options-menu-repo-view-file-level.png" alt="menu opções de arquivo " width="500">


### Outras melhorias no Editor da Web

* Nos Guias AEM, é possível executar algumas operações comuns para imagens e arquivos de mídia usando o menu de contexto. Agora, também é possível localizar a imagem ou a mídia selecionada no repositório ou visualizar o arquivo na interface do usuário do Assets.

* O nome do Perfil da pasta atual é exibido como um rótulo para o ícone Preferências do usuário na barra de ferramentas principal. Isso ajuda a identificar o perfil da pasta em que você está trabalhando.

* Ao abrir um mapa na exibição de mapa, o título do mapa atual é exibido no centro da barra de ferramentas principal. Isso é útil para informar aos usuários qual mapa está aberto no momento.


### Exibir título no lugar de UUID no Editor de Oxigênio

Agora, AEM Guias permite escolher **Usar título no Editor e no Gerenciador de Mapas** em Configurações. Se você selecionar essa opção, o título do arquivo será exibido na guia do arquivo, quando aberto no Editor ou no Gerenciador de mapas DITA. Se você não selecionar essa opção, a UUID do arquivo será exibida na guia do arquivo.

### Publicação com base em microsserviços para guias de AEM as a Cloud Service

O novo microsserviço de publicação permite executar grandes cargas de trabalho de publicação simultaneamente nos Guias AEM as a Cloud Service e aproveitar a plataforma sem servidor Adobe I/O Runtime líder do setor.

Para cada solicitação de publicação AEM Guias as a Cloud Service executa um contêiner separado que é dimensionado horizontalmente de acordo com as solicitações do usuário. Isso permite que você execute várias solicitações de publicação e obtenha um desempenho aprimorado.

Para obter mais detalhes, consulte [Configurar a nova publicação baseada em microsserviços para guias de AEM as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/knowledge-base/publishing/configure-microservices.md).

### PDF nativo | Adicionar um marcador personalizado na saída do PDF

Agora é possível adicionar um marcador personalizado em um conteúdo específico na saída final do PDF para facilitar a navegação. Isso seria adicionado ao TOC, que é criado a partir dos títulos de tópico ou seção no mapa DITA.

### PDF nativo | Aplicar estilo personalizado em entradas de sumário e conteúdo de tópico

AEM Guias fornece o recurso para aplicar estilo personalizado às entradas TOC ou a um tópico específico na saída do PDF. Por exemplo, você pode alterar a cor do texto no sumário e o título do tópico. Também é possível aplicar estilos em todo o conteúdo do tópico.


### PDF nativo | Estilo do marcador de página no componente de nota de rodapé

Agora você pode criar um estilo para o marcador de página nas notas. Por exemplo, é possível adicionar colchetes ou alterar a cor. Esses estilos ajudam os usuários a identificar facilmente os marcadores de página no documento.

### PDF nativo | Barra de alterações para indicar tópicos alterados no Índice

Os Guias de AEM agora permitem identificar rapidamente os tópicos alterados no TOC da saída do PDF.  Mostra uma barra de alteração à esquerda dos tópicos alterados no TOC. Você pode clicar no tópico no sumário e exibir as alterações detalhadas.

<img src="assets/change-marker-toc.png" alt="Alterar marcador no sumário " width="500">

## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

### Criação  

* As alterações no html do Editor da Web causam problemas com `<dl>` e `<dlentry>`. (11024)
* Alguns atributos não estão sendo tratados como condicionais e causando problemas. (10895)
* Três níveis ou mais aninhados `<indexterm>` não estão aninhados na exportação de PDF nativo. (10799)
* O conteúdo desaparece no corpo de uma tarefa ao alternar da exibição Autor para Origem. (10735)
* Os comentários de revisão são colocados incorretamente em uma tarefa de revisão. (10625)
* **Desfazer** ou **Refazer** O não está funcionando corretamente em alguns arquivos. (10373)
* Os metadados personalizados não são retidos na ação de copiar e colar. (10367)
* A opção Desfazer no Editor XML leva o usuário para a parte superior da página. (10091)
* As propriedades de nó são removidas após a operação de copiar e colar um ativo. (10053)
* mimeType é codificado para criação e atualização de ativos DITA. (8979)
* O nome do criador da versão no Histórico da versão é &quot;fmdita-serviceuser&quot; para os arquivos carregados por meio da interface do usuário do Assets. (8910)
* Os fragmentos de conteúdo não podem ser copiados e colados quando os Guias de AEM estão instalados no Cloud. (11315)
* O navegador (editor da Web) congela ao carregar conteúdo com esquema personalizado. (11211)

### Gerenciamento

* Copiar um ativo de mapa DITA (da interface do usuário do ativo ) causa erros nas linhas de base no ativo copiado. (11218)
* A mensagem de aviso não é exibida no upload de um arquivo maior que o limite permitido em AEM (2 GB por padrão). (10817)
* Linha de Base do Editor da Web | O comportamento da coluna Mais recente é diferente no novo painel de linha de base no Editor da Web. (10808)
* Tradução | O trabalho de tradução não é iniciado devido a /libs/fmdita/i18n/ja.json inválido. (10543)
* Tradução | Um erro ocorre em um projeto de tradução de escopo criado a partir do painel de tradução (Tradução Humana). (10526)
* Tradução | O pós-processamento é bloqueado para a pasta de idioma inteira cujos ativos estão presentes em um projeto de tradução ativo. (10332)
* Vários pop-ups são exibidos para qualquer ativo se a versão for alterada e salva no editor de Linha de base. (10399)
* O vazamento da sessão ocorre em `com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210)`. (10279)

### Publicação

* A regeneração de tópico não está funcionando para alguns cenários. (10635)
* O Publishlistener não exibe os dados solicitados em logs de informações e também contém alguns logs de lixo.( 10567)
* PDF nativo | Ao criar uma predefinição de saída com a opção &quot;Adicionar ao perfil da pasta&quot;, a geração de PDF falha com uma exceção de ponteiro nulo. (10950)
* PDF nativo | Problemas ao girar o cabeçalho da Tabela. (10555)
* PDF nativo | Aninhado `<indexterm>` não estão aninhados na exportação de PDF nativo. (10521)
* PDF nativo | Topicref aninhado em apêndices são todos transformados em h1 no HTML temporário. (10454)
* A publicação da linha de base falha para PDF gerado usando o FrameMaker Publishing Server 2020. (10551)
* PDF nativo | Adição de `xref` para uma Imagem não renderiza a imagem no PDF gerado. (11346)
* PDF nativo | A tag da imagem adiciona o atributo display-inline a todas as imagens. (10653)
* PDF nativo | Os comentários de rascunho são ocultos por padrão na saída gerada. (10560)
* PDF nativo | navtitle não é homenageado por topichead. (10509)
