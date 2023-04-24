---
title: Notas de versão para [!DNL AEM Guides], versão de março de 2022
description: Lançamento de março [!DNL Adobe Experience Manager Guides] as a Cloud Service
exl-id: 885edbb5-dfe4-4bdc-bb66-0df64addb094
source-git-commit: 67ba514616a0bf4449aeda035161d1caae0c3f50
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 2%

---

# Lançamento de março [!DNL Adobe Experience Manager Guides] as a Cloud Service

## Atualize para a versão de março

Atualize seu [!DNL Adobe Experience Manager Guides] as a Cloud Service (mais tarde conhecido como *[!DNL AEM Guides]as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação do Cloud Services configurada no pipeline correspondente ao ambiente que você deseja atualizar.
1. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.3.123.
1. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de março de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software suportados por [!DNL AEM Guides] Versão as a Cloud Service de março de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |


### Conector de oxigênio

| [!DNL AEM Guides] Versão da nuvem | Janelas do conector de oxigênio | Conector de oxigênio Mac |
| --- | --- | --- |
| 2022.3.0 | 2.4.0 | 2.4.0 |
|  |  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

## Novos recursos e melhorias

### Novo painel de linha de base

[!DNL AEM Guides] A versão de março as a Cloud Service fornece o recurso Linha de base integrado ao Editor da Web. Agora é possível criar linhas de base no Editor da Web e usá-las para publicar ou traduzir tópicos de diferentes versões.

Observação: Para o sistema atualizado, atualize o mais recente **ui_config.json** para Perfil da pasta.

Use esse recurso para criar uma linha de base com uma versão específica dos tópicos disponíveis em uma data e hora específicas. Além disso, você obtém o suporte da API para criar ou atualizar uma linha de base com um rótulo definido para uma versão de tópicos.

![guia gerenciar linha de base](assets/baseline-manage.png)

Você pode pesquisar os arquivos com base em nomes de arquivo ou no local do arquivo. Você também pode filtrar os tópicos a serem exibidos na janela de edição da linha de base e classificá-los com base em colunas específicas.

![guia gerenciar linha de base](assets/baseline-filter.png)

O desempenho do processo de criação da linha de base foi aprimorado ainda mais. O processo para criar linhas de base é assíncrono, portanto, você pode continuar editando outros arquivos no Editor da Web enquanto a linha de base estiver sendo criada. Para obter mais detalhes, consulte *Criar e gerenciar linhas de base no Editor da Web* no Guia do usuário.

Observação: A guia Linha de base no painel de mapa está oculta por padrão. O administrador pode ativar a guia Linha de base no painel de mapa.

### Melhora do comportamento de atualização do Editor da Web

Os seguintes aprimoramentos agora estão disponíveis com a operação de atualização do navegador no Editor da Web:

* Agora você tem suporte para atualizar o navegador enquanto edita seu conteúdo no Editor da Web. Se você clicar no ícone de atualização do navegador enquanto um ou mais arquivos com alterações não salvas forem abertos para edição, será solicitado a salvar seus arquivos ou cancelar a ação de atualização.

* Mesmo ao atualizar o navegador, as exibições do painel esquerdo e do painel direito são mantidas.

* O tópico ativo ou mapa DITA é reaberto na área de edição de conteúdo.

### Aprimoramentos de publicação

O processo de publicação foi aprimorado com a versão de março de [!DNL AEM Guides] as a Cloud Service:

* As linhas de base foram respeitadas para os metadados de saída AEM site. Também é possível processar as propriedades de uma versão da linha de base como metadados. Se nenhuma linha de base for definida, as propriedades da versão mais recente serão processadas como metadados.

* O **Nome do arquivo** e **Argumentos da linha de comando DITA-OT** foram adicionadas opções para HTML5, EPUB e predefinições de saída Personalizadas. Agora é possível especificar o nome do arquivo com o qual deseja salvar a saída. Você também pode especificar os argumentos adicionais que deseja que o DITA-OT processe ao gerar a saída.

## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* Não é possível adicionar elementos de matéria de frente e de fundo em um mapa de favoritos usando a visualização Autor do Editor da Web. (7652)
* A árvore de referência é interrompida após a remoção de um tópico e a execução de uma operação de movimentação. (8804)
* Uma exceção é recebida na visualização do conteúdo após o upload de um ativo. (3638)
* Ocorre um erro quando os arquivos cuja pasta principal tem caracteres especiais no nome do arquivo são abertos no Oxygen (usando o **Editar no oxigênio** botão). (8918)
* O **Localizar no repositório** não localiza e realça o mapa DITA no Editor XML. (8796)
* A filtragem não mostra os resultados apropriados quando vários atributos são adicionados ao conteúdo no Editor XML. (8795)
* Ocorre um erro ao adicionar um usuário como administrador no perfil da pasta quando a ID do usuário é numérica. (8908)

## Problemas conhecidos

O Adobe identificou o seguinte problema conhecido na [!DNL AEM Guides] Versão as a Cloud Service de março.

* Remover rótulos em referências diretas também remove os rótulos de referências indiretas.

* Não é possível refletir o título atualizado da linha de base sem atualizar manualmente o painel de linha de base.

* O recurso de visualização de versão no painel Histórico de versões não mostra a visualização de um tópico selecionado.
