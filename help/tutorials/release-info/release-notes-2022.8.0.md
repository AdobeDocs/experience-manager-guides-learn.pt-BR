---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de agosto de 2022
description: Versão de agosto dos Guias do Adobe Experience Manager as a Cloud Service
source-git-commit: d49ccb3f654dede0c0447849d89ecbab333a1055
workflow-type: tm+mt
source-wordcount: '1156'
ht-degree: 2%

---

# Versão de agosto dos Guias do Adobe Experience Manager as a Cloud Service

## Atualize para o lançamento de agosto

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação do Cloud Services configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.8.167.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de agosto AEM Guias as a Cloud Service.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software compatíveis com AEM Guias as a Cloud Service versão de agosto de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac |
| --- | --- | --- |
| 2022.8.0 | 2.7.5 | 2.7.5 |
|  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service oferecem muitos aprimoramentos e novos recursos na versão de agosto:

### Exibição de layout no Editor de mapa

Agora é possível exibir o layout completo de um mapa DITA no Editor de mapa. Ao abrir um mapa para edição, ele abre o **Layout** exibição do Editor de mapa. Nesta visualização, você pode ver a hierarquia do mapa em uma visualização em árvore e também organizar ou estruturar os tópicos em um mapa.

![exibição de layout](assets/layout-view-map.png)

A exibição Layout contém uma barra de ferramentas separada que ajuda a executar muitas tarefas nos tópicos presentes em um mapa.
Você pode inserir referências de tópico, grupo de tópicos, definições-chave em um mapa. Você pode reorganizar os tópicos presentes em um mapa movendo-os para cima, para baixo, para a esquerda ou para a direita. Você também pode arrastar e soltar os tópicos para movê-los em um mapa. O Editor de mapa também fornece ícones para bloquear ou desbloquear arquivos, verificar o histórico de versões e fazer um gerenciamento de rótulos de versão.


A exibição Layout também fornece a variável **Opções de Exibição** para mostrar ou ocultar o número da linha, mostrar ou ocultar a caixa de seleção ou mostrar o nome do arquivo ou o título dos tópicos em um mapa.


![opções de exibição](assets/view-options.png)

Também é possível exibir os tópicos com base nos filtros condicionais aplicados neles.

Além de organizar tópicos no arquivo de mapa, você também pode adicionar, mover, copiar, colar ou excluir referências usando o **Opções** disponível para um elemento na exibição Layout. Você também pode arrastar e soltar um tópico ou um mapa do painel do repositório para o mapa aberto no Editor de mapa.

O painel direito exibe as Propriedades do conteúdo e as Propriedades do mapa na exibição Layout do Editor de mapa. Os Atributos em linha definidos para o tópico selecionado são exibidos em relação ao tópico na exibição Layout. Por exemplo, você pode encontrar rapidamente todos os tópicos que têm o atributo da plataforma definido como `IOS`.

Agora, também é possível definir as informações de metadados para os tópicos ou o mapa. É possível definir o Título da navegação, o Texto do link, a Descrição curta e as Palavras-chave para o tópico ou mapa selecionado.

![painel direito da exibição de layout](assets/layout-inline-attributes.png)

Para obter mais detalhes, consulte *Exibição de layout* em Usar guias do Adobe Experience Manager as a Cloud Service.

### Atributos embutidos nas configurações do editor

Guias de AEM agora permitem a configuração de **Atributos em linha** pelo administrador do **Configurações do editor**. Você também pode adicionar novos atributos em linha ou excluir os existentes da variável **Atributos em linha** nas Configurações do editor.
Os atributos em linha configurados definidos para um tópico são exibidos em relação ao tópico na exibição Layout.

![Configurações do editor](assets/editor-settings-inline-attributes.png)


### Filtros adicionais na exibição Repositório

Agora, a pesquisa de filtro na visualização do repositório ficou mais poderosa. Dois novos critérios de pesquisa, **Última modificação** e **Tags** foram adicionadas para filtrar os arquivos e restringir sua pesquisa no repositório AEM:
* **Última modificação**: Você pode procurar arquivos que foram modificados pela última vez após uma data selecionada, mas antes de uma data selecionada. Você também tem a opção de usar os critérios predefinidos e procurar arquivos que foram modificados pela última vez nas últimas 2 horas, na semana passada, no mês passado ou no ano passado.
* **Tags**: Você também pode procurar arquivos que tenham tags específicas aplicadas a eles. Você pode digitar a tag ou selecioná-la na lista suspensa.

![Filtros de visualização do repositório](assets/repo-filter-search.png)


## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* O índice Lucene obsoleto é usado em /core/article-publish/src/main/java/com/adobe/dxml/article/publish/util/DoxUtils.java (9291)
* Node.js atualizado não é usado para publicação. (9835)
* O tópico DITA não é atualizado automaticamente com as alterações feitas no **Propriedades** página. (8745)
* O elemento Frontmatter quando adicionado a um bookmap DITA não funciona corretamente. (9507)
* PDF nativo | Um PDF em branco é gerado ao usar **Geração rápida** para vários arquivos quando um elemento vazio é selecionado. (9822)
* PDF nativo | O apêndice é publicado como um capítulo na saída do PDF. (9829)
* PDF nativo | Quando uma imagem SVG é editada, ela não é mostrada atualizada no layout da página. (9069)
* Um caractere de hífen regular é inserido quando um `Nonbreaking Hyphen` é inserido usando o **Inserir Caractere Especial** caixa de diálogo. (8919)
* O Editor XML não mostra imagens atualizadas nos tópicos se elas tiverem sido editadas. (9500)
* Ao publicar a saída por meio do Editor, as predefinições não podem ser excluídas do **Saída** guia . (9100)
* Os submapas de um mapa DITA não são verificados usando o **Selecionar tudo** no menu reticências. (9814)
* Não é possível arrastar o mapa de soltar ou os modelos de tópico da **Modelos** para o modelo de mapa personalizado no editor da Web. (9846)
* Não é possível criar um novo tópico ou modelo de mapa na subpasta de um mapa ou modelo de tópico. (9888)
* Nenhuma opção está presente para navegar pelos tópicos ou mapas presentes dentro das subpastas de um mapa ou modelo de tópico. (9889)
* Quando um arquivo Schematron é atualizado e salvo junto com o arquivo DITA, o painel direito não é exibido (se o arquivo DITA quebrar as validações presentes no arquivo Schematron). (9986)
* Uma nova predefinição de saída duplicada pode ser criada se seu nome for igual a uma predefinição existente. (997)
* As imagens de SVG são corrompidas e não são publicadas corretamente na geração da saída do HTML. (9949)


## Problemas conhecidos

O Adobe identificou os seguintes problemas conhecidos para a versão dos Guias de AEM as a Cloud Service de agosto de 2022.

### Problemas conhecidos com solução alternativa

Use a solução alternativa fornecida para os seguintes problemas conhecidos:

* A exibição Layout não está visível no Editor de mapa.

   **Solução alternativa**: Atualize o ui_config.json no Perfil da pasta.

* Symbols.json é substituído, portanto, a edição 8919 ocorre.

   **Solução alternativa**: A biblioteca de símbolos.json atualizada deve ser unida com símbolos.json substituídos.

### Outros problemas conhecidos

* Se vários arquivos forem selecionados na seção de resultado exibida ao executar uma pesquisa no repositório e, em seguida, arrastar e soltar na exibição do autor, somente um único arquivo será adicionado.
