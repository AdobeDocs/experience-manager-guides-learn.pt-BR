---
title: Criação e publicação com linhas de base
description: Criação e publicação com linhas de base em [!DNL Adobe Experience Manager Guides]
exl-id: 3c229c30-f2e0-4fb0-b60c-7bae60ef1a5b
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 1%

---

# Criação e publicação com linhas de base

Usar uma linha de base permite criar uma versão dos tópicos do mapa e do conteúdo de referência relacionado. Isso pode ser baseado em uma data, hora ou rótulos específicos.

>[!VIDEO](https://video.tv.adobe.com/v/338993?quality=12&learn=on)

## Acesso à guia Linhas de base no painel Mapa

Você pode acessar suas linhas de base no Painel do mapa.

1. Exibição do Repositório, selecione o ícone Reticências no seu mapa para abrir o menu Opções e **Abra o painel Mapa.**

   ![ellipsis-map-dashboard.png](images/ellipsis-map-dashboard.png)
O painel Mapa é aberto em outra guia.

1. Selecionar **Linhas de base**.

   ![baseline-tab.png](images/baseline-tab.png)

A guia Linhas de base é exibida.

## Criar uma linha de base com base em rótulos

1. Na guia Linhas de base , selecione **Criar**.

   ![create-baseline.png](images/create-baseline.png)

   As informações da nova linha de base são exibidas. Seu nome padrão é baseado na data de criação.

1. Dê um novo nome à linha de base, se necessário.

1. No cabeçalho &quot;Definir a versão com base em&quot;, selecione o círculo para Rótulo.
   ![set-the-version.png](images/set-the-version.png)

   >[!NOTE]
   >
   >OBSERVAÇÃO: O *Use a versão mais recente se o rótulo não estiver presente* A caixa de seleção é selecionada por padrão. Se isso não for selecionado e houver tópicos ou arquivos de mídia sem o rótulo escolhido no mapa, o processo de criação da Linha de base falhará.

1. Insira o rótulo que deseja usar.

1. Selecione **Salvar**.

Sua linha de base é criada. Uma tabela de todos os tópicos e suas informações associadas é exibida.

### Uso do recurso Procurar todos os tópicos

O recurso Procurar todos os tópicos permite exibir as informações do tópico, incluindo a versão e o rótulo, bem como especificar a versão usada. Você pode acessá-lo selecionando **Procurar todos os tópicos** ao criar ou editar sua linha de base.

![browse-all-topics.png](images/browse-all-topics.png)

## Criar uma linha de base com base na data e hora

Você também pode criar linhas de base que são um instantâneo no tempo.

1. Certifique-se de que a guia Linhas de base esteja aberta e selecione Criar.

   ![create-baseline.png](images/create-baseline.png)

1. No cabeçalho &quot;Definir a versão com base em&quot;, selecione o círculo para &quot;Versão ativada&quot;.

   ![version-on.png](images/version-on.png)

1. Selecione o ícone do calendário e especifique a data e a hora desejadas.

   ![calendar.png](images/calendar.png)

1. Dê um novo nome à linha de base, se necessário.

1. Selecione **Salvar**.

Sua linha de base é criada. Uma tabela de todos os tópicos e suas informações associadas é exibida.

### Adicionar rótulos à sua linha de base

Talvez você queira atribuir um novo rótulo em massa a todo o conteúdo do mapa.

1. Selecione a linha de base para a qual deseja adicionar rótulos.

1. Selecionar **Adicionar rótulos**.

   ![add-labels.png](images/add-labels.png)

   A caixa de diálogo Adicionar rótulo é exibida.

1. Insira o rótulo que deseja atribuir e selecione **Adicionar**.

O rótulo foi adicionado a todos os tópicos.

## Gerar uma saída do Site de AEM usando uma linha de base

1. Navegue até a guia Predefinições de saída no painel Mapa.

1. Marque a caixa de seleção Site de AEM.

   ![aem-site-checkbox.png](images/aem-site-checkbox.png)

1. Selecione **Editar**.

   ![edit-aem.png](images/edit-aem.png)

   Uma nova página é exibida.

1. Marque a caixa de seleção Usar linha de base e escolha a linha de base que deseja usar na lista suspensa.

   ![baseline.png](images/baseline.png)

1. Selecionar **Concluído**.

   ![done.png](images/done.png)

1. Selecionar **Gerar**.

   ![generate.png](images/generate.png)

   Sua saída foi gerada com uma linha de base.

## Exibição da saída gerada

1. Navegue até a guia Saídas no Painel do Mapa.

1. Selecione o texto na coluna Configuração de Geração para abrir a saída.
   ![aem-site-link.png](images/aem-site-link.png)

## Remoção de uma linha de base

1. Na guia Linhas de base , selecione a linha de base que deseja remover.

1. Selecionar **Remover**.

   ![remove-baseline.png](images/remove-baseline.png)

   A caixa de diálogo Remover linha de base é exibida.

1. Selecionar **Remover**.

A linha de base é removida.

## Duplicação de uma linha de base

1. Na guia Linhas de base , selecione a linha de base que deseja duplicar.

1. Selecionar **Duplicar**.

   ![duplicate.png](images/duplicate.png)

1. Selecione **Salvar**.

   ![save.png](images/save.png)

A linha de base duplicada é criada.

## Modificação de uma linha de base

Você pode especificar diretamente a versão de um tópico usado em uma linha de base.

1. Na guia Linhas de base , selecione a linha de base que deseja modificar.
1. Selecione **Editar**.

   ![edit-aem.png](images/edit-aem.png)

1. Selecionar **Procurar todos os tópicos**.

   ![browse-all-topics.png](images/browse-all-topics.png)

   Uma tabela de tópicos e suas informações associadas é exibida.

1. Para os tópicos que deseja modificar, selecione a versão desejada na lista suspensa na coluna Versão .

   ![version-dropdown.png](images/version-dropdown.png)

1. Selecione **Salvar**.

Suas alterações foram salvas. Sua linha de base agora usará as versões do tópico que você especificou.

## Criação de uma predefinição de saída do Site de AEM personalizada

É difícil distinguir entre saídas padrão do mesmo tipo na guia Saídas . Usar uma predefinição de saída personalizada com um nome exclusivo e amigável para o usuário permite solucionar esse problema.

Nesse caso, estamos criando uma predefinição de saída com base em uma linha de base.

1. Navegue até a guia Predefinições de saída no painel Mapa.

1. Selecione **Criar**.

   ![create-output-preset.png](images/create-output-preset.png)

   Uma nova página predefinida de saída é exibida, chamada Nova saída.
1. No campo Nome da configuração , insira um nome amigável para o usuário.

1. Marque a caixa de seleção Usar linha de base e selecione a linha de base desejada no menu suspenso.

   ![baseline.png](images/baseline.png)

1. Selecionar **Concluído**.

Sua nova predefinição de saída foi criada e é exibida na página de predefinições de saída.
