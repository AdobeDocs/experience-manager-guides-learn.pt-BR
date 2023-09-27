---
title: Usar predefinições de condição
description: Conhecer o uso de predefinições de condição em Guias AEM. Saiba como criar, editar, copiar e excluir predefinições de condição no AEM.
exl-id: cd8f8196-ba03-4a4b-9ce8-2651de4e5cc2
source-git-commit: 8504a0a52d381044bf1f0d6e7de3585ebecf3a7b
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 2%

---

# Usar predefinições de condição {#id1825FL004PN}

Você pode definir atributos em seus tópicos DITA e usar a predefinição de condição para especificar o que acontece com o atributo na saída final. Por exemplo, você pode adicionar atributos como versão 1.0 e versão 2.0 no conteúdo e usar uma predefinição de condição para incluir a versão 1.0 para a versão 1.0 e excluir a versão 2.0. Da mesma forma, você pode adicionar atributos como SO Windows e OS Linux ao seu conteúdo e, em seguida, incluir ou excluir o conteúdo relevante para sua saída final de acordo com o sistema operacional.

## Criar uma predefinição de condição

Execute as seguintes etapas para criar uma predefinição de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Clique em **Criar** botão.
1. Insira um nome para a predefinição em **Condição de nome**.
1. Selecione uma das seguintes ações padrão em **Definir ação padrão como** lista suspensa:

   - Incluir
   - Excluir
   - Passagem
   - Sinalizador A ação é definida como ação padrão para todos os atributos, sejam eles adicionados à predefinição de condição ou não.

   Por exemplo, você tem 15 atributos de condição no documento e incluiu quatro deles na predefinição de condição. Se você selecionar **excluir** como ação padrão, é aplicada a todos os 15 atributos.

1. Siga qualquer um destes procedimentos para adicionar os atributos:
   - Clique em **Adicionar** a um atributo para a predefinição de condição. Você pode repetir essa etapa para adicionar mais atributos.
   - Clique em **Adicionar tudo** para adicionar todos os atributos à predefinição de condição.
1. \(Opcional\) Se necessário, é possível substituir a ação padrão aplicada aos atributos na Etapa 4. Siga uma das seguintes opções:
   - Selecione vários atributos, escolha uma ação em **Definir a ação das condições selecionadas como** e clique em **Aplicar**.
   - Selecione uma ação para um atributo na **Ação** menu suspenso.
1. Clique em **Salvar**.

## Editar uma predefinição de condição

É possível fazer alterações em uma predefinição de condição existente para alterar as ações aplicadas aos atributos na predefinição de condição. Execute as seguintes etapas para editar uma predefinição de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Clique em **Editar** botão.
1. Faça as alterações necessárias para todos os atributos na predefinição de condição.
1. Clique em **Salvar**.

## Criar uma cópia de uma predefinição de condição

É possível criar uma cópia de uma predefinição de condição e modificá-la de acordo com suas necessidades. Execute as seguintes etapas para criar uma cópia de uma predefinição de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Clique em **Duplicar** botão.

   >[!NOTE]
   >
   > O nome padrão da predefinição é `<selected condition preset name>_Duplicate`

   Você pode alterar o nome de acordo com sua exigência.

1. \(Opcional\) Faça as alterações necessárias para todos os atributos na predefinição de condição.
1. Clique em **Salvar**.

## Excluir predefinição de condição

É possível excluir uma ou mais predefinições de condição do **Predefinição de condição** do console de mapa DITA. Execute as seguintes etapas para excluir predefinições de condição:

1. Clique em **Predefinições de condição** no console do mapa DITA.
1. Selecione a predefinição de condição\(s\) que deseja excluir.
1. Clique em **Remover** botão.
1. Clique em **Remover** para confirmar a ação

**Tópico pai:**[ Geração de saída](generate-output.md)
