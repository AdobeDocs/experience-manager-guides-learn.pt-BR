---
title: Configurar caracteres especiais adicionais na barra de ferramentas do Editor da Web
description: Como configurar caracteres especiais adicionais na barra de ferramentas do Editor da Web
feature: Web Editor
role: User
exl-id: 0fbc05a5-a6b0-4f6b-bbc4-8fca03581d90
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# Como configurar caracteres especiais adicionais na barra de ferramentas do Editor da Web

Há uma opção de atalho na barra de ferramentas do editor da Web para permitir que o autor insira os caracteres especiais.
O mesmo pode ser visto na captura de tela abaixo:

![Caracteres especiais](assets/special-chars.png)


Essa lista de caracteres pode ser configurada aqui. Se precisar adicionar mais caracteres, siga as etapas abaixo:

+ Faça logon no AEM e abra o modo CRXDE Lite.

+ Crie o arquivo símbolos.json no seguinte local: &#39;/apps/fmdita/xmleditor/&#39; (Você pode copiar o padrão do local - &#39;/libs/fmdita/clientlibs/clientlibs/xmleditor/symbols.json&#39;)

+ Adicione a definição de caractere especial no arquivo símbolos.json como:

```
{
      "label": "Logical Symbols",
      "items": [
        {
          "name": "≥",
          "title": "Greater-Than or Equal To"
        },
        {
          "name": "≤",
          "title": "Smaller-Than or Equal To"
        }
      ]
}
```

A estrutura do arquivo símbolos.json é explicada abaixo:

+ &quot;label&quot;: &quot;Símbolos lógicos&quot;: Especifica a categoria para os caracteres especiais. No trecho, uma categoria com o nome &quot;Símbolo lógico&quot; é definida.

+ &quot;itens&quot;: Isso define a coleção de caracteres especiais na categoria .

+ &quot;name&quot;: &quot;≥&quot;, &quot;title&quot;: &quot;Maior que ou igual a&quot;: Esta é a definição do caractere especial. Ela começa com o rótulo &quot;name&quot;, que não deve ser alterado. O nome é seguido pelo caractere especial. O &quot;título&quot; é o nome ou o título do caractere especial que aparece como a dica de ferramenta desse caractere especial.

É possível definir várias definições de caracteres especiais em uma categoria.

Isso adicionará outra categoria na caixa de diálogo caracteres especiais:

![Categoria de Símbolo Especial](assets/special-char-category.png)

![Inserir Caractere Especial](assets/insert-special-char.png)

>[!MORELIKETHIS]
>
>+ [Guia de Instalação e Configuração](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/3-6/XML-Documentation-for-Adobe-Experience-Manager_Installation-Configuration-Guide_EN.pdf)

