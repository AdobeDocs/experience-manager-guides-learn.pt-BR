---
title: Recurso de publicação de PDF nativo | Componentes de um modelo de PDF
description: Saiba mais sobre os vários componentes de um modelo de PDF e como personalizá-los e configurá-los.
exl-id: 0ddb3b81-42ca-4a66-be7d-051a5175d53a
source-git-commit: 360bba8b5e6ab61314486497e9cc41348ff903c1
workflow-type: tm+mt
source-wordcount: '2938'
ht-degree: 0%

---

# Componentes de um modelo de PDF {#components-pdf-template}

Um modelo de PDF tem quatro componentes: Layouts de página, Folhas de estilos, Recursos e Configurações. Você pode criar um modelo personalizando esses componentes individuais e associando o modelo a uma predefinição de saída ao gerar uma saída de PDF. As seções a seguir abordam esses componentes e seu processo de personalização em detalhes.


## Criar e personalizar layouts de página {#create-customize-page-layout}

As configurações no componente Layouts de página permitem que você crie a estrutura de uma página definindo o cabeçalho, o rodapé e a área de conteúdo em uma página. Usando o editor de layout de página WYSIWYG, você pode criar um layout de página para diferentes seções em um PDF, como as páginas de capa e contracapa, capítulo, Índice, página em branco, Páginas de matéria frontal, Páginas de matéria traseira, Lista de figuras (LOF), Lista de tabelas (LOT), glossário ou criar um layout para uma página personalizada. Nas Configurações do modelo de PDF, é possível atribuir um layout de página com diferentes seções dentro de um PDF, que são usadas para gerar a saída de PDF.

### Criar um novo layout de página {#create-page-layout}

>[!NOTE]
>
>Há exemplos de layouts de página que foram enviados imediatamente. É possível personalizar esses layouts ou criar novos layouts de página.

1. No Editor da Web, vá para a **Output** guia.
1. Expanda a barra lateral esquerda e clique em **Modelos**.
1. Abra o modelo com o qual deseja trabalhar.
   >[!NOTE]
   >
   >É possível abrir um modelo clicando duas vezes no nome ou clicando no ícone > ao lado do nome.
1. Para criar um novo layout de página, siga um destes procedimentos:
   * Focalizar **Layouts de página** e clique no botão *Opções* ícone) **..** e escolha **Novo layout de página**.
   * No **Modelos** clique no botão **+** ícone ao lado de **Modelos** e escolha **Layout da página** no menu de contexto.

     Isso abre a caixa de diálogo Adicionar layout.

     <img src="assets/add-layout-2.png" alt="Caixa de diálogo Adicionar layout" width="250">
1. Especifique um nome para o novo layout de página.
   >[!NOTE]
   >
   >Evite usar caracteres especiais ao nomear um layout de página. Um espaço no nome é substituído por um sublinhado &quot;_&quot;.
1. Clique em **Concluído**.

   O novo layout é criado e adicionado em Layouts de página.

### Duplicação de um layout de página {#duplicate-page-layout}

1. No **Modelos** do modelo que deseja duplicar, clique duas vezes em  **Layouts de página** ou clique no link **>** ícone antes **Layouts de página**.

   Isso exibe a lista de layouts de página no modelo.

1. Passe o mouse sobre o layout de página que você deseja duplicar e clique no ícone (*Opções* ícone) **..** e selecione **Duplicar** no menu de contexto.

1. No _Duplicar layout_ digite um nome para o layout da página.

1. Clique em **Concluído**.
Uma cópia do layout de página selecionado é criada e adicionada em Layouts de página.

### Personalizar um layout de página {#customize-page-layout}

1. No **Modelos** do modelo que deseja editar, clique duas vezes em **Layouts de página** ou clique no link **>** ícone antes **Layouts de página**.

   Isso exibe a lista de layouts de página no modelo.
1. Para personalizar qualquer layout de página, siga um destes procedimentos:
   * Clique duas vezes em qualquer layout de página.
   * Passe o mouse sobre qualquer layout de página e clique no ícone (*Opções* ícone) **..** e selecione **Editar** no menu de contexto.

   Isso abre o editor de layout de página para personalização.
1. Depois de fazer as alterações desejadas, clique em *Salvar tudo* (ou `Crl+S`).

   Para obter mais informações sobre como definir elementos de layout individuais, como cabeçalho, rodapé, número de página, título e muito mais, consulte [Criar um layout de página](design-page-layout.md).

## Usar folhas de estilos para personalizar o PDF {#stylesheet-customization}

As configurações no componente Folhas de estilos permitem estilizar os componentes do layout da página e o conteúdo DITA usando o editor WYSIWYG ou trabalhar diretamente com o arquivo CSS. Você pode criar seus próprios estilos ou personalizar as propriedades de estilo padrão. O editor WYSIWYG fornece acesso à maioria das propriedades que seriam necessárias para criar o estilo do layout da página ou do conteúdo DITA. Para personalizações avançadas, você pode trabalhar diretamente na Visualização de código-fonte.

### Criar uma nova folha de estilos {#create-stylesheet}

Embora os arquivos CSS sejam fornecidos para conteúdo e layout, você pode criar uma nova folha de estilos para aplicar várias personalizações a um tipo de estilo específico que pode ser aplicado a um componente de destino. Por padrão, os arquivos CSS de amostra são agrupados no produto. Esses arquivos CSS destinam-se a ajudar você a organizar suas informações de estilo em todo o conteúdo e layouts. Você pode optar por mesclar esses estilos em um único arquivo CSS ou em vários arquivos.

Por padrão, sempre que você criar um novo layout de página, a variável `layout.css` O arquivo de está incluído no novo layout da página. Se quiser que o layout de página contenha estilos de um arquivo CSS diferente, basta arrastar e soltar o arquivo CSS desejado na área de edição de conteúdo do novo layout de página. Para validar se o arquivo CSS foi incorporado no layout da página, alterne para a visualização Código-fonte e você encontrará um link para o arquivo CSS na `<head>` elemento.


Para criar uma folha de estilos, siga as etapas abaixo:
1. No **Modelos** , siga um destes procedimentos:
   * Passe o mouse sobre **Folhas de estilos** e clique no botão direito (*Opções* ícone) **..** e escolha **Nova folha de estilos**.
   * Clique em **+** ícone ao lado de **Modelos** e escolha **Folha de estilos** no menu de contexto.

   Isso abre a caixa de diálogo Adicionar folha de estilos.

   <img src="assets/add-stylesheet.png" alt="Adicionar folha de estilos" width="250">
1. Especifique um nome para a nova folha de estilos.
1. Clique em **Concluído**.

   Uma nova folha de estilos é criada e adicionada na seção Folhas de estilos.

### Criar um novo estilo {#create-style}

Por padrão, os arquivos CSS contêm estilos para cabeçalho, parágrafo, caractere, hiperlink, imagem, tabela, div, página e outros estilos. É possível substituir o formato de estilo padrão ou criar um novo estilo.

Normalmente, você criará um novo estilo quando quiser associar um estilo personalizado a qualquer elemento DITA. Para que esses estilos personalizados funcionem, você deve garantir que esteja associando o nome de classe do estilo ao atributo outputclass do elemento DITA.


Para criar um novo estilo, siga as etapas abaixo:
1. Clique com o botão direito em qualquer estilo e escolha Novo estilo no menu de contexto.

   Isso abre a caixa de diálogo Adicionar estilo.

   <img src="assets/add-style.png" alt="Adicionar novo estilo" width="300"/>
1. No **Tag** escolha uma tag para a qual deseja criar um novo estilo.
1. Especificar um **Classe** nome.

   Esse nome de classe deve ser associado ao atributo outputclass da tag no conteúdo de origem.
1. Selecione um **Pseudo-classe** para aprimorar o estilo do elemento.
1. Clique em **Concluído**.

   Um novo estilo é criado e adicionado sob o estilo base.

### Personalizar um estilo predefinido ou novo {#customize-style}

Depois de criar um novo arquivo CSS com estilos padrão ou personalizar estilos em um arquivo CSS existente, você pode usar o editor de estilos para fazer isso.

Para personalizar um estilo, siga as etapas abaixo:
1. Clique duas vezes **Folhas de estilos** ou clique no link **>** ícone antes **Folhas de estilos**.

   Isso exibe os arquivos CSS padrão (Conteúdo e Layout) e personalizados.
1. Abra uma folha de estilos para edição.

   Para abrir a folha de estilos para edição, siga um destes procedimentos:
   * Clique duas vezes no nome da folha de estilos.
   * Passe o mouse sobre o nome da folha de estilos, clique em (ícone Options ) ... e escolha Edit.

   Essa ação abre a folha de estilos para edição e exibe a lista de estilos no painel Estilos.

   <img src="assets/customize-style.png" alt="Personalizar estilo" width="450">

1. Para personalizar um estilo, clique duas vezes em um estilo ou clique no ícone > antes de um estilo para exibi-lo e personalizá-lo usando o editor de Estilos.

Para obter detalhes sobre como trabalhar com os estilos mais comuns, consulte [Trabalhar com os estilos de conteúdo comuns](stylesheet.md).

## Trabalhar com recursos {#work-with-resources}

Este é um contêiner de todos os ativos usados para criar um modelo. Pense nisso como uma pasta, que contém ativos como imagens de fundo, fontes personalizadas, logotipos e muito mais. Sempre que você adiciona um ativo no modelo, ele é carregado ou registrado na pasta de ativos. Em seguida, você pode usar esses ativos para personalizar ou projetar seus modelos de PDF.

Para adicionar um arquivo de ativo à pasta Recursos, siga as etapas abaixo:
1. Passe o mouse sobre a guia Resources folder, clique em (Options icon) ... e escolha Import.

   Isso abre a caixa de diálogo Fazer upload de ativos.

   <img src="assets/resources-import-assets.png" alt="Fazer upload de ativos" width="300">

   O caminho onde o arquivo do ativo será carregado é mostrado na **Selecionar pasta de ativos** campo.
   >[!NOTE]
   >
   >Não é possível alterar o caminho para fazer upload de ativos. Por padrão, todos os ativos são armazenados no `/content/dam/dita-templates/pdf/<PDF-template-name>` pasta.

1. Clique em **Escolher arquivos** para procurar o arquivo de ativo no computador local

1. Clique em **Carregar**.
O arquivo selecionado é importado e listado na pasta Recursos.

## Configurações avançadas de PDF {#advanced-pdf-settings}

Use a seção Configurações para definir as configurações avançadas para o layout de página de PDF, iniciando em PDF ou página par, formatos para as referências cruzadas e ativando as marcas de impressão no PDF final gerado usando o modelo.

Para configurar, clique em **Configurações** no **Modelos** para exibir as seguintes opções:

**Geral**

Defina as configurações básicas para iniciar um capítulo a partir de uma página ímpar ou par, a estrutura do sumário e defina o formato da linha de chamada para as entradas do sumário. Você pode definir a seguinte configuração:

* **Inicie qualquer novo capítulo em**: permite definir como cada capítulo é publicado no PDF final. Você pode escolher entre uma **Nova página**, **Página ímpar**, **Página par** ou **Página atual**  opções. Se você optar por iniciar um novo capítulo a partir de uma página ímpar, uma página em branco será inserida depois de um capítulo que termina em uma página ímpar. Por exemplo, se o capítulo terminar na página número 15, o processo de publicação inserirá um 16 em branco<sup>th</sup> para que o novo capítulo possa começar no 17<sup>th</sup> página.  Se você escolher a variável **Página atual** , todos os capítulos serão publicados na continuação sem nenhuma quebra de página. Por exemplo, se um capítulo terminar no meio da página 15, o próximo capítulo também será iniciado a partir da própria 15 página.

* **Iniciar cada tópico a partir de uma nova página**: Se quiser que cada tópico do capítulo comece em uma nova página, selecione **Iniciar cada tópico a partir de uma nova página** opção. Se quiser manter os tópicos em continuação sem qualquer intervalo de página, desmarque essa opção.

* **Estrutura do índice**: permite personalizar a hierarquia do Sumário. Ele usa as seguintes configurações adicionais:

   * **Usar cabeçalhos até o nível**: permite ajustar o número de níveis de cabeçalho a serem exibidos na estrutura de índice do seu PDF.
   * **Não mostrar o número de página do primeiro nível no índice**: selecione esta opção para ocultar os números de página correspondentes para todos os capítulos que contenham tópicos aninhados ou filhos. Considere o exemplo a seguir em que uma saída é criada sem selecionar essa opção.

  <img src="assets/page-number-in-toc.png" alt="Fazer upload de ativos" width="250">

  No exemplo acima, Configurações avançadas de PDF, Apêndice e Ofício são os títulos de tópico de primeiro nível ou títulos de capítulo. Um número de página é atribuído a todos esses cabeçalhos.

  Agora, se você selecionar essa opção e gerar a saída, você obterá o seguinte índice:

  <img src="assets/page-number-missing-in-toc.png" alt="Fazer upload de ativos" width="250">

  Aqui você pode notar que o primeiro capítulo Configurações avançadas de PDF não recebe nenhum número de página, pois tem tópicos aninhados ou filhos. Ao passo que um número de página se atribuído ao Apêndice e Legal porque são tópicos independentes sem nenhum tópico secundário.

* **Formato do líder**: use o menu suspenso para selecionar linhas pontilhadas, sólidas ou com preenchimento de espaço a fim de conectar níveis de cabeçalho aos números de página correspondentes.
Para aplicar a estrutura de índice e os níveis de cabeçalho de estilo, consulte [Adicionar um índice de capítulo](design-page-layout.md#add-chapter-toc).

  >[!NOTE]
  >
  >Se você for um desenvolvedor de CSS, também poderá definir o formato de líder diretamente no arquivo CSS.

* **Usar marcador de continuação de tabela**: selecione essa opção para definir marcadores para tabelas longas espalhadas em várias páginas. <!--For more information on using table continuation markers, see Use table continuation markers.-->

**Layouts de página**

As configurações de Layouts de página oferecem controle total sobre a especificação de qual layout de página deve ser usado para uma seção específica do documento. Por exemplo, para selecionar um layout para o Sumário, clique no menu suspenso sob o campo Sumário e selecione o layout criado para gerar o Sumário.

É importante observar que as configurações do mapa de favoritos têm prioridade sobre as configurações do layout da página.

As seguintes configurações estão disponíveis na seção Layout da página:

<img src="assets/template-page-layout.png" alt="Layouts de página" width="550">


**Layout de página padrão**: selecione um layout de página que atue como o layout padrão para todas as páginas no PDF. Esse é o layout de página base aplicado às seções ou aos tópicos em que você não criou um layout de página dedicado.

**Layout de página para diferentes seções**: é possível mapear um layout de página com as seguintes seções da saída do PDF. Se você tiver criado um layout de página para a seção relacionada, selecione-o na lista suspensa. Se nenhum layout de página tiver sido criado para seções específicas, o layout de página padrão será aplicado.

* **Capítulos e tópicos**: Você pode especificar o layout da página para o Capítulo e Tópicos. O layout selecionado será aplicado a todos os capítulos e tópicos.

* **TOC**: Se você tiver criado o layout de página de índice, selecione **TOC** na lista suspensa, e todas as páginas de índice no documento terão o layout de página de índice.

* **Lista de figuras e Lista de tabelas**: Também é possível especificar o layout da página para figuras e tabelas. O layout selecionado será aplicado a todas as figuras e tabelas.

* **Índice e Glossário**: se você tiver projetado um layout de página de índice, mapeie-o para a opção Índice. Se você tiver um layout de página do Glossário, mapeie-o para a opção Glossário.

* **Páginas de primeiro plano e de segundo plano**: esses layouts de página definem o estilo das páginas principais ou secundárias do livro. Se você projetou o layout da frente, mapeie-o para o **Páginas Principais** opção. Quando você seleciona o layout da frente na lista suspensa, o layout da frente é aplicado a todos os tópicos presentes na frente.

  Se você projetou o layout de material de fundo, mapeie-o para o **Páginas de fundo importantes** opção. Quando você seleciona o layout de material de fundo na lista suspensa, o layout de material de fundo é aplicado a todos os tópicos presentes no material de fundo.

  **Páginas Principais** também é usado como layout de fallback para **TOC**, **Lista de figuras** e Lista de tabelas.  Da mesma forma, **Páginas de fundo importantes** também é usado como layout de fallback para **Índice** e **Glossário** layouts. Se você não tiver selecionado o layout dessas páginas, o layout selecionado de Páginas da frente ou do verso será aplicado.  Se você não tiver selecionado o layout Páginas da frente ou do verso, o layout padrão da página será aplicado a elas.

* **Layout de página para páginas vazias**: também é possível especificar o layout das páginas vazias. O layout selecionado será aplicado a todas as páginas vazias. Por exemplo, se você tiver criado um layout de página em branco para todas as páginas vazias, selecione **Em branco** na lista suspensa, e todas as páginas vazias no documento terão o layout Página em branco.

* **Página de capa e página traseira**: Se você tiver criado um layout de folha de rosto, mapeie-o para a tag **Folha de rosto** opção. Da mesma forma, se você tiver um layout de página de trás, mapeie-o para a tag **Voltar à página** opção. Se nenhum layout de folha de rosto ou de página posterior tiver sido criado, o layout de página padrão será aplicado.



Para obter mais informações sobre layouts de página, consulte [Criar um layout de página](design-page-layout.md).

**Ordem da página**

Você pode ativar ou desativar as seguintes seções no PDF e também organizar a ordem em que elas devem aparecer na saída final do PDF:

<img src="assets/page-order-advance-settings.png" alt="Layouts de página" width="550">

* TOC
* Capítulos e tópicos
* Lista de figuras
* Lista de tabelas
* Índice
* Glossário

Se você não quiser mostrar uma seção específica na saída do PDF, desative o botão de alternância.

Você também pode definir a ordem em que essas diferentes seções são geradas no PDF. Para alterar a ordem padrão dessas páginas, selecione as barras pontilhadas para arrastar e soltar o layout da página no local desejado.

>[!NOTE]
>
> Essas configurações de ordem e inclusão se aplicam somente a um mapa DITA. Para um mapa, essas configurações não se aplicam. As páginas em um mapa são exibidas de acordo com a ordem das seções no mapa.


Seu PDF conterá os layouts de página ativados na ordem em que você os organizou aqui.
**Capítulo e tópicos** o layout é sempre ativado e **Glossário** o layout é sempre desativado por padrão. Não é possível alterná-los.




**Imprimir**

Configure as configurações de produção de impressão para atribuir marcas de impressora, selecionar modelos de cores e especificar propriedades relacionadas à impressão da saída de PDF.

* **Marcas da impressora**: quando você prepara um documento para produção de impressão, marcas de impressora são adicionadas aos limites da página para auxiliar no alinhamento, corte e seleção de cores adequados durante a impressão. Ao selecionar uma marca de impressora, o limite da página é estendido para acomodar a marca, que é aparada durante a impressão. Você pode optar por exibir as seguintes marcas de impressora na saída do PDF:
   * **Marcas aparadas**: selecione a opção para colocar uma marca em cada canto da área de aparagem para indicar onde o papel precisa ser aparado após a impressão.
   * **Marcas de sangramento**: selecione para colocar uma marca em cada canto da caixa de sangria para indicar a área de aparagem da imagem estendida.
   * **Marcas de registro**: selecione para colocar uma marca fora da área de corte para alinhar as diferentes separações em um documento colorido.
   * **Barras de cores**: selecione para adicionar uma faixa de cores fora da área de apara, a fim de manter a consistência das cores e ajustar a densidade da tinta ao imprimir.

  Definir dimensões para as marcas de impressora selecionadas usando o **Largura da linha**, **Cor da linha**, e **Largura da caixa de sangria** opções.

* **Tamanho da caixa de mídia**: este é o tamanho geral da página, incluindo a área estendida ocupada pelas marcas da impressora. Use a opção suspensa para selecionar o tamanho da página para a saída de PDF ou criar seu próprio tamanho personalizado.

* **Espaço de cor**: você tem a opção de escolher entre espaços de cores RGB ou CMYK para imprimir o documento PDF. Escolha RGB para exibir o PDF gerado digitalmente e o CMYK para impressão física. As cores definidas no documento são convertidas no espaço de cores escolhido.
  >[!NOTE]
  >
  >Um perfil de cores ICC é necessário para a criação de PDF/A se estiver usando o espaço de cores CMYK.

  <!--For more information on applying these print settings, see *Printing preferences*.-->

**Referências cruzadas**

Use a guia Referência cruzada para definir como as referências cruzadas são publicadas no PDF. É possível formatar as referências cruzadas para título de tópico, tabelas, figuras e muito mais. <!--For more information, see *Format cross-references*.-->
