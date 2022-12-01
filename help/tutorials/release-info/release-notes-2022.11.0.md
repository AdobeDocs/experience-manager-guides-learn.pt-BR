---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de novembro de 2022
description: Versão mais recente dos Guias do Adobe Experience Manager as a Cloud Service
source-git-commit: 549417d6a45508d0afe98574499f1694ae32e708
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 2%

---

# Versão mais recente dos Guias do Adobe Experience Manager as a Cloud Service

## Atualizar para a versão mais recente

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.11.198.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão mais recente dos Guias AEM as a Cloud Service.

## Etapas para indexar o conteúdo existente (somente se você estiver em uma versão anterior à versão de setembro AEM Guias as a Cloud Service)

Execute as seguintes etapas para indexar o conteúdo existente e use o novo texto localizar e substituir no nível de mapa:

* Execute uma solicitação de POST para o servidor (com autenticação correta) - `http://<server:port>/bin/guides/map-find/indexin`.
(Opcional: Você pode passar caminhos específicos dos mapas para indexá-los, por padrão, todos os mapas serão indexados || Exemplo : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com ID do trabalho para o mesmo ponto final - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por exemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Quando a tarefa for concluída, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados dos logs do servidor.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software compatíveis com AEM Guias as a Cloud Service versão de novembro de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac | Editar no Windows Oxygen | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.11.0 | 2.7.13 | 2.7.13 | 2.3 | 2,3 |
|  |  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service fornecem aprimoramentos e novos recursos na versão mais recente:


### Excluir arquivos do painel de repositório

Agora, é possível excluir facilmente os arquivos (um único arquivo de cada vez) do **Opções** do arquivo selecionado no painel de repositório.
<img src="assets/repository-delete-file.png" alt="Excluir do repositório" width="500">

Um prompt de confirmação é exibido antes de excluir o arquivo. Se o arquivo não for referenciado de nenhum outro arquivo, ele será excluído e uma mensagem de sucesso será exibida.

Se o arquivo selecionado estiver com check-out, você não poderá excluí-lo e uma mensagem de erro será exibida. Se o arquivo selecionado for adicionado a uma coleção de favoritos ou for referenciado a partir de qualquer outro arquivo, o guia AEM verificará sua confirmação e dará a você a opção de excluí-lo com força. Se você excluir um tópico referenciado e tiver aberto o arquivo que contém referências para edição, ele mostrará o link quebrado para o arquivo referenciado.

**Observação**: Também é possível excluir o arquivo selecionado usando a tecla Delete do teclado.


### Limpeza de versões selecionadas de arquivos

À medida que você cria e mantém o conteúdo, muitas versões podem ser criadas para os arquivos DITA no repositório. AEM Guias permitem limpar versões mais antigas dos arquivos DITA do repositório e liberar espaço em disco.

<img src="assets/preview-purge-report.png" alt="Visualizar relatório de limpeza" width="500">


AEM Guias não exclui a primeira versão do arquivo ou uma versão que esteja incluída em uma linha de base, ou tenha um rótulo aplicado a ele. A operação de limpeza nem exclui arquivos incluídos em uma tradução ou em um fluxo de trabalho de revisão. Você pode escolher o número de versões a serem mantidas e também decidir excluir os arquivos que são mais antigos do que o número definido de dias.

Antes de iniciar a operação de limpeza, é possível visualizar o relatório para ver as versões que serão limpas. Em seguida, você pode decidir iniciar ou cancelar a operação de limpeza.

<img src="assets/download-purge-report.png" alt="Relatório de limpeza de PDownload" width="500">

Quando a operação de limpeza estiver concluída, você poderá verificar o relatório de limpeza para ver os arquivos limpos.

### Gerenciar predefinições de saída do Perfil global e de pasta

Os Guias AEM fornecem o recurso para criar e gerenciar predefinições de saída para os Perfis Global e de Pasta. Em seguida, você pode usar facilmente essas predefinições de saída para gerar saída para todos os mapas relacionados a esse perfil Global ou Folder.

<img src="assets/add-global-output-preset.png" alt="Adicionar perfil global" width="400">

**Observação** Somente usuários administrativos de nível de pasta podem criar predefinições de Perfil Global e de Pasta.

Essas predefinições globais aparecem sob a **Saída** de todos os mapas relacionados. Você pode usá-los para gerar a saída para todos os mapas relacionados. Você pode selecionar a predefinição como PDF padrão para gerar a saída do PDF. Você também pode **Editar**, **Renomear**, **Duplicar** ou **Excluir** uma predefinição de saída existente do **Opções** menu.

### Coluna Rótulo da versão adicionada ao painel de tradução

No painel de tradução, você também pode ver a coluna Rótulo da versão . Isso exibe o Rótulo da versão selecionada do arquivo de origem. Isso pode ajudá-lo a selecionar todos os arquivos com um rótulo específico e traduzi-los de uma só vez.

<img src="assets/send-translation.png" alt="enviar para tradução" width="600">


## Aprimoramentos de publicação de PDF nativo

### PDF com barra de alteração mostrando a diferença entre as versões do documento

Agora é possível criar uma PDF que mostre as diferenças no conteúdo entre duas versões usando a barra de alterações. Você pode optar por comparar a versão atual com uma linha de base da versão anterior ou comparar entre as duas versões de linha de base selecionadas.

<img src="assets/pdf-change-version.png" alt="spdf-change-version" width="600">

Uma barra de alteração é exibida no PDF para indicar o conteúdo modificado, inserido ou excluído. Você também tem as opções para fazer o seguinte:
* Mostrar o conteúdo inserido em cor verde e sublinhado
* Mostrar o conteúdo excluído em cor vermelha e marcado com um tachado

### Suporte a variáveis para Caminho de saída e Nome do arquivo PDF

Agora você também pode usar as seguintes variáveis prontas para uso para definir o Caminho de saída e o Arquivo PDF. Você pode usar uma única ou uma combinação de variáveis para definir estas opções:
* `${map_filename}`
* `${map_title}`
* `${preset_name}`
* `${language_code}`
* `${map_parentpath}` (Somente para Caminho de Saída)
* `${path_after_langfolder}` (Somente para Caminho de Saída)


### Gerar Índice para mapas DITA e reorganizar layouts de página

Agora você também pode gerar o TOC em mapas DITA usando uma configuração de PDF avançada do modelo. Você pode optar por ativar ou desativar a exibição dos vários layouts de página e também reorganizar sua posição.

## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* PDF nativo | Uma nota de rodapé no cabeçalho da tabela leva a um texto de nota de rodapé em negrito e alinhado no centro no rodapé dentro da saída do PDF. (10610)
* PDF nativo | `conkeyref` não é resolvido na saída do PDF gerado. (10564)
* PDF nativo | Problemas ao acessar metadados de um mapa na saída do PDF. (10556)
* PDF nativo | O estilo em linha é usado para gerar tags em vez do nome da classe.  (10498)
* O Editor da Web carrega uma página em branco intermitentemente. (10678)
* A publicação do PDF falha se criarmos uma predefinição duplicando uma predefinição existente. (10584)
* **Exibir registro** não está funcionando quando a geração de PDF falha em uma predefinição. (10576)
* Observação dentro de uma tag para , que é conref, não está sendo exibida na visualização. (10559)
* A ocorrência do backspace no final de um item de lista remove toda a lista. (10540)
* Ao usar um PDF nativo, exporte o aninhado `<indexterm>` não estão aninhados no índice. (10521)
* Ao usar a publicação da linha de base errada `cq:tags` são selecionadas (extraídas da cópia de trabalho atual em vez da cópia da versão). (10494)
* **Recuo automático** na barra de ferramentas está ausente na Visualização de Origem. (10448)
* O primeiro caractere de um item de lista é perdido enquanto a lista está sendo criada no editor. (10447)
* Vários pop-ups serão exibidos se qualquer versão do ativo DITA for alterada e salva na janela de edição da linha de base. (10399)
* Ocorre um erro de aplicativo ao clicar **Editar** depois de selecionar todas as predefinições de Saída no painel Geração rápida . (10388)
* Os metadados personalizados para o tópico DITA não são retidos quando uma ação de copiar e colar é executada da interface do usuário do Assets. (10367)
* O processamento de postagens é bloqueado para a pasta de idioma inteira cujos ativos estão presentes em um projeto de tradução ativo. (10332)
* A guia Modelo no Editor XML não está visível para os administradores do perfil da pasta. (10266)
* Problemas de navegação ocorrem no Editor da Web após a atualização 4.0. (10159)
* O primeiro caractere é quebrado no idioma coreano durante a criação no Editor da Web. (10049)
* Os arquivos SVG não estão sendo exibidos no modo de Visualização. (10010)
* Se a guia Saída do Editor contiver mais predefinições, a seção predefinições não poderá ser rolada e todas as predefinições não serão exibidas. (9787)
* **Editar** e **Anotar** as opções para uma imagem não estão funcionando corretamente na exibição de coluna. (8758)
* O link de par não é resolvido e é exibido como um texto normal na saída gerada. (7774)
