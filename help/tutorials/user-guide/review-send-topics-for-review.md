---
title: Enviar tópicos para revisão
description: Saiba como Enviar tópicos para revisão
exl-id: 7a9b36ad-44d4-4952-9906-d95feb95d0c6
source-git-commit: 8823669fd29e8a40a41f9ca5d654b38fbea8e2fa
workflow-type: tm+mt
source-wordcount: '2733'
ht-degree: 0%

---

# Enviar tópicos para revisão {#id199RD0S035Z}

O fluxo de trabalho de revisão cria um ambiente de vários revisores, em que o iniciador especifica uma lista de tópicos para revisão, adiciona vários revisores e atribui uma linha do tempo para a tarefa de revisão. AEM Guias permite que os usuários pertencentes aos grupos Autores e Editores iniciem uma revisão.

Como o fluxo de trabalho de revisão é específico do projeto, o iniciador da revisão deve fazer parte da equipe do projeto ou ter direitos para criar um projeto. No momento da criação de um projeto, você define os membros da equipe para o projeto e atribui a eles várias funções ou grupos. Para obter mais informações sobre projetos, consulte [Criar um projeto DITA](authoring-create-dita-project.md#).

Você pode criar uma tarefa de revisão a partir de:

- **Editor da Web**: Permite enviar um tópico individual ou mapa DITA para revisão. Observe que o fluxo de trabalho para criar uma tarefa de revisão é comum no Editor da Web e na interface do usuário do Assets. Somente o método de inicialização do workflow de revisão é diferente. Para obter informações sobre como iniciar o workflow de revisão no Editor da Web, consulte o [Criar tarefa de revisão](web-editor-features.md#id215OCJ00JXA) no Editor da Web.

- **Interface do usuário do Assets**: Permite enviar um ou vários tópicos e o mapa DITA para revisão. O compartilhamento de documentos para revisão do fluxo de trabalho da interface do usuário do Assets é abordado neste tópico.


Na interface do usuário do Assets, há duas maneiras pelas quais um Autor/Editor pode criar uma tarefa de revisão:

- Enviar um ou mais tópicos para revisão
- Enviar vários tópicos de um mapa DITA para revisão

## Enviar um ou mais tópicos para revisão {#id1721E600FY4}

>[!IMPORTANT]
>
> Antes de criar uma tarefa de revisão, verifique se você criou um projeto e adicionou revisores a esse projeto.

Para criar uma tarefa de revisão e enviar tópicos para revisão, execute as seguintes etapas:

>[!NOTE]
>
> Você pode criar uma tarefa de revisão somente se for um autor ou editor em um projeto DITA.

1. Navegue até a pasta desejada na interface do usuário do Assets.

1. Clique no ícone Selecionar na ação rápida e selecione os tópicos que deseja enviar para revisão.

   ![](images/select-asset-62.png){width="300" align="left"}

1. Na barra de ferramentas, clique em **Criar tarefa de revisão**. A página de criação da tarefa de revisão é exibida.

   >[!NOTE]
   >
   > Você pode criar uma tarefa de revisão somente para os tópicos que têm uma revisão. Caso o tópico selecionado não tenha uma revisão, você receberá um prompt.

   ![](images/create-review-task-023.png){width="650" align="left"}

1. Insira um **Título** para a tarefa e selecione um DITA **Projeto** na lista suspensa.

1. No **Atribuir a** no campo suspenso , selecione os revisores para os quais deseja enviar os tópicos para revisão.

   Você pode atribuir uma tarefa de revisão a usuários individuais do projeto ou a grupos de usuários. Observe que é possível atribuir uma tarefa de revisão a usuários individuais somente quando você faz parte do grupo de administradores do projeto; caso contrário, você verá apenas os grupos de usuários no campo Atribuir a.

   >[!NOTE]
   >
   > O fluxo de trabalho de revisão é específico do projeto. Ao criar projetos, você adiciona os membros da equipe ao projeto e os atribui a grupos. Então, quando você seleciona o projeto aqui, você pode escolher os membros que fazem parte desse projeto. Para obter mais informações sobre projetos, consulte [Criar um projeto DITA](authoring-create-dita-project.md#).

1. Insira um **Descrição** para a tarefa.

   Essa descrição é usada como o corpo do email de notificação enviado aos revisores.

1. Selecione o **Data de vencimento** e a hora para marcar o prazo para a revisão.

   >[!NOTE]
   >
   > Ao atingir o prazo, um email é enviado ao iniciador notificando que a tarefa de revisão foi concluída. O iniciador pode estender o prazo da tarefa de revisão a partir do [Painel de revisão](review-manage-tasks-review-dashboard.md#).

1. Selecione o mapa raiz no **Caminho do Rootmap**. Este roteiro é usado para resolver todas as referências principais e termos de glossário usados no conteúdo da revisão. Se você não selecionar o rootmap, as principais referências ou termos de glossário associados ao tópico DITA não serão resolvidos antes de enviar o tópico para revisão.

   Se você estiver criando a revisão de um mapa DITA, então por padrão **Caminho do Rootmap** é definida para o caminho desse mapa. Se você estiver criando a revisão para um único ou vários tópicos, então por padrão a variável **Caminho do Rootmap** é definida como o mapa definido nas Preferências do usuário.

   >[!NOTE]
   >
   > O mapa-raiz selecionado tem a maior precedência para resolver referências-chave. Para obter mais detalhes, consulte [Resolver referências de chave](map-editor-other-features.md#id176GD01H05Z).

1. Como é possível atribuir diferentes revisores a tópicos diferentes, **Permitir que os destinatários analisem qualquer tópico** controla se os revisores podem revisar todos os tópicos em uma tarefa de revisão ou apenas os tópicos que estão atribuídos à revisão.

   Se desejar permitir que todos os revisores revisem qualquer tópico na tarefa de revisão, selecione **Permitir que os destinatários analisem qualquer tópico**.

   Se você não selecionar essa opção, os revisores serão adicionados à **Atribuir a** terá acesso para revisar apenas os tópicos atribuídos a eles.

1. Clique em **Avançar**.

   A página Conteúdo é exibida.

   ![](images/content_page_review.png){width="800" align="left"}

1. Na página Conteúdo , selecione uma versão do tópico que deseja compartilhar para revisão.

   Você pode usar um dos métodos a seguir para selecionar uma versão:

   - *\(Padrão\)* Escolha a opção **Sua Versão Mais Recente** para selecionar a última revisão salva dos tópicos.
   - Escolha a **Versão ativada** e especifique a data e a hora para selecionar uma versão como na data e hora especificadas. Se não houver versão do tópico disponível na data especificada, então uma versão disponível imediatamente após a data e hora especificadas será selecionada.
   - Escolha a **Selecionar um rótulo** e selecione um rótulo na lista suspensa.
1. Depois de fazer a seleção para escolher uma versão, clique em **Aplicar**.

   A versão baseada na opção selecionada é escolhida para os tópicos.

   >[!NOTE]
   >
   > Você também pode selecionar manualmente a versão desejada no **Versão** lista suspensa de cada tópico.

1. Clique em **Avançar**.

   A página Revisores é exibida, onde você pode adicionar ou remover revisores. Por padrão, os revisores adicionados no campo Atribuir a são adicionados automaticamente a cada tópico selecionado para a revisão.

   ![](images/add-reviewers-topics.png){width="650" align="left"}

1. Na página Revisores , é possível adicionar ou remover revisores. As seguintes operações estão disponíveis na página Revisores:

   - **Selecionar tudo**: Seleciona todos os tópicos na lista de tópicos. Você pode executar facilmente uma operação em lote após selecionar todos os tópicos.
   - **Limpar seleção**: Desmarca os tópicos selecionados na lista de tópicos.

      >[!NOTE]
      >
      > Você também pode selecionar ou desmarcar um tópico individualmente clicando na caixa de seleção ao lado do tópico.

   - **Adicionar**: Exibe a caixa de diálogo Adicionar Revisores. Você pode digitar o nome de um revisor ou função de usuário \(ou grupo\) que deseja adicionar como revisor aos tópicos selecionados.
   - **Remover**: Exibe a caixa de diálogo Remover Revisores. Você pode digitar o nome de um revisor ou função de usuário \(ou grupo\) que deseja remover como revisor dos tópicos selecionados.

      >[!NOTE]
      >
      > Também é possível remover uma revisão de um tópico clicando no sinal de cruz na caixa do revisor.

   - **Atribuir novamente**: Exibe a caixa de diálogo Atribuir Revisores. Você pode digitar o nome de um revisor ou função de usuário \(ou grupo\) ao qual deseja atribuir a tarefa de revisão. Isso remove todos os revisores existentes dos tópicos selecionados e atribui os revisores recém-selecionados a esses tópicos.
   - **Exportar**: Permite exportar os detalhes da tarefa de revisão em um arquivo CSV. O arquivo contém detalhes como o caminho e o título do tópico, o nome do revisor e a versão dos tópicos enviados para revisão.
   - **Editar Revisores**: Clicar no ![](images/edit_pencil_icon.svg)ícone na lista de tópicos exibe a caixa de diálogo Editar Revisores . É possível adicionar ou remover revisores para o tópico selecionado nessa caixa de diálogo.
1. Clique em **Criar** para criar a tarefa de revisão.

   Uma mensagem de confirmação é exibida quando a tarefa de revisão é criada com êxito. O [Estado do documento](web-editor-document-states.md#) para os tópicos enviados para revisão é definido como Em revisão.

   >[!NOTE]
   >
   > Você também pode clicar em Notifications bell na parte superior direita da tela e confirmar que a tarefa de revisão foi criada com êxito. No painel Notificações , você encontrará uma notificação cada para os revisores que faziam parte da tarefa de revisão e uma notificação para o iniciador da revisão.


Um email é enviado a todos os revisores, notificando que eles receberam um tópico ou vários tópicos para revisão. O email contém um link direto no qual eles podem clicar e acessar o tópico em uma janela do navegador.

Caso vários tópicos sejam atribuídos, os revisores podem visualizá-los e selecioná-los em uma lista suspensa de tópicos no navegador da Web.

## Enviar vários tópicos para análise a partir de um mapa DITA

Um mapa DITA é uma organização lógica de tópicos dentro de um livro. Quando você envia um tópico individual para revisão, o revisor não recebe informações sobre a localização desse tópico no livro. Se um revisor tiver informações sobre a localização exata do tópico que está sendo revisado, ele obterá um contexto melhor do tópico que está sendo revisado.

AEM Guias permitem enviar um ou mais tópicos em um mapa DITA para revisão ao mesmo tempo. O revisor consegue ver o arquivo de mapa completo, juntamente com os tópicos que foram compartilhados para revisão. Isso facilita para o revisor obter um contexto do tópico no mapa ou no arquivo de livro.

Você pode compartilhar o mesmo mapa DITA no para análise em várias tarefas de revisão. Por exemplo, se em um mapa DITA houver o tópico A, B, C, D e E. Em uma tarefa de revisão, você pode compartilhar A, B e C para revisão e em outra tarefa de revisão, é possível enviar os tópicos C, D e E para revisão. O processo de revisão permite o compartilhamento do mesmo tópico e arquivo de mapa em várias tarefas de revisão. Para o tópico comum em várias tarefas de revisão, os comentários fornecidos em uma tarefa de revisão não substituem ou se mesclam aos comentários em outras tarefas de revisão.

>[!IMPORTANT]
>
> No caso de um tópico de um arquivo de mapa ter sido compartilhado em várias tarefas de revisão, seu status seria exibido em Revisão até que todas as tarefas de revisão tenham sido concluídas.

Para enviar um ou vários tópicos juntamente com o arquivo de mapa para revisão, execute as seguintes etapas:

>[!IMPORTANT]
>
> Depois de iniciar uma revisão por meio de um arquivo de mapa, você não deve alterar a estrutura do arquivo de mapa adicionando novos tópicos ou removendo tópicos existentes.

1. Navegue até a pasta desejada na interface do usuário do Assets.

   >[!NOTE]
   >
   > Verifique se a exibição do console está definida como exibição de cartão ou de lista.

1. Selecione o mapa para onde deseja enviar os tópicos para revisão.

1. Na barra de ferramentas, clique em **Criar tarefa de revisão**. A página de criação da tarefa de revisão é exibida.

1. Insira um **Título** para a tarefa e selecione um DITA **Projeto** na lista suspensa.

   >[!NOTE]
   >
   > Você pode criar uma tarefa de revisão somente para os tópicos que têm uma revisão. Caso seu mapa contenha tópicos que não têm uma revisão, você verá um prompt com uma lista desses arquivos. Arquivos sem uma revisão são excluídos da tarefa de revisão.

1. No **Atribuir a** no campo suspenso , selecione os revisores para os quais deseja enviar os tópicos para revisão.

   Você pode atribuir uma tarefa de revisão a usuários individuais do projeto ou a grupos de usuários. Observe que é possível atribuir uma tarefa de revisão a usuários individuais somente quando você faz parte do grupo de administradores do projeto; caso contrário, você verá apenas os grupos de usuários no campo Atribuir a.

   >[!NOTE]
   >
   > O fluxo de trabalho de revisão é específico do projeto. Ao criar projetos, você adiciona os membros da equipe ao projeto e os atribui a grupos. Então, quando você seleciona o projeto aqui, você pode escolher os membros que fazem parte desse projeto. Para obter mais informações sobre projetos, consulte [Criar um projeto DITA](authoring-create-dita-project.md#).

1. Insira um **Descrição** para a tarefa.

   Essa descrição é usada como o corpo do email de notificação enviado aos revisores.

1. Selecione o **Data de vencimento** e a hora para marcar o prazo para a revisão.

   >[!NOTE]
   >
   > Ao atingir o prazo, um email é enviado ao iniciador notificando que a tarefa de revisão foi concluída. O iniciador pode estender o prazo da tarefa de revisão a partir do [Painel de revisão](review-manage-tasks-review-dashboard.md#).

1. Como é possível atribuir diferentes revisores a tópicos diferentes, **Permitir que os destinatários analisem qualquer tópico** controla se os revisores podem revisar todos os tópicos em uma tarefa de revisão ou apenas os tópicos que estão atribuídos à revisão.

   Se desejar permitir que todos os revisores revisem qualquer tópico na tarefa de revisão, selecione **Permitir que os destinatários analisem qualquer tópico**.

   Se você não selecionar essa opção, os revisores serão adicionados à **Atribuir a** terá acesso para revisar apenas os tópicos atribuídos a eles.

1. Clique em **Avançar**.

   A página Conteúdo é exibida com todos os tópicos referenciados do arquivo de mapa. Se o mapa DITA contém mapas aninhados, os tópicos dos mapas aninhados também serão listados aqui.

   ![](images/content-page-map-review.png){width="800" align="left"}

1. Na página Conteúdo , selecione uma versão do tópico que deseja compartilhar para revisão.

   Você pode usar um dos métodos a seguir para selecionar uma versão:

   - *\(Padrão\)* Escolha a opção **Sua Versão Mais Recente** para selecionar a última revisão salva dos tópicos.
   - Escolha a **Versão ativada** e especifique a data e a hora para selecionar uma versão de acordo com a data e a hora. Se não houver versão do tópico disponível na data especificada, então uma versão disponível imediatamente após a data e hora especificadas será selecionada.
   - Escolha a **Selecionar um rótulo** e selecione um rótulo na lista suspensa. Todos os tópicos que contêm o rótulo selecionado são selecionados na variável **Versão** lista suspensa.
   - Escolha a **Selecionar uma Linha de Base** e selecione uma linha de base na lista suspensa. Todas as versões de tópico que fazem parte da linha de base selecionada são selecionadas na variável **Versão** lista suspensa.
1. Depois de fazer a seleção para escolher uma versão, clique em **Aplicar**.

   A versão baseada na opção selecionada é escolhida para os tópicos.

   >[!NOTE]
   >
   > Você também pode selecionar manualmente a versão desejada no **Versão** lista suspensa de cada tópico.

1. Clique em **Avançar**.

   A página Revisores é exibida, onde você pode adicionar ou remover revisores. Por padrão, os revisores adicionados no campo Atribuir a são adicionados automaticamente a cada tópico selecionado para a revisão.

1. Na página Revisores , é possível adicionar ou remover revisores. As seguintes operações estão disponíveis na página Revisores:

   - **Selecionar tudo**: Seleciona todos os tópicos na lista de tópicos. Você pode executar facilmente uma operação em lote após selecionar todos os tópicos.
   - **Limpar seleção**: Desmarca os tópicos selecionados na lista de tópicos.

      >[!NOTE]
      >
      > Você também pode selecionar ou desmarcar um tópico individualmente clicando na caixa de seleção ao lado do tópico.

   - **Adicionar**: Exibe a caixa de diálogo Adicionar Revisores. Você pode digitar o nome de um revisor ou função de usuário \(ou grupo\) que deseja adicionar como revisor aos tópicos selecionados.
   - **Remover**: Exibe a caixa de diálogo Remover Revisores. Você pode digitar o nome de um revisor ou função de usuário \(ou grupo\) que deseja remover como revisor dos tópicos selecionados.
   - **Atribuir novamente**: Exibe a caixa de diálogo Atribuir Revisores. Você pode digitar o nome de um revisor ou função de usuário \(ou grupo\) ao qual deseja atribuir a tarefa de revisão. Isso remove todos os revisores existentes dos tópicos selecionados e atribui os revisores recém-selecionados a esses tópicos.
   - **Exportar**: Permite exportar os detalhes da tarefa de revisão em um arquivo CSV. O arquivo contém detalhes como o caminho e o título do tópico, o nome do revisor e a versão dos tópicos enviados para revisão.
   - **Editar Revisores**: Clicar no ![](images/edit_pencil_icon.svg)ícone na lista de tópicos exibe a caixa de diálogo Editar Revisores . É possível adicionar ou remover revisores para o tópico selecionado nessa caixa de diálogo.

   >[!IMPORTANT]
   >
   > Você deve atribuir pelo menos um revisor para criar a tarefa de revisão.

1. Clique em **Criar** para criar a tarefa de revisão.

   Uma mensagem de confirmação é exibida quando a tarefa de revisão é criada com êxito. O [Estado do documento](web-editor-document-states.md#) para os tópicos enviados para revisão é definido como Em revisão.

   >[!NOTE]
   >
   > Você também pode clicar no painel Notificações na parte superior direita da interface e confirmar que a tarefa foi criada com êxito. No painel Notificações , você encontrará uma notificação cada para as revisões que faziam parte da tarefa de revisão e uma notificação para o iniciador da revisão.

   >[!IMPORTANT]
   >
   > Depois de iniciar uma revisão, você não deve mover ou excluir o mapa DITA ou os tópicos para um local diferente. Isso resultará em uma quebra no processo de revisão.


Um email é enviado a todos os revisores, notificando que eles receberam tópicos para revisão. O email contém um link direto no qual eles podem clicar e acessar o tópico em uma janela do navegador. Os tópicos junto com o mapa DITA são abertos no modo de revisão.

**Tópico principal:**[ Rever tópicos ou mapas](review.md)
