---
title: Gerar saída para um mapa DITA a partir do console de mapa
description: Saiba como Gerar saída para um mapa DITA no console de mapa
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---


# Gerar saída para um mapa DITA a partir do console de mapa {#id1825FG00UHT}

Execute as seguintes etapas para gerar saída para um mapa DITA:

1. Na interface do usuário do Assets, navegue até o arquivo de mapa DITA que deseja publicar e clique nele.

   O console de mapa DITA é exibido com a lista de Predefinições de saída disponíveis para gerar saída.

1. Selecione uma ou várias Predefinições de Saída que você deseja usar para gerar a saída.

   ![](images/generate-multiple-outputs-uuid.png)

   >[!NOTE]
   >
   > Se você estiver gerando a saída do Site de AEM, o processo de publicação usará a estrutura definida na variável `.ditamap` para criar AEM estrutura do Site.

1. Clique no ícone Generate para iniciar o processo de geração de saída.


Você pode visualizar o status atual da solicitação de geração de saída clicando em Saídas. Para obter mais informações, consulte [Exibir o status da tarefa de geração de saída](#viewing_output_history)

>[!IMPORTANT]
>
> Se um processo de geração de saída para uma predefinição estiver na fila ou em andamento, não será possível iniciar outra tarefa de geração de saída para a mesma predefinição.

Você pode gerar a saída do PDF para uma ou mais predefinições de saída criadas para um mapa DITA no Editor da Web. Para obter mais detalhes, consulte [Usar o painel Geração rápida para gerar e exibir a saída das predefinições](web-editor-quick-generate-panel.md#).

Você também pode gerar a saída do Site de AEM para um ou mais tópicos, ou o mapa DITA inteiro do Editor da Web. Para obter mais detalhes, consulte [Publicação baseada em artigo no Editor da Web](web-editor-article-publishing.md#id218CK0U019I).

## Geração de produção incremental {#generating_standalone_topic}

>[!NOTE]
>
> A geração de saída incremental é aplicável somente para AEM saída do Site. Além disso, você só pode gerar novamente os tópicos DITA \(.dita/.xml\) de um mapa ou submapas DITA. Se você selecionar um mapa DITA, submapa, grupo de tópicos ou um tópico com `@processing-role="resource-only"`, então a opção regenerar não está disponível.

Pode haver várias instâncias em que você atualizaria apenas alguns tópicos no mapa DITA e enviaria apenas esses tópicos atualizados para o ativo. Para lidar com esses cenários, os Guias de AEM permitem criar saídas incrementais. Se você atualizou alguns tópicos, não precisará gerar novamente o mapa DITA inteiro. Você pode selecionar apenas os tópicos atualizados e regenerá-los.

Se o mapa estiver fragmentado e você tiver atualizado um único tópico nesse mapa, será necessário gerar novamente o mapa inteiro para o tópico ou conteúdo atualizado para refletir na saída. Você não obterá a opção de regeneração de saída em um nível de tópico, ela só estará disponível no nível de mapa \(fragmentado\). Isso é aplicável ao mapa pai e a todos os submapas.

Execute as seguintes etapas para gerar novamente a saída de um tópico específico ou de um grupo de tópicos:

>[!IMPORTANT]
>
> Quando você está regenerando a saída do Site de AEM, a saída é criada usando a versão atual dos arquivos e não a linha de base anexada.

1. Na interface do usuário do Assets, navegue até o arquivo de mapa DITA e clique nele.

   O console de mapa DITA é exibido com a lista de Predefinições de saída disponíveis para gerar saída.

1. Selecione o **Tópicos** guia .

   Uma lista de tópicos disponíveis no mapa DITA é exibida.

1. Selecione os tópicos que deseja gerar novamente.

   >[!NOTE]
   >
   > Se você tiver adicionado novos tópicos ao mapa DITA, não poderá gerar esses novos tópicos a partir daqui. Primeiro, publique os tópicos recém-adicionados usando a função de publicação do mapa DITA.

   ![](images/regenerate-topics.png)

1. Clique em **Regenerar**.

   A página Gerar novamente tópicos selecionados é exibida.

1. Selecione a predefinição de saída que deseja usar para gerar novamente os tópicos selecionados.

1. Clique em **Regenerar** para iniciar o processo de geração de saída.


>[!IMPORTANT]
>
> Se você renomear um título de tópico e gerar novamente o tópico, o título do tópico atualizado não será refletido no índice do mapa DITA. Para atualizar o título do tópico no TOC, você deve gerar o mapa DITA inteiro.

Você pode visualizar o status atual da solicitação de geração de saída clicando em Saídas. Para obter mais informações, consulte [Exibir o status da tarefa de geração de saída](#viewing_output_history).

## Exibir o status da tarefa de geração de saída {#viewing_output_history}

Depois de iniciar a tarefa de geração de saída para um mapa ou gerar novamente os tópicos selecionados, AEM Guias envia essa tarefa para a fila de geração de saída. Essa fila é atualizada em tempo real, mostrando o status de cada tarefa de geração de saída na fila.

Execute as seguintes etapas para exibir a fila de geração de saída:

1. Na interface do usuário do Assets, navegue e clique no arquivo de mapa para o qual deseja verificar o status de geração de saída.

1. Clique em **Saídas**.

   ![](images/output-queued.png)

   A página Saídas é dividida em duas partes:

   - **Saídas em fila:**

      Lista as saídas que estão aguardando para serem geradas ou que estão em processo de geração. As tarefas em fila ou em andamento são mostradas com um ícone de cor azul antes do nome predefinido. Você também pode encontrar a configuração de geração de saída ou a predefinição usada para a tarefa em fila, o tipo, o usuário que iniciou a tarefa, o tempo desde quando a tarefa está em fila e o status atual.

      Clique no link para acessar o **Publicar painel** e exibir o status de execução atual. Uma lista de todas as tarefas de publicação ativas está disponível no Painel de publicação. O **Saídas em fila** e **Publicar painel** são exibidos somente quando há saídas que estão aguardando para serem geradas ou que estão em processo de geração. Eles não aparecem quando as tarefas de saída são concluídas. Para obter mais detalhes sobre o Painel de Publicação, consulte [Gerenciar tarefas de publicação usando o painel Publicar](generate-output-publish-dashboard.md#).

   - **Saídas Geradas**

      Lista as tarefas de saída que foram concluídas. Novamente, as informações mostradas aqui são semelhantes à seção Saídas na fila com algumas diferenças. Você tem um novo conjunto de informações na forma do ícone de resultado de saída e o tempo de geração de saída.

      Nesta lista, você pode ter tarefas que foram executadas com êxito, tarefas que foram executadas com mensagem ou tarefas com falha. As tarefas bem-sucedidas são mostradas com o ícone de cor verde, as tarefas com uma mensagem têm um ícone de cor laranja e as tarefas com falha são mostradas com o ícone de cor vermelha.

      Para todas as tarefas, o processo de publicação cria um arquivo de log \(logs.txt\) que pode ser acessado ao clicar no link na coluna Gerado em . Para tarefas que falharam ou que têm mensagens, você pode verificar o arquivo de log, que é explicado na seção . [Visualizar e verificar o arquivo de log](generate-output-basic-troubleshooting.md#id1822G0P0CHS).

      >[!NOTE]
      >
      > Ao clicar em um link da saída do PDF gerado, você é solicitado a baixar o PDF. Esse é o comportamento padrão nos AEM 6.5 e 6.4.


## Cancelar uma tarefa de geração de saída {#id2061H100T5Z}

Os Guias de AEM oferecem aos editores uma maneira simples e fácil de cancelar qualquer tarefa de publicação em andamento. Como editor, você pode cancelar uma tarefa de publicação em andamento no console do mapa DITA ou no [Publicar painel](generate-output-publish-dashboard.md#).

Execute as seguintes etapas para cancelar uma tarefa de geração de saída do console de mapa DITA:

1. Na interface do usuário do Assets, navegue e clique no arquivo de mapa para o qual deseja cancelar uma tarefa de geração de saída em andamento.

1. Clique em **Saídas**.

1. Na lista Saídas em fila, passe o ponteiro do mouse sobre uma tarefa que deseja cancelar.

1. Clique no botão *Cancelar esta Tarefa* ícone .

   ![](images/cancel-publish-task-map-console.png)

1. Clique em **Sim** no prompt Confirmar mensagem de cancelamento.

   ![](images/confirm-cancel-output-map-condole.png)

   Se a tarefa ainda não tiver sido iniciada, o comando cancel será executado na tarefa. Para uma tarefa que está sendo cancelada, o Status é definido como Cancelar.

   Depois que a tarefa for cancelada com êxito, ela será movida para a função **Saídas Geradas** com uma **Cancelado** status. Ao passar o mouse sobre a tarefa cancelada, ele mostra o nome do usuário que cancelou a tarefa. Na captura de tela a seguir, a variável *HTML5* tarefa cancelada.

   ![](images/cancelled-output-task.png)


## Excluir uma tarefa de saída do console de mapa DITA

Quando você gera várias saídas para um mapa DITA, durante um período a lista de Saídas Geradas para esse mapa se torna muito longa. Como editor, você pode limpar o histórico de saída de qualquer arquivo de mapa removendo as tarefas desatualizadas do *Saídas Geradas* lista. Observe que a saída não é removida do sistema, somente a entrada da saída gerada é removida do *Saídas Geradas* lista.

Execute as seguintes etapas para remover uma tarefa de saída da lista Saída gerada:

1. Na interface do usuário do Assets, navegue até o arquivo de mapa do qual deseja excluir as tarefas e clique nele.

1. Clique em **Saídas**.

1. Na lista Saídas Geradas , passe o ponteiro do mouse sobre uma tarefa que deseja excluir.

1. Clique no ícone excluir.

   ![](images/delete-output-task.png)

1. Clique em **Sim** no prompt de mensagem Confirmar exclusão.

   A tarefa é excluída da lista de Saídas Geradas.


**Tópico principal:**[ Geração de saída](generate-output.md)

