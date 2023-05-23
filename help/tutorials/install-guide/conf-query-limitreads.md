---
title: Configurar o número de LimitReads para uma consulta
description: Saiba como Configurar o número de LimitReads para uma consulta
source-git-commit: 801c306fa120e7889d4b9428fd5bee2849bf1956
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---


# Configurar o número de LimitReads para uma consulta {#id231RC0HL0ID}

Para aumentar o número de nós que uma consulta pode ler de cada vez, execute as seguintes etapas:

1. Abra a página JMX do console da Web da Adobe Experience Manager.

   O URL padrão para acessar a página de configuração é:

   ```http
   http://<server name>:<port>/system/console/jmx
   ```

1. Procure por e clique em **QueryEngineSettings**.

1. Alterar valor de atributo para o **LimitReads** atributo.

1. Clique em **Salvar**.


Quando você aumenta esse valor de atributo, ele ajuda a gerar o relatório para mapas DITA maiores.

**Tópico pai:**[ Personalizar editor da Web](conf-web-editor.md)

