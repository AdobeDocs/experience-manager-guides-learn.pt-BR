---
title: Trabalhar com linha de base
description: Saiba como trabalhar com linha de base
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '1917'
ht-degree: 0%

---


# Trabalhar com linha de base {#id1825FI0J0PF}

O recurso Linha de base permite criar uma versão dos tópicos e ativos que pode ser usada para publicação ou tradução. Por exemplo, se o mapa DITA tiver `topicA` e `imageA`, você pode criar uma linha de base para usar a terceira versão do `topicA`, mas a quarta versão do `ImageA`. Depois que tiver uma Linha de base em vigor, você poderá publicar ou traduzir tópicos de diferentes versões com um único clique.

A seleção de uma Linha de base é opcional para predefinições de saída e um mapa DITA pode ter mais de uma Linha de base. No entanto, cada predefinição de saída em um mapa DITA pode ser associada a apenas uma única Linha de base. Se nenhuma Linha de base for especificada no momento da publicação, a saída será publicada usando a versão mais recente do conteúdo.

Da mesma forma, selecionar uma Linha de base para traduzir o conteúdo é opcional. No entanto, se você optar por traduzir o conteúdo usando uma Linha de base, o conteúdo da Linha de base também será salvo junto com as cópias traduzidas. Em seguida, você pode usar a Linha de base traduzida para executar outras operações, como compartilhá-la com editores externos ou arquivá-la. Para obter mais informações sobre como exportar uma Linha de Base traduzida, consulte [Exportar linha de base traduzida](#id196SE600GHS).

>[!TIP]
>
> Consulte a *Linha de base* seção no guia de práticas recomendadas para obter as práticas recomendadas relacionadas ao trabalho com linhas de base.

O administrador pode configurar a guia Linha de base no painel do mapa. Para obter mais detalhes, consulte *Guia Configurar linha de base no painel do mapa DITA* no Guia de Instalação e Configuração.

Você pode acessar o recurso Linha de base executando as seguintes etapas:

1. Na interface do usuário do Assets, navegue até o arquivo de mapa DITA e clique nele.
1. Vá para o **Linhas de base** guia .

Na guia Linhas de base, é possível executar as seguintes ações:

- [Criar uma linha de base](#id195FI0I0MUQ)
- [Exibir o conteúdo de uma linha de base](#id195FI0I0TLN)
- [Editar, duplicar ou remover Linhas de Base](#id195FI0I0YJL)
- [Adicionar rótulos a uma linha de base](#id184KD0T305Z)

## Criar uma linha de base {#id195FI0I0MUQ}

Você pode criar uma Linha de base com uma versão específica dos tópicos e do conteúdo referenciado disponível em uma data e hora específicas, ou com um rótulo definido para uma versão dos tópicos. Você pode especificar individualmente as versões dos tópicos selecionados em uma Linha de base para que, cada vez que aplicar a Linha de base em fluxo de trabalho de publicação ou tradução, os tópicos selecionados e suas versões correspondentes sejam incluídos para geração ou tradução de saída.

Execute as seguintes etapas para criar uma linha de base:

1. Na página Linhas de base , clique em **Criar**.
1. Insira um nome para a Linha de Base em **Nome da linha de base**.
1. Em **Defina a versão com base em**, selecione uma das seguintes opções:

   - **Rótulo**: Selecione essa opção para escolher os tópicos de acordo com o rótulo aplicado a eles. Insira um rótulo para filtrar a lista com base na string inserida. Na lista filtrada, é possível escolher um rótulo para selecionar tópicos e outros ativos com o rótulo especificado.

      Ao selecionar **Rótulo**, você também recebe uma opção adicional para usar a versão mais recente dos tópicos que não têm o rótulo especificado aplicado neles. Se você não selecionar essa opção e houver um tópico ou arquivo de mídia que não tenha o rótulo especificado, o processo de criação da linha de base falhará. Para obter mais informações sobre como adicionar rótulos, consulte [Usar rótulos](web-editor-use-label.md#).

   - **Versão em** &lt;*carimbo de data e hora*\>: Seleciona a versão dos tópicos como na data e hora especificadas. Observe que a hora especificada aqui corresponde ao fuso horário do seu servidor AEM. Se o servidor estiver em um fuso horário diferente, os tópicos serão selecionados de acordo com o fuso horário do servidor e não com o fuso horário local.

   Depois de selecionar um rótulo ou versão como data, todos os tópicos e arquivos de mídia referenciados no mapa serão selecionados adequadamente. Essa seleção de tópicos não é mostrada na interface do usuário, mas é salva no back-end.

1. Se quiser usar uma versão diferente para um ou mais tópicos, poderá fazer isso selecionando manualmente esses tópicos. Clique em **Pesquisar tópico**, selecione o tópico para o qual deseja usar uma versão diferente. Na lista suspensa Selecionar uma versão para o tópico selecionado, selecione uma versão do tópico que deseja usar na linha de base e clique em **OK**.

   ![](images/baseline-select-version-drop-down.png)

   As informações sobre o tópico e sua versão selecionada são armazenadas no back-end. Você pode repetir essa etapa para alterar a versão selecionada de vários tópicos.

1. Clique no botão **Procurar todos os tópicos** link para carregar todos os tópicos e arquivos de mídia referenciados do mapa DITA.A UUID de tópicos e arquivos de mídia também é mostrada abaixo do título do tópico ou do nome do arquivo \(mídia\).

   >[!NOTE]
   >
   > Se você tiver um conjunto muito grande de arquivos no mapa DITA, com mapas e tópicos aninhados, clicar em Procurar todos os tópicos poderá levar algum tempo para carregar todos os arquivos.

   O conteúdo do mapa é apresentado nas três seções: o arquivo de mapa, Conteúdo \(referências de tópico\) e Conteúdo referenciado \(tópicos aninhados, mapas e outros ativos\). Após ter todo o conteúdo referenciado disponível, você pode selecionar individualmente a versão do tópico que deseja usar na linha de base.

   O **Versão** a lista suspensa mostra as versões disponíveis dos tópicos ou do conteúdo referenciado. Para o conteúdo referenciado, você tem a opção de escolher uma versão automaticamente.

   Se você escolher **Selecionar Automaticamente** para o conteúdo referenciado, o sistema escolhe automaticamente a versão do conteúdo referenciado correspondente à versão do conteúdo no qual é referenciado. Por exemplo, digamos que um tópico A tenha uma referência a uma imagem B. Quando a versão 1.5 do tópico A foi criada, a versão da imagem B era 1.2 no repositório. Agora, quando uma linha de base é criada com a versão 1.5 do tópico A com a imagem B definida como **Selecionar Automaticamente**, o sistema selecionará automaticamente a versão 1.2 da imagem B.

   Se você criar uma linha de base usando os rótulos , **Selecionar Automaticamente** é aplicada à versão de todo o conteúdo referenciado.

   Se o conteúdo ou os ativos referenciados \(tópico, submapas, imagens ou vídeos\) não tiverem controle de versão \(como o conteúdo recém-carregado\), a criação de uma linha de base criará uma versão para esses arquivos. No entanto, se os arquivos tiverem controle de versão, nenhuma versão incremental será criada para esses arquivos. Esse comportamento é controlado pela configuração de versão de criação automática, que é habilitada por padrão. Isso também é necessário para a tradução de conteúdo, onde o processo de tradução espera que todos os arquivos tenham uma versão.

   >[!NOTE]
   >
   > Se quiser especificar uma versão diferente para qualquer recurso específico, é possível fazer isso escolhendo a versão desejada no **Versão** lista suspensa.

1. Clique em **Salvar**.

## Exibir o conteúdo de uma linha de base {#id195FI0I0TLN}

É possível exibir o conteúdo de uma Linha de Base existente clicando na guia Linhas de Base e selecionando a versão da Linha de Base desejada na lista. A página Linhas de base é dividida em três partes: arquivo de mapa DITA, conteúdo ou tópicos do mapa e o conteúdo referenciado. Se o seu mapa contiver submapas, os tópicos referenciados do submapa também serão exibidos na seção Conteúdo . As várias colunas na página Linha de Base estão descritas abaixo:

- **Nome**: Lista o mapa DITA, o título do tópico ou o nome do ativo, como o nome do arquivo de uma imagem.

- **Tipo**: Lista o tipo ou o tipo de ativo no mapa, como mapa DITA, tópico DITA ou formato de imagem.

- **Versão**: Lista a versão do ativo disponível na Linha de base.

- **Data e hora da versão**: Lista a data e a hora de criação do ativo para a versão selecionada.

- **Mais recentes**: Lista se a versão mais recente do ativo é usada na Linha de Base.

- **Mapa principal**: Se o arquivo de mapa contém submapas, essa coluna contém o nome do mapa no qual um tópico é referenciado.

- **Rótulo**: Lista o rótulo\(s\) aplicado à versão do tópico.

- **Referenciado por**: Essa coluna está disponível somente para o conteúdo referenciado. Indica o tópico principal do ativo referenciado. Caso um ativo seja referenciado por vários tópicos, os tópicos serão separados por vírgulas.

## Editar, duplicar ou remover Linhas de Base {#id195FI0I0YJL}

**Editar Linhas de Base**

Execute as seguintes etapas para editar uma linha de base existente:

1. Selecione a Linha de base e clique em **Editar**.
1. Faça as alterações necessárias na linha de base. Você pode alterar o nome e a versão do tópico ou do conteúdo referenciado.
1. Clique em **Salvar**.

**Duplicar Linhas de Base**

Selecione a Linha de base e clique em **Duplicar** para criar uma cópia de uma linha de base existente. Especifique um nome diferente para a linha de base e escolha o número da versão para os tópicos e o conteúdo referenciado e clique em **Salvar**.

**Remover Linhas de Base**

Selecione a versão das Linhas de Base e clique em **Remover** para remover uma linha de base.

## Adicionar rótulos a uma linha de base {#id184KD0T305Z}

A adição de rótulos a cada tópico pode ser demorada. AEM Guias fornece um mecanismo de clique único para adicionar rótulos a vários tópicos e ao conteúdo referenciado em um mapa DITA.

Execute as seguintes etapas para adicionar um rótulo a vários tópicos e ao conteúdo referenciado em um mapa DITA:

1. Na página Linhas de base , selecione uma linha de base contendo os tópicos e o conteúdo referenciado no qual deseja adicionar um rótulo.

   >[!NOTE]
   >
   > Certifique-se de que sua linha de base não tenha a versão mais recente de nenhum tópico ou ativo. Um rótulo só pode ser adicionado a um tópico ou ativo com versão.

1. Clique em **Adicionar rótulos**.

   ![](images/add-label-baseline-uuid.png)

1. No **Adicionar etiqueta** , especifique um rótulo exclusivo para associar a essa linha de base.

   Se o administrador configurou rótulos predefinidos, eles serão exibidos em uma lista suspensa. Você precisa escolher um rótulo na lista.

1. Se quiser aplicar o rótulo aos tópicos referenciados nos submapas, selecione **Aplicar etiqueta a mapas e dependentes filhos** opção.

   - Clique em **Adicionar**.
O rótulo especificado é adicionado ao mapa DITA e aos tópicos e conteúdo referenciados.

      ![](images/label-added-baseline-uuid.png)


## Exportar linha de base traduzida {#id196SE600GHS}

Você pode usar a Linha de base para traduzir o conteúdo. Por exemplo, você pode criar uma linha de base para a versão 1.1 que está pronta para tradução em francês. Na guia Tradução , é necessário usar a Linha de base para filtrar o conteúdo, em seguida, selecionar a Linha de base da versão 1.1 do conteúdo. Usar a linha de base para traduzir o conteúdo facilita o gerenciamento do conteúdo.

Depois que o conteúdo é traduzido, você pode exportar a linha de base traduzida para arquivamento ou compartilhá-la com equipes diferentes em sua organização. Você deve considerar os seguintes pontos antes de exportar uma Linha de Base traduzida:

- A exportação de uma Linha de base só é possível após a tradução do conteúdo na Linha de base. Se você tentar exportar uma linha de base para a qual a tradução não foi iniciada ou não foi concluída, aparecerá um erro.
- Você só pode transferir a Linha de base para uma versão já traduzida. Por exemplo, se você criou uma Linha de base para a versão 1.1 do seu conteúdo e a mesma for traduzida, é possível exportar essa linha de base. No entanto, se tiver criado uma Linha de base para a versão 1.2, que não foi traduzida, não será possível exportar essa Linha de base.
- Se uma Linha de base já tiver sido exportada, é possível substituir a linha de base existente selecionando a variável *Substituir Linha de Base Existente* durante a exportação.

Execute as seguintes etapas para exportar uma linha de base traduzida:

1. Abra o mapa DITA que contém a Linha de base traduzida.

1. No **Tradução** , expanda a **Linha de base** disponível no painel esquerdo.

   ![](images/export-baseline.png)

1. Selecione o **Usar linha de base** e escolha a Linha de Base que deseja exportar.

1. Clique em **Exportar linha de base**.

   O Status da exportação é exibido. Se o processo for bem-sucedido, será exibida uma mensagem mencionando o idioma para o qual a Linha de base é exportada. No caso de uma falha, a causa da falha é exibida.

   Se você tentar exportar a Linha de Base que já foi exportada, também será exibida a mensagem de falha de criação da Linha de Base .

1. \(Opcional\) Para exportar uma Linha de Base que já foi exportada, selecione **Substituir Linha de Base Existente** e, em seguida, clique em **Exportar linha de base**.


**Tópico principal:**[ Geração de saída](generate-output.md)

