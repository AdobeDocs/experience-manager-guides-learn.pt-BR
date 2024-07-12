---
title: Introdução ao Painel do Mapa
description: Introdução ao Painel do Mapa
exl-id: c2efa073-15e7-42a0-aaa8-04859b0fdf62
source-git-commit: 1c4d278a05f2612bc55ce277efb5da2e6a0fa9a9
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 0%

---

# Introdução ao Painel do Mapa

A seguir será apresentada uma visão geral dos principais recursos do painel de mapa.

>[!VIDEO](https://video.tv.adobe.com/v/339040?quality=12&learn=on)

## Abrir um mapa no Painel do Mapa

1. Na Exibição de Repositório, selecione o ícone de Reticências no mapa para abrir o menu Opções e, em seguida, Abrir Painel de Mapa.
   ![images/ellipsis-map-dashboard.png](images/ellipsis-map-dashboard.png)

   O Painel do mapa é aberto em outra guia.

## Componentes do painel do mapa

O Painel do Mapa contém várias guias, incluindo predefinições de saída, resultados de saída, tópico usado, linhas de base e muito mais.

### Predefinições de saída

A guia Predefinições de saída exibe as predefinições padrão para os diferentes tipos de saídas: AEM Site, PDF, HTML5, ePub e Personalizado.

![images/output-presets.png](images/output-presets.png)

É possível selecionar uma predefinição de saída para exibir os detalhes de suas configurações, incluindo o nome da transformação, o caminho de destino, as linhas de base e as condições aplicadas.

### Saídas

A guia Saídas exibe todas as saídas geradas anteriormente e geradas no momento.

![images/generated-outputs.png](images/generated-outputs.png)

Um círculo verde na coluna Configurações de geração indica que a saída foi gerada com sucesso. O texto desta coluna atua como um hiperlink ativo e você pode selecioná-los para abrir a saída gerada. As entradas na coluna Tipo indicam o tipo de saída.
Outras informações de geração de saída também são exibidas aqui, incluindo o nome do usuário que gerou a saída, a data e hora da geração e o tempo necessário para que a geração ocorresse. Se houver um erro durante a geração, você poderá selecionar a data e a hora da geração na coluna Gerado em para abrir e revisar o log de erros.

### Tópicos

A guia Topics (Tópicos) exibe uma lista de todos os tópicos do mapa.

![images/topics.png](images/topics.png)

Marcar a caixa de seleção de um tópico permite executar ações adicionais. É possível editá-la, gerá-la novamente e mostrar, aplicar ou ocultar suas tags.

### Predefinições de condição

A guia Predefinições de condição exibe as configurações para que um conteúdo condicional específico seja incluído ou excluído.

![images/condition-presets.png](images/condition-presets.png)

Aqui, marcar a caixa de seleção da edição Somente autor resultará em uma saída que exclui todo o conteúdo com o atributo &quot;público-alvo&quot; que tem o rótulo &quot;designers&quot; e inclui todo o conteúdo com o rótulo &quot;escritores&quot;.

### Linhas de Base

A guia Linhas de Base permite exibir suas linhas de base.

![images/baselines.png](images/baselines.png)

As linhas de base atuam como snapshots no tempo e permitem criar uma versão dos tópicos e ativos para publicação. Por exemplo, uma linha de base que captura conteúdo em uma data e hora específicas pode usar a versão 1.3 de um tópico e a 1.0 de outro tópico, com base nas respectivas versões no momento.
Se não houver uma linha de base especificada, a saída será gerada com as versões mais recentes de todo o conteúdo.

### Relatórios

A guia Relatórios exibe um resumo das informações do tópico, incluindo o número total de tópicos em uso, os elementos ausentes nesses tópicos e o estado do documento.

![images/reports.png](images/reports.png)

Se um tópico não tiver um elemento, você poderá selecionar a seta mais à direita na linha para expandir a entrada e exibir detalhes sobre o erro.
