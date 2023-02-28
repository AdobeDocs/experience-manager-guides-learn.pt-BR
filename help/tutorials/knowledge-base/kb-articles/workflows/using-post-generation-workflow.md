---
title: Fluxo de trabalho de pós-geração
description: Uma visão geral do fluxo de trabalho de pós geração com um exemplo
source-git-commit: 447cd512d1b6cdce3bd1ddded1575dab87daa04a
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 0%

---


# Publicação dos guias de AEM - Fluxo de trabalho de geração de postagem

AEM Guias oferece a flexibilidade para especificar um fluxo de trabalho de geração de pós-saída. Você pode executar algumas tarefas de pós-processamento na saída gerada usando os Guias AEM.
Por exemplo, talvez você queira definir certas propriedades na saída do PDF ou enviar um email para um conjunto de usuários depois que a saída for gerada.


## Quais são as etapas envolvidas para utilizar os workflows de pós-geração

### Criar um processo de workflow

Crie um processo de workflow baseado em Java ou ECMA que execute a operação na saída gerada. Por exemplo, copiar alguns metadados da origem para o conteúdo gerado ou manipular metadados da saída gerada.
- Usaremos um exemplo de criação desse processo usando o script ECMA (é possível consultar o pacote anexado)
- Para processos de fluxo de trabalho baseados em Java, consulte a seção &quot;*Personalizar fluxo de trabalho de geração de pós-saída*&quot; [Guia de instalação e configuração](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_Installation-Configuration-Guide_EN.pdf#page=119)


### Criar um modelo de fluxo de trabalho

Com o processo de fluxo de trabalho personalizado criado na etapa anterior, crie um modelo de fluxo de trabalho e adicione a etapa do processo a ele.
- Você também precisa adicionar uma etapa obrigatória do processo &quot;*Finalizar pós-geração*&quot; como a última etapa do fluxo de trabalho.

Consulte modelo de fluxo de trabalho de exemplo mostrado abaixo:

![Modelo de fluxo de trabalho de pós-geração](../assets/workflows/pgwf-workflow-model.png)


### Usar este fluxo de trabalho de geração de postagens em um mapa

O fluxo de trabalho de pós-geração é uma propriedade que pode ser configurada em qualquer predefinição de saída dentro AEM mecanismo de publicação dos Guias. Exemplo:

![Fluxo de trabalho de pós-geração na predefinição de saída](../assets/workflows/pgwf-preset-settings.png)


Supondo que o modelo selecionado já foi criado.


### Testes

Agora você pode executar a publicação usando esta predefinição e validar a saída da etapa do processo


## Amostra

Para sua referência, você pode usar o pacote abaixo e instalá-lo por meio do gerenciador de pacotes para testar o fluxo de trabalho de pós-geração de amostra (*conforme mencionado acima nas capturas de tela*)

[Um exemplo de modelo de fluxo de trabalho de pós geração baseado em ECMA](../assets/workflows/sample-pgwf-ecma-test-wfmetadata.zip)
