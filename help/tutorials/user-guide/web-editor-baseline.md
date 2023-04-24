---
title: Criar e gerenciar linhas de base no Editor da Web
description: Saiba como criar e gerenciar linhas de base no Editor da Web
source-git-commit: 873111892d5b479f80a40c0b18cda9b538f5a1de
workflow-type: tm+mt
source-wordcount: '1190'
ht-degree: 0%

---


# Criar e gerenciar linhas de base no Editor da Web {#id223MB0ZF043}

>[!TIP]
>
> É recomendável usar esse recurso da Linha de base no Editor da Web se você tiver atualizado para a versão Guias AEM as a Cloud Service de março ou posterior.

AEM Guias fornece o recurso Linha de base integrado ao Editor da Web, que permite que os usuários criem linhas de base e as usem para publicar ou traduzir tópicos de diferentes versões.

## Criar uma linha de base

Você pode criar uma linha de base no Editor da Web executando as seguintes etapas:

1. No painel Repositório, abra o arquivo de mapa DITA na Visualização de mapa.
1. Clique no botão **Gerenciar** guia . O **Linha de base** painel exibe as linhas de base do mapa DITA.

   ![](images/baseline-manage.png)

1. No **Linha de base** clique no ícone + na parte superior direita. Você pode criar uma linha de base com uma versão específica dos tópicos e do conteúdo referenciado disponível em uma data e hora específicas, ou com um rótulo definido para uma versão dos tópicos.
1. Insira um nome para a linha de base em **Nome da linha de base**.
1. Em **Opção de linha de base**, você pode escolher **Usar versão de arquivo** ou **Usar rótulos** opção:

   **Usar versão de arquivo**: Você pode criar uma linha de base estática com uma versão específica dos tópicos e do conteúdo referenciado disponível em uma data e hora específicas, ou com um rótulo definido para uma versão dos tópicos:

   - Em **Defina a versão mais recente com base em,** selecione uma das seguintes opções:


      1. **Data** &lt;time stamp=&quot;&quot;>: Seleciona a versão dos tópicos como na data e hora especificadas.
      1. **Rótulo**: Selecione essa opção para escolher os tópicos de acordo com o rótulo aplicado a eles. Se os tópicos tiverem rótulos especificados para eles, os rótulos serão listados na lista suspensa. Você pode escolher um rótulo na lista. Você também pode adicionar um rótulo na caixa de texto.\
         Ao selecionar **Rótulo,** é possível escolher as referências diretas e indiretas.
      - Para referências diretas no mapa DITA, você tem a opção de usar a versão mais recente dos tópicos que não têm o rótulo especificado aplicado a eles.

      >[!NOTE]
      >
      > Se você inserir um rótulo que não existe e selecionar a opção **Não criar uma linha de base** em seguida, a criação da linha de base falhará e fornecerá uma mensagem de erro próxima ao nome da linha de base no painel Linha de base .

      - Para referências indiretas no mapa DITA, você recebe uma opção adicional para usar a versão mais recente dos tópicos que não têm o rótulo especificado aplicado neles. Você também pode optar por **Selecionar Automaticamente** para o conteúdo referenciado, e o sistema escolhe automaticamente a versão do conteúdo referenciado correspondente à versão do conteúdo no qual é referenciado.

   Depois de selecionar um rótulo ou versão como data, todos os tópicos e arquivos de mídia referenciados no mapa serão selecionados adequadamente. Essa seleção de tópicos não é mostrada na interface do usuário, mas é salva no back-end.

   **Usar rótulos**: Selecione essa opção para a criação da linha de base para escolher os tópicos de acordo com o rótulo aplicado a eles.

   As linhas de base baseadas em rótulos são atualizadas dinamicamente. Se você gerar uma linha de base, baixar uma linha de base ou criar um projeto de tradução usando uma linha de base, os arquivos serão selecionados dinamicamente com base nos rótulos atualizados. Por exemplo, se você tiver usado a versão 1.2 de um tópico com o Rótulo Versão 1.0 para a linha de base e a versão 1.5 atualizada posteriormente com o Rótulo Versão 1.0, a linha de base será atualizada dinamicamente e a versão 1.5 será usada.

   ![](images/dynamic-baseline.png)

   - **Selecionar rótulos**: Se os tópicos tiverem rótulos especificados para eles, os rótulos serão listados na variável **Selecionar rótulos** lista suspensa. Você pode escolher o rótulo\(s\) na lista. Os rótulos selecionados primeiro recebem prioridade mais alta do que os mais recentes.
1. **Referências indiretas**: Para referências indiretas no mapa DITA, você recebe as seguintes opções:

   - **Selecionar automaticamente**: Você pode optar por **Selecionar Automaticamente** para o conteúdo referenciado, e o sistema escolhe automaticamente a versão do conteúdo referenciado correspondente à versão do conteúdo no qual é referenciado.

   - **Usar rótulo selecionado**: Você pode criar uma linha de base com o rótulo selecionado definido para uma versão de tópicos.
   - **Usar a versão mais recente ou a cópia de trabalho**: Use a versão mais recente dos tópicos que não têm o rótulo especificado aplicado a eles ou se nenhuma versão foi criada, em seguida, use a cópia de trabalho dos tópicos para criar a linha de base.
1. Clique em **Aplicar**.

A linha de base é criada. A criação da linha de base ocorre de forma assíncrona, portanto, é possível continuar trabalhando em outros arquivos no Editor da Web. Depois que a linha de base é criada, uma mensagem pop-up é exibida confirmando que a linha de base foi criada e você também recebe uma notificação da Caixa de entrada para a mesma linha.

## Gerenciar linhas de base

Você pode gerenciar suas linhas de base existentes usando os vários recursos no painel Linha de base.

- Você pode pesquisar uma linha de base existente usando a caixa de texto no painel Linha de base . Use o **Aplicar filtro** ícone para mostrar todas as linhas de base ou listar as linhas de base com o status de criação como Sucesso, Em Andamento ou Falha.
- Use o **Atualizar** ícone no painel Linha de base para verificar novamente todas as linhas de base e exibir uma nova lista de linhas de base para o mapa DITA aberto na Visualização de mapa.
- Você pode visualizar ou editar o conteúdo de uma linha de base existente clicando duas vezes na linha de base da lista no painel Linha de Base. A janela de edição da linha de base no centro exibe o arquivo de mapa DITA, o conteúdo ou tópicos do mapa e o conteúdo referenciado.


![](images/baseline-options.png)

Também é possível executar as seguintes operações na linha de base no menu Opções :

- **Editar**, **Duplicar,** ou **Excluir** uma linha de base existente.
- Adicione, remova ou faça alterações em rótulos existentes na **Gerenciar rótulos** opção. Se o administrador tiver configurado rótulos predefinidos, você verá esses rótulos na lista suspensa Adicionar rótulo. Para obter mais informações sobre como adicionar rótulos, consulte [Usar rótulos](web-editor-use-label.md#).

   >[!NOTE]
   >
   > O processo para adicionar ou remover rótulos ocorre de forma assíncrona, portanto, você pode continuar trabalhando em outros arquivos no Editor da Web. Depois que o rótulo é adicionado ou removido, uma mensagem pop-up é exibida confirmando que o rótulo foi adicionado ou removido e você também recebe uma notificação da Caixa de entrada para o mesmo.

- **Editar propriedades** de uma linha de base existente que você definiu ao criar a linha de base.
- Exporte o instantâneo de uma linha de base em um arquivo CSV com a variável **Exportar linha de base** opção.

**Filtros de linha de base**

Uso do ícone Filtros na **Filtros da linha de base** painel é possível aplicar filtros na linha de base aberta na janela de edição da linha de base:

![](images/baseline-filter.png)

- Filtre os arquivos com base em nomes de arquivo ou no local do arquivo.
- Filtre os arquivos com base nos valores de diferentes colunas, como Tipo de arquivo, Tipo de referência e assim por diante.
- Escolha as colunas a serem exibidas na janela de edição da linha de base.

>[!NOTE]
>
> Você pode clicar em um cabeçalho de coluna e classificar os arquivos com base nas colunas na janela de edição da linha de base.

**Salvar ou redefinir uma linha de base**

Depois de editar a linha de base, clique no botão **Salvar** na parte superior para salvar as alterações na linha de base. Você pode clicar no botão **Redefinir** se não quiser salvar a alteração e redefinir a linha de base. Ao clicar no botão **Redefinir** Um aviso é exibido informando que as alterações não salvas serão perdidas.

**Tópico principal:**[ Trabalhar com o editor da Web](web-editor.md)

