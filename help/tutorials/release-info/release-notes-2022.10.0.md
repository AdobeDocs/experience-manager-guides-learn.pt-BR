---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de outubro de 2022
description: Versão mais recente dos Guias do Adobe Experience Manager as a Cloud Service
source-git-commit: f673d53a1f3c76e1089e0a0c633c402722f99d00
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 4%

---

# Versão mais recente dos Guias do Adobe Experience Manager as a Cloud Service

## Atualizar para a versão mais recente

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.10.183.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão mais recente dos Guias AEM as a Cloud Service.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software compatíveis com AEM Guias as a Cloud Service versão de outubro de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac | Editar no Windows Oxygen | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2022.10.0 | 2.7.13 | 2.7.13 | 2.3 | 2,3 |
|  |  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service fornecem aprimoramentos e novos recursos na versão mais recente:


### Painel Geração rápida

Agora, as Guias AEM fornecem a variável **Geração rápida** painel que ajuda a gerar e exibir rapidamente a saída para predefinições criadas para o mapa DITA.

![Ícone Gerar rapidamente](assets/quick-generate-icon.png)

No **Geração rápida** , é possível ver a lista de todas as predefinições de saída criadas para o mapa DITA.

![Painel Geração rápida](assets/quick-generate-panel.png)

Selecione uma ou mais predefinições e gere rapidamente a saída. Também é possível visualizar rapidamente a saída gerada para as predefinições. Uma mensagem de sucesso é exibida na geração da saída. Uma mensagem de erro é exibida se a geração de saída falhar. Você também pode visualizar o log de erros para ver os detalhes do erro que ocorreu no processo de geração.


## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* PDF nativo | Ocorre um erro na remoção de tópicos somente de recursos da saída do PDF. (10554)
* PDF nativo | Keyrefs vazios são exibidos na saída do PDF. (10553)
* PDF nativo | `navtitle` para `topichead` não é honrado. (10509)
* PDF nativo | Suporte necessário para sabores do JDK amd64. (10465)
* PDF nativo | Não é possível ocultar os tópicos da frente do Índice. (10355)
* PDF nativo | Reiniciar o número de página no layout do capítulo inicia aleatoriamente a numeração a partir do fim do capítulo anterior. (10154)
* Navegador Chrome | A tela está ficando em branco ao arrastar e soltar qualquer elemento da interface do usuário. Por exemplo, ao arrastar uma condição do painel Condições . (10524)
* As propriedades de nó estão sendo removidas após a operação de copiar e colar de um ativo. (10053)
* Ao clicar  **Fechar** os usuários eram redirecionados para ativos - a experiência foi corrigida para levar os usuários para a página inicial do AEM. (9654)
