---
title: Relatório de histórico de versão dos arquivos revertidos
description: Saiba como reverter o relatório de histórico de versão dos arquivos
source-git-commit: bb7a8d49e5425b7fc856277c054558c75394fcb2
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 0%

---


# Relatório de histórico de versão dos arquivos revertidos {#id205BBC00PRK}

Quando você está trabalhando em várias versões simultâneas junto com vários autores, o conteúdo deve ter várias versões. Pode haver algumas informações comuns em várias versões, que diferentes autores poderiam usar em seu projeto. Para lidar com tais atribuições de trabalho, os autores podem acabar com várias versões de arquivos. Essas versões podem ser apenas uma versão mais recente de um arquivo ou uma reversão para uma versão anterior. É uma tarefa complexa para identificar quando um arquivo foi revertido e por quê.

AEM Guias permite gerar um relatório de histórico de versões para um arquivo individual ou para todos os arquivos em uma pasta. Esse histórico de versão fornece uma visualização consolidada de todas as versões de um arquivo que foram revertidas e que criaram essas versões, além do motivo para criar essas versões.

Você pode acessar esse relatório nos seguintes lugares:

- **Interface do usuário do Assets**: selecionando um arquivo e abrindo o **Histórico da versão** no painel esquerdo. O **Histórico da versão** a exibição contém o **Reverter registros de versão** na parte inferior do painel. Ao clicar neste link, o histórico do arquivo selecionado das versões revertidas é exibido.

   ![](images/revert-log-from-assets-ui.png)

- **Visualização do tópico**: quando você estiver visualizando um tópico, você também poderá exibir a variável **Histórico da versão** no painel esquerdo. Você obterá um painel semelhante à interface do usuário do Assets, onde é possível clicar no botão **Reverter registros de versão** link para acessar o histórico de versão revertido do documento ativo.

- **Seção Ferramentas AEM**: também é possível acessar esse relatório na seção Ferramentas AEM . O procedimento a seguir explica como você pode acessar o histórico de versões de reversão na seção Ferramentas de AEM .


Execute as etapas a seguir para acessar o relatório Histórico de Reversão :

1. Clique no link do Adobe Experience Manager na parte superior e escolha **Ferramentas**.

1. Selecionar **Guias** na lista de ferramentas.

1. Clique no botão **Histórico de Reversão** mosaico.

   Uma página Reverter histórico da versão em branco é exibida, onde é necessário procurar e selecionar um arquivo ou pasta para gerar o relatório.

1. Clique em **Mostrar registros** para gerar o relatório para o arquivo ou pasta selecionado.

   ![](images/revert-version-history-report.png)

   O relatório contém os seguintes detalhes:

   - **Nome do arquivo**: O título do tópico. Clicar no link de título do tópico abre a visualização do tópico.

   - **Carimbo de data e hora**: A data e a hora em que o tópico foi revertido para uma versão anterior.

   - **Usuário**: Nome do usuário que reverteu para uma versão anterior.

   - **Reverter de**: O número da versão original do arquivo de onde ele foi revertido.

   - **Reverter para**: A versão para a qual o arquivo foi revertido.

   - **Comentário**: Qualquer comentário fornecido pelo usuário que reverteu o arquivo.


**Tópico principal:**[ Relatórios](reports-intro.md)

