---
title: Notas de versão | Versão do Adobe Experience Manager Guides 4.2
description: Versão mais recente dos Guias do Adobe Experience Manager
exl-id: 8a7fef77-63af-462f-89c5-054ab31e079b
source-git-commit: 890d64aed5f4005e3f4d3143bc35804e39036ad3
workflow-type: tm+mt
source-wordcount: '3668'
ht-degree: 2%

---

# Versão 4.2 do Adobe Experience Manager Guides (fevereiro de 2023)

Esta nota de versão aborda as instruções de atualização, os novos recursos e os aprimoramentos na versão 4.2 do Adobe Experience Manager Guides (mais tarde chamada de *Guias do AEM*).

## Atualizar para a versão mais recente

Você pode facilmente atualizar sua versão atual dos Guias do AEM para a versão 4.2. Antes de prosseguir com a atualização para a versão 4.2 dos Guias do AEM, você deve considerar os seguintes pontos:
* Se você estiver usando a versão 4.0, 4.1 ou 4.1.x, é possível atualizar diretamente para a versão 4.2.
* Se você estiver usando a versão 3.8.5, será necessário atualizar para a versão 4.0 antes de atualizar para a versão 4.2.
* Se você estiver em uma versão anterior à 3.8.5, consulte a *Atualizar guias do AEM* no guia de instalação específico do produto.

>[!NOTE]
>
>Você deve instalar o service pack AEM antes de atualizar a versão dos Guias AEM.

Para obter detalhes, consulte [Instruções de atualização](assets/Adobe-Experience-Manager-Guides-Upgrade-Instructions-EN.pdf).

## 4.2 | Notas de versão

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade dos aplicativos de software suportados pela versão 4.2 dos Guias AEM.

### Adobe Experience Manager

**Não UUID**
Versão 6.5 Service Pack 15, 14, 13 ou 12

**UUID**
Versão 6.5 Service Pack 15, 14, 13 ou 12

Para obter mais detalhes, consulte *Requisitos técnicos* no guia Instalar e configurar o Adobe Experience Manager Guides.

### FrameMaker e FrameMaker Publishing Server

| Versão | FMPS 2022 | FMPS 2020 | Fm 2022 | Fm 2020 |
| --- | --- | --- | --- | --- |
| 4.2 (Não UUID) | 2022 ou superior | 2020.2 ou superior* | 2022 ou superior | 2020.3 ou superior |
| 4.2 (UUID) | 2022 ou superior | 2020.2 ou superior* | 2022 ou superior | 2020.4 ou superior |
|  |  |  |  |

*A linha de base e as condições criadas no AEM são compatíveis com as versões do FMPS a partir de 2020.2.

### Conector de oxigênio

| Versão | Janelas do conector Oxygen | Conector Oxygen Mac | Editar no Oxygen Windows | Editar no Oxygen Mac |
| --- | --- | --- |--- |--- |
| 4.2 (Não UUID) | 2.1-regular-4 | 2.1-regular-4 | 1.6 | 1.6 |
| 4.2 (UUID) | 2.8-uuid-8 | 2.8-uuid-8 | 2.3 | 2.3 |
|  |  |  |


## Novos recursos e melhorias

Os Guias do AEM fornecem muitas melhorias e novos recursos na versão 4.2:

### Gerar relatórios pelo Editor da Web

O AEM Guides vem com um recurso no Editor da Web que permite verificar a integridade geral de seus documentos técnicos e gerar relatórios para eles.
Você pode exibir a lista de tópicos e gerenciar os metadados de todas as referências para o mapa atual no
**Relatórios** no Editor da Web.

**Gerar a exibição da Lista de tópicos**

Você pode gerar a Lista de tópicos que fornece informações detalhadas sobre os tópicos, como tipo de referência, estado do documento e autor. Você também pode gerar o CSV para baixar o instantâneo atual dos tópicos no mapa DITA.

**Gerenciar metadados e alterar estado do documento**

Você pode aplicar tags a um tópico individual ou usar o recurso de marcação em massa para aplicar várias tags a vários tópicos, um mapa DITA ou um submapa. Você também pode alterar o estado do documento de todos os tópicos selecionados para o próximo estado de documento comum possível.

<img src="assets/web-editor-metadata-panel.png" alt="gerenciar metadados" width="600">

### UX renovado para a funcionalidade de revisão

Agora, os guias de AEM fornecem um UX aprimorado que ajuda a analisar os tópicos compartilhados para análise. Na experiência mais recente, a funcionalidade de revisão tem as seguintes melhorias:

* Interface do usuário atualizada
* Painel Condições que permite realçar o conteúdo de acordo com as condições disponíveis no tópico.
* Cada comentário no painel de comentários é vinculado ao texto correspondente no tópico atual. Isso ajuda a identificar o texto comentado.
* Os comentários são exibidos na ordem do texto comentado no documento.
* O nome da tarefa de revisão é exibido no workflow de revisão.
* Selecione o roteiro da tarefa de revisão que é usado para resolver todas as referências principais e termos de glossário usados no conteúdo da revisão.
* Barra de ferramentas contextual que ajuda a destacar ou tachar rapidamente o texto.
* Menu Opções para editar ou excluir seus próprios comentários.
* Para comentários desatualizados, você tem acesso à visualização lado a lado, o que ajuda a comparar a versão anterior do tópico com a versão de revisão atual
* Ao usar os filtros, os comentários no painel direito são filtrados de acordo com a seleção e o número de comentários no painel esquerdo é atualizado adequadamente.


<img alt="tarefa de revisão" src="assets/comment-pop-up-panel.png" width="600">


Para obter mais detalhes, consulte *Revisar tópicos ou mapas* no guia Uso dos guias do Adobe Experience Manager.

### Aprimoramentos de tradução

Agora você tem aprimoramentos mais fáceis de usar no painel Tradução que ajudam a traduzir facilmente seus documentos do Editor da Web.


**Coluna Rótulo da versão adicionada ao painel de tradução**

No painel de tradução, também é possível ver a coluna Rótulo da versão. Isso exibe o Rótulo da versão selecionada do arquivo de origem. Isso pode ajudá-lo a selecionar todos os arquivos com um rótulo específico e traduzi-los de uma só vez.

**Visualizar diferença de versão para arquivos Fora de sincronização no painel de tradução**

Agora você pode verificar as diferenças entre a versão selecionada e a última versão de origem traduzida dos tópicos. Você também pode optar por traduzir a variável **Fora de sincronia** arquivos com base nas alterações feitas entre as duas versões de um tópico.

<img src="assets/translation-version-diff.png" alt="quadro de tradução" width="600">



**Passar o rótulo da versão para a versão de destino**

Guias do AEM permitem passar o rótulo do arquivo de origem para o arquivo de destino. Isso ajuda a identificar facilmente a versão de origem do arquivo traduzido.

<img alt="rótulos de tradução" src="assets/translation-pass-source-label.png" width="600">

Por exemplo, se você tiver alguns arquivos de origem com o rótulo da versão Release 1.0 aplicado a eles, também será possível passar o rótulo de origem (Release 1.0) para o arquivo traduzido.

**Forçar sincronização para ativos fora de sincronização**

Se você fizer alterações em alguns ativos, os Guias do AEM os marcará como Fora de sincronia. Você pode traduzir novamente os ativos modificados ou optar por descartar o status Fora de sincronização. Por exemplo, se você tiver feito algumas pequenas alterações que realmente não precisam de uma tradução, poderá marcar o status delas como Em sincronia.

**Exibir projetos de tradução em andamento para um tópico ou mapa**

Algumas das referências no painel de tradução podem estar em andamento. Agora, o AEM Guides fornece um recurso para ajudar você a visualizar a lista de todos os projetos de tradução em andamento (juntamente com o idioma de destino) que contêm a referência selecionada.

Para obter mais detalhes, consulte *Traduzir documentos do Editor da Web* no guia Uso dos guias do Adobe Experience Manager.

### Gerar saída em vários formatos no Editor da Web

Agora é possível gerar facilmente a saída dos tópicos ou do mapa DITA no Editor da Web. Você pode configurar várias predefinições de saída, como AEM Site, PDF, HTML5, JSON (um formato de saída headless) e saída personalizada. Use-os para gerar as respectivas saídas. Você pode definir atributos em seus tópicos DITA e, em seguida, usar a predefinição de condição para aplicar uma condição ao publicar a saída. Você também pode usar o recurso de publicação de linha de base para publicar seletivamente uma versão específica do mapa ou tópico DITA.

**Gerenciar predefinições de saída de perfil global e de pasta**

Os Guias do AEM fornecem o recurso para criar e gerenciar predefinições de saída para Perfis globais e de pastas. Em seguida, é possível usar facilmente essas predefinições de saída para gerar saída para todos os mapas relacionados a esse perfil Global ou de Pasta.

<img alt="adicionar predefinição" src="assets/add-global-output-preset.png" width="400">


Essas predefinições globais aparecem sob a tag **Output** de todos os mapas relacionados. Você pode usá-los para gerar a saída para todos os mapas relacionados. É possível selecionar a predefinição como a predefinição de PDF padrão para gerar a saída de PDF. Também é possível **Editar**, **Renomear**, **Duplicar** ou **Excluir** uma predefinição de saída existente do **Opções** menu.

>[!NOTE]
>
>Somente usuários administrativos no nível da pasta podem criar predefinições Globais e de Perfil de Pasta.

### Localizar e substituir o texto no nível do mapa

Agora é possível pesquisar arquivos em um mapa que contenha texto específico. O texto pesquisado é destacado nos arquivos. Você também pode substituir a palavra ou frase pesquisada por outra palavra ou frase dentro dos arquivos. Selecione o **Substituir ocorrência única** ícone para substituir a ocorrência atual e o **Substituir tudo no arquivo** ícone para substituir todas as ocorrências no arquivo selecionado. É possível selecionar **Substituir tudo** ícone para substituir todas as ocorrências do termo pesquisado em todos os arquivos.

<img src="assets/map-find-replace.png" alt="mapa localizar substituir" width="600">


Por padrão, as opções **Fazer check-out do arquivo antes de substituir** e **Criar nova versão após substituir** são selecionados, portanto, um arquivo é submetido a check-out antes da substituição do texto e uma nova versão é criada depois que o texto é substituído. Também é possível pesquisar a string nas referências indiretas no mapa DITA. Por padrão, isso fica desativado para que a pesquisa seja executada somente nas referências diretas.

### Exibição de layout no Editor de mapa


Agora é possível exibir o layout completo de um mapa DITA no Editor de mapas. Quando você abre um mapa para edição, ele abre a exibição de Layout do Editor de Mapas. Nesta exibição, é possível ver a hierarquia de mapas em uma exibição em árvore. Também é possível editar e organizar ou estruturar os tópicos em um mapa.

<img src="assets/layout-view-map.png" alt=" exibição do layout do mapa" width="600">

A exibição de layout contém uma barra de ferramentas separada que ajuda a executar muitas tarefas nos tópicos presentes em um mapa.
Você pode inserir referências de tópico, grupo de tópicos, definições de chave em um mapa. Você pode reorganizar os tópicos presentes em um mapa movendo-os para cima, para baixo, para a esquerda ou para a direita. Você também pode arrastar e soltar os tópicos para movê-los em um mapa. O Editor de mapa também fornece os ícones para bloquear ou desbloquear arquivos, verificar o histórico da versão e fazer um gerenciamento de rótulo de versão.


A exibição de layout também fornece a **Opções de exibição** para mostrar ou ocultar o número de linha, mostrar ou ocultar a caixa de seleção ou mostrar o nome de arquivo ou título dos tópicos em um mapa.
Você também pode exibir os tópicos com base nos filtros condicionais aplicados neles.

Além de organizar tópicos no arquivo de mapa, também é possível adicionar, mover, copiar, colar ou excluir referências usando o **Opções** menu disponível para um elemento na exibição de layout.

<img src="assets/layout-inline-attributes.png" alt=" mapear atributos de layout" width="600">


O painel direito exibe as Propriedades do Conteúdo e as Propriedades do Mapa na exibição de Layout do Editor de Mapas. Agora, também é possível definir as informações de metadados dos tópicos ou do mapa. Você pode definir o Título de navegação, Texto do link, Descrição curta e Palavras-chave para o tópico ou mapa selecionado.

Para obter mais detalhes, consulte *Exibição de layout* no guia Uso dos guias do Adobe Experience Manager.

### Painel Geração rápida

Agora, o AEM Guides fornece o painel Geração rápida, que ajuda a gerar e visualizar rapidamente a saída das predefinições criadas para o mapa DITA.

<img src="assets/quick-generate-map-view.png" alt=" painel de geração rápida" width="600">

No **Geração rápida** é possível ver a lista de todas as predefinições de saída criadas para o mapa DITA. Também é possível visualizar rapidamente a saída gerada para as predefinições. Uma mensagem de sucesso ou falha é exibida na conclusão da geração de saída. Você também pode exibir o log de erros, que contém detalhes do erro que ocorreu no processo de geração.

### Criar uma linha de base dinâmica com base em rótulos

Agora, o AEM Guides fornece o recurso para criar linhas de base dinâmicas com base em rótulos. Se você gerar uma linha de base, baixar uma linha de base ou criar um projeto de tradução usando uma linha de base, os arquivos serão selecionados dinamicamente com base nos rótulos atualizados. Esse recurso é útil, pois você não precisa modificar a linha de base ao atualizar os rótulos.

<img src="assets/dynamic-baseline.png" alt=" linha de base dinâmica" width="400">

### Excluir e duplicar arquivos no painel de repositório

Agora é possível excluir facilmente arquivos (um único arquivo por vez) do **Opções** do arquivo selecionado no painel repositório. Um prompt de confirmação é exibido antes de excluir o arquivo. Se o arquivo não for referenciado a partir de outro arquivo, ele será excluído e uma mensagem de sucesso será exibida.

<img src="assets/options-menu-repo-view-file-level.png" alt="menu de opções de arquivo " width="500">

Você também pode criar uma duplicata ou uma cópia do arquivo selecionado. Por padrão, o arquivo é criado com um sufixo (como filename_1.extension).


### Outras melhorias no Editor da Web

* Nos Guias do AEM, você pode executar algumas operações comuns para imagens e arquivos de mídia usando o menu de contexto. Agora, também é possível localizar a imagem ou mídia selecionada no repositório ou visualizar o arquivo na interface do usuário do Assets.

* O nome do Perfil de pasta atual é exibido como um rótulo para o ícone Preferências do usuário na barra de ferramentas principal. Isso ajuda a identificar o perfil da pasta em que você está trabalhando.

* Quando você abre um mapa na exibição de mapa, o título do mapa atual é exibido no centro da barra de ferramentas principal. Isso é útil para informar aos usuários qual mapa está aberto no momento.

### Remoção de versões selecionadas de arquivos

À medida que você cria e mantém seu conteúdo, muitas versões podem ser criadas para seus arquivos DITA no repositório. Guias do AEM permitem que você remova do repositório versões anteriores dos arquivos DITA e libere espaço em disco.

<img src="assets/preview-purge-report.png" alt="Visualizar relatório de limpeza" width="500">

As Guias do AEM não excluem a primeira versão do arquivo ou uma versão que esteja incluída em uma linha de base, ou tenha um rótulo aplicado a ela. A operação de limpeza nem mesmo exclui arquivos incluídos em uma tradução ou em um fluxo de trabalho de revisão. Você pode escolher o número de versões a serem mantidas e também decidir excluir os arquivos mais antigos que o número definido de dias.

Antes de iniciar a operação de expurgação, você pode visualizar o relatório para ver as versões que serão expurgadas. Você pode decidir iniciar ou cancelar a operação de expurgação.

<img src="assets/download-purge-report.png" alt="Relatório de limpeza de PDownload" width="500">

Quando a operação de expurgação estiver concluída, você poderá verificar o relatório de expurgação para ver os arquivos expurgados.

### Visualizar o título no lugar da UUID no editor de oxigênio

Agora o AEM Guides permite que você escolha **Usar Título no Editor e no Gerenciador de Mapas** em Configurações. Se você selecionar essa opção, o título do arquivo será exibido na guia do arquivo quando aberto no Editor ou no Gerenciador de mapas DITA. Se você não selecionar essa opção, a UUID do arquivo será exibida na guia do arquivo.

### Interface de metadados disponível para predefinições de PDF

É possível definir os metadados na predefinição de saída de um mapa DITA. É possível definir os metadados de Título, Autor, Assunto e Palavras-chave. Esses metadados são mapeados para os metadados nas Propriedades do arquivo do PDF de saída. Esses metadados substituem os definidos no nível de livro. Você pode definir os metadados especificamente em cada predefinição de saída e passá-los para o PDF de saída.

### PDF nativo | PDF com barra de alterações que mostra a diferença entre as versões do documento

Agora você pode criar um PDF que mostra as diferenças no conteúdo entre duas versões usando a barra de alteração. Você pode optar por comparar a versão atual com uma linha de base da versão anterior ou comparar entre as duas versões de linha de base selecionadas.

<img src="assets/pdf-change-version.png" alt="pdf-change-version" width="600">

Uma barra de alteração aparece no PDF para indicar o conteúdo modificado, inserido ou excluído. Você também tem as opções para fazer o seguinte:
* Mostrar o conteúdo inserido em verde e sublinhado
* Mostrar o conteúdo excluído em vermelho e marcado com um tachado

### PDF nativo | Suporte a variáveis para caminho de saída e nome do arquivo PDF

Agora, você também pode usar as variáveis prontas para uso a seguir para definir o Caminho de saída e o Arquivo PDF. Você pode usar uma única variável ou uma combinação de variáveis para definir essas opções:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (Somente para Caminho de saída)
* `${path_after_langfolder}` (Somente para Caminho de saída)

### PDF nativo | Gerar sumário para mapas DITA e reordenar layouts de página

Agora, você também pode gerar o índice em mapas DITA usando uma configuração de PDF avançada do modelo. Você pode optar por ativar ou desativar a exibição dos vários layouts de página e também reordenar sua posição.

### PDF nativo | Adicionar um marcador personalizado na saída do PDF

Agora é possível adicionar um marcador personalizado em um conteúdo específico na saída final do PDF para facilitar a navegação. Isso seria adicionado ao índice criado a partir dos títulos de tópico ou seção no mapa DITA.

### PDF nativo | Aplicar estilo personalizado em entradas de índice e conteúdo de tópico

Guias de AEM fornecem o recurso para aplicar um estilo personalizado nas entradas do índice ou em um tópico específico na saída do PDF. Por exemplo, é possível alterar a cor do texto no índice e no título do tópico. Também é possível aplicar estilos a todo o conteúdo do tópico.




## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

### Criação  

* O painel esquerdo é interrompido ao adicionar uma guia. (11126)
* As alterações no html do Editor da Web causam problemas com `<dl>` e `<dlentry>`. (11024)
* Alguns atributos não estão sendo tratados como condicionais e estão causando problemas. (10895)
* Três níveis ou mais aninhados `<indexterm>` não estão aninhados na exportação de PDF nativa. (10799)
* O conteúdo desaparece no corpo de uma tarefa ao alternar da visualização Autor para Fonte. (10735)
* Comentários de revisão são colocados fora do lugar em uma tarefa de revisão. (10625)
* `<conref>` a nota em uma tag para não é exibida no modo de visualização. (10559)
* Acertar o espaço traseiro no final de um item de lista remove a lista inteira. (10540)
* A tela é exibida em branco no Chrome v106 ao arrastar e soltar qualquer elemento da interface do usuário ( por exemplo, no painel Condições ). (10524)
* O botão Recuo automático está ausente na barra de ferramentas no **Origem** exibição. (10448)
* O primeiro caractere de um item de lista é perdido às vezes quando a lista está sendo criada no editor.( 10447)
* **Desfazer** ou **Refazer** O não está funcionando corretamente em alguns arquivos. (10373)
* Os metadados personalizados não são mantidos na ação de copiar e colar. (10367)
* Ocorre um erro ao fazer uma cópia (ctrl+c) e colar (ctrl+v) de conteúdo. (10304)
* O painel Estrutura de Tópicos não exibe o conteúdo quando alternado do modo Autor para o modo Origem. (10296)
* O Submapa não é criado quando se refere a um mapa principal em Modelos DITA. (10231)
* Problemas de navegação ocorrem no Editor da Web após a atualização 4.0. (10159)
* A opção Desfazer no Editor de XML leva o usuário para a parte superior da página. (10091)
* As propriedades do nó são removidas após a operação de copiar e colar de um ativo. (10053)
* Os arquivos SVG adicionados aos tópicos DITA não são exibidos no modo de visualização do editor. (10010)
* Os resultados da pesquisa para localizar e substituir no Editor da Web não são legíveis no modo Escuro. (9978)
* Não existe carregador ao criar um mapa a partir do modelo de mapa. (9891)
* O Conref no modelo de tópico não funciona e a ID de hash copiada não é atualizada na cópia de conteúdo. (9890)
* Nenhuma opção é exibida para procurar os tópicos ou mapear modelo dentro das subpastas do tópico ou da pasta do mapa. (9889)
* Não há opção para criar um novo modelo nas subpastas de tópicos ou mapas. (9888)
* O Editor de XML não atualiza as imagens nos tópicos. (9500)
* O mimeType é codificado para criação e atualização de ativos DITA. (8979)
* Um hífen normal é inserido ao selecionar Hífen não-separável no **Inserir caractere especial** diálogo. (8919)
* O nome do criador de versão no Histórico de versão é &quot;fmdita-serviceuser&quot; para os arquivos carregados pela interface do usuário do Assets. (8910)
* A opção Editar não funciona para imagens ao trabalhar na exibição Coluna da interface do usuário do Assets. (8758)
* O tópico DITA não é atualizado automaticamente com alterações feitas em **Propriedades** página. (8745)
* Ao mover elementos dentro do tópico no Editor da Web, as IDs atribuídas nos elementos são substituídas pelas IDs atribuídas automaticamente. (7895)

### Gerenciamento

* Copiar um ativo de mapa DITA (da interface do usuário do Assets ) causa linhas de base incorretas no ativo copiado. (11218)
* A mensagem de aviso não é exibida no upload de um arquivo maior do que o limite permitido no AEM (2 GB por padrão). (10817)
* Editor da Web - Linha de base | O comportamento da coluna Mais recente é diferente no novo painel da linha de base no Editor da Web. (10808)
* Tradução | A tarefa de tradução não é iniciada devido a /libs/fmdita/i18n/ja.json inválido. (10543)
* Tradução | Ocorre um erro em um projeto de tradução de escopo criado a partir do painel de tradução (Tradução humana). (10526)
* Tradução | O pós-processamento está bloqueado para toda a pasta de idioma cujos ativos estão presentes em um projeto de tradução ativo. (10332)
* Tradução | Os metadados e as tags não estão sendo propagados para as cópias traduzidas. (4696)
* Vários pop-ups são exibidos para qualquer ativo se a versão for alterada e salva no editor de linha de base. (10399)
* O vazamento da sessão ocorre em com.day.cq.search.impl.builder.QueryBuilderImpl.createResourceResolver(QueryBuilderImpl.java:210). (10279)
* O arquivo de vídeo está ausente na linha de base se a pasta pai contiver espaço no nome. (10031)

### Publicação

* A regeneração de tópico não está funcionando para alguns cenários. (10635)
* A publicação de PDF falha ao gerar a saída para uma predefinição duplicada (de uma predefinição existente). (10584)
* O botão Visualizar log não funciona caso a geração de PDF falhe para uma predefinição. (10576)
* O Publishlistener não exibe os dados solicitados em logs de informações e também contém alguns logs de lixo eletrônico.( 10567)
* PDF nativo | Falha na geração de PDF com uma exceção de Null Pointer. (10950)
* PDF nativo | conkeyref não está sendo resolvido na saída gerada. (10564)
* PDF nativo | Problemas ocorrem com os metadados de um mapa que precisa ser referido na saída do PDF.( 10556)
* PDF nativo | Problemas ao girar o cabeçalho da tabela. (10555)
* PDF nativo | Ocorrem problemas ao remover tópicos com função de processamento=&#39;resource-only&#39;. (10554)
* PDF nativo | Teclas vazias são exibidas na saída do PDF. (10553)
* PDF nativo | Aninhado `<indexterm>` não estão aninhados na exportação de PDF nativa. (10521)
* PDF nativo | O PDF nativo usa o estilo em linha em vez do nome da classe para as tags geradas. (10498)
* PDF nativo | Tópicos aninhados nos apêndices são todos transformados em h1 no HTML temporário.( 10454)
* PDF nativo | Não é possível ocultar tópicos do assunto principal do sumário. (10355)
* PDF nativo | Atributo de quadro de tabela não propagado para o HTML temporário (como classe). (10353)
* PDF nativo | Arquivos de HTML temporários adicionam as classes colsep e rowsep a <td> e <th> mesmo que o valor seja 0 no DITA de origem. (10352)
* PDF nativo | Reiniciar os números de página no layout do capítulo inicia aleatoriamente a numeração a partir do final do capítulo anterior. (10154)
* PDF nativo | As referências principais de keydefs com imagem ou links externos não estão sendo resolvidas. (10063)
* PDF nativo | O apêndice está sendo exibido como um capítulo no PDF gerado. (9829)
* A guia Modelo no editor xml não está sendo exibida para os administradores de Perfil de pasta. (10266)
* Falha na publicação da linha de base para o PDF gerado usando o FrameMaker Publishing Server 2020. (10551)
* Ocorre um erro de aplicativo ao clicar no botão Editar após marcar todas as predefinições por meio da caixa de seleção Predefinições de saída na janela pop-up Geração rápida. (10388)
* Se a guia Saída no Editor da Web estiver tendo mais predefinições, a seção Predefinições não será rolável verticalmente e não exibirá todas as predefinições disponíveis. (9787)
* Não é possível excluir predefinições do Fluxo de trabalho de saída durante a publicação pelo Editor. (9100)
* O link par é renderizado como texto normal em vez de um link na página gerada. (7774)

### Problema conhecido

o Adobe identificou o seguinte problema conhecido para a versão AEM Guides 4.2:

* Os usuários podem executar operações de revisão mesmo após a conclusão da tarefa de revisão.
