---
title: Solução de problemas de erros de publicação
description: Solução de problemas de erros de publicação no [!DNL Adobe Experience Manager Guides]
exl-id: b37ea3e7-59cf-4fc5-8fae-e1fadd26f8d8
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 0%

---

# Solução de problemas de erros de publicação

Publicar um mapa geralmente é simples. Abra o mapa, selecione uma Predefinição de saída e gere a saída! No entanto, se um mapa ou seus tópicos apresentarem erros, a geração de saída poderá falhar. Quando isso ocorrer, é importante saber como solucionar os problemas.

>[!VIDEO](https://video.tv.adobe.com/v/338990?quality=12&learn=on)

## Preparação para o exercício

Você pode baixar arquivos de amostra para o exercício aqui.

[Download de exercício](assets/exercises/publishing-basic-to-advanced.zip)

## Causas comuns de erros de publicação

Erros podem ser introduzidos no conteúdo de origem. Por exemplo:

* Referência de caminho de arquivo com nome incorreto

* Pasta nomeada incorretamente

* Gráfico ou arquivo ausente

* Referência de conteúdo configurada incorretamente

* Referência cruzada corrompida

* Erros nos valores de um atributo (por exemplo, uma string em vez de um número)

* Configuração incorreta de componentes usados por [!DNL AEM Guides]

## Impacto dos erros

Um erro pode ser pequeno e resultar em uma observação simples para informar que um arquivo não foi empacotado com êxito ou grave o suficiente para resultar em uma falha completa na geração de saída. A guia Saídas exibe ícones codificados por cor para mostrar sucesso, erros ou falhas relacionados à geração de saída.

![error-impact](images/error-impact.png)

## Abrir e revisar logs de erros

O arquivo de log gerado pode ser aberto para revisão.

1. No **Saídas** clique na guia **data/hora em Gerado às.**

   ![log de erros](images/error-log.png)

1. Percorra o log de erros.

## Mostrando e ocultando tipos de erro

O registro de erros exibe cada tipo de erro em uma cor exclusiva.

![erros de navegação](images/navigate-errors.png)

1. **Selecionar** ou **desmarcar** qualquer tipo de erro para mostrar ou ocultar o realce.

1. Navegar por erros usando o **próximo** ou **anterior** botões (setas).

## Resolução de erros

Dependendo do tipo de erro, a resolução pode ser simples ou complexa. Ele pode ser preenchido por um autor no Editor XML ou pode exigir que um administrador trabalhe com [!DNL AEM Guides]. Correções específicas dependem do erro, do impacto e dos workflows organizacionais.

* Referência de caminho de arquivo com nome incorreto

       Os autores podem atualizar a referência do caminho no documento de origem.
       
   
* Pasta nomeada incorretamente

       Os autores podem atualizar o nome da pasta ou mover arquivos conforme necessário.
       
   
* Gráfico ou arquivo ausente

       Os autores podem fazer upload de um gráfico/arquivo ausente, renomear um gráfico/arquivo ou mover um gráfico/arquivo
       
   
* Referência de conteúdo configurada incorretamente

       Os autores podem corrigir o local do conteúdo referenciado ou alterar o caminho para a referência de conteúdo.
       
   
* Referência cruzada corrompida

       Os autores podem corrigir o local para o qual a referência cruzada aponta ou alterar o nome ou as propriedades do arquivo de destino
       
   
* Erros nos valores de um atributo (por exemplo, uma string em vez de um número)

       Os autores podem atualizar o atributo para um valor correto ou os administradores podem atualizar o sistema para suportar novos valores.
       
   
* Configuração incorreta de componentes usados por [!DNL AEM Guides]

       Os administradores podem atualizar a instalação do sistema, seus componentes ou permissões.
       
   