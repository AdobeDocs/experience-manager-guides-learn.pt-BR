---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de maio de 2022
description: Versão de maio dos Guias do Adobe Experience Manager as a Cloud Service
exl-id: 7928a300-5ec9-492c-b9be-02b6f87638c6
source-git-commit: 0f5c1cabdbda9fa2606f67faedbf9a38ca1ec0aa
workflow-type: tm+mt
source-wordcount: '1874'
ht-degree: 4%

---

# Versão de maio dos Guias do Adobe Experience Manager as a Cloud Service

## Atualize para a versão de maio

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação do Cloud Services configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.5.144.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de maio AEM Guias as a Cloud Service.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software compatíveis com AEM Guias as a Cloud Service versão de maio de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac |
| --- | --- | --- |
| 2022.5.0 | 2.6.9 | 2.6.9 |
|  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service oferecem muitos aprimoramentos e novos recursos na versão de maio:

### Editor da Web aprimorado

* **Criar mapas com base em modelos personalizados**

Agora você tem o recurso avançado para criar modelos de mapa personalizados. Você pode usá-los para criar mapas DITA junto com os modelos de tópico e modelos de mapa referenciados no modelo de mapa.

![modelos](assets/dita-templates.png)

Também é possível consultar outros modelos de mapa e modelos de tópico do modelo de mapa personalizado. Os modelos de mapa referenciados podem se referir a vários modelos de mapa, modelos de tópico, tópicos, mapas, imagens, vídeos e outros ativos.

![criar modelos ditos](assets/create-dita-template.png)

O modelo de mapa personalizado pode ajudar você a replicar facilmente os modelos de mapa e toda a estrutura de pasta referenciada. Esses modelos personalizados são especialmente úteis para criar e recriar vários mapas que têm estruturas e referências recursivas.

* O **Inserir palavra-chave** foi aprimorado. Agora é possível encontrar uma Palavra-chave mais facilmente a ser inserida, pois as palavras-chave estão listadas em ordem alfabética. Também é possível pesquisar palavras-chave digitando uma sequência de caracteres de pesquisa na caixa Pesquisar.

![inserir palavra-chave](assets/insert-keyword.png)

* Agora, os arquivos de Exibição do Repositório são carregados em lotes. 75 arquivos são carregados de cada vez. Esse carregamento em lote é eficiente e você pode acessar os arquivos mais rápido em comparação ao carregamento de todos os arquivos existentes em uma pasta.

![carregar mais arquivos](assets/load-more-files.png)

* É possível renderizar imagens SVG que incluam dados incorporados ou links em todas as telas do editor XML, incluindo, entre outras, a Visualização e a Visualização do autor.

* O XSD/DTD padrão pode ser atualizado para a versão mais recente

### Processo de tradução aprimorado

* **Capacidade de criar um projeto de tradução de escopo**
Se você precisar criar apenas o escopo de um projeto a ser traduzido, poderá selecionar 
**Criar um novo projeto de tradução de escopo**. Isso não enviará as cópias para tradução e o status de tradução original dos arquivos será mantido.

![projeto de tradução de escopo](assets/scoping-translation-project.png)

* Se você rejeitar a tradução de um ou mais tópicos em um trabalho de tradução, o status de tradução Em andamento de todos os tópicos rejeitados será revertido para o status original.

* O **Languages** exibe as pastas de idioma junto com seus códigos de idioma. Por exemplo, francês (fr) e alemão (de).

* O recurso de tradução agora também suporta o código de idioma que inclui país e idioma. Por exemplo, `fr-fr`, `en-us`.

![idioma de tradução](assets/translation-languages.png)

* Ao carregar um mapa DITA que esteja fora da pasta de idioma, nenhuma exceção é registrada no back-end.

Para obter mais detalhes sobre a tradução, consulte *Traduzir documentos do Editor da Web* em Usar guias do Adobe Experience Manager as a Cloud Service.


### Publicação aprimorada

* Você também pode acessar a variável **Publicar painel** na guia Saídas enquanto você gera a saída do painel de mapa. Uma lista de todas as tarefas de publicação ativas está disponível no Painel de publicação.

![saídas em fila](assets/queued-output.png)

* No painel de mapa, você pode selecionar vários arquivos DITAVAL para gerar conteúdo condicional. Você pode manter a ordem dos arquivos adicionando ou excluindo arquivos. Você também pode passar o mouse sobre o nome do arquivo para ver o caminho no repositório AEM onde o arquivo está armazenado.

* **Recurso obsoleto**
AEM as a Cloud Service não oferece mais suporte à geração do formato de saída DITA para documentos do FrameMaker. Essa opção do DITA também foi removida das Predefinições de saída do painel do Mapa.

### Publicação aprimorada baseada em artigos

O Editor XML fornece a capacidade de mapear mais de uma categoria de produto a um artigo ao publicar em um perfil do Salesforce.

### Outras melhorias de recursos

* O modo de Visualização também é compatível `deliveryTarget` atributo de processamento condicional no DITA. Está disponível como uma opção no filtro suspenso junto com **público**, **plataforma**, **produto**, props, **otherprops**.
* Foi fornecida uma opção para sincronizar com força entre o servidor AEM no Oxygen e o sistema local.

## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* No painel de revisão do Editor da Web, o usuário não pode responder aos comentários de revisão. (9667)
* O aplicativo fica em branco ao clicar em uma pasta em branco depois de atualizá-la por meio do menu Opções. (9639)
* Uma nova versão está sendo criada ao **Salvar e fechar** o arquivo de check-in. (9638)
* O botão Fechar não é exibido quando **Salvar como nova versão** estiver ativada. (9637)
* O PDF correto não publicado se for publicado pela primeira vez por meio de um PDF separado para cada capítulo e, em seguida, um único arquivo PDF (Criar arquivos PDF separados está desmarcado). (9632)
* O painel de mapa está gerando um problema de metadados para usuários não administradores. (9620)
* Depois que uma linha de base é criada, o status é definido para falhar na interface (a chamada de status get está falhando) se o servidor estiver tendo mais de 10000 arquivos. (9608)
* Armazenar dados grandes nas propriedades resulta em um erro de publicação, pois o fluxo de trabalho de publicação dividido falha. (9586)
* O estado dos Filtros de atributos condicionais não é preservado ao alternar entre a Visualização para a Origem e novamente o modo Visualização. (9553)
* O nome do Bookmap fica em branco na exibição Repositório, caso nenhum nome seja fornecido por meio do `mainbooktitle` . (9538)
* O erro HTTP 400 ocorre ao abrir um arquivo carregado com o Oxygen. (9535)
* As Predefinições de um mapa aberto anteriormente permanecem visíveis na guia Saída ao abrir um mapa sem predefinições definidas. (9523)
* A funcionalidade de pesquisa para Tags e Atributos não está funcionando no painel Contorno. (9506)
* A Coleção recém-criada não fica visível até que o navegador seja atualizado. (9505)
* Os rótulos de Atributos condicionais (não os valores) aparecem no modo de origem ao adicionar todas as condições por meio da opção &quot;Adicionar todas as props&quot;. (9501)
* O check-out dos arquivos é feito automaticamente ao reverter para qualquer versão. (9482)
* As diferenças incorretas no carimbo de data e hora são exibidas na interface do usuário do Assets ao reverter uma versão de arquivo. (9480)
* Vários itens dos resultados da pesquisa são adicionados ao inserir itens no elemento topicref do mapa DITA. (9474)
* Se a configuração **Criar nova versão para o arquivo carregado** estiver ATIVADO, uma nova versão será criada ao reverter e salvar em qualquer nó congelado. (9473)
* O texto de exibição de Referência da chave e Referência da chave de conteúdo não é mantido ao alterar o URL do link, se o texto de exibição não for adicionado ao definir a referência da chave. (9458)
* No Histórico da Versão, o número da versão e o rótulo não são exibidos para a versão atual. (9446)
* O editor congela quando determinados arquivos de conteúdo são abertos no editor. (9443)
* A pesquisa no painel Repositório e na caixa de diálogo de navegação topicref congela a tela quando o conteúdo é grande. (9432)
* Os metadados passados para AEM saída do site não respeitam a linha de base do conteúdo. (9416)
* O Oxigênio verifica uma versão incorreta de um tópico após a reversão de uma versão em AEM. (9411)
* Falha na linha de base desativa a edição na guia Predefinição do painel de mapa. (9403)
* O erro sempre é registrado na criação do novo conteúdo. (9388)
* Os ativos DITA recém-criados são sempre verificados por outro usuário. (9387)
* O elemento Renomear não está funcionando corretamente ao converter topicref em glossref. (9380)
* O Rótulo da Versão não vem como lista suspensa em **Salvar como nova versão** caixa de diálogo. (9379)
* As condições não estão sendo aplicadas ao alternar entre diferentes versões do **Mostrar Diff** lista suspensa. (9366)
* Vários problemas ocorrem ao usar os filtros de Visualização. (9365)
* Não é possível inserir ativos não-DITA e DITAVAL em topicref. (9363)
* A tradução aprovada não é integrada ao idioma de destino quando o código de idioma de destino contém cinco caracteres como `fr_ca`. (9357)
* Não é possível pesquisar arquivos usando **Localizar arquivos na pasta** do **Mais opções** e o aplicativo fica sem resposta. (9337)
* A caixa de diálogo Procurar trava se houver um grande número de chaves. (9332)
* Arquivos DITAVAL não funcionam durante a publicação baseada em artigo. (9330)
* A ordem das notas de rodapé está incorreta na saída do Site de AEM. (9327)
* A pesquisa não é executada automaticamente quando o caminho de seleção é alterado. (9323)
* Quando a tradução é feita, uma versão adicional é criada para o ativo traduzido. (9310)
* Não é possível excluir os usuários do Administrador no perfil da pasta. (9306)
* O mapa raiz atualizado da Referência da chave de conteúdo não é definido até que a página seja atualizada. (9302)
* A autenticação da Web não está funcionando no Oxygen. (9296)
* Os links da Web com caracteres codificados não estão funcionando corretamente. (9227)
* O arquivo não é verificado quando aberto no Oxigênio. (9217)
* A atualização dos arquivos com check-out não está funcionando no logon com autenticação da Web no Oxygen. (9179)
* As guias Tradução e Linha de base ficam visíveis por algum tempo no painel Mapa. (9146)
* Problemas de experiência ou recursos ocorrem ao recarregar o Perfil da pasta. (9103)
* A exclusão do editor de layout de página não o fecha do painel central na exibição Autor. (9087)
* O erro de validação ocorre no Editor da Web ao remover uma imagem e depois salvar a nova versão do documento. (8985)
* Não é possível exibir todos os `glossrefs` no painel Glossário (conteúdo específico). (8886)
* `xref` sem texto não é exibido na saída de publicação baseada em artigo. (8764)
* As referências são quebradas em imagens móveis ou arquivos de multimídia que têm um espaço nos nomes de arquivos. (8624)
* Quebra de referências na escolha `Select All` e mover os arquivos multimídia ou o conteúdo DITA para outra pasta. (8622)
* Trabalhos de saída com status como &quot;Aguardando&quot; ou &quot;Executando&quot; não são limpos no Painel de publicação.  (8569)
* O recurso de limpeza de saída falha se houver um grande número de nós do histórico de saída restantes. (8568)
* O pacote DITA Add on impede a detecção de ativos duplicados do DAM. (8417)
* Botão Criar tarefa de revisão ativado para arquivos não-DITA. (8401)
* A caixa de diálogo Inserir referências é aberta ao adicionar subjetivo a um mapa usando a interface do usuário. (8212)
* Espaço inesperado encontrado em cada espaço em branco `entry` elemento quando o atributo outputclass é adicionado a `tgroup` elemento. (7532)
* O painel Repositório não exibe ícones de bloqueio de arquivo com check-in ou com check-out assim que a ação é concluída. (5817)
* O ícone de cadeado é exibido na visualização do repositório mesmo quando o arquivo é feito com check-in no editor.  (5756)
* Os sites estão ausentes AEM predefinições na guia Saída. (9567)
* O Editor XML trava ao tentar editar alguns arquivos DITA. (9537)
* Realizar uma pesquisa no Editor XML faz com que a página fique congelada. (9452)
* O mapa de download com linha de base não funcionará se o conteúdo for movido para outra pasta. (9331)
* O recarregamento falha no Oxygen quando o(s) arquivo(s) já existe(m) no AEM no mesmo local. (9328)
* A posição do realce está incorreta na exibição Lado a Lado. (9305)
* Após o check-in de um documento do Oxygen para o AEM, o conteúdo japonês no documento é substituído por pontos de interrogação (???). (9276)
* Falha no upload de arquivos do Oxygen para AEM. (9157)
* A notificação por email não está sendo enviada quando uma tarefa de revisão está sendo atribuída novamente na Caixa de entrada. (8376)

## Problemas conhecidos

A página em branco é exibida intermitentemente ao abrir o editor.
