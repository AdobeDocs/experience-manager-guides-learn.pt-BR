---
title: Condições
description: Trabalhar com condições nas guias de AEM
exl-id: 2cb670d9-1a22-47c6-8409-52d1d526010a
source-git-commit: 01083e771baced42146044bf319d3897a2c5f51b
workflow-type: tm+mt
source-wordcount: '497'
ht-degree: 3%

---

# Condições

No DITA, as condições geralmente são orientadas por atributos como Produto, Plataforma e Público-alvo. Eles também podem ter valores específicos atribuídos a eles. Os usuários podem controlar tudo isso por meio de Perfis de pasta.

Os arquivos de amostra que você pode optar por usar para esta lição são fornecidos no arquivo [conditions.zip](assets/conditions.zip).

>[!VIDEO](https://video.tv.adobe.com/v/342755)

## Atribuir condições a um Perfil de pasta

1. Selecione o **Perfis de pasta** mosaico.

2. Clique em [!UICONTROL **Atributos condicionais**].

3. Clique em [!UICONTROL **Editar**] no canto superior esquerdo do perfil.

4. Clique em [!UICONTROL **Adicionar**].

   ![Condições nos perfis da pasta](images/lesson-13/add-name.png)

5. Preencha os campos obrigatórios.

   - O Nome deve corresponder a um atributo usado para criação de perfis.

   - O valor é a entrada exata que será usada na fonte de código DITA.

   - O Rótulo é a palavra que será vista pelo usuário que está inserindo atributos.

6. Clique em [!UICONTROL **Salvar**].

>[!NOTE]
>
>OBSERVAÇÃO: configurar um Perfil global pode ser uma maneira precoce e eficiente de controlar o uso de atributos e valores para seguir um guia de estilo consistente.

## Atribuir atributos a elementos

Se nenhum Perfil de pasta personalizado tiver sido atribuído a um conceito, convém atribuir atributos a elementos específicos, como parágrafos.

1. No **Exibição do Repositório**, clique no elemento com o qual deseja trabalhar para selecioná-lo.

2. No **Propriedades de conteúdo** clique no painel [!UICONTROL **Atributo**] lista suspensa.

3. Escolha o atributo que deseja atribuir.

4. Adicione um **Valor**.

O emparelhamento de atributo e valor agora é atribuído ao elemento selecionado.

## Atribuir emparelhamentos de atributo e valor usando condições

O painel Condições permite a atribuição controlada de pares de Atributo e Valor.

1. Modifique o **Preferências do usuário**.

   a. Clique no ícone Preferências do usuário.

   ![Ícone de Preferências do usuário](images/lesson-13/user-prefs-icon.png)

   b. Preencha os campos obrigatórios na **Preferências do usuário** caixa de diálogo. Por exemplo:

   ![Preferências de usuário](images/lesson-13/user-preferences.png)

   c. Clique [!UICONTROL **Salvar**].

2. No painel Condições , expanda as listas suspensas para Público-alvo e Plataforma. Observe que as condições disponíveis são específicas do Perfil da pasta.

3. Arraste e solte uma condição no elemento desejado para atribuí-la.

## Atribuir um esquema de assunto

Os mapas do Esquema de Assunto são uma forma especializada de mapa de espaço e são referenciados por um mapa. Esquemas de assunto são usados para definir taxonomias. Eles fornecem controle sobre os valores disponíveis.

1. Navegue até o **Exibição do Repositório**.

2. Selecione um mapa que faça referência ao mapa digital do Esquema de Assunto. Este exemplo usa o mapa chamado _Design e layout_.

   ![Preferências de usuário](images/lesson-13/subject-scheme-map.png)

3. Configurar preferências de usuário.

   a. Clique no botão [!UICONTROL **Preferências do usuário**] ícone .

   ![Preferências de usuário](images/lesson-13/user-prefs-icon-2.png)

   b. Preencha os campos no **Preferências do usuário** caixa de diálogo.

   c. Clique no símbolo da pasta ao lado do campo Caminho básico para escolher o caminho para o arquivo desejado.

   d. Clique em [!UICONTROL **Selecionar**].

   e. Clique no símbolo de chave ao lado do **Mapa raiz** para inserir um caminho.

   >[!IMPORTANT]
   >
   >Importante: o Root Map selecionado deve ser o mapa que contém o Subject Scheme.

   ![Preferências de usuário](images/lesson-13/user-preferences-2.png)

   f. Restrinja os ativos exibidos selecionando as pastas que deseja usar.

   g. Clique em [!UICONTROL **Selecionar**].

   h. Clique em [!UICONTROL **Salvar**].

O Esquema de Assunto foi atribuído.

## Exibir o Esquema de assunto no painel Condições

1. Navegar para **Configurações do editor**.

2. Selecione o **Condições** guia .

3. Marque a caixa **Mostrar esquema de assunto no painel Condições**
