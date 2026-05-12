---
title: Fluxos de trabalho simples de criação de conteúdo
description: Criação de conteúdo no AEM Guides
exl-id: e4b8e512-0688-44f7-b981-78af33b57b08
TQID: https://experienceleague.adobe.com/fLMRJWYDwHU-0ZbbUQ2kFZ1ZUM4vIwHccPV3q-pkn0I
product_v2:
  - id: fae5e35a-80c9-4b94-9352-1a060a6aab1d
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 27ffc636d63300fb2e99903d92cab12f0cfcbb25
workflow-type: tm+mt
source-wordcount: 720
ht-degree: 1%

---

# Fluxos de trabalho de criação de conteúdo simples

O Editor do AEM Guides tem vários atalhos que simplificam o fluxo de trabalho de criação de conteúdo. Esses atalhos permitem que os usuários adicionem e modifiquem imagens rapidamente, trabalhem com vários tópicos de uma só vez, corrijam erros, baixem PDFs de tópicos e trabalhem com versões e rótulos.

>[!VIDEO](https://video.tv.adobe.com/v/342770?quality=12&learn=on)

## Adicionar uma imagem

As imagens podem ser adicionadas diretamente de uma unidade local.

1. Arraste e solte a imagem diretamente no tópico. A caixa de diálogo **Carregar Assets** é exibida.

   ![Carregar caixa de diálogo do Assets](images/lesson-15/upload-assets-dialog.png)

1. Modifique o caminho da pasta para o local da imagem desejado.

1. Altere o nome da imagem para algo que represente sua finalidade.

1. Clique em [!UICONTROL **Fazer upload**].

## Modificar uma imagem

1. Redimensionar uma imagem arrastando e soltando um canto.

1. Mova uma imagem para outro local dentro do tópico arrastando-a e soltando-a.

1. Use as **Propriedades de Conteúdo** no painel direito para modificar a imagem

   - escala

   - position

   - alinhamento, ou

   - outros atributos.

   ![Propriedades do conteúdo](images/lesson-15/content-properties.png)

## Trabalhar com vários tópicos

A exibição dividida é útil ao comparar tópicos, copiar e colar entre tópicos ou arrastar e soltar conteúdo de um tópico para outro.

1. Abra dois ou mais tópicos relacionados.

1. Clique na guia Título de um arquivo para abrir o menu contextual.

1. Selecione [!UICONTROL **Split**].

1. Escolha **Right**.

   ![Modo de Exibição Dividido](images/lesson-15/split-view.png)

## Corrigir erros tipográficos

1. Localize a palavra ou frase que contém o erro.

1. Pressione e segure [!UICONTROL **Ctrl**].

1. Clique no botão secundário do mouse no erro.

1. Selecione a ortografia correta.

O erro foi corrigido no texto do tópico.

## Baixar um tópico do PDF

Os usuários podem baixar uma PDF do tópico atual para marcar ou compartilhar com outros.

1. Clique em [!UICONTROL **Visualizar**] na parte superior direita da tela.

1. Clique no [!UICONTROL **ícone do PDF**] acima do tópico. Uma caixa de diálogo é exibida.

   ![Exportação PDF](images/lesson-15/pdf-export.png)

1. Preencha as informações para o **Nome da Transformação** ou os **Argumentos de Linha de Comando DITA-OT**, se necessário. Observe que uma PDF ainda será gerada se todos os campos forem deixados em branco.

1. Clique em [!UICONTROL **Baixar**]. O PDF gera.

1. Use os ícones disponíveis para configurar, baixar ou compartilhar o tópico do PDF.

## Localizar um tópico no Repositório ou no Mapa

1. Abra o tópico.

1. Clique no botão secundário do mouse na guia Título.

1. Selecione **Localizar Em**.

1. Escolha **Repositório** ou **Mapa** para ir para o local do tópico desejado.

## Versão de um tópico

1. Fazer uma alteração em um tópico.

1. Salve o tópico.

1. Clique no ícone **Repositório** no menu superior esquerdo.

   ![Ícone de Repositório](images/lesson-15/repository-icon.png)

1. Na caixa de diálogo, adicione **Comentários para Nova Versão**.

   ![Caixa de Diálogo Nova Versão](images/lesson-15/version-dialog.png)

1. Clique em [!UICONTROL **Salvar**].

O número da versão é atualizado.

## Carregar rótulos de versão

Tentar rastrear o estado de um tópico com base somente no Número da versão pode ser difícil. Os rótulos facilitam a identificação do estado exato de um tópico que passou por várias revisões.

1. Selecione um **Perfil de Pasta**.

1. No Perfil de pasta, configure o Editor de XML.

   a) Selecione Editar na parte superior esquerda da tela.

   b) Em Rótulos de versão do conteúdo XML, adicione um novo tópico ou use um existente.

   ![Rótulos de Versão de Conteúdo](images/lesson-15/version-labels.png)

1. Selecione [!UICONTROL **Carregar**].

1. Escolha um arquivo como ReviewLabels.json ou similar. Detalhes sobre como criar esse arquivo são abordados em outro vídeo.

1. Clique em [!UICONTROL **Abrir**].

1. Clique em [!UICONTROL **Salvar**] na parte superior esquerda da tela Perfil da Pasta.

1. Clique em [!UICONTROL **Fechar**] na parte superior direita.

Os rótulos de versão agora são carregados.

## Atribuir rótulos de versão

1. Carregar rótulos de versão.

1. Clique no ícone [!UICONTROL **Preferências do Usuário**] na parte superior esquerda do tópico atual.

   ![Perfil de pasta](images/lesson-15/folder-profile-icon.png)

1. Selecione o mesmo Perfil de pasta onde os rótulos de versão foram carregados anteriormente.

1. Na caixa de diálogo Preferências do usuário, verifique se o Caminho base faz referência às mesmas informações às quais o Perfil de pasta foi aplicado.

   ![Preferências do usuário](images/lesson-15/user-preferences.png)

1. Clique em [!UICONTROL **Salvar**].

1. Versão do tópico.

1. Adicione um comentário e selecione um rótulo de versão na lista suspensa.

   ![Caixa de Diálogo Rótulo da Nova Versão](images/lesson-15/labels-dialog.png)

1. Clique em [!UICONTROL **Salvar**].

O número da versão é atualizado.

## Exibir o histórico de versões e os rótulos

1. No painel esquerdo, localize o título do tópico atual.

1. Clique no título para abrir o menu contextual.

1. Selecione [!UICONTROL **Exibir na Interface do Usuário do Assets**].

   ![INTERFACE DO USUÁRIO DO Assets](images/lesson-15/view-assets-ui.png)

   - O histórico de versões com rótulos é exibido à esquerda.

   ![Histórico de Versões](images/lesson-15/version-history.png)

1. Clique em uma versão para acessar opções como **Reverter para esta Versão** e **Visualizar Versão**.

## Criar um novo modelo

Existem modelos para tópicos e mapas. Os administradores podem acessar os Modelos no painel esquerdo.

1. Clique em [!UICONTROL **Modelos**] no painel esquerdo.

1. Selecione Mapa ou Tópico para abrir o menu contextual associado.

1. Clique em para adicionar o novo template.

   ![Novo Modelo de Tópico](images/lesson-15/version-history.png)

1. Preencha os campos na caixa de diálogo resultante.

O modelo de shell é exibido, contendo conteúdo de amostra e uma estrutura de amostra.
