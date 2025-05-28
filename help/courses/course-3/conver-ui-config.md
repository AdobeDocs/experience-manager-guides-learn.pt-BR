---
title: Configuração do editor AEM Guides
description: Personalização de configurações JSON e conversão de configurações da interface do usuário para o novo Editor do AEM Guides.
exl-id: bb047962-0e2e-4b3a-90c1-052a2a449628
source-git-commit: efdb02d955e223783fc1904eda8d41942c1c9ccf
workflow-type: tm+mt
source-wordcount: '1197'
ht-degree: 0%

---

# Visão geral

Ao migrar da interface antiga para a nova interface do AEM Guides, as atualizações do **ui_config** devem ser convertidas em configurações de interface mais flexíveis e modulares. Esta estrutura ajuda a adotar as alterações facilmente na **barra_de_ferramentas_do_editor** e em [outras barras de ferramentas](/help/courses/course-3/conver-ui-config.md#editing-json-for-different-screens). O processo também suporta a modificação de outras visualizações e widgets no aplicativo.

>[!NOTE]
>
>As personalizações aplicadas a botões específicos podem enfrentar problemas durante a transição para a estrutura de extensão. Se isso ocorrer, você poderá levantar um tíquete de suporte em relação a esta página para obter suporte imediato e resolução.

## Edição de JSON para telas diferentes

Arquivos JSON podem ser adicionados à seção Configuração da interface do editor XML para várias telas e widgets. Veja abaixo uma lista de widgets amplamente usados e suas IDs:

1. [editor_toolbar](assets/toolbars/editor_toolbar.json): barra de ferramentas do Webeditor que consiste em ações de arquivo e conteúdo.
1. [editor_tab_bar](assets/toolbars/editor_tab_bar.json): o modo de exibição com guias de arquivos abertos no webeditor possui ações que você pode executar em arquivos abertos.
1. [file_mode_switcher](assets/toolbars/file_mode_switcher.json): ajuda a alternar entre os diferentes modos disponíveis (autor, origem, visualização) para os arquivos abertos no webeditor.

   ![barra_de_ferramentas_do_editor](images/reuse/editor_toolbar.png)

1. [map_console_navigation_bar](assets/toolbars/map_console_navigation_bar.json): é a barra de informações do mapa aberto no console do mapa. Permite alterar o mapa e fornece acesso às configurações.
1. [map_console_action_bar](assets/toolbars/map_console_action_bar.json): esta é a barra de ação para itens de console do mapa, como Predefinição de saída, Linha de base, Tradução e Relatórios, que fornece informações relevantes, juntamente com seus respectivos botões de ação.

   ![map_console](images/reuse/map_console.png)

1. [home_navigate_bar](assets/toolbars/home_navigation_bar.json): barra de cabeçalho da página inicial do Guides, onde a mensagem de boas-vindas é exibida junto com o perfil da pasta selecionada.

   ![barra_de_navegação_inicial](images/reuse/home_navigation_bar.png)

<br>

## Estrutura geral de cada JSON

Cada JSON segue uma estrutura consistente:

1. `id`: Especifica o widget em que o componente está sendo personalizado.
1. `targetEditor`: define quando exibir ou ocultar um botão usando as propriedades de modo e editor:

   As seguintes opções são suportadas em `targetEditor`:

   - `mode`
   - `displayMode`
   - `editor`
   - `documentType`
   - `documentSubType`
   - `flag`

   Para obter detalhes, consulte [Noções básicas sobre as propriedades do targetEditor](#understanding-targeteditor-properties)

   >[!NOTE]
   >
   > A versão 2506 do Experience Manager Guides apresenta novas propriedades: `displayMode`, `documentType`, `documentSubType` e `flag`. Essas propriedades são compatíveis somente a partir da versão 2506. Da mesma forma, a alteração de `toc` para `layout` na propriedade mode também se aplica a partir desta versão.
   >
   > Um novo campo, `documentType`, agora está disponível junto com o campo `editor` existente.  Ambos os campos são compatíveis e podem ser usados conforme necessário. No entanto, é recomendado usar `documentType` para garantir a consistência entre implementações, especialmente ao trabalhar com a propriedade `documentSubType`. O campo `editor` permanece válido para oferecer suporte à compatibilidade com versões anteriores e integrações existentes.


1. `target`: especifica onde o novo componente será adicionado. Isso usa pares de valores chave ou índices para identificação exclusiva. Os estados de exibição incluem:

   - **anexar**: adicionar no final.

   - **anexar**: adicionar no início.

   - **substituir**: substitui um componente existente.

Exemplo de estrutura JSON:

```json
{
  "id" : "editor_toolbar",
  "view": {
    "items": [
      {
        ...,
        "targetEditor": {
          "mode": [
            "preview"
          ],
          "editor": [
            "xml"
          ]
        },
        "target": {
          "key": "label",
          "value": "Table",
          "viewState": "prepend"
        },
        ...
      },
    ]
  }
}
```

<br>

## Compreendendo as propriedades de `targetEditor`

Abaixo está um detalhamento de cada propriedade, sua finalidade e valores compatíveis.

### `mode`

Define o modo operacional do editor.

**Valores com suporte**: `author`, `source`, `preview`, `layout` (anteriormente `toc`), `split`

### `displayMode` *(opcional)*

Controla a visibilidade ou a interatividade dos componentes da interface do usuário. O valor padrão é definido como `show`, se não for especificado.

**Valores com suporte**: `show`, `hide`, `enabled`, `disabled`

Exemplo:

```
 {
        "icon": "textBulleted",
        "title": "Custom Insert Bulleted",
        "on-click": "$$AUTHOR_INSERT_REMOVE_BULLETED_LIST",
        "key": "$$AUTHOR_INSERT_REMOVE_BULLETED_LIST",
        "targetEditor": {
          "documentType": [
            "ditamap"
          ],
          "mode": [
            "author"
          ],
          "displayMode": "hide"
        }
      },
```

### `editor`

Especifica o tipo de documento primário no editor.

**Valores com suporte**: `ditamap`, `bookmap`, `subjectScheme`, `xml`, `css`, `translation`, `preset`, `pdf_preset`

### `documentType`

Indica o tipo de documento principal.

**Valores com suporte**: `dita`, `ditamap`, `bookmap`, `subjectScheme`, `css`, `preset`, `ditaval`, `reports`, `baseline`, `translation`, `html`, `markdown`, `conditionPresets`

> Valores adicionais podem ser suportados para casos de uso específicos.

Exemplo:

```
 {
        "icon": "textNumbered",
        "title": "Custom Numbered List",
        "on-click": "$$AUTHOR_INSERT_REMOVE_NUMBERED_LIST",
        "key": "$$AUTHOR_INSERT_REMOVE_NUMBERED_LIST",
        "targetEditor": {
          "documentType": [
            "dita",
            "ditamap"
          ],
          "mode": [
            "author",
            "source"
          ]

        }
      },
```

### `documentSubType`

Classifica ainda mais o documento com base em `documentType`.

- **Para`preset`**: `pdf`, `html5`, `aemsite`, `nativePDF`, `json`, `custom`, `kb`
- **Para`dita`**: `topic`, `reference`, `concept`, `glossary`, `task`, `troubleshooting`

> Valores adicionais podem ser suportados para casos de uso específicos.

Exemplo:

```
 {
        "icon": "rename",
        "title": "Custom Rename",
        "on-click": "$$PUBLISH_PRESETS_RENAME",
        "label": "Custom Rename",
        "key": "$$PUBLISH_PRESETS_RENAME",
        "targetEditor": {
          "documentType": [
            "preset"
          ],
          "documentSubType": [
            "nativePDF",
            "aemsite",
            "json"
          ]

        }
      },
```

### `flag`

Indicadores booleanos para o estado ou os recursos do documento.

**Valores com suporte**: `isOutputGenerated`, `isTemporaryFileDownloadable`, `isPDFDownloadable`, `isLocked`, `isUnlocked`, `isDocumentOpen`

Além disso, você também pode criar um sinalizador personalizado dentro de `extensionMap` que é usado como um sinalizador em `targetEditor`. Aqui, `extensionMap` é uma variável global usada para adicionar chaves personalizadas ou valores observáveis.

Exemplo:

```
 {
        "icon": "filePDF",
        "title": "Custom Export pdf",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "documentType": [
            "markdown"
          ],
          "mode": [
            "preview"
          ],
          "flag": ["isPDFDownloadable"]

        }
      },
```


## Exemplos

Veja abaixo um exemplo de como adicionar, excluir ou substituir um botão na barra de ferramentas do editor.

### Adição de um botão

Adicionando um novo botão **Inserir Tabela Personalizada** em **editor_toolbar** para adicionar uma tabela simples que seja visível somente no modo de visualização.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "table",
        "title": "Insert Custom Table",
        "on-click": {
          "name": "$$AUTHOR_INSERT_ELEMENT",
          "args": [
            "simpletable",
            "table",
            "choicetable"
          ]
        },
        "key": "$$AUTHOR_INSERT_ELEMENT",
        "targetEditor": {
          "mode": [
            "preview"
          ],
        },
        "target": {
          "key": "label",
          "value": "Table",
          "viewState": "prepend"
        }
      }
    ]
  }
}
```

![Inserir tabela personalizada](images/reuse/insert-custom-table.png)

### Excluir um botão

Excluir um botão da barra de ferramentas. Aqui removemos o botão de adição de imagens da barra de ferramentas do editor.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "hide": true,
        "target": {
          "key": "label",
          "value": "Image",
          "viewState": "replace"
        }
      }
    ]
  }
}
```

### Substituição de um botão

Substituindo o botão **Multimídia** da barra de ferramentas pelo botão de inserção de link do **Youtube**, que só é visível no modo de autor.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "s2youtube",
        "title": "Youtube",
        "on-click": {
          "name": "$$AUTHOR_INSERT_ELEMENT",
          "args": "<object data='http://youtube.com'></object>"
        },
        "targetEditor": {
          "mode": [
            "author"
          ]
        },
        "target": {
          "key": "elementId",
          "value": "toolbar-multimedia",
          "viewState": "replace"
        }
      }
    ]
  }
}
```

![Botão do Youtube](images/reuse/youtube-button.png)

<br>

### Adição de um botão no modo de visualização

De acordo com o design, a visibilidade do botão é gerenciada separadamente para modos bloqueados e desbloqueados (somente leitura) para manter uma experiência do usuário clara e controlada. Por padrão, qualquer botão recém-adicionado fica oculto quando a interface está no modo somente leitura.
Para tornar um botão visível no modo **somente leitura**, você deve especificar um destino que o coloque dentro de uma subseção da barra de ferramentas que permaneça acessível mesmo quando a interface estiver bloqueada.
Por exemplo, ao especificar o destino como **Baixar como PDF**, você pode garantir que o botão apareça na mesma seção que um botão visível existente, tornando-o acessível no modo desbloqueado.

```json
"target": {
  "key": "label",
  "value": "Download as PDF",
  "viewState": "prepend"
}
```

Adicionando um botão **Exportar como PDF** no modo **Visualização**, que estará visível no modo de bloqueio e desbloqueio.

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "filePDF",
        "title": "Export as PDF",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "editor": [
            "ditamap",
            "xml"
          ],
          "mode": [
            "preview"
          ]
        },
        "target": {
          "key": "label",
          "value": "Download as PDF",
          "viewState": "prepend"
        }
      },
      {
        "icon": "filePDF",
        "title": "Export as PDF",
        "on-click": "$$DOWNLOAD_TOPIC_PDF",
        "key": "$$DOWNLOAD_TOPIC_PDF",
        "targetEditor": {
          "editor": [
            "ditamap",
            "xml"
          ],
          "mode": [
            "preview"
          ]
        }
      }
    ]
  }
}
```

O trecho a seguir mostra o botão **Exportar como PDF** com o cenário de bloqueio.

![Exportar como PDF](images/reuse/lock.png)

Além disso, o botão **Exportar como PDF** com o cenário de desbloqueio pode ser visto no trecho abaixo.

![Exportar como PDF](images/reuse/unlock.png)

## Como fazer upload de JSONs personalizados

1. Na guia Configuração do **Editor XML**, clique em **Editar** na barra superior.
1. Agora, na subseção **Configuração da interface do Editor de XML**, você poderá ver um botão **carregar**.

   ![Botão Carregar](images/reuse/ui-config-upload.png){width="400" height="150"}

1. Você pode clicar em e fazer upload do json modificado. (O json a ser carregado deve ter o mesmo nome da ID do widget que está sendo personalizado)
1. Depois de carregado, clique em **Salvar** na barra superior.

   Para cada arquivo carregado, você também pode **excluir** o json para remover sua personalização da interface ou **baixar** para exibi-lo ou modificá-lo novamente.

   ![Botão Baixar](images/reuse/download-delete-json.png){width="400" height="150"}

<br>


## Como fazer upload de CSS personalizado

Você também pode adicionar css para personalizar a aparência dos botões adicionados personalizados ou widgets ou botões já existentes na interface do usuário.

Para um botão personalizado recém-adicionado, adicione uma **classe_de_extração** ao botão ou componente personalizado dentro do JSON.
Para uma classe antiga, você também pode inspecionar o elemento e modificar as classes existentes.

```json
{
  "icon": "table",
  "title": "Insert Custom Table",
  "extraclass": "custom-css",
  "key": "$$AUTHOR_INSERT_ELEMENT",
  "targetEditor": {
    "mode": [
      "preview"
    ],
  },
  "target": {
    "key": "label",
    "value": "Table",
    "viewState": "prepend"
  }
}
```

1. Na guia Configuração do **Editor XML**, clique em **Editar** na barra superior.
1. Agora, na subseção **Layout da página do Editor de XML**, você poderá ver um botão **carregar**.

   ![Botão Carregar](images/reuse/page-layout-upload.png){width="400" height="150"}

1. Você pode clicar em e fazer upload do css modificado. (Somente arquivos css são suportados)
1. Depois de carregado, clique em **Salvar** na barra superior.

   Para cada arquivo carregado, você também pode **excluir** o css para remover sua personalização da interface ou **baixar** para exibi-lo ou modificá-lo novamente.

   ![Botão Baixar](images/reuse/download-delete-css.png){width="400" height="150"}


<br>

### Exemplo para personalizar o css do botão

Aqui adicionamos um novo botão **Inserir Tabela Personalizada** na **editor_toolbar** para adicionar uma tabela simples que é visível somente no modo de visualização e aplicar um css personalizado a ela.
Esse css modifica o plano de fundo do botão e o tamanho da fonte de seu título.

![Exemplo de CSS](images/reuse/css-customization.png)


```css
#editor_toolbar {
  .custom-css {
    background-color: burlywood;
    font-size: 2rem;  
  }
}
```

```json
{
  "id": "editor_toolbar",
  "view": {
    "items": [
      {
        "icon": "table",
        "title": "Insert Custom Table",
        "extraclass": "custom-css",
        ...
      }
    ]
  }
}
```

<br>

## Etapas para converter a configuração da interface do usuário em Json modulares

1. Na tela Navegação, clique no ícone [!UICONTROL **Ferramentas**].

   ![Ícone de Ferramentas](images/reuse/tools.png)

1. Selecione **Guias** no painel esquerdo.

1. Clique no bloco [!UICONTROL **Perfis de pasta**].

   ![Perfis de pasta](images/reuse/folder-profiles-tile.png)

1. Selecione um Perfil de pasta.

1. Clique na guia [!UICONTROL **Configuração do editor XML**].

1. Você pode clicar no botão **Converter configuração da interface para JSON**. Isso gerará o **editor_toolbar** e o **map_console_action_bar** json, que contém as alterações feitas no **ui_config**.

   ![Converter configuração de interface para JSON](images/reuse/convert-ui-config-json.png)

1. Você pode fazer check-out da amostra gerada de jsons para a [Barra de ferramentas do editor](assets/editor_toolbar.json) e a [Barra de ação do console de mapa](assets/map_console_action_bar.json)


>[!NOTE]
>
>As alterações feitas nas seções da **barra de ferramentas** e da **barra de ferramentas** foram adicionadas ao json **barra_de_ferramentas_do_editor**, que pode ser visto na página Editor. As alterações feitas nos botões relacionados a Predefinições ou Tradução em **ui_config** são adicionadas ao **map_console_action_bar** json, que pode ser visto na página Console do Mapa.
