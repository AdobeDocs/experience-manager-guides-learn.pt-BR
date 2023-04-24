---
title: Criar um projeto DITA
description: Saiba como criar um projeto DITA
source-git-commit: 101766d51d43eb728f0316155acffd19548f83be
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---


# Criar um projeto DITA {#id1645HA00NM6}

AEM Guias fornece um modelo de projeto DITA que pode ser usado para criar e gerenciar as tarefas de revisão.

Você pode criar um projeto DITA e usá-lo para iniciar suas revisões. Um projeto permite definir um prazo e controlar as tarefas e o tempo necessário para concluir a tarefa de revisão para a qual você criou o projeto.

Você pode adicionar membros da equipe a um projeto que pode receber várias funções - Autores, Revisores e Editores.

Após criar o projeto DITA, é possível iniciar a revisão no Editor da Web ou na interface do usuário do Assets. Para obter mais detalhes, consulte [Enviar tópicos para revisão](review-send-topics-for-review.md#).

Da mesma forma, sempre que um autor inicia qualquer fluxo de trabalho de revisão, os membros selecionados do projeto recebem uma notificação por email. Para configurar notificações por email, consulte *Personalizar modelos de email* em Instalar e configurar os Guias do Adobe Experience Manager as a Cloud Service.

Execute as seguintes etapas para criar um projeto DITA:

1. Abra o console Projetos .

   Você também pode acessar o console Projetos usando o seguinte URL:

   ```http
   http://<server name>:<port>/projects.html
   ```

1. Clique em **Criar** \> **Projeto** para iniciar o assistente Criar projeto .

   ![](images/project-console-63.png)

1. Na página Criar projeto , selecione o **Projeto DITA** modelo e clique em **Próximo**.

1. Na página Propriedades do projeto , insira os seguintes detalhes:

   Informações no **Básico** guia :

   ![](images/create-project.png)

   - Insira o **Título**, **Descrição** e **Data de vencimento**.

   - Como opção, você pode escolher uma miniatura para o projeto.

   - Por padrão, você é o proprietário do projeto. Para adicionar mais usuários a este projeto:
   1. Insira ou escolha um usuário no **Usuário** lista suspensa.

   1. Escolha um tipo de usuário - Autores, Revisores ou Editores.

      >[!NOTE]
      >
      >Você verá outros tipos de usuários nessa lista suspensa, mas, para um projeto DITA, deverá escolher somente um dos tipos de usuário Autores, Revisores ou Publicadores . Mesmo que você adicione um usuário de um tipo diferente, ele não poderá acessar nenhum recurso específico do DITA disponível nos Guias AEM.

   1. Clique em **Adicionar**.

      >[!NOTE]
      >
      >Se estiver usando AEM Guias versão 3.5 ou anterior, será exibida uma opção para selecionar um arquivo de mapa DITA para resolver referências principais para fluxos de trabalho de edição, visualização e revisão de tópicos. Em 3.6 e versões posteriores, é possível definir o mapa raiz por meio do Editor da Web. Para obter mais informações, consulte o [Preferências do usuário](web-editor-features.md#id2087G0P40SB) no Editor da Web. Outra maneira de definir o mapa-raiz é configurá-lo nos perfis globais ou de nível de pasta. Para obter mais detalhes, consulte *Configurar perfis globais ou de nível de pasta* no Guia de Instalação e Configuração.
   Informações no **Avançado** guia :

   - Insira um nome para o projeto. Esse nome é usado para criar o URL para este projeto.



1. Clique em **Criar**.

   A caixa de diálogo Projeto criado é exibida.

1. Clique em **Abrir** para abrir a página do projeto.


**Tópico principal:**[ Rever tópicos ou mapas](review.md)

