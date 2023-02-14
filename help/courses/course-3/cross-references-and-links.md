---
title: Referências cruzadas e links
description: Criação de referências cruzadas e links nos Guias AEM
exl-id: bee7d50f-cbdd-4ac8-b15b-101febc4ae80
source-git-commit: 1c4d278a05f2612bc55ce277efb5da2e6a0fa9a9
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Referências cruzadas e links

O Editor XML e o DITA fornecem uma maneira poderosa de se vincular entre tópicos. É importante gerenciar efetivamente as Referências de conteúdo, inclusive trabalhar com valores de ID exclusivos.

Os arquivos de amostra que você pode optar por usar para esta lição são fornecidos no arquivo
[cross-referencesandlinks.zip](assets/crossreferencesandlinks.zip)

>[!VIDEO](https://video.tv.adobe.com/v/342764?quality=12&learn=on)

## Criar uma referência cruzada para um tópico externo

É possível criar uma referência cruzada externa arrastando e soltando um tópico do Repositório em um arquivo aberto. No entanto, para evitar referências cruzadas, uma ID deve primeiro ser definida como um valor relacionado ao elemento pai. Essa é uma maneira fácil de criar uma referência cruzada, garantindo que as IDs sejam atribuídas corretamente.

1. Abra um arquivo onde deseja inserir uma referência cruzada externa.

2. Atribua uma ID ao elemento a ser referenciado.

   a. Clique dentro do elemento .

   b. No painel Propriedades de conteúdo , escolha **ID** na lista suspensa Atributo .

   c. Digite um nome lógico no campo Valor .

   d. Visualize o elemento e seu valor em **Exibição da Estrutura de Tópicos** se desejar.

3. **Salvar** o tópico para garantir que o Repositório tenha a ID atualizada.

4. Clique no botão [!UICONTROL **Referência**] na barra de ferramentas superior.

   ![Barra de ferramentas](images/lesson-7/references-icon.png)

5. No **Referência de conteúdo** selecione a ID e o emparelhamento de elementos que deseja inserir como uma referência cruzada.

6. Clique em [!UICONTROL **Selecionar**].

A referência cruzada foi adicionada ao tópico.

## Link para um site

Você pode inserir um link para um site dentro de qualquer tópico. Consulte o vídeo Guias do AEM Curso 1 sobre Vincular a sites para obter mais informações.


## Exibir links quebrados

Algumas modificações podem resultar em referências cruzadas quebradas. Isso inclui excluir um tópico, reorganizar uma seção que contenha uma referência cruzada ou alterar uma ID após a inserção da referência cruzada. Observe que um tópico de amostra _cross-referencesandlinks.zip_ O é fornecido com esta lição que fará com que várias das referências cruzadas com marcadores ao conteúdo interno sejam quebradas.

1. Navegue até o **Exibição da Estrutura de Tópicos** no painel esquerdo.

2. Clique no botão [!UICONTROL **Filtro**] ícone .

3. Selecionar **Links quebrados**.

   ![Lista suspensa de filtros](images/lesson-7/broken-links.png)

Links quebrados são exibidos como objetos clicáveis. Você pode identificá-los em texto vermelho no tópico.
