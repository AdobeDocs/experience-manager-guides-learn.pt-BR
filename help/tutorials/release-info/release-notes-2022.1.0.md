---
title: Notas de versão para [!DNL AEM Guides], versão de janeiro de 2022
description: Versão de janeiro de [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: b2da77fa-f17c-440b-be59-acaafcd9a57c
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '2429'
ht-degree: 3%

---

# Versão de janeiro de [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Atualize para a versão de janeiro

Atualize seu [!DNL Adobe Experience Manager Guides] as a Cloud Service (mais tarde conhecido como [!DNL AEM Guides] as a Cloud Service) ao executar as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação do Cloud Services configurada no pipeline correspondente ao ambiente que você deseja atualizar.
1. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.1.78.
1. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de janeiro de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software suportados por [!DNL AEM Guides] Versão as a Cloud Service de janeiro de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |


### Conector de oxigênio

| [!DNL AEM Guides] Versão da nuvem | Janelas do conector de oxigênio | Conector de oxigênio Mac | Editar no Windows Oxygen | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.1.0 | 2.4.0 | 2.4.0 | 2.2 | 2.2 |
|  |  |  |  |  |


## Novos recursos e melhorias

### Publicação baseada em artigo

Com a versão de janeiro, introduzimos um recurso de publicação baseado em artigos integrado ao Editor da Web. Você pode usar o recurso de publicação baseado em artigos para gerar de forma incremental a saída de um ou mais tópicos ou publicar seu conteúdo em uma plataforma de base de conhecimento.

Esse recurso permite que os usuários criem o mapa DITA de forma aditiva e publiquem tópicos como e quando estiverem prontos. Depois de publicar seu mapa, use o recurso de publicação baseado em artigos para obter a publicação incremental somente para os artigos atualizados.

![Publicação baseada em artigo](assets/article-based-publishing.png)

Além do AEM, você pode usar esse recurso exclusivo para publicar seus artigos em qualquer portal da base de conhecimento, como o Salesforce. Esse recurso também vem com um modelo de conteúdo OOTB, criado sobre AEM componentes principais, que permite criar um repositório baseado em conhecimento do conteúdo técnico. O que há de melhor neste modelo é que ele é totalmente personalizável para atender aos seus requisitos organizacionais e também pode suportar casos de uso como portais da intranet corporativa.
Também é possível filtrar os artigos com base no estado do documento e no tempo de modificação.

Essa publicação de artigos em movimento não somente oferece controle total sobre a publicação de conteúdo, como também reduz o tempo geral para publicar seu conteúdo atualizado.
À medida que você publica seus artigos usando esse modelo, ele também pode transmitir os metadados para suas páginas publicadas.
Para obter mais detalhes, consulte *Publicação baseada em artigo no Editor da Web* no Guia do usuário.

### Editor da Web aprimorado

Há muitas melhorias e novos recursos que são introduzidos no Editor da Web:

* O suporte para o esquema de assunto também foi adicionado no Editor da Web. Agora é possível criar e usar o esquema de assunto usando o painel Esquema de assunto . Com a adição do esquema de assunto, agora você pode usar metadados corporativos e taxonomia próprios.

![Regime de auxílios](assets/subject-scheme-panel.png)

* Uma nova ferramenta de ponto de acesso de glossário foi introduzida nesta versão para gerenciar glossários em massa. Com essa ferramenta, você pode converter rapidamente o texto em glossário e glossário em termos em massa para um mapa selecionado ou abrir tópicos.

![Ponto de conexão do glossário](assets/glossary-hotspot-tool.png)

* Adição da funcionalidade de atualização no painel Conteúdo reutilizável , que permite que você atualize rapidamente o conteúdo reutilizável em arquivos de referência.
* O novo indicador de cópia de trabalho mostra se o arquivo atual (cópia de trabalho) está sincronizado com a versão salva ou não.

![Indicador de versão](assets/version-update-indicator.png)

* O filtro de pesquisa no painel Repositório e na caixa de diálogo de navegação de arquivos foi aprimorado para fornecer mais opções de filtragem, que podem ser personalizadas.

![Pesquisar filtros no repositório](assets/repository-filter-search.png)

* Agora é possível fazer upload de arquivos .docx no Editor da Web.

### Autor com FrameMaker

Agora você pode criar e publicar seus documentos no FrameMaker. O FrameMaker é enviado com um conector pronto para uso para o Adobe Experience Manager. No FrameMaker, você obtém uma interface fácil de usar que permite manter versões de seus documentos em um ambiente distribuído e colaborativo.

Após criar o conteúdo, o FrameMaker permitirá que você publique seus documentos em diferentes formatos: PDF, HTML5, EPUB e DITA. Você também pode executar várias operações de gerenciamento de arquivos, como check-out, check-out com dependentes, check-in, atualização e assim por diante.
Para criar com o FrameMaker em [!DNL AEM Guides] Uso as a Cloud Service do FrameMaker versão 2020.4 e superior.

### Novo painel de tradução

Um novo painel de tradução foi introduzido no Editor da Web com os seguintes recursos:

* Classificação, pesquisa e filtragem da lista de tópicos.
* Filtrar o conteúdo por tipo de referência - referências diretas ou indiretas.
* Navegação fácil para localizar um projeto existente ao iniciar uma solicitação de tradução.
* Introdução de um mecanismo de tradução em vários idiomas para evitar a criação de vários projetos para cada idioma quando a solicitação de tradução é iniciada para mais de um idioma.
* Introdução de uma configuração para ocultar a guia de tradução no painel do mapa. Por padrão, ele fica visível. Você pode optar por traduzir o conteúdo usando o painel de mapa ou o Editor da Web.

![Painel de tradução](assets/translation-from-web-editor.png)

### Publicação aprimorada

* Agora, os autores podem enviar metadados em nível de mapa e tópico para a publicação de DITA-OT. Isso é útil quando modelos PDF personalizados são projetados para usar propriedades de metadados de arquivo, como tags, autor, estado do documento e muito mais.

![Metadados DITA-OT](assets/custom-meta-data-output-preset.png)

* Uma nova configuração foi adicionada para permitir que os usuários mantenham ou excluam as versões dos tópicos que estão sendo excluídos quando **Excluir e criar** é usada na geração de saída AEM Site.

### Manuseio de arquivo aprimorado

As seguintes melhorias podem ser vistas ao trabalhar com arquivos no AEM Assets:
* Uma nova experiência de upload de arquivo e um novo diálogo para escolher uma estratégia de resolução de conflitos foram introduzidos.

![Conflito de upload de arquivo](assets/file-upload-name-conflict.png)

* Capacidade de criar uma nova versão do arquivo carregado com uma capacidade de impedir a substituição de um arquivo com check-out.
* Agora é possível visualizar imagens diretamente da exibição Histórico de versão. Além disso, para arquivos DITA e não-DITA, o Histórico de versões mostra as informações da versão atual separadamente.

![Miniatura do histórico de versões](assets/version-history-preview-image.png)

* Sempre que o usuário cria um arquivo DITA, o nome de arquivo padrão aparece em uma pequena caixa para estar em conformidade com o cenário de criação de pasta Native AEM.

### Novo recurso de exportação de relatório

Os relatórios são muito úteis para identificar a integridade do seu conteúdo. [!DNL AEM Guides] as a Cloud Service fornece vários relatórios para assumir o controle do conteúdo. Agora, é possível não apenas visualizar os relatórios, mas também exportar os dados do relatório em um arquivo CSV para exibir e compartilhar com a equipe maior. Os dados dos relatórios podem fornecer um rápido resumo de qualquer link quebrado ou imagem ausente.

![Exportação de relatório](assets/export-report.png)

### Melhoria na experiência de atualização do DAM de oxigênio

Quando você atualiza arquivos de AEM Server no Oxygen, uma mensagem de aviso é exibida se você tiver arquivos não salvos em sua sessão atual do Oxygen. Você pode optar por cancelar a operação de atualização para salvar arquivos não salvos. Sem esse recurso, os usuários perdiam informações não salvas em seus documentos.


### Outras melhorias de recursos

* Agora você pode criar um novo **Projeto Dita** sob o **/apps/projects/templates** caminho.
* Agora baixe o padrão **ui_config.json** dos perfis da sua pasta. Isso pode ser usado para mesclar alterações personalizadas do **ui_config.json** durante a atualização.
* Você não precisa limpar o cache do navegador mesmo quando novas versões de arquivos JS estão presentes.

## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

### Editor da Web

* Conrefs aparecem em vermelho mesmo quando não estão quebrados. (8239)
* O valor do atributo condicional não é preenchido automaticamente quando Adicionar todas as propriedades está selecionado no editor DISAVAL. (8234)
* Os autores não podem inserir uma imagem em um tópico usando o caminho relativo. (8112)
* Revise a página de tarefa não mostrando os arquivos multimídia se houver espaços no nome do arquivo. (8111)
* Ph conref adicionado na célula da tabela é exibido em cor vermelha. (8083)
* Os links na tarefa de revisão não serão atualizados quando os arquivos sob revisão forem movidos. (8080)
* O Editor da Web não renderiza corretamente as imagens que têm a propriedade de dimensionamento definida como 75% ou superior. (8073)
* Imagens GIF são renderizadas como imagens estáticas no Editor da Web. (8024)
* Um conkeyref em um elemento de observação não é exibido na visualização do Editor da Web ou na saída. (8006)
* xref para um elemento que é um conref não é resolvido no editor. (7933)
* O título com chave não é renderizado corretamente na visualização do editor e no painel Repositório. (7909)
* Os trechos com caracteres especiais não são armazenados corretamente. (7908)
* Salvar um tópico após a formatação de equações de MathML resulta em um erro. (7954)
* o keydef having (tm) não é renderizado corretamente no editor e a saída do site AEM continha símbolos TM duplicados. (7859)
* Arrastar e soltar um trecho não funciona de acordo com os DTDs. (7758)
* O HTML está ignorando dimensões personalizadas definidas para gráficos. (7718)
* o atributo conrefend não é atualizado quando o arquivo de origem é movido. (7698)
* Trabalhar com documentos do tipo Tópico de referência leva a vários problemas da interface do usuário. (7656)
* Os arquivos DITAVAL não são exibidos quando o autor adiciona ditavalref em um mapa. (7594)
* Espaço inesperado encontrado em cada espaço em branco `<entry>` elemento quando o atributo outputclass é adicionado a `<tgroup>` elemento. (7532)
* O botão Origem não funciona para tópicos abertos pelo painel de mapa. (7465)
* A impressão parcial insere linhas e espaços em branco que podem ser vistos quando o arquivo é aberto no FrameMaker ou Oxygen. (7408)
* Mapas com href=&quot;/&quot; em qualquer um dos tópicos não são publicados em sites AEM. (7405)
* Problemas de desempenho encontrados no editor quando o mapa raiz tem um grande número de definições de chave. (7400)
* O estado do documento para um mapa com modelo personalizado não está sendo herdado de seu perfil de estados correspondente. (7359)
* `<tm>` elemento renderizado incorretamente como um elemento de bloco. (7286)
* Os modelos duplicados são exibidos no painel modelos do editor quando um novo modelo é criado. (5814)
* Os modelos definidos em ui_config para imagens para definir atributo adicional não são aplicáveis para casos de arrastar/soltar. (5713)
* Aspecto padrão incorreto do uicontrol na menucascata. (5483)
* Os modelos personalizados para Tópico/Mapa não mostram um novo nome na interface do usuário. Ele mostra o nome como &quot;Tópico&quot;/&quot;Mapa&quot; em vez de mostrar o nome configurado. (4958)
* Capacidade de limpar o roteiro das configurações de preferências do usuário. (8534)
* Uma coleção de mapa recém-criada não é listada, mesmo depois de atualizar a página.(8603)
* Não é possível fechar o tópico desbloqueado. (8545)
* A alternância entre o modo de origem e autor marca o tópico como sujo e requer que o conteúdo seja salvo novamente.(8524)
* Reutilizar o painel de conteúdo trava ao pesquisar caracteres especiais `[` ou `*` .(8279)
* O cursor não é exibido na barra de pesquisa quando a caixa de diálogo Inserir elemento é aberta usando o atalho de teclado Alt+Enter.(7912)
* A opção de pesquisa pesquisa pesquisa somente pesquisa em nomes de arquivo e não em conteúdo. (7784)


### Conector de oxigênio

* Os arquivos cuja pasta pai tem caracteres especiais dão erro ao carregar no Oxygen. (8054)
* Quando um documento recém-criado é aberto no Oxygen, ele gera o erro &quot;Não é possível encontrar GUID&quot;. (7856)
* A opção de check-in é desativada depois que o arquivo é tirado do AEM usando Editar no Oxygen. (7471)


### Análise

* A sincronização em tempo real não está funcionando para comentários. (7661)

### Painel de mapa

* Não é possível ver o conteúdo conref no título de um tópico na guia de tópicos ou relatórios do painel de mapa. (8263)
* Saída AEM Sites | jcr:title da página do site gerada não é atualizado quando o título do tópico DITA é atualizado. (8131)
* O MAPA de download não baixa os arquivos de vídeo usados nos tópicos. (8070)
* Os arquivos de mídia não são baixados quando a tag do objeto é usada por meio da API do mapa de download. (8057)
* Um relatório incorreto é mostrado na guia Relatórios se qualquer tópico tiver uma referência de arquivo cujo título começa com conref. (4698)
* A caixa de diálogo Aplicar rótulos na guia Linha de base não exibe rótulos na lista suspensa. (8455)

### Publicação

* A criação do PDF falha pela primeira vez quando a opção Ativar controle de versão é selecionada. (8053, 8294)
* O caractere de espaço em branco é adicionado automaticamente após um &#39;tm; na saída AEM Site. (7964)
* Não é possível exibir vídeos do YouTube AEM saída do Site. (7401)
* O filtro por rótulo falha no conteúdo referenciado depois que o usuário clica em navegar em todos os tópicos na guia linha de base do painel de mapa. (7388)
* Tópico de publicação com elemento `<tm>` ter o valor da propriedade SM ou reg é exibido incorretamente na saída gerada. (7239)
* A publicação da linha de base com imagem não está escolhendo a versão mais recente da imagem na saída publicada. (7231)
* Os tópicos referenciados relacionados são mostrados na guia da linha de base. (5424)
* A publicação incremental de um tópico com conkeyref em seu título não funciona conforme o esperado. (4474)
* O título da página não é usado para geração do URL de saída, mesmo que essa configuração esteja marcada. (8257)
* Publicação na linha de base escolhendo a versão atual das imagens em vez do nó congelado. Isso também é visto se uma imagem tiver espaço ou caracteres especiais no nome do arquivo. (8274, 8322)
* A publicação incremental falha para o mapa DITA com o esquema de assunto de tipo com mapref. (8218)
* Nulo é adicionado sempre que um mapa é adicionado ao Painel de publicação em massa. (8695)
* Ao usar a publicação da linha de base com imagem como conref no tópico, a imagem não é publicada na saída. (8564)
* A publicação falha com uma exceção se a linha de base usada AEM publicação do site for excluída. (8572)
* A regeneração de tópico não está funcionando. (8091)
* Existem problemas com a publicação de notas de rodapé em tabelas. (4709)

### AEM Assets

* Problemas de desempenho encontrados ao executar seleção/exclusão em um grande conteúdo definido na interface do usuário do Assets. (8238)
* O recurso de pesquisa salva (coleção inteligente) é interrompido se o Predicado DITA for adicionado aos filtros de Pesquisa. (8048)
* A reversão da imagem para a versão mais antiga não funciona. (DXML-7903)
* A opção Excluir também está visível para os autores que não têm permissão para excluir. (7322)
* A sobreposição do CCMS para o Editor de ativos interrompe a renderização da opção Excluir. (8093)
* O perfil de documento não está sendo excluído. (8604)
* As referências são quebradas ao executar &quot;Selecionar tudo&quot; e mover o multimídia/Dita_Content para outra pasta. (8621)
* Referências incorretas ocorrem na origem ao mover os ativos. (8627)
* A exibição de lista fixa não é carregada. (8542)

### Importação de conteúdo

* Conversão de HTML para DITA | A tabela com &#39;tr&#39; com entradas &#39;td&#39; vazias causa linhas adicionais na saída. (8132)
* Conversão de HTML para DITA | HTML com uma tabela com vários corpos falha com exceção. (7940)
* Conversão de HTML para DITA | erros se o HTML de origem tiver comentários. (7937)
* A importação de arquivos DITA 1.3 DITA faz com que algum href se transforme em links malformados. (8019)

## Problemas conhecidos

O Adobe identificou os seguintes problemas conhecidos para [!DNL AEM Guides] Versão as a Cloud Service de janeiro de 2022.


### Problemas conhecidos com solução alternativa

Use a solução alternativa fornecida para os seguintes problemas conhecidos:

* A autenticação da Web não está funcionando para o conector Oxygen no Mac.
   **Solução alternativa**: Use o conector Oxygen no Windows por enquanto.

* No navegador Firefox, os comentários de revisão não podem ser importados sem abrir a exibição lado a lado.
   **Solução alternativa**: Use o navegador Chrome por enquanto.

* As referências se quebram ao mover imagens ou arquivos de multimídia que tenham espaço(s) nos nomes de arquivos.
   **Solução alternativa**: Renomeie o arquivo e remova os espaços do nome do arquivo antes de movê-los.

* O painel de mapa não é carregado intermitentemente na versão mais recente do navegador Chrome.
   **Solução alternativa**: Atualize a página do painel de mapa.

### Outros problemas conhecidos

* Se o oxigênio estiver ligado a [!DNL AEM Guides] solução que usa autenticação da Web e falha no logout.
* As tarefas de revisão não podem ser reatribuídas aos usuários.
* Problemas estão presentes na interface do usuário da coleção de mapas, como o texto está distorcido e **Selecionar tudo** não está funcionando corretamente.
