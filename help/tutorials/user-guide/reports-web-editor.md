---
title: Relatório de mapa DITA do Editor da Web
description: Saiba como fazer o mapeamento DITA no Editor da Web
exl-id: b1011cec-6374-4026-bf1c-54a1981c760e
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 0%

---

# Relatório de mapa DITA do Editor da Web {#id231HF0Z0NXA}

O AEM Guides vem com um recurso no Editor da Web que permite verificar a integridade geral de suas referências e gerar relatórios para elas.

Você pode exibir a lista de tópicos, gerenciar os metadados de todas as referências e exibir a lista multimídia do mapa atual na **Relatórios** no Editor da Web.

## Gerar um CSV na exibição da Lista de tópicos

A variável **Lista de tópicos** a exibição fornece informações detalhadas sobre os tópicos, como tipo de referência, estado do documento e autor.

Você pode criar um relatório dos tópicos executando as seguintes etapas:

1. No **Repositório** abra o arquivo de mapa DITA na Exibição de mapa.
1. Clique em **Gerenciar** guia.
1. Clique duas vezes **Lista de tópicos** à esquerda. A lista de tópicos presentes no mapa DITA é exibida.

   ![](images/web-editor-topiclist-panel.png){width="800" align="left"}

1. No **Filtros** Painel onde você pode filtrar seus tópicos com base na variável **Tipo de referência** \(direto ou indireto\), **Estado do documento** \(o estado atual de seus tópicos. Por exemplo, se os tópicos estiverem no estado Editar, Em revisão ou Revisado, eles serão listados\) ou **Autor** do tópico.

1. Você também pode usar as seguintes opções de filtragem de tópico para exibir as seguintes colunas na lista:

   - **Tópico** O título do tópico é especificado no mapa DITA. Você pode clicar no tópico para editá-lo.
   - **Nome do arquivo** Nome do arquivo.
   - **UUID** O identificador exclusivo universal \(UUID\) do arquivo.
   - **Local do arquivo** O caminho completo do tópico.
   - **Tipo de referência** O tipo de referência - direta ou indireta.
   - **Estado do documento** O estado atual do tópico.
   - **Autor** O usuário que trabalhou por último no tópico.
   - **Mapa principal** A lista de todos os mapas em que o tópico é referenciado diretamente.

   >[!NOTE]
   >
   > Clique em **Atualizar** para obter uma nova lista de tópicos e ver qualquer alteração no arquivo de mapa ou se qualquer referência no arquivo de tópico for atualizada.

1. Clique em **Baixar CSV** para baixar o instantâneo atual dos tópicos no mapa DITA. O CSV contém as colunas selecionadas e os tópicos filtrados no **Lista de tópicos** exibição. Em seguida, você pode abrir esse arquivo CSV da lista de tópicos em qualquer editor CSV.

**Gerenciar metadados em massa a partir do Relatório de metadados**

O AEM Guides permite marcar o conteúdo DITA no editor da Web. Você pode aplicar tags a um tópico individual ou usar o recurso de marcação em massa para aplicar várias tags a vários tópicos, um mapa DITA ou um submapa. Você também pode alterar o estado do documento de todos os tópicos selecionados para o próximo estado de documento comum possível.

## Exibir metadados

Para exibir os metadados de suas referências no mapa DITA atual, execute as seguintes etapas:

1. No painel Repositório, abra o arquivo de mapa DITA na Exibição de mapa.
1. Clique em **Gerenciar** guia.
1. Clique duas vezes **Metadados** à esquerda. A lista de metadados de todas as referências no mapa DITA é exibida. Isso também inclui as referências de mídia.

   ![](images/web-editor-metadata-panel.png){width="800" align="left"}

1. No **Filtros** você pode filtrar seus tópicos com base na variável **Estado do documento** \(o estado atual de seus tópicos. Por exemplo, se os tópicos estiverem no estado Editar, Em revisão ou Revisado, eles serão listados\), **Referências** \(direto ou indireto\), **Tipo de arquivo** \(Mapa, Tópico e Imagem\) da referência.
1. Você também pode optar por exibir somente a **Arquivos sem tags** ou também escolha tags específicas na **Tags** filtro para exibir os arquivos associados a eles.
   1. Você também pode usar as seguintes opções de filtragem de tópico para exibir as seguintes colunas na lista de metadados:
      - **Título** \(selecionado por padrão\) O título do arquivo referenciado é especificado no mapa DITA. Você pode clicar no arquivo para editá-lo.Você também pode clicar e reproduzir um arquivo de áudio ou vídeo no Editor da Web. Você pode alterar o volume ou a visualização do vídeo. No menu de atalho, você também tem as opções para baixar, alterar a velocidade de reprodução ou visualizar uma imagem na imagem.

         >[!NOTE]
         >
         > Um ícone de check-out também é exibido próximo ao título de um arquivo com check-out. Você pode passar o mouse sobre o ícone para visualizar o nome do usuário.

      - **Nome do arquivo** O nome do arquivo.
      - **Local do arquivo** O caminho completo do arquivo.
      - **Tags** \(selecionado por padrão\) Tags aplicadas ao arquivo.

         >[!NOTE]
         >
         > Por padrão, você pode ver duas tags para um arquivo. Para exibir mais tags, clique em **Mostrar mais**. Clique em **Mostrar menos** para contrair a lista novamente.

      - **Tipo de referência** O tipo de referência - direta ou indireta
      - **Estado do documento** \(selecionado por padrão\) O estado atual do arquivo de referência.
      - **Tipo de arquivo** \(selecionado por padrão\) Tipo do arquivo de origem. As opções disponíveis são Mapa, Tópico e Imagem.
      - **Retirado por** O usuário que fez check-out do arquivo.
1. Clique em **Baixar CSV** para baixar o instantâneo atual das referências no mapa DITA. O CSV contém as colunas selecionadas e as referências filtradas na exibição da Lista de tópicos. Em seguida, você pode abrir esse arquivo CSV de metadados em qualquer editor CSV.

**Atualizar metadados**

1. Para atualizar metadados, selecione os arquivos que deseja atualizar.

   >[!NOTE]
   >
   > Não é possível selecionar arquivos com check-out. Um ícone de check-out também é exibido próximo ao título de um arquivo com check-out. Você pode passar o mouse sobre o ícone para visualizar o nome do usuário.

1. Selecionar **Gerenciar** do topo.

   ![](images/web-editor-manage-metadata.png){width="350" align="left"}

1. Se quiser adicionar novas tags, selecione novas tags na lista suspensa para aplicá-las a todos os tópicos selecionados. Também é possível excluir qualquer tag ao clicar no ícone de cruz próximo à tag.

   >[!NOTE]
   >
   > As tags comuns aplicadas em todos os tópicos selecionados são listadas.

1. Selecione um novo estado do documento se desejar alterar o estado do documento de todas as referências selecionadas. A lista suspensa exibe o estado comum possível de todos os tópicos selecionados. Por exemplo, se o estado atual dos tópicos for Em revisão, você poderá ver o estado Rascunho, Aprovado ou Revisado.
1. Clique em **Atualizar** para atualizar os metadados. Uma mensagem de confirmação é exibida para os metadados, independentemente de ela ser atualizada com sucesso ou ter atualizações com falha. Clique também em **Baixar relatório** para baixar o CSV de metadados na caixa de diálogo de confirmação. Este CSV contém os detalhes do status de atualização das referências selecionadas.

## Gerar um relatório multimídia

A variável **Multimídia** O relatório fornece informações detalhadas sobre a multimídia usada no mapa, como título, tipo \(áudio, vídeo e imagens\), arquivos nos quais a multimídia é usada e o tipo de referência dos arquivos nos quais eles foram usados. Você também pode visualizar a UUID e o local da multimídia no repositório. Você pode criar um relatório multimídia executando as seguintes etapas:

1. No **Repositório** abra o arquivo de mapa DITA na Exibição de mapa.
1. Clique em **Gerenciar** guia.
1. Clique duas vezes **Multimídia** à esquerda. A lista de multimídia presente no mapa DITA é exibida.
1. No **Filtros** você pode ordenar a lista por multimídia ou pelos nomes de usados nas referências.

   - Quando você faz pedidos por **Multimídia**, o nome **** da multimídia é exibido na primeira coluna e, em seguida, os nomes de todas as referências nas quais foram usados são exibidos em outra coluna na mesma linha. Por exemplo, a captura de tela a seguir mostra a multimídia WarmCoolForC.gif na primeira coluna e três referências nas quais ela é usada são exibidas na terceira coluna na mesma linha.

      ![](images/multimedia-report-file-order.png){width="650" align="left"}

   - Se você fizer o pedido até **Usado em** , você verá a visualização transposta onde os nomes das referências nas quais o multimídia foi usado são listados na primeira coluna, enquanto os nomes multimídia são listados em outra coluna em linhas separadas. Por exemplo, a captura de tela a seguir mostra os nomes de três referências \(Ajustar a temperatura da cadeira, Alterar a exibição da temperatura da cadeira e Área da tripulação\) na primeira coluna e a multimídia WarmCoolForC.gif é exibida na terceira coluna em três linhas separadas.

      ![](images/multimedia-report-used-in-order.png){width="650" align="left"}

1. Você pode filtrar seus multimídia com base no **Tipo de multimídia**, e **Tipo de referência**. A lista de arquivos multimídia é exibida com base na sua seleção na lista suspensa. Por exemplo, você pode optar por exibir somente as referências de áudio no mapa DITA, e um arquivo mostra somente as referências de áudio usadas nele.

   >[!NOTE]
   >
   > Dependendo do tipo de multimídia usado no seu mapa, Imagem, Vídeo e Áudio estão listados na **Tipo de multimídia** e Direto ou Indireto estão listados na lista suspensa **Tipo de referência** lista suspensa.

1. Você também pode usar as seguintes opções de filtro para optar por exibir as seguintes colunas na lista:

   - **Multimídia** \(selecionado por padrão\) O título da multimídia é especificado no mapa DITA. Você pode clicar na multimídia para editá-la.
   - **Localização de multimídia** O caminho completo da multimídia.
   - **UUID de multimídia** O identificador exclusivo universal \(UUID\) do arquivo.
   - **Tipo de multimídia** \(selecionado por padrão\) Tipo de multimídia. As opções disponíveis são Áudio, Vídeo ou Imagem.
   - **Usado em** \(selecionado por padrão\) As referências nas quais a multimídia foi usada. Você pode clicar na referência para editá-la.
   - **Tipo de referência** \(selecionado por padrão\) O tipo de referência - direta ou indireta.

   >[!NOTE]
   >
   > Clique em **Atualizar** para obter uma nova lista de multimídia e ver qualquer alteração no arquivo de mapa ou se alguma multimídia no mapa DITA for atualizada.

1. Você também pode clicar e reproduzir um arquivo de áudio ou vídeo no Editor da Web. Você pode alterar o volume ou a visualização do vídeo. No menu de atalho, você também tem as opções para baixar, alterar a velocidade de reprodução ou visualizar uma imagem na imagem.

   ![](images/video-web-editor.png){width="800" align="left"}

1. Clique em **Baixar CSV** para baixar o instantâneo atual da multimídia no mapa DITA. O CSV contém as colunas selecionadas e os arquivos multimídia filtrados no **Multimídia** exibição. Em seguida, você pode abrir esse arquivo CSV multimídia em qualquer editor CSV.

**Tópico pai:**[ Relatórios](reports-intro.md)
