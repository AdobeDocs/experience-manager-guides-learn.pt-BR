---
title: Gerenciar tarefas de revisão usando o Painel de revisão
description: Saiba como gerenciar tarefas de revisão usando o Painel de revisão
source-git-commit: f3d747082103c73a365ee400cbd4dcdabd36eabf
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---


# Gerenciar tarefas de revisão usando o Painel de revisão {#id2056B0Y70X4}

O fluxo de trabalho de gerenciamento de revisão pode incluir várias tarefas. Por exemplo, é possível adicionar revisores para um tópico específico ou estender o prazo para uma revisão. Você também pode querer marcar a tarefa de revisão como concluída se achar que todos os participantes deram seus comentários. Essas tarefas podem ser gerenciadas usando o Painel de revisão.

Execute as seguintes etapas para acessar e usar o Painel de revisão:

>[!NOTE]
>
> Você pode gerenciar tarefas de revisão somente para os projetos para os quais você é o Autor \(ou iniciador\). Mesmo se você for Revisor ou Publicador \(usuário\), não terá acesso a nenhuma das tarefas do projeto.

1. No **Projetos** , clique no projeto de revisão que deseja gerenciar.

   Um painel Projeto com blocos de tarefas é exibido.

   ![](images/review-management.png)

1. Clique nos três pontos no **Resenhas** mosaico.

   O Painel de revisão é exibido. O painel lista todas as tarefas de revisão que você criou.

   ![](images/review-dashboard.png)

   O Painel de Revisão exibe os detalhes sobre a tarefa de revisão, como o nome da tarefa, quem iniciou a revisão, a data em que a revisão foi iniciada, a data de vencimento, o status, o número de novos comentários que não foram aceitos ou rejeitados pelo autor e o nome dos revisores. As tarefas são listadas na ordem de tarefas recém-criadas para tarefas mais antigas.

   >[!NOTE]
   >
   > Se você clicar no link Revisar tarefa , o tópico ou arquivo de mapa enviado para revisão será aberto.

1. Selecione uma tarefa de revisão.

   Você verá Editar propriedades e [Status](#check-review-status-id199RF0A0UHS) na barra de ferramentas.

1. Se você clicar em **Editar propriedades**, a página Detalhes da tarefa é exibida.

   Há três guias na página Detalhes da tarefa - Tarefa, Conteúdo e Revisores. As seções a seguir explicam as várias funções disponíveis em cada guia.


## Guia Tarefa

![](images/review-task-page.png)

Você pode executar as seguintes ações no **Tarefa** guia :

- Modifique o título da tarefa na **Título** campo.
- Adicione os destinatários padrão no **Atribuir a** lista suspensa. Os revisores adicionados a partir daqui recebem acesso para revisar todos os tópicos que fazem parte dessa tarefa de revisão. Você pode optar por remover ou adicionar seletivamente mais revisores a tópicos específicos da [Guia Revisores](#reviewer-tab-id199RF0N0MUI).
- Atualize a descrição da tarefa no **Descrição** campo.
- Modifique o **Data de vencimento**. Você pode antecipar ou adiar o prazo para a conclusão da tarefa.
- Selecione a opção para restringir que os usuários revisem apenas os tópicos atribuídos a eles.
- Clique em **Atualizar** para atualizar os detalhes modificados.
- Clique em **Concluído** para marcar a tarefa de revisão como concluída antes da data de vencimento. Quando a tarefa de um tópico individual é marcada como Concluído, a revisão do tópico selecionado é fechada. No entanto, no caso de tópicos compartilhados para revisão por meio de um mapa DITA, marcar a tarefa do mapa DITA como Complete encerrará a revisão de todos os tópicos no mapa que foram compartilhados para revisão.
- Clique em **Duplicar** para criar uma cópia da tarefa de revisão. O processo de criação de uma tarefa de revisão duplicada é semelhante à criação de uma nova tarefa de revisão. Depois de iniciar o fluxo de trabalho da tarefa duplicada, é exibida a página Criar tarefa de revisão . Você precisa fornecer os novos detalhes da tarefa, conforme explicado em [Enviar tópicos para revisão](review-send-topics-for-review.md#).

   Se você selecionou uma tarefa de revisão criada a partir de um mapa DITA, será mostrado os tópicos que são parte do mapa. Você pode escolher os tópicos que deseja incluir na nova tarefa de revisão.

   No caso de tarefa de revisão duplicada de um ou vários tópicos serem revisados, apenas esses tópicos serão mostrados na lista de tarefas de revisão. Você pode optar por compartilhar esses tópicos para revisão com um conjunto diferente de revisores.

- Clique em **Fechar** para acessar a página Caixa de entrada.

## Guia Content

![](images/review-content-page.png)

Você pode executar as seguintes ações no **Conteúdo** guia :

- Alterar a versão do tópico enviado para revisão. Você pode escolher a versão mais recente do tópico, a versão como data, a versão com rótulo específico ou a versão com uma linha de base específica \(para um mapa DITA\).

- Clique em **Atualizar** para compartilhar a versão atualizada do tópico com os revisores. Os revisores recebem uma notificação por e-mail informando que a versão mais recente do tópico foi enviada para revisão. Na próxima vez que um revisor abrir o tópico, ele verá a versão atualizada do tópico.

   >[!NOTE]
   >
   > No caso de uma versão atualizada de um tópico, os comentários antigos também são retidos na versão mais recente. Os revisores também podem ver as diferenças entre as duas versões.

- Clique em **Concluído** para marcar a tarefa de revisão como concluída antes da data de vencimento. Quando a tarefa de um tópico individual é marcada como Concluído, a revisão do tópico selecionado é fechada. No entanto, no caso de tópicos compartilhados para revisão por meio de um mapa DITA, marcar a tarefa do mapa DITA como Complete encerrará a revisão de todos os tópicos no mapa que foram compartilhados para revisão.

- Clique em **Duplicar** para criar uma nova tarefa de revisão usando a tarefa atual como base.


## Guia Revisores {#reviewer-tab-id199RF0N0MUI}

![](images/reviewers-tab.png)

Você pode executar as seguintes ações no **Revisores** guia :

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

## Verifique o status de uma tarefa de revisão {#check-review-status-id199RF0A0UHS}

Na página principal Revisar painel , se você selecionar uma tarefa de revisão e clicar em **Status**, o relatório de status da tarefa de revisão é mostrado:

![](images/review-status-report.png)

O relatório de status da tarefa de revisão contém os seguintes detalhes:

- Nome\(s\) do revisor ao qual a tarefa de revisão está atribuída.
- A coluna Status indica o status da revisão. O Status pode ser um dos seguintes:
   - **Não iniciado**: O revisor ainda não abriu o link de revisão.
   - **Em Andamento**: O revisor abriu o link de revisão e está em processo de revisão do tópico.
   - **Concluído**: O revisor concluiu a revisão concluindo a tarefa de revisão atribuída a ele. A tarefa de revisão está na Caixa de entrada de notificação de AEM para cada revisor.
- Quando um revisor abre um link de revisão e navega até um tópico específico que é adicionado à lista Tópicos revisados . Isso ajuda os autores a determinar se os revisores abriram ou não as respectivas seções. Se forem apresentados comentários, estes são apresentados entre parênteses.
- Número total de comentários feitos em todos os tópicos. No caso de vários tópicos em revisão, o número de comentários para cada tópico é mencionado \(entre colchetes\) em relação ao nome do tópico.
- A data em que qualquer tópico foi acessado pela última vez pelo revisor.

**Tópico principal:**[ Rever tópicos ou mapas](review.md)

