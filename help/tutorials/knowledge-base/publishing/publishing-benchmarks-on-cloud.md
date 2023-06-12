---
title: Guias de publicação de benchmarks no AEMaaCS
description: Entenda os limites do sistema em Publicação na Nuvem AEM.
source-git-commit: e64430bb968b18090c3981cc2d21ebe6593ba933
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 7%

---


# Guias do AEM publicam benchmarks no AEMaaCS

Atualmente, o serviço em nuvem AEM Guides tem alguns limites de tamanhos de mapa de publicação para os quais a equipe do Guides está trabalhando ativamente para resolver.

A equipe do Guides já introduziu um [Microsserviço de publicação](publish-microservice-architecture-and-performance.md) para oferecer suporte a mapas grandes e várias publicações simultâneas. Por enquanto, esse microsserviço oferece suporte a um subconjunto de tipos de saída e o suporte para outros tipos está em desenvolvimento ativo.

Para configurar o novo serviço de publicação para qualquer ambiente de nuvem AEM, consulte [Configurar nova publicação baseada em microsserviços](configure-microservices.md)

## Ambiente de execução

    Versão do AEM: 2023.5.11983.20230511T173830Z
    Suplemento do guia versão: 2023.6.0
    Modelo de site do AEM: modelo OOTB dos guias do AEM
    Versão do DITA-OT: 3.5.4
    Tipo de fluxo de trabalho de publicação: dividir fluxo de trabalho de publicação
    Saída compatível com microsserviço: PDF nativo, PDF (Dita-OT)

## Números de Geração de Saída

| Tipo de saída | Tamanho do Mapa (Referências de Tópico) | Tempo de execução (em segundos) | Microsserviço de publicação |
|---------------|------------------------------|----------------------------|-----------------------|
| Site AEM | 3500 | 5220 | Não |
| PDF nativo | 3500 | 780 | Sim |
| PDF (DITA-OT) | 11000 | 960 | Sim |
| HTML 5 | 3500 | 240 | Não |
| Personalizado | 300 | 300 | Não |

## Pontos principais a serem lembrados

- O site AEM cria muitos nós cq:Page e nivela ao renderizá-los individualmente durante o tempo de geração. Por isso, é aconselhável evitar a execução de várias publicações simultâneas no site AEM, pois isso pode sobrecarregar o sistema.
- O tempo de geração do site de AEM depende do modelo usado. O tempo de execução pode aumentar se um template complexo for usado.
- O tempo de execução de publicação personalizado serve para obter um exemplo de saída personalizada. O tempo de publicação personalizado depende exclusivamente da lógica de transformação do próprio cliente.
