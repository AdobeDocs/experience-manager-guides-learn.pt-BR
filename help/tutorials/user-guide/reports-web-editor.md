---
title: Relatório de mapa DITA do Editor da Web
description: Saiba como elaborar o relatório de mapa DITA no Editor da Web
exl-id: b1011cec-6374-4026-bf1c-54a1981c760e
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '1608'
ht-degree: 0%

---

# Relatório de mapa DITA do Editor da Web {#id231HF0Z0NXA}

AEM Guias vem com um recurso no Editor da Web que permite verificar a integridade geral de suas referências e gerar relatórios para elas.

Você pode exibir a lista de tópicos, gerenciar os metadados de todas as referências e exibir a lista de multimídia para o mapa atual do **Relatórios** no Editor da Web.

## Gerar um CSV na exibição da Lista de tópicos

O **Lista de tópicos** A exibição fornece informações detalhadas sobre seus tópicos, como tipo de referência, estado do documento e autor.

Você pode criar um relatório dos tópicos executando as seguintes etapas:

1. No **Repositório** , abra o arquivo de mapa DITA na Visualização de mapa.
1. Clique no botão **Gerenciar** guia .
1. Clique duas vezes **Lista de tópicos** à esquerda. A lista de tópicos presentes no mapa DITA é exibida.

   ![](images/web-editor-topiclist-panel.png){width="800" align="left"}

1. No **Filtros** É possível filtrar os tópicos com base no **Tipo de referência** \(direto ou indireto\), **Estado do documento** \(o estado atual de seus tópicos. Por exemplo, se os tópicos estiverem no estado Editar, Em revisão ou Revisado, eles serão listados\) ou a variável **Autor** do tópico.

1. Você também pode usar as seguintes opções de filtragem de tópicos para escolher exibir as seguintes colunas na lista:

   - **Tópico** O título do tópico é especificado no mapa DITA. Você pode clicar no tópico para editá-lo.
   - **Nome do arquivo** Nome do arquivo.
   - **UUID** O identificador universal exclusivo \(UUID\) do arquivo.
   - **Local do arquivo** O caminho completo do tópico.
   - **Tipo de referência** O tipo de referência - direta ou indireta.
   - **Estado do documento** O estado atual do tópico.
   - **Autor** O usuário que trabalhou por último no tópico.
   - **Mapa principal** A lista de todos os mapas em que o tópico é referenciado diretamente.

   >[!NOTE]
   >
   > Clique em **Atualizar** para obter uma nova lista de tópicos e ver qualquer alteração no arquivo de mapa ou se qualquer referência no arquivo de tópico for atualizada.

1. Clique em **Baixar CSV** para baixar o instantâneo atual dos tópicos no mapa DITA. O CSV contém as colunas selecionadas e os tópicos filtrados no **Lista de tópicos** exibir. Em seguida, você pode abrir esse arquivo CSV de lista de tópicos em qualquer editor CSV.

**Gerenciar metadados em massa a partir do relatório de Metadados**

AEM Guias permitem marcar o conteúdo do DITA no editor da Web. Você pode aplicar tags em um tópico individual ou usar o recurso de marcação em massa para aplicar várias tags em vários tópicos, um mapa DITA ou em um submapa. Também é possível alterar o estado do documento de todos os tópicos selecionados para o próximo estado comum possível do documento.

## Exibir metadados

Para exibir os metadados de suas referências no mapa DITA atual, execute as seguintes etapas:

1. No painel Repositório, abra o arquivo de mapa DITA na Visualização de mapa.
1. Clique no botão **Gerenciar** guia .
1. Clique duas vezes **Metadados** à esquerda. A lista de metadados de todas as referências no mapa DITA é exibida. Isso também inclui as referências de mídia.

   ![](images/web-editor-metadata-panel.png){width="800" align="left"}

1. No **Filtros** você pode filtrar seus tópicos com base no painel **Estado do documento** \(o estado atual de seus tópicos. Por exemplo, se os tópicos estiverem no estado Editar, Em revisão ou Revisado, eles serão listados\), **Referências** \(direto ou indireto\), **Tipo de arquivo** \(Mapa, Tópico e Imagem\) da referência.
1. Você também pode optar por exibir somente a variável **Arquivos sem tags** ou também escolha tags específicas no **Tags** para exibir os arquivos associados a eles.
   1. Você também pode usar as seguintes opções de filtragem de tópicos para escolher exibir as seguintes colunas na lista de metadados:
      - **Título** \(selecionado por padrão\) O título do arquivo referenciado é especificado no mapa DITA. Você pode clicar no arquivo para editá-lo.Também pode clicar e reproduzir um arquivo de áudio ou vídeo no Editor da Web. Você pode alterar o volume ou a visualização do vídeo. No menu de atalho, você também tem as opções para baixar, alterar a velocidade de reprodução ou exibir a imagem na imagem.

         >[!NOTE]
         >
         > Um ícone com check-out também é exibido próximo ao título de um arquivo com check-out. Você pode passar o mouse sobre o ícone para visualizar o nome do usuário.

      - **Nome do arquivo** O nome do arquivo.
      - **Local do arquivo** O caminho completo do arquivo.
      - **Tags** \(selecionado por padrão\) Tags aplicadas no arquivo.

         >[!NOTE]
         >
         > Por padrão, você pode visualizar duas tags para um arquivo. Para exibir mais tags, clique em **Mostrar mais**. Clique em **Mostrar menos** para contrair a lista novamente.

      - **Tipo de referência** O tipo de referência - direta ou indireta
      - **Estado do documento** \(selecionado por padrão\) O estado atual do arquivo de referência.
      - **Tipo de arquivo** \(selecionado por padrão\) Tipo do arquivo de origem. As opções disponíveis são Mapa, Tópico e Imagem.
      - **Check-out por** O usuário que fez check-out do arquivo.
1. Clique em **Baixar CSV** para baixar o instantâneo atual das referências no mapa DITA. O CSV contém as colunas selecionadas e as referências filtradas na exibição Lista de tópicos. Em seguida, você pode abrir esse arquivo CSV de metadados em qualquer editor CSV.

**Atualizar metadados**

1. Para atualizar metadados, selecione os arquivos para os quais deseja atualizar.

   >[!NOTE]
   >
   > Não é possível selecionar nenhum arquivo com check-out. Um ícone com check-out também é exibido próximo ao título de um arquivo com check-out. Você pode passar o mouse sobre o ícone para visualizar o nome do usuário.

1. Selecionar **Gerenciar** do topo.

   ![](images/web-editor-manage-metadata.png){width="350" align="left"}

1. Se desejar adicionar novas tags, selecione novas tags na lista suspensa para aplicá-las a todos os tópicos selecionados. Também é possível excluir qualquer tag ao clicar no ícone de cruz próximo à tag .

   >[!NOTE]
   >
   > As tags comuns aplicadas em todos os tópicos selecionados são listadas.

1. Selecione um novo estado de documento se desejar alterar o estado do documento de todas as referências selecionadas. A lista suspensa exibe o estado comum possível para todos os tópicos selecionados. Por exemplo, se o estado atual de seus tópicos for Em revisão, você poderá ver o estado Rascunho, Aprovado ou Revisado.
1. Clique em **Atualizar** para atualizar os metadados. Uma mensagem de confirmação é exibida para os metadados, independentemente de eles terem sido atualizados com êxito ou de terem alguma atualização com falha. Você também pode clicar em **Baixar relatório** para baixar o CSV de metadados na caixa de diálogo de confirmação. Esse CSV contém os detalhes do status de atualização das referências selecionadas.

## Gerar um relatório de multimídia

O **Multimídia** O relatório fornece informações detalhadas sobre a multimídia usada no mapa, como o título, o tipo \(áudio, vídeo e imagens\), os arquivos nos quais a multimídia é usada e o tipo de referência dos arquivos nos quais eles foram usados. Você também pode visualizar o UUID e o local da multimídia no repositório. Você pode criar um relatório da multimídia executando as seguintes etapas:

1. No **Repositório** , abra o arquivo de mapa DITA na Visualização de mapa.
1. Clique no botão **Gerenciar** guia .
1. Clique duas vezes **Multimídia** à esquerda. A lista de multimídia presente no mapa DITA é exibida.
1. No **Filtros** painel, é possível ordenar a lista por multimídia ou pelos nomes dos usados nas referências.

   - Ao solicitar por **Multimídia**, o nome***da multimídia é exibido na primeira coluna e, em seguida, os nomes de todas as referências em que foram usadas são exibidos em outra coluna na mesma linha. Por exemplo, a captura de tela a seguir mostra o WarmCoolForC.gif multimídia na primeira coluna e três referências em que é usado são exibidas na terceira coluna na mesma linha.

      ![](images/multimedia-report-file-order.png){width="650" align="left"}

   - Se você solicitar por **Usado em** , você verá a visualização transposta, na qual os nomes das referências em que a multimídia foi usada são listados na primeira coluna, enquanto os nomes da multimídia são listados em outra coluna em linhas separadas. Por exemplo, a captura de tela a seguir mostra os nomes de três referências \(Ajustar a temperatura do assento, Alterar a exibição da temperatura do assento e Área da tripulação\) na primeira coluna e o WarmCoolForC.gif multimídia é exibido na terceira coluna em três linhas separadas.

      ![](images/multimedia-report-used-in-order.png){width="650" align="left"}

1. Você pode filtrar sua multimídia com base na variável **Tipo de multimídia** e **Tipo de referência**. A lista de arquivos multimídia é exibida com base na sua seleção no menu suspenso . Por exemplo, você pode optar por exibir apenas as referências de áudio no mapa DITA e um arquivo mostra apenas as referências de áudio usadas nele.

   >[!NOTE]
   >
   > Dependendo do tipo de multimídia usada em seu mapa, imagem, vídeo e áudio, são listadas na **Tipo de multimídia** e Direto ou Indireto estão listados na variável **Tipo de referência** lista suspensa.

1. Também é possível usar as seguintes opções de filtragem para exibir as seguintes colunas na lista:

   - **Multimídia** \(selecionado por padrão\) O título da multimídia é especificado no mapa DITA. Você pode clicar na multimídia para editá-la.
   - **Localização de multimídia** O caminho completo da multimídia.
   - **UUID de multimídia** O identificador universal exclusivo \(UUID\) do arquivo.
   - **Tipo de multimídia** \(selecionado por padrão\) Tipo de multimídia. As opções disponíveis são Áudio, Vídeo ou Imagem.
   - **Usado em** \(selecionado por padrão\) As referências em que a multimídia foi usada. Você pode clicar na referência para editá-la.
   - **Tipo de referência** \(selecionado por padrão\) O tipo de referência - direta ou indireta.

   >[!NOTE]
   >
   > Clique em **Atualizar** para obter uma nova lista de multimídia e ver qualquer alteração no arquivo de mapa ou se alguma multimídia em seu mapa DITA for atualizada.

1. Você também pode clicar e reproduzir um arquivo de áudio ou vídeo no Editor da Web. Você pode alterar o volume ou a visualização do vídeo. No menu de atalho, você também tem as opções para baixar, alterar a velocidade de reprodução ou exibir a imagem na imagem.

   ![](images/video-web-editor.png){width="800" align="left"}

1. Clique em **Baixar CSV** para baixar o instantâneo atual da multimídia no mapa DITA. O CSV contém as colunas selecionadas e a multimídia filtrada no **Multimídia** exibir. Em seguida, você pode abrir esse arquivo CSV de multimídia em qualquer editor CSV.

**Tópico principal:**[ Relatórios](reports-intro.md)
