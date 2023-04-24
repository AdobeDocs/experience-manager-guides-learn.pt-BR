---
title: Use variáveis para definir as opções Caminho de destino, Nome do site ou Nome do arquivo
description: Saiba como Usar variáveis para definir as opções Caminho de destino, Nome do site ou Nome do arquivo
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---


# Use variáveis para definir as opções Caminho de destino, Nome do site ou Nome do arquivo


Ao gerar saídas AEM Site ou PDF, você pode usar variáveis para definir as opções Caminho de destino, AEM Nome do site ou Nome do arquivo PDF. É possível usar uma única ou uma combinação de variáveis para definir essas opções.

A tabela a seguir lista as variáveis compatíveis prontas para uso:

| Variável | Caminho de destino final | Exemplo |
| --- | --- | --- |
| `${map_filename}` | Usa o nome dos arquivos do mapa DITA para criar o caminho de destino. | **Nome do arquivo de mapa DITA**:<br>`AEMGuides.ditamap`<br><br>**Caminho de destino** configurado como:<br>`/content/output/sites/${map_filename}`<br><br>**Local de saída final**:<br>`/content/output/sites/aemGuides/AEMGuides.html` |
| `${map_title}` | Usa o título do mapa DITA para criar o caminho de destino. | **Nome do arquivo de mapa DITA**:<br>`AEMGuides.ditamap`<br><br>**Título do mapa DITA**:<br>`AEMGuides`<br><br>**Caminho de destino** configurado como:<br>`/content/output/sites/${map_title}`<br><br>**Local de saída final**:<br>`/content/output/sites/AEMGuides/AEMGuides.html` |
| `${preset_name}` | Usa o nome predefinido de saída para criar o caminho de destino. | **Nome da predefinição de saída**:<br>`AEM Guides PDF Output`<br><br>**Nome do arquivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Caminho de destino** configurado como:<br>`/content/output/sites/${preset_name}`<br><br>**Local de saída final**:<br>`/content/output/sites/AEM Guides PDF Output/SampleDita.html` |
| `${language_code}` | Usa o código de idioma onde o arquivo de mapa está localizado para criar o caminho de destino. | **Nome do arquivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Caminho do arquivo de mapa DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Caminho de destino** configurado como:<br>`/content/output/sites/${language_code}`<br><br>**Local de saída final**:<br>`/content/output/sites/en/SampleDita.html` |
| `${map_parentpath}` | Usa o caminho completo do arquivo de mapa para criar o caminho de destino.<br><br>**Observação**: essa variável não pode ser usada para especificar o Nome do Site ou o Nome do Arquivo de PDF. | **Nome do arquivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Caminho do arquivo de mapa DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide`/<br><br>**Caminho de destino** configurado como:<br>`/content/output/sites/${map_parentpath}`<br><br>**Local de saída final**:<br>`/content/output/sites/content/dam/projects/AEM-Guides/en/user-guide/SampleDita.html` |
| `${path_after_langfolder}` | Usa o caminho do arquivo de mapa após a pasta de idioma para criar o caminho de destino.<br><br>**Observação**: Essa variável não pode ser usada para especificar o Nome do Site ou o Nome do Arquivo de PDF. | **Nome do arquivo de mapa DITA**:<br>`SampleDita.ditamap`<br><br>**Caminho do arquivo de mapa DITA**:<br>`/content/dam/projects/AEM-Guides/en/user-guide/`<br><br>**Caminho de destino** configurado como:<br>`/content/output/sites/${path\_after\_langfolder}`<br><br>**Local de saída final**:<br>`/content/output/sites/user-guide/SampleDita.html` |

Além disso, também é possível usar os metadados definidos para o mapa DITA ou o arquivo de marcador como variáveis. Os metadados podem ser encontrados no `/jcr:content/metadata` nó do mapa DITA ou do arquivo de mapa de favoritos. Por exemplo, uma das propriedades de metadados definidas no `/jcr:content/metadata` o nó é `dc:title`. Você pode especificar `${dc:title}` e o valor do título é usado na saída final.
**Tópico principal:**[ Geração de saída](generate-output.md)

