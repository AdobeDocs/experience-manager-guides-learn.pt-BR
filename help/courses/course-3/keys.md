---
title: Chaves
description: As chaves permitem incluir informações variáveis ao trabalhar com DITA no AEM Guides
exl-id: cb64e094-fe6d-4a5e-8f0e-25ae58aaa2c6
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '585'
ht-degree: 0%

---

# Chaves

Diferentes conjuntos de materiais podem conter informações semelhantes que precisam ser personalizadas em locais selecionados. As teclas permitem incluir informações variáveis no ao trabalhar com DITA.

Os arquivos de exemplo que você pode optar por usar nesta lição são fornecidos no arquivo [keys.zip](assets/keys.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342756?quality=12&learn=on)

## Ativar teclas

1. Faça upload do conjunto de arquivos de amostra fornecido.

   a. Carregue o arquivo zip.

   b. Atualize o ambiente do AEM.

   c. Selecione o arquivo para extração.

   ![Selecionar CEP](images/lesson-9/select-zip.png)

   d. Clique em [!UICONTROL **Extrair Arquivo**] na barra de ferramentas superior.

   ![Barra de ferramentas](images/lesson-9/extract-archive.png)

   e. Na caixa de diálogo, escolha o local específico para os arquivos a serem extraídos, como uma pasta chamada Chaves.

   f. Clique em [!UICONTROL **Avançar**].

   g. Ignore quaisquer conflitos, pois eles não existirão em conteúdo que nunca foi carregado antes.

   h. Selecione [!UICONTROL **Extrair**] na parte superior direita da tela.

1. Quando a extração for concluída, clique em [!UICONTROL **Ir para a pasta de destino**].

   ![Confirmação](images/lesson-9/go-to-target.png)

## Resolver chaves para valores referenciados

Para usar Chaves corretamente, as Preferências do usuário devem fazer referência a um mapa específico como o Mapa raiz. Dentro deste mapa há uma coleção de Chaves agrupadas dentro de um grupo de tópicos. Abrir o mapa e os tópicos resolve as Chaves para os valores aos quais este mapa faz referência.

1. Especifique um Mapa raiz.

   a. Na tela Chaves, abra um mapa.

   b. Configure as Preferências do Usuário.

   c. Clique no ícone [!UICONTROL **Preferências do Usuário**] na barra de ferramentas superior.

   ![Barra de Ferramentas Superior](images/lesson-9/author-view.png)

   d. Clique no ícone de chave para especificar um **Mapa de Raiz** que será usado para resolver Chaves.

   e. Marque as caixas de seleção para qualquer Assets desejada.

   ![Lista Suspensa do Assets](images/lesson-9/select-assets.png)

   f. Clique em [!UICONTROL **Selecionar**].

   g. **Salvar** as Preferências do Usuário.

1. Navegue até a **Exibição do mapa**.

1. Abra o mapa especificado.

As Chaves são resolvidas.

## Adicionar um novo keydef manualmente

1. Abra um mapa com um Mapa de Raiz especificado.

1. Selecione uma chave.

   ![Lista Suspensa de Chaves](images/lesson-9/hybrid-key.png)

1. Insira um novo keydef.

   a. Clique em um local válido no mapa.

   b. Selecione o ícone **Keydef** na barra de ferramentas superior.

   ![Barra de ferramentas Keydef](images/lesson-9/key-icon.png)

   c. Na caixa de diálogo Inserir keydef, digite um valor exclusivo para Chaves que faça sentido para a definição que você está criando.

   d. Clique em [!UICONTROL **Inserir**].

1. Adicione topicmeta dentro do keydef.

   a. Clique no ícone [!UICONTROL **Inserir elemento**] na barra de ferramentas superior.

   ![Barra de ferramentas Keydef](images/lesson-9/add-icon.png)

   b. Na caixa de diálogo Inserir elemento, procure e selecione &quot;topicmeta&quot;.

1. Adicione palavras-chave no topicmeta.

   a. Clique no ícone [!UICONTROL **Inserir elemento**] na barra de ferramentas superior.

   ![Barra de ferramentas Keydef](images/lesson-9/add-icon.png)

   b. Na caixa de diálogo Inserir elemento, procure e selecione &quot;palavras-chave&quot;.

1. Adicione uma palavra-chave no topicmeta.

   a. Clique no ícone [!UICONTROL **Inserir elemento**] na barra de ferramentas superior.

   ![Barra de ferramentas Keydef](images/lesson-9/add-icon.png)

   b. Na caixa de diálogo **Inserir elemento**, pesquise e selecione &quot;palavra-chave&quot;

1. Digite o valor de keydef na palavra-chave.

No mapa, sua definição de chave agora deve ser semelhante a:

![Keydef Concluído](images/lesson-9/keydef.png)

## Configurar um keydef como um trecho

Os trechos são pequenos fragmentos de conteúdo que podem ser reutilizados em vários tópicos do projeto de documentação. Em vez de gerar manualmente cada keydef, você pode configurar uma única keydef como um snippet.

1. Selecione um elemento keydef no mapa.

1. No menu contextual, clique em [!UICONTROL **Criar trecho**].

1. Na caixa de diálogo Novo trecho, adicione um Título e uma Descrição.
Você também pode remover chaves ou definições de palavras-chave existentes do Conteúdo.

1. Clique em [!UICONTROL **Criar**].

1. No painel esquerdo, selecione **trechos**.

1. Arraste e solte o trecho recém-criado do painel Trechos no mapa.

1. Atualize o keydef conforme necessário usando as Propriedades de conteúdo.
Quando salvo e atualizado, esse conjunto de chaves estará disponível para qualquer usuário que tenha definido um mapa que contenha o mesmo Mapa raiz.
