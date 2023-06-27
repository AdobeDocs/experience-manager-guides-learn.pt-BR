---
title: Substituições de configuração
description: Saiba como configurar substituições
source-git-commit: 6051181e243cf71919901093c1b5590f21832545
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---


# Substituições de configuração {#id216IFC003XA}

Para fazer atualizações de configuração, a seguinte abordagem genérica deve ser usada:

1. Acesse o repositório Git do Cloud Manager.

1. Crie um novo arquivo JSON no seguinte local:

   src/main/content/jcr\_root/apps/fmditaCustom/config/

1. Nomeie o arquivo no seguinte formato:

   $\{PID\}.cfg.json

   Aqui, o PID é a ID do processo da configuração.

1. Adicione propriedades no arquivo JSON usando o seguinte formato:

   ```
   {
      "aem.adminuname": "updatedUserjson",
      "valid.characters": "[-a-zA-Z0-9_@$]",
      "dita.serialization": true
   }
   ```

1. Confirme as alterações e execute o pipeline do Cloud Manager para implantar a configuração atualizada.


**Tópico pai:**[ Baixar e instalar](download-install.md)

