---
title: Criar e personalizar modelos de PDF nativos
description: Saiba como criar e personalizar modelos de PDF nativo.
exl-id: 7660da8e-8a1e-4493-b99b-9b5de9a7483f
source-git-commit: 49fa930483f48cafd057002ee26c9499ce967c60
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# modelo PDF {#PDF-template}

O uso de um modelo garante a consistência do layout e da estrutura do conteúdo. Como os modelos são predefinidos, você pode evitar retrabalho em problemas de formatação que surgem para cada novo projeto ou atualização. Os modelos permitem criar layouts de página, conteúdo de estilo e aplicar várias configurações para personalizar o PDF.

Embora os autores possam usar as predefinições de PDF para gerar saída, os desenvolvedores podem criar seus próprios templates. Há modelos de envio prontos para uso, que podem ser personalizados ou duplicados pelos desenvolvedores de acordo com seus requisitos organizacionais.


## Criar um novo modelo de PDF {#create-pdf-template}

Você pode criar modelos de PDF personalizados com layouts de página específicos e definir a formatação de componentes de layout de página (como índice, glossário) ou componentes DITA (como cabeçalho, parágrafo, lista) usando folhas de estilos. Você pode criar um novo modelo do zero ou criá-lo usando um modelo de amostra.

Para criar um novo modelo de PDF, siga as etapas abaixo:
1. No Editor da Web, vá para a **Output** guia.
1. Expanda a barra lateral esquerda e selecione **Modelos**.
<img src="assets/create-pdf-template.png" alt="Criar modelo de PDF" width="400">
1. No painel **Modelos**, selecione o ícone **+** ao lado de **Modelos** e escolha **Modelo de PDF**.
1. Especifique um nome para o modelo na caixa de diálogo **Novo modelo**.
1. Clique em **Concluído**.

O novo modelo é criado e adicionado na variável *Modelos* painel.

## Duplicação de um modelo de PDF {#duplicate-pdf-template}

Para criar um novo modelo com os mesmos layouts e formatação de página de um modelo existente, é possível criar uma cópia. Depois que um modelo for duplicado, você poderá personalizar ainda mais seus componentes conforme necessário.

Para duplicar um template de PDF existente, siga as etapas abaixo:
1. No Editor da Web, vá para a **Output** guia.
1. Expanda a barra lateral esquerda e selecione **Modelos**.

   Isso abre o painel Modelos.
1. Passe o mouse sobre o modelo que deseja duplicar e selecione o (*Opções* ícone) **..** e escolha **Duplicar** no menu de contexto.

   Isso abre a caixa de diálogo Duplicar modelo.\
   <img src="assets/duplicate-template.png" alt="Duplicar modelo de PDF" width="250">
1. Especifique um nome para o modelo.

   A variável **Nome** O campo é pré-preenchido como uma cópia do mesmo nome do modelo de origem.

1. Para especificar um nome preferencial, remova o nome pré-preenchido e especifique um nome.
1. Clique em **Concluído**.

   Um modelo duplicado é criado e adicionado em Modelos.

## Personalizar um modelo de PDF {#customize-pdf-template}

É possível personalizar modelos ajustando os componentes do modelo e aplicando formatos de estilo usando folhas de estilos.

Para personalizar um modelo de PDF, siga as etapas abaixo:
1. No Editor da Web, vá para a guia Saída.
1. Expanda a barra lateral esquerda e selecione Modelos.

   Isso abre o painel Modelos.
1. Para exibir os componentes de um modelo, siga um destes procedimentos:

   * Selecione o ícone > ao lado de um modelo ou clique duas vezes no nome do modelo.
   * Passe o mouse sobre qualquer modelo, selecione o ... (ícone Options ) e escolha Edit no menu de contexto.

     Por padrão, isso abre o painel Configurações no editor de modelos.
   <img src="assets/customize-pdf-template.png" alt="Personalizar o PDF Template" width="350">

   >[!NOTE]
   >
   >  O administrador pode baixar os modelos mais recentes no caminho a seguir e substituir os existentes:
   >
   > `/libs/fmdita/pdf`

   Os vários componentes do modelo que você pode personalizar são categorizados nas seguintes seções:
   * Layouts de página: um PDF típico contém páginas diferentes, como uma capa ou página de título, índice, capítulo, índice, citações e muito mais. A seção Layouts de página permite que você crie a aparência de páginas diferentes que formariam seu PDF. Para obter mais detalhes, consulte [Layouts de página](../native-pdf/components-pdf-template.md#page-layouts).

     Além da aparência, também é possível definir a organização dos elementos da página, como o cabeçalho, o rodapé e as áreas de conteúdo em uma página. Para saber mais sobre como personalizar o layout de uma página, consulte [Criar e personalizar layouts de página](components-pdf-template.md#create-customize-page-layout).

   * Folhas de estilos: as configurações na seção Folhas de estilos permitem personalizar a aparência dos componentes de layout da página, como índice, glossário, citações e muito mais. Além disso, também é possível personalizar os estilos do conteúdo DITA, como cabeçalhos, parágrafos, listas e muito mais. Para saber mais sobre como usar as folhas de estilos, consulte [Usar folhas de estilos para personalizar o PDF](components-pdf-template.md#stylesheet-customization).
   * Recursos: armazene arquivos de ativos que você precisaria personalizar ou criar modelos de PDF. Ativos como logotipos, fontes personalizadas, imagens de fundo e muito mais são armazenados em Recursos. Para saber mais sobre a utilização de recursos, consulte [Trabalhar com recursos](components-pdf-template.md#work-with-resources).
   * Configurações: defina as configurações de saída para gerar um PDF usando o modelo. Esta seção permite definir o mapeamento de modelo para várias páginas em um PDF, página inicial de capítulo, marcadores de impressão, citações e muito mais.
Você também pode organizar a ordem em que eles devem aparecer na saída final do PDF.
Para obter mais informações sobre como aplicar configurações, consulte [Configurações avançadas de PDF](components-pdf-template.md#advanced-pdf-settings).


1. Para personalizar um componente de modelo, clique duas vezes em um componente de modelo ou selecione o ícone > antes dele.

   Por exemplo, clique duas vezes em *Layouts de página* ou selecione o *>* ícone antes *Layouts de página* para visualizar os layouts de página disponíveis.
1. Depois de fazer as alterações desejadas, selecione *Salvar tudo* (ou `Ctrl+S`).
