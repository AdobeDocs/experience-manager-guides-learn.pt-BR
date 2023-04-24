---
title: Gerenciar conteúdo
description: Saiba como gerenciar conteúdo
source-git-commit: bad2f5cea2c00ca6c9758da27f0dba89a8579eb7
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 10%

---


# Gerenciar conteúdo {#id164JBG0M0T1}

Antes de começar a criação de conteúdo real, você deve se familiarizar com alguns conceitos básicos de gerenciamento de conteúdo nos Guias AEM. Em seguida, comece criando grupos de usuários diferentes e organizando seus ativos.

## Principais conceitos

Alguns dos principais conceitos de gerenciamento de conteúdo no AEM são:

**Gerenciamento de ativos**

AEM Guias usa AEM gerenciamento de ativos digitais \(DAM\) para gerenciar seus arquivos DITA. Os arquivos carregados ou verificados no DAM são armazenados como ativos digitais. Você pode gerenciar e editar seus ativos no AEM Assets. Para obter mais informações sobre o gerenciamento de ativos, consulte [Gerenciar ativos](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/manage/manage-digital-assets.html?lang=en).

**Gerenciamento de links**

Mova ou renomeie arquivos ou altere a estrutura da pasta no repositório de conteúdo, sem se preocupar com referências quebradas. Todas as referências a e do conteúdo afetado são atualizadas automaticamente. Receba avisos ao excluir conteúdo referenciado de outro lugar, para evitar interrupções não intencionais.

**Gerenciamento de versões**

AEM Guias fornece o gerenciamento de versões para seus ativos digitais. Você pode facilmente habilitar essa funcionalidade em um aplicativo de criação DITA de sua escolha. Permitir que seus gravadores executem as funções padrão de controle de versão, como check-in e check-out.

Para obter mais informações sobre como criar versões ou reverter para uma versão específica, consulte [Ramificação, reversão e controle de versão subsequente](web-editor-preview-topics.md#id193PG0Y051X).

**Manuseio de DITA nativo**

Embora AEM Guias mantenha a estrutura dos arquivos DITA, ele também permite que o AEM manipule DITA nativamente o mapeamento de elementos para mapear os elementos DITA para AEM componentes. A manipulação do DITA nativo é usada em recursos como visualização de tópico, publicação no AEM Sites e fluxos de trabalho de revisão.

## Identificar sua função e permissões {#id181TF0K0MHT}

AEM Guias fornece três grupos predefinidos. Esses grupos são: *Autores*, *Revisores* e *Editores*. Dependendo do grupo com o qual você está associado, você tem permissões para executar tarefas específicas, conforme mencionado na tabela fornecida abaixo. Por exemplo, a tarefa de publicação pode ser executada somente por um editor, mas não por um autor ou um revisor. Da mesma forma, um autor pode criar um novo tópico, e um revisor só pode revisar um tópico.

>[!TIP]
>
> Consulte a *Permissões* no guia Práticas recomendadas para práticas recomendadas relacionadas à configuração de permissões do usuário.

A tabela a seguir lista várias tarefas e os grupos que podem executar essas tarefas:

| Tarefa | Autores | Revisores | Editores |
|----|-------|---------|----------|
| Criar tópico DITA | Sim |   | Sim |
| Criar mapa DITA | Sim |   | Sim |
| Mapear coleções | Sim |   | Sim |
| Criar tarefa de análise | Sim |   | Sim |
| Tópico de revisão[1](#fntarg_1) | Sim | Sim | Sim |
| Resolução de Chave | Sim |   | Sim |
| Check-out/Check-in | Sim |   | Sim |
| Editar tópico | Sim |   | Sim |
| Mover tópico | Sim |   | Sim |
| Editar propriedades de tópico | Sim |   | Sim |
| Copiar | Sim |   | Sim |
| Excluir | Sim |   | Sim |
| Compartilhar | Sim |   | Sim |
| **Estado do documento** |
| Criar/editar perfil de estado do documento |   |   | Sim |
| Alterar estado do documento[2](#fntarg_2) | Sim | Sim | Sim |
| **Recursos disponíveis no console do mapa DITA \(guia Predefinições de saída\)** |
| Gerar |   |   | Sim |
| Editar |   |   | Sim |
| Duplicar |   |   | Sim |
| Criar |   |   | Sim |
| Excluir predefinição |   |   | Sim |
| **Recursos disponíveis no console do mapa DITA \(guia Saídas\)** |
| Exibir saída gerada | Sim |   | Sim |
| **Recursos disponíveis no console do mapa DITA \(guia Tópicos\)** |
| Criar tarefa de análise | Sim |   | Sim |
| Editar | Sim |   | Sim |
| **Recursos disponíveis no console do mapa DITA \(guia Linhas de base\)** |
| Criar |   |   | Sim |
| Editar |   |   | Sim |
| Duplicar |   |   | Sim |
| Remover |   |   | Sim |
| Console de mapa DITA \(guia Relatórios\) | Sim |   | Sim |
| **Recursos disponíveis no console de mapa DITA \(Predefinições de condição\)** |
| Criar/editar predefinição de condição |   |   | Sim |

[1](#fnsrc_1) If *Autores* e *Editores* são convidados para uma revisão.

[2](#fnsrc_2) Dependendo dos direitos dados ao usuário no perfil de estado do documento.

## Pré-requisitos para a criação de conteúdo

**Trabalhar com perfis globais ou de nível de pasta**

Em uma empresa, diferentes grupos ou produtos podem usar diferentes modelos de criação, modelos de saída, perfis de atributo condicional \(ou esquemas de assunto\) e configurações do Editor da Web. A configuração somente em um nível corporativo \(ou global\) pode dificultar a experiência dos autores, pois eles verão modelos ou perfis que não são relevantes para eles.

AEM Guias permite configurar a criação de modelos \(tópico ou mapa\), modelos de saída, atributo condicional e configurações do Editor da Web em um nível corporativo \(global\), bem como em um nível de pasta. Dessa forma, você pode segregar as configurações de diferentes departamentos ou produtos na sua empresa.

Além disso, você pode delegar as configurações específicas da pasta a um departamento ou administradores de produtos para descentralizar a administração.

Para obter detalhes sobre como configurar perfis globais e de nível de pasta, consulte *Configurar perfis globais ou de nível de pasta* em Instalar e configurar os Guias do Adobe Experience Manager as a Cloud Service.





