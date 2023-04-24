---
title: Usar predefinições de condição
description: Saiba como usar predefinições de condição
source-git-commit: 6eb8d29e71301581e8dbb5b6a4252194c5a89f96
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 2%

---


# Usar predefinições de condição {#id1825FL004PN}

Você pode definir atributos nos tópicos do DITA e usar a predefinição de condição para especificar o que acontece com o atributo na saída final. Por exemplo, você pode adicionar atributos como versão 1.0 e versão 2.0 em seu conteúdo e usar uma predefinição de condição para incluir a versão 1.0 para a versão 1.0 e excluir a versão 2.0. Da mesma forma, você pode adicionar atributos como SO Windows e OS Linux ao seu conteúdo e, em seguida, incluir ou excluir o conteúdo relevante para sua saída final de acordo com o sistema operacional.

## Criar uma predefinição de condição

Execute as seguintes etapas para criar uma predefinição de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Clique em **Criar** botão.
1. Insira um nome para a predefinição em **Condição de nome**.
1. Selecione uma das seguintes ações padrão de **Definir ação padrão como** lista suspensa:

   - Incluir
   - Excluir
   - Passagem
   - Sinalizador A ação é definida como ação padrão para todos os atributos, sejam eles adicionados ou não à predefinição de condição.

   Por exemplo, você tem 15 atributos de condição em seu documento e incluiu quatro deles na predefinição de condição. Se você selecionar **exclude** como ação padrão, ela é aplicada a todos os 15 atributos.

1. Siga qualquer um destes procedimentos para adicionar os atributos:
   - Clique em **Adicionar** para um atributo para a predefinição de condição. É possível repetir essa etapa para adicionar mais atributos.
   - Clique em **Adicionar tudo** para adicionar todos os atributos à predefinição de condição.
1. \(Opcional\) Se necessário, é possível substituir a ação padrão aplicada aos atributos na Etapa 4. Siga uma das seguintes opções:
   - Selecione vários atributos, escolha uma ação de **Defina a ação das condições selecionadas como** e clique em **Aplicar**.
   - Selecione uma ação para um atributo da **Ação** lista suspensa.
1. Clique em **Salvar**.

## Editar uma predefinição de condição

É possível fazer alterações em uma predefinição de condição existente para alterar as ações aplicadas aos atributos na predefinição de condição. Execute as seguintes etapas para editar uma predefinição de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Clique em **Editar** botão.
1. Faça as alterações necessárias para todos os atributos na predefinição de condição.
1. Clique em **Salvar**.

## Criar uma cópia de uma predefinição de condição

Você pode criar uma cópia de uma predefinição de condição e depois modificá-la de acordo com sua necessidade. Execute as seguintes etapas para criar uma cópia de uma predefinição de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Clique em **Duplicar** botão.

   >[!NOTE]
   >
   > O nome padrão da predefinição é `<selected condition preset name>_Duplicate`

   Você pode alterar o nome de acordo com sua necessidade.

1. \(Opcional\) Faça as alterações necessárias para todos os atributos na predefinição de condição.
1. Clique em **Salvar**.

## Excluir predefinição de condição

É possível excluir uma ou mais predefinições de condição do **Predefinição de condição** guia do console do mapa DITA. Execute as seguintes etapas para excluir predefinições de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Selecione a predefinição de condição\(s\) que deseja excluir.
1. Clique em **Remover** botão.
1. Clique em **Remover** para confirmar a ação.

**Tópico principal:**[ Geração de saída](generate-output.md)

