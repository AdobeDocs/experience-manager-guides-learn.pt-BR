---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de setembro de 2022
description: Versão mais recente dos Guias do Adobe Experience Manager as a Cloud Service
source-git-commit: f2ad6e920c47fff61dd85e3aeafb558c7fd6cfea
workflow-type: tm+mt
source-wordcount: '1284'
ht-degree: 3%

---

# Versão mais recente dos Guias do Adobe Experience Manager as a Cloud Service

## Atualizar para a versão mais recente

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação do Cloud Services configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.9.178.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão mais recente dos Guias AEM as a Cloud Service.

## Etapas para indexar o conteúdo existente

Execute as seguintes etapas para indexar o conteúdo existente e use o novo texto localizar e substituir no nível de mapa:
* Execute uma solicitação de POST para o servidor (com autenticação correta) - `http://<server:port>/bin/guides/map-find/indexin`.
(Opcional: Você pode passar caminhos específicos dos mapas para indexá-los, por padrão, todos os mapas serão indexados || Exemplo :   `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)
* A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com ID do trabalho para o mesmo ponto final - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por exemplo: `http://<_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)`
* Quando a tarefa for concluída, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados dos logs do servidor.


## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software compatíveis com AEM Guias as a Cloud Service versão de setembro de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac | Editar no Windows Oxygen | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.9.0 | 2.7.13 | 2.7.13 | 2.3 | 2,3 |
|  |  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service fornecem muitos aprimoramentos e novos recursos na versão mais recente:


### Criar uma linha de base dinâmica com base em rótulos

Agora AEM Guias fornece o recurso para criar linhas de base dinâmicas com base em rótulos. Se você gerar uma linha de base, baixar uma linha de base ou criar um projeto de tradução usando uma linha de base, os arquivos serão selecionados dinamicamente com base nos rótulos atualizados. Esse recurso é útil, pois não é necessário modificar a linha de base ao atualizar os rótulos.
Também é possível exportar o instantâneo da linha de base como CSV.

![Criar linhas de base](assets/preset-metadata.png)

### Localizar e substituir o texto no nível de mapa

Agora é possível pesquisar arquivos em um mapa que contenha texto específico. O texto pesquisado é realçado nos arquivos. Também é possível substituir a palavra ou frase pesquisada por outra palavra ou frase dentro dos arquivos.
Selecione o **Substituir** ícone para substituir a ocorrência atual e o **Substituir tudo no arquivo** ícone para substituir todas as ocorrências no arquivo selecionado.

![Localizar Substituir no mapa](assets/map-find-replace.png)

Por padrão, as opções **Arquivo de check-out antes de substituir** e **Criar nova versão após substituir** estiverem selecionadas, portanto, o check-out de um arquivo é realizado antes da substituição do texto, e uma nova versão é criada após a substituição do texto.

### Exibir diferença de versão para arquivos Fora de Sincronização no painel de tradução

Agora você pode optar por traduzir a variável **Fora de Sincronização** arquivos com base nas alterações feitas entre as duas versões de um tópico.\
![Painel de tradução](assets/translation-version-diff.png)
No painel de tradução, é possível ver facilmente as diferenças entre a última versão traduzida e a versão atual do arquivo selecionado.

![caixa de diálogo de diferença de versão](assets/version-diff.png)

Com base nas diferenças, você pode decidir se deseja traduzir um tópico ou não.

### Interface de usuário de metadados disponível para predefinições do PDF

Você pode definir os metadados da predefinição de saída de um mapa DITA. É possível definir os metadados de Título, Autor, Assunto e Palavras-chave. Esses metadados são mapeados para os metadados nas Propriedades do arquivo do PDF de saída.
Esses metadados substituem os metadados definidos no nível do livro. Você pode definir os metadados especificamente em cada predefinição de saída e passá-los para o PDF de saída.

![Metadados na predefinição](assets/preset-metadata.png)


## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* Editor da Web | Em mover elementos dentro de um tópico, as IDs atribuídas nos elementos são substituídas por IDs atribuídas automaticamente. (7895)
* Rastrear alterações | O conteúdo é perdido quando um novo elemento é inserido usando a tecla Enter. (10246)
* O submapa referenciado ao mapa principal em templates não está sendo criado. (10231)
* Editor XML | Copiar-colar não está funcionando no modo de autor. (10309)
* Vários rótulos de versão depois de selecionados não estão sendo desmarcados. (9561)
* A navegação automática para o caminho na caixa de diálogo de navegação do site não está funcionando como navegação de arquivo. (9920)
* O painel Contorno não exibe o conteúdo quando alterado de **Autor** para **Origem** modo. (10319)
* O contexto em um novo tópico criado usando um conteúdo no modelo de tópico não funciona. A ID de hash copiada não é atualizada na cópia de conteúdo. (9890)
* Editor da Web | Nenhum carregador existe ao criar um mapa a partir do modelo de mapa. (9891)
* Novo editor de mapa | O texto negrito ou itálico adicionado no título do mapa não é retido se alternarmos de **Autor** para **Layout** exibir. (10218)
* Novo editor de mapa | As condições aplicadas em qualquer referência não podem ser removidas da exibição Layout. (10213)
* Novo editor de mapa | A aplicação de referências de condições não funciona na exibição Layout como na exibição Autor. (10198)
* Novo editor de mapa | Mover para a esquerda no menu de contexto remove a referência se não puder ser movida para a esquerda. (10219)
* Novo editor de mapa |O ícone é exibido incorretamente para as referências em um mapa criado usando a exibição Layout. (10197)
* Painel do repositório | O clique com o botão direito do mouse no painel do repositório gera um erro de aplicativo. (10123)
* Localizar e substituir | O modo escuro não é legível para Resultados da pesquisa no Editor da Web. (9978)
* Tradução | Metadados e tags não são propagados para as cópias traduzidas. (4696)
* Copiar o conteúdo (ctrl+c/ctrl+v) gera um erro no modo de criação. (10304)
* Modelo PDF | A adição de imagens de plano de fundo a qualquer layout de página exibe Caminho de imagem absoluto, e as imagens não são exibidas no PDF de saída. (10297)
* PDF nativo | O título do capítulo e o cabeçalho do capítulo não estão funcionando na publicação do PDF. (9947)
* PDF nativo | `xref` para um conceito não é resolvido corretamente para um tópico DITA específico. (10229)
* PDF nativo | Não é possível exibir o texto da legenda de uma tabela na saída PDF gerada. (9827)
* PDF nativo | As referências em apêndices não são exibidas como apêndices na saída do PDF. (10182)
* PDF nativo | O atributo de quadro para uma tabela não é propagado para o HTML temp (como classe). (10353)
* PDF nativo | os arquivos HTML temp adicionam as classes colsep e rowsep ao td e o mesmo se o valor for 0 no DITA de origem. (10352)
* PDF nativo | Os metadados para critérios adicionados no layout da página não são honrados. (10377)
* PDF nativo | A geração de PDF falha para conteúdo específico. (9927)
* PDF nativo | O conteúdo via conkeyref não está sendo exibido na saída do PDF. (9836)
* PDF nativo | As referências de chave para KeyDefs com imagens ou links externos não são resolvidas. (10063)
* A exibição Autor de um mapa não exibe o texto de espaço reservado para a lista de tabulações e a lista de figuras. (10330)
* Quando criamos uma nova linha de base, o filtro de linha de base já selecionado não é aplicado. (9954)
* O arquivo de vídeo está ausente na linha de base se o nome da pasta pai tiver um caractere de espaço. (10031)
* A criação da linha de base não escolhe a versão mais recente quando o fuso horário do usuário é diferente do fuso horário do servidor. (10190)
* O atalho Control + F não abre o modal de pesquisa do navegador no Console de Ativos após instalar AEM Guias 4.1 no AEM 6.5.12. (10189)


## Problemas conhecidos

O Adobe identificou os seguintes problemas conhecidos para a versão dos Guias de AEM as a Cloud Service em setembro de 2022.


* A linha de base dinâmica não é integrada à publicação da base de conhecimento.

* Tradução | O ícone de diferença de versão é exibido para o conteúdo de origem devido a qualquer alteração no conteúdo de destino.
