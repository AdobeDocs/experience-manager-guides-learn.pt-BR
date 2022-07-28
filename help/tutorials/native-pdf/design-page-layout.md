---
title: Recurso de publicação do PDF nativo | Criar um layout de página
description: Saiba como criar o layout da página para apresentar informações em diferentes seções da saída do PDF.
hide: true
hidefromtoc: true
exl-id: b4d3bdc4-0d01-46eb-b182-540380220485
source-git-commit: 64e8ab1288674437f6182010ce4963b3780e98a9
workflow-type: tm+mt
source-wordcount: '3289'
ht-degree: 0%

---


# Criar um layout de página

Ao criar um documento do PDF, você teria seções diferentes para apresentar diferentes tipos de informações. Por exemplo, um documento de PDF começaria de uma página inicial ou de capa, que teria o logotipo, o título do livro ou as informações da versão da sua empresa. Em seguida, haveria capítulos, apêndices ou páginas de glossário. Cada seção em um documento do PDF parece diferente e isso é obtido pela criação e personalização do layout da página.

Ao projetar o layout da página, você pode definir os vários elementos que compõem uma página. Por exemplo, você pode definir o tamanho da página, as margens, o cabeçalho e o rodapé, a orientação e outras especificações da página em uma página. O recurso Publicação PDF nativa permite que você crie sua página de acordo com os padrões de Mídia paginada CSS. A maioria das configurações abrangidas pela Mídia com paginação de CSS pode ser facilmente personalizada usando a interface do usuário do recurso PDF nativo. Para alguma outra formatação de nível avançado, você pode usar a Visualização de origem para gravar seu próprio código CSS.

Depois de criar os layouts de página, é necessário associar esses layouts às respectivas seções nas configurações de Layout de página do PDF. Consulte a _Criar e personalizar layouts de página_ para obter detalhes sobre como criar e abrir um layout de página para personalização.

## Tipos de layouts de página e suas variantes

Um documento PDF normalmente contém as seguintes seções:

* Capa
* Índice
* Aumento de números
* Aumento das tabelas
* Capítulo ou páginas de tópico
* Glossário
* Índice
* Página de trás

Essas seções precisariam de um layout de página correspondente para apresentar as informações em um formato específico. Além disso, também é possível ter uma página em branco usada como usuário para iniciar um novo capítulo de uma página ímpar ou par. Nesse caso, seria necessário um layout de página em branco.

As configurações de Layouts de página na seção **Modelo > Configurações** permitem definir qual modelo deve ser usado para diferentes seções do PDF. Cada layout de página pode ter combinações diferentes de página inicial, direita ou esquerda. Estas regras são regidas pelas regras definidas no *Mídia de página CSS* normas.

## Criar os layouts de página inicial, direita ou esquerda

Diferentes layouts de página no modelo de PDF podem ser personalizados com diferentes layouts de página inicial, direita ou esquerda. Você pode criar essas páginas de forma diferente usando o designer de layout de página.

>[!NOTE]
>
>Se quiser ter um layout de página único para uma seção do seu livro, não será necessário criar os layouts de página Primeiro, Direito ou Esquerdo.


Considere os seguintes pontos ao criar layouts de página:

* Se você quiser usar um layout de página único para todas as páginas em um capítulo, crie apenas um layout de página do Capítulo.
* Se você quiser ter uma aparência diferente para a primeira página de capítulos do seu livro, será necessário criar um layout de Primeira página para os seus capítulos.
* Se você quiser ter uma aparência diferente para cada página lateral esquerda e direita do seu livro, será necessário criar as variantes dos lados esquerdo e direito para o layout da página de capítulo.
* Se quiser que seus capítulos iniciem de uma página ímpar ou par, será necessário criar um layout de página em branco. Esse layout de página é usado para preencher a lacuna entre dois capítulos, para garantir que o capítulo inicie da página ímpar ou par desejada.

O exemplo a seguir guiará você pelo processo de criação de variantes de um layout de página:

1. Crie um layout de página do &quot;Capítulo&quot; usando as etapas fornecidas em *Criar um novo layout de página* procedimento.

   Um layout de página do Capítulo em branco é criado e adicionado sob os Layouts da página.

   Por padrão, ao criar um layout de página, ele também é aberto para edição. A captura de tela a seguir exibe um layout de página em branco (padrão):

   <img src="./assets/default-blank-page-layout.png" width="300">

   A área de cabeçalho, rodapé e conteúdo em um modelo é criada por padrão. Você pode personalizar facilmente essas áreas usando as ferramentas, as propriedades da página e as propriedades do conteúdo fornecidas na interface do usuário. Para configuração avançada, você pode usar a Visualização de origem e adicionar o HTML personalizado e o código CSS.

1. Para criar uma variante para o layout da página do Capítulo:

   1. Passe o mouse sobre **Capítulo** e clique em **Opções** para exibir o menu de contexto.

   1. Clique ou passe o mouse sobre o mouse **Adicionar variável de layout** e escolha o layout de página desejado (Primeiro, Esquerda ou Direita) que deseja criar.

   O layout de página selecionado é criado usando uma cópia do layout básico do Capítulo. Isso significa que, se você tiver alterado o layout padrão da página do Capítulo, as mesmas alterações serão replicadas no layout da página da variante.

## Trabalhar com imagens em um layout de página

Com base em seus requisitos, você pode adicionar uma imagem que aparece em cada primeira página de uma saída do Capítulo (PDF). O <u>**Adicionar imagem**</u> no editor de layout de página é usada para inserir imagens em um layout de página.

Por exemplo, se você quiser inserir uma imagem na área de cabeçalho da Primeira página da saída do capítulo, execute as seguintes etapas:

1. Abra o layout de página necessário para edição.

   >[!NOTE]
   >
   >Consulte _Personalizar um layout de página_ seção para abrir um layout de página para personalização ou edição.

1. Clique em Editar cabeçalho (<img src="./assets/header-icon.svg" width="25">) para trazer o cursor para a área do cabeçalho.

1. Clique na Imagem de inserção (<img src="./assets/insert-image-icon.svg" width="25">) ícone.

   A janela pop-up Selecionar caminho é exibida.

1. Navegue até o local da imagem e clique em Selecionar para inseri-la na área do cabeçalho.

   A captura de tela a seguir mostra uma imagem de amostra adicionada na área do cabeçalho.

   <img src="./assets/image-in-header-area.png" width="500">

   Depois que uma imagem é inserida, você pode modificar seus atributos para dar a ela a aparência desejada. A maneira mais fácil de alterar a aparência de uma imagem ou de qualquer outro elemento no layout da página é usar o painel Propriedades de conteúdo para fazer isso. Consulte _Trabalhar com o painel Propriedades de conteúdo_ para as várias propriedades disponíveis por meio da interface do usuário personalizada.

## Trabalhar com campos

Os campos são muito úteis quando você deseja inserir uma parte das informações predefinidas. Por exemplo, você pode incluir um campo Título de capítulo na área de cabeçalho do capítulo que é substituído pelo título do capítulo real quando publicado.

Existem as seguintes categorias para campos que podem ser inseridas no layout da página:

* Data
* Hora
* Título do tópico
* Título do projeto
* Número da página
* Página Total
* Título do capítulo
* Número do capítulo
* Metadados

Cada uma dessas categorias de campo contém diferentes variações nas quais as informações de campo podem ser inseridas. Por exemplo, um campo Data pode ter variações diferentes, como `YYYY-MM-DD`, `MM/DD/YY`, `MM/DD/YYYY` e assim por diante.

No exemplo a seguir, inserimos um número de página e um título de tópico na área de rodapé do layout da página.

1. Abra o layout de página necessário para edição.

   >[!NOTE]
   >
   >Consulte _Personalizar um layout de página_ seção para abrir um layout de página para personalização ou edição.

1. Clique no rodapé Editar (![](./assets/footer-icon.svg)) para trazer o cursor para a área do rodapé.

1. Insira um elemento de parágrafo clicando em Inserir elementos de HTML <img src="./assets/insert-html-element-2.svg" width="25"> e selecionando Parágrafo na lista de elementos.

1. Clique em Inserir campos ( ![](./assets/insert-fields-icon.svg)).

   A janela pop-up Campos é exibida.

1. Selecione o **Número da página** na lista Campo, a categoria **default(1)** formato de número de página na lista Formato e clique em **Inserir**.

   <img src="./assets/insert-page-number-field.svg" width="400">

   <br>

   >[!NOTE]
   >
   >Também é possível editar o formato de todos os campos, exceto o formato padrão. Para fazer isso, clique no ícone Edit ao lado do formato que deseja editar, faça alterações e clique em OK.

   O campo de número de página padrão é inserido na área de rodapé do layout da página.

   <img src="./assets/page-number-field-in-footer.png" width="400">

   A navegação estrutural superior lista os elementos em que as informações são armazenadas.

1. Insira um espaço em branco depois do campo de número de página e clique no botão **Inserir campos** ícone .

1. Selecione o **Título do tópico** na lista Campo, a categoria **Chapter.ptl** formato de título na lista Formato e clique em Inserir.

   O `Chapter.ptl` , que é preenchido com o título do tópico no momento da publicação, é inserido na área do rodapé. No momento, os campos número da página e título do tópico são separados por um espaço.

   <img src="./assets/page-number-topic-title-near-footer.png" width="400">

1. Para alinhar o título do Tópico à direita, execute as seguintes etapas:

   1. Clique no elemento Campo na navegação estrutural para selecionar o campo de título do tópico.

   1. No painel direito, clique em HTML Content Properties.

      <img src="./assets/right-pane-content-properties.png" width="350">

   1. Expanda o **Layout** e defina a **Flutuar** valor da propriedade para **right**.

      <img src="./assets/float-prop-html-content.png" width="350">

      O campo de título do tópico é alinhado ao lado direito do rodapé da página.

      <img src="./assets/topic-title-moved-right-footer.png" width="500">

| Canto do desenvolvedor: | <img src="./assets/developer-corner-icon.svg" width="25"> |
|--- |--- |
| Se você quiser trabalhar diretamente com o CSS e o HTML code, também poderá fazer isso acessando a Exibição da fonte do layout da página e fazendo alterações no código. O trecho de código a seguir mostra a mesma configuração de rodapé feita pelo código: |

```md
…
<div data-region="footer">
	<p>
		<span data-field="page-number" data-format="default">1</span>
		<span data-field="title" data-format="default" style="float: right">Chapter.plt</span>
	</p>
</div>
…
```

## Adicionar um sumário de capítulo

Um capítulo ou um mini índice serve como uma referência rápida para os leitores saberem o que está no capítulo. Normalmente, um sumário de capítulo é adicionado no início de um capítulo. Portanto, se você quiser usar um sumário de capítulo, poderá adicioná-lo ao layout da página de capítulo principal ou ao layout da Primeira página de um capítulo.

No exemplo a seguir, vamos inserir um sumário de capítulo no layout da Primeira página de um capítulo:

1. Abra o layout de página necessário para edição.

   >[!NOTE]
   >
   >Consulte _Personalizar um layout de página_ seção para abrir um layout de página para personalização ou edição.

1. Coloque o cursor na área de conteúdo do layout da página.
1. Clique no sumário do capítulo (<img src="./assets/chapter-toc-icon.svg">) ícone.

   O índice padrão do capítulo é inserido na área de conteúdo.

   <img src="./assets/chapter-toc-default.png" width="400">

   >[!NOTE]
   >
   >O índice padrão contém os cabeçalhos 1 a 4. Aqui, o Título 1 é o próprio Título do Capítulo. Portanto, talvez você não queira ter o título do capítulo novamente no TOC ou talvez queira aumentar o nível de cabeçalhos que deseja no TOC. Você pode personalizar o sumário alterando as propriedades.

1. Abra o painel Propriedades de conteúdo do HTML para personalizar os níveis de cabeçalho do sumário.

   Por exemplo, se você quiser começar do Cabeçalho 2, altere a primeira lista suspensa para iniciar em 2.

   <img src="./assets/customize-chapter-toc.png" width="400">

   Da mesma forma, se você quiser ter cabeçalhos até o nível 5, altere a segunda lista suspensa para 5. O sumário atualizado será exibido conforme mostrado abaixo:

   <img src="./assets/chapter-toc-updated.png" width="400">

   <br>

   >[!NOTE]
   >
   >O PDF publicado final mostrará apenas as entradas do TOC com base no conteúdo dos capítulos. Se você não tiver cabeçalhos de nível 5 em um capítulo, eles não serão mostrados na saída final.

## Trabalhar com layout de página de várias colunas

Layouts de página com várias colunas são muito comuns em publicações de revistas ou índices em um livro. O recurso de publicação PDF nativo permite dividir facilmente seu documento em várias colunas. Usando diferentes layouts de página, você pode optar por manter apenas uma seção específica dividida em várias colunas, mantendo as outras seções em um único layout de coluna (ou normal).

Para criar um layout de página com várias colunas, execute as seguintes etapas:

1. Abra o layout de página necessário para edição.

   >[!NOTE]
   >
   >Consulte _Personalizar um layout de página_ seção para abrir um layout de página para personalização ou edição.

1. Como o layout de várias colunas é aplicado ao conteúdo, excluindo a área de cabeçalho e rodapé, é necessário selecionar o elemento de conteúdo na navegação estrutural.

   Após selecionar a navegação estrutural do conteúdo, o painel Propriedades do conteúdo do HTML mostrará as propriedades de Várias colunas.

   <img src="./assets/multiple-columns-properties.png" width="400">

1. Use as propriedades de várias colunas para personalizar o layout de página de várias colunas:

   * **Contagem de Colunas:** Especifique o número de colunas para dividir a página. Use os ícones de seta para cima e para baixo ou insira um número para definir o número de colunas.

   * **Largura da coluna:** Especifique a largura de uma coluna em um layout de várias colunas. Por padrão, o tamanho é definido em pixels (px), você também pode especificá-lo em pt, rem, em, % ou em unidades.

      >[!NOTE]
      >
      >Se você não especificar um tamanho, as colunas serão dimensionadas automaticamente para se ajustarem às margens de determinada página.

   * **Intervalo de colunas** : Especifique o espaço entre colunas individuais.

   * **Gasto da coluna** : Se você quiser que qualquer elemento no layout da página se estenda entre colunas, será necessário usar essa propriedade. Isso é feito modificando o estilo do elemento desejado usando as Folhas de estilos. Para obter mais informações, consulte _\&lt;section explaining=&quot;&quot; style=&quot;&quot; customization=&quot;&quot;>_.

   No layout da página, se você quiser que um determinado texto apareça na primeira página de todos os layouts de página de capítulo, poderá adicioná-lo à variante Primeira página do layout de página do Capítulo.

   Como mostrado no exemplo a seguir, a propriedade Coluna de expansão para o texto de cabeçalho é definida como tudo. Isso garante que, mesmo que o documento tenha várias colunas, o cabeçalho se expanda entre as colunas.

   <img src="./assets/element-span-across-columns.png" width="400">

   <br>

   >[!IMPORTANT]
   Você pode aplicar a propriedade Coluna de expansão a qualquer elemento DITA.

   * **Preenchimento da coluna** : Especifique como o conteúdo preenche colunas. Por padrão, é definido como Saldo, que preenche cada coluna com a mesma quantidade de conteúdo.

   * **Regra de coluna** : Se você quiser ter uma linha entre colunas, use essa propriedade para definir os estilos de linha ou de regra. Especifique os valores para Estilo, Cor e Largura da regra para adicionar uma linha entre colunas.


## Usar as Propriedades da página para uma orientação de página diferente

Ao projetar um layout de página, é essencial ter controle sobre várias propriedades da página. O recurso PDF nativo encapsula todas as principais propriedades da página sob o painel Propriedades da página. O painel Propriedades da página fornece acesso a várias propriedades nas seguintes seções:

* **Tamanho da página**: Especifique o tamanho de página que deseja usar para o layout de página. A lista suspensa Tamanho da página permite escolher entre mais de 15 tamanhos de página.

* **Orientação**: Especifique a orientação de página a ser usada para o layout de página. É possível escolher entre as orientações da página Retrato ou Paisagem. Observe que é possível optar por ter diferentes orientações aplicadas a diferentes variantes de página em um layout de página. Por exemplo, você pode definir a orientação Retrato na Primeira página e Paisagem nos layouts das páginas Esquerda e Direita.

* **Exibir rotação**: Especifique a exibição ou a direção na qual o conteúdo da página é apresentado. Você pode escolher 90 graus no sentido horário, 90 no sentido anti-horário ou 180 graus no sentido anti-horário. Isso é muito útil em uma situação em que você deseja usar uma combinação de layouts Retrato e Paisagem na saída. Por exemplo, você pode usar o retrato como o layout de página genérico e definir o layout de página paisagem para capturar tabelas longas. Nessa situação, você pode optar por exibir o conteúdo da tabela em 90 graus no sentido horário. Dessa forma, a página será orientada em paisagem e o conteúdo será girado 90 graus para manter a continuidade na exibição. Veremos como isso será feito posteriormente nesta seção.

* **Reinicie a numeração a partir de**: Especifique o número de página de onde a numeração para este layout de página será iniciada. Por exemplo, você pode criar um layout de página para a seção Apêndice no seu livro e definir a numeração para reiniciar de 1.

* **Layout**: Especifique as margens da página junto com o preenchimento para os lados superior, inferior, esquerdo e direito.

* **Histórico**: Inclua uma imagem como a imagem de fundo no layout da página. Você pode especificar a altura e a largura da imagem, juntamente com as propriedades de repetição e posição.

* **Nota**: Especifique as propriedades para exibir notas de rodapé em sua saída. Você pode optar por especificar as margens e as propriedades de preenchimento, juntamente com um estilo de borda.

Vamos ver um exemplo em que uma combinação de orientação de página retrato e paisagem e propriedades de rotação da exibição é usada. Neste exemplo, criaremos um PDF com a orientação de retrato padrão, mas uma tabela será renderizada na orientação de paisagem com conteúdo na exibição de 90 graus no sentido horário. A saída final será semelhante a:

<img src="./assets/portrait-landscape-page-layouts.png" width="400">

Na saída acima, as informações da Lista de contatos são apresentadas no modo paisagem com o conteúdo também girado em 90 graus. O conteúdo restante é exibido no modo de retrato normal.

Para alcançar esse tipo de saída, precisamos executar as seguintes tarefas principais:

1. Crie um layout de página com a orientação Paisagem.
1. Altere a propriedade Exibir rotação para renderizar o conteúdo em 90 graus no sentido horário.
1. Crie um estilo personalizado para usar o novo layout de página.
1. Adicione o estilo na definição de saída da tabela que queremos renderizar no layout da página paisagem.

Execute as seguintes etapas para realizar as tarefas acima:

1. Crie um layout de página com a orientação Paisagem.
   1. Crie um layout de página &quot;Paisagem&quot; usando as etapas fornecidas em &quot;Criar um novo layout de página&quot;.

   1. No painel direito, clique em **Propriedades da página**.

      <img src="./assets/page-properties-panel.png" width="300">
   1. Altere o **Orientação** para **Paisagem**.

1. Altere a propriedade Exibir rotação para renderizar o conteúdo em 90 graus no sentido horário.

   1. Selecionar **90° no sentido horário** na lista suspensa Exibir rotação .

   1. Clique em **Salvar tudo** para salvar as propriedades atualizadas do layout da página.

1. Crie um estilo personalizado para usar o novo layout de página.
   1. Expanda a barra lateral esquerda e clique duas vezes no modelo no qual deseja criar o estilo.

   1. Expanda a seção Folhas de estilos .

   1. Passe o mouse sobre a folha de estilos Layout e clique no botão (_Opções_ ícone ) **...** e escolha **Editar**.

      A folha de estilos Layout é aberta para edição.

   1. Clique com o botão direito em **Outros estilos** e escolha **Novo estilo**.

      <img src="./assets/stylesheet-other-new-style.png" width="300">

   1. No **Adicionar estilo** pop-up, enter `landscape-style` no **Classe** campo de nome.

      <img src="./assets/stylesheet-new-landscape-style.png" width="400">

   1. Clique em **Concluído**.

      Um novo estilo chamado `.landscape-style` é criado e adicionado ao final de **Outros estilos** lista.

   1. Clique duas vezes no `.landscape-style` estilo para abri-lo para edição.

   1. Expanda o **Paginação** propriedade.

   1. Enter `Landscape` no **Layout da página** propriedade.

      <img src="./assets/new-style-with-landscape-layout.png" width="500">

1. Adicione o estilo na definição de saída da tabela que queremos renderizar no layout da página paisagem.

   1. No Editor da Web, abra o arquivo no qual deseja aplicar o novo layout de página.

   1. Encontre a `<table>` elemento , que deve ser renderizado no modo Paisagem.

   1. Na navegação estrutural, clique no botão `table` elemento para selecionar a tabela.

      <img src="./assets/new-style-table-element.png" width="400">

   1. No painel direito, clique em e abra o **Propriedades de conteúdo** painel.

   1. No **Propriedades de conteúdo** , adicionar um novo `outputclass` propriedade com `landscape-style` como valor da propriedade.

      <img src="./assets/new-style-table-outputclass.png" width="300">

   1. Clique em **Salvar tudo** para salvar o arquivo atualizado.

   1. Gere a saída do PDF.

O PDF final terá o conteúdo da tabela renderizado no modo paisagem, como mostrado no início do exemplo.

## Trabalhar com o painel Propriedades de conteúdo

O painel Propriedades de conteúdo permite atualizar facilmente a aparência dos elementos no layout da página. As propriedades no painel Propriedades de conteúdo são divididas nas seguintes seções:

>[!NOTE]
Para obter mais detalhes sobre o uso dessas propriedades, consulte a documentação Padrões de mídia da página W3C CSS .

* **Atributos**: Contém propriedades de ID, classe e tradução. Se você definir a propriedade Translate como não, o conteúdo nesse elemento específico não será traduzido.

* **Fonte**: Contém propriedades relacionadas a fontes. Você pode definir Família de fontes, Peso, Tamanho, Decoração de texto (como sublinhado, linha sobreposta, passagem de linha), Estilo de texto (como Negrito, Itálico e muito mais), Alinhamento de texto (como esquerda, direita, centro ou justificado), manipular Espaços brancos (como formato predefinido, sem quebra automática de linha, e muito mais), Altura da linha, Espaçamento entre letras e Recuo de texto.

* **Borda**: Contém propriedades para adicionar e formatar uma borda para um elemento no layout da página. É possível definir Lado da Borda (como tudo, parte superior, inferior, direita ou esquerda), Estilo da Borda (como Sólido, Tracejado, Linhas Pontilhadas ou mais), Cor da Borda, Largura e Raio para ter borda curva. No exemplo a seguir, uma borda curva foi adicionada na área de cabeçalho da página.

   <img src="./assets/border-properties.png" width="500">

* **Layout**: Contém propriedades para configurar o layout de um elemento no layout da página. É possível definir Altura, Largura, Margens e Preenchimento (para cima, inferior, esquerda ou direita), Horizontal ou Vertical alignment, Float (à esquerda, direita ou nenhum), Clear (à esquerda, à direita ou nenhum), Clear (à direita ou nenhum), Elemento (como absoluto, fixo, relativo ou mais), Display (como bloco, conteúdo, correção ou mais), Z Index, Transparency, Transform (por rotação ou escala) e Transformar origem (por X e Y-offset).

* **Histórico**: Contém propriedades para incluir uma imagem de fundo ou sombra de cores. É possível definir o Tamanho da imagem (definindo Altura ou Largura), a Repetição do Plano de Fundo (como repetição, não repetição, arredondar ou mais) e a Posição do Plano de Fundo (como parte superior esquerda, centro direito, parte inferior central ou mais).

* **Várias colunas**: Contém propriedades para configurar propriedades de várias colunas para a página ou qualquer elemento específico, como o Índice do capítulo. Para obter mais detalhes sobre as propriedades e como usá-las, consulte _Trabalhar com layout de página de várias colunas_.
