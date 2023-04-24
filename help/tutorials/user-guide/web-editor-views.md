---
title: Exibições do editor da Web
description: Saiba como acessar visualizações do Editor da Web
source-git-commit: fa6e9f8b32d191f5b6f7136724d2145d81317767
workflow-type: tm+mt
source-wordcount: '1424'
ht-degree: 0%

---


# Exibições do editor da Web {#id204GK0D0V5Z}

O Editor da Web dos Guias AEM suporta a exibição de documentos em três modos ou exibições diferentes:

## Autor

Essa é uma visualização típica do que você vê é a exibição do \(WYSISYG\) do Editor da Web. Você pode editar o tópico como faria em qualquer editor de rich text regular. Na exibição Autor, você tem as opções para salvar uma revisão do documento, localizar e substituir conteúdo, inserir elemento, inserir hiperlink, inserir referência de conteúdo e muito mais.

>[!NOTE]
>
> Quando você usa a referência de conteúdo, o conteúdo referenciado também é exibido na exibição Autor em cor azul. O conteúdo referenciado não é editável.

## Origem

A exibição Origem exibe o XML subjacente que compõe o tópico. Se você estiver familiarizado com XML diretamente, use a Visualização de fonte. Além de fazer edições de texto regulares nesta exibição, você também pode adicionar elementos e atributos usando o Catálogo inteligente, ou localizar e substituir texto, elementos ou atributos.

- Para chamar o Catálogo inteligente, coloque o cursor no final de qualquer tag de elemento onde deseja inserir o novo elemento e insira &quot;&lt;&quot;. O editor mostra uma lista de todos os elementos XML válidos que você pode inserir nesse local. Use as teclas de seta para selecionar o elemento que deseja inserir e pressione Enter. Ao inserir o colchete de fechamento &quot;\>, a tag de fechamento do elemento é automaticamente adicionada.

   ![](images/smart-catalog-elements.png){width="400" align="left"}

- Você também pode alterar um elemento facilmente da exibição Origem. Por exemplo, se você alterar a tag de abertura de um `p` elemento para `note`, depois o fechamento `p` é automaticamente alterada para `/note`. Caso você substitua um elemento por um elemento incorreto, então você imediatamente recebe o Erro de validação.

- Se quiser adicionar um atributo a um elemento, coloque o cursor dentro da tag de elemento e pressione a barra de espaço. Uma lista de atributos válidos para esse elemento é mostrada no Catálogo inteligente. Use as teclas de seta para selecionar o elemento desejado e pressione Enter para inserir o elemento. Para especificar um valor para o atributo, insira o sinal de igual \(=\) e o editor insere automaticamente as aspas de abertura e fechamento &quot;&quot;, onde você pode especificar o valor do atributo.

   ![](images/smart-catalog-attribute.png){width="350" align="left"}

- Na exibição Origem, há uma opção de Recuo automático que reorganiza o código XML no formato apresentável e facilmente legível. Além disso, se você selecionar qualquer texto e alternar de Autor para Origem ou de Origem para Autor, o texto selecionado também será destacado na outra visualização.
- Outro recurso poderoso na exibição Origem é a validação XML no seu documento. Se você abrir um documento contendo XML inválido, ele será aberto na exibição Origem com as informações sobre XML inválido. Por exemplo, na captura de tela a seguir, as informações exatas sobre o XML incorreto são fornecidas no pop-up Erro de análise .

   ![](images/invalid-topic-xml.png){width="650" align="left"}

   Na captura de tela acima, um realce cruzado é usado para apontar a linha que contém XML incorreto.

- O recurso Localizar e substituir permite que você pesquise qualquer texto, elemento ou atributo na Visualização de origem.
Para obter mais detalhes, consulte a **Localizar e substituir** descrição do recurso na [Barra de ferramentas principal](web-editor-features.md#id#id2051EA0G05Z) seção.

- A Exibição da origem fornece vários atalhos para ajudá-lo a navegar e trabalhar rapidamente em um documento. A tabela a seguir lista as ações compatíveis e suas teclas de atalho:

   | Para fazer isso | Usar este atalho |
   |----------|-----------------|
   | Adicionar vários cursores | **Ctrl**+Clique esquerdo |
   | Várias seleções de texto não consecutivas | **Ctrl**+Clique esquerdo para arrastar e selecionar texto |
   | Selecionar texto entre e entre linhas | **Alt**+Clique esquerdo para arrastar e selecionar texto |
   | Desfazer várias seleções ou sair do modo de tela cheia | **Esc** |
   | Mostrar preenchimento automático | **Ctrl**+**Espaço** |
   | Ir para a tag de abertura ou fechamento da tag atual | **Ctrl**+**J** |
   | Expandir ou recolher a marca atual e o seu conteúdo | **Ctrl**+**Q** |
   | Selecione o elemento atual e seu conteúdo | **Ctrl**+**L** |
   | Recuar o elemento atual | **Shift**+**Tabulação** |
   | Excluir o elemento atual e seu conteúdo | **Shift**+**Ctrl**+**K** |
   | Cursor de uma palavra para a esquerda | **Alt**+**Seta para a esquerda** |
   | Mover cursor uma palavra para a direita | **Alt**+**Seta para a direita** |
   | Rolar uma linha para cima sem alterar o local do cursor | **Ctrl**+**Seta para cima** |
   | Rolar uma linha para baixo sem alterar o local do cursor | **Ctrl**+**Seta para baixo** |
   | Alternar tela cheia | **F11** |
   | Inserir uma nova linha após o elemento atual | **Ctrl**+**Enter** |
   | Inserir uma nova linha antes do elemento atual | **Shift**+**Ctrl**+**Enter** |
   | Localizar e selecionar a próxima ocorrência da palavra atual | **Ctrl**+**D** |
   | Mova o elemento atual e seu conteúdo um elemento para cima | **Shift**+**Ctrl**+**Seta para cima** |
   | Mova o elemento atual e seu conteúdo um elemento para baixo | **Shift**+**Ctrl**+**Seta para baixo** |
   | Vincule o elemento atual na tag de comentário | **Ctrl**+**/** |
   | Duplicar o elemento atual e seu conteúdo | **Shift**+**Ctrl**+**D** |
   | Exclua o texto após o cursor. Se o cursor estiver antes de um elemento de abertura, o elemento inteiro será excluído. | **Ctrl**+**K**+**K** |
   | Exclua o texto à esquerda do cursor na linha atual. Se o cursor estiver após a tag de fechamento de um elemento, o elemento inteiro será excluído. | **Ctrl**+**K**+**Backspace** |
   | Converter o texto atual em maiúsculas | **Ctrl**+**K**+**U** |
   | Converter o texto atual em minúsculas | **Ctrl**+**K**+**L** |
   | Role o elemento atual até o centro do editor | **Ctrl**+**K**+**C** |
   | Adicionar um cursor acima da posição atual | **Ctrl**+**Alt**+**Seta para cima** |
   | Adicionar um cursor abaixo da posição atual | **Ctrl**+**Alt**+**Seta para baixo** |
   | Localizar recursivamente a palavra atual \(na direção para a frente\) | **Ctrl**+**F3** |
   | Localizar recursivamente a palavra atual \(na direção para trás\) | **Shift**+**Ctrl**+**F3** |


## Visualizar

Abrir um tópico no modo de Visualização mostra como um tópico será exibido quando for visualizado por um usuário em seu navegador. No caso de um mapa DITA, é mostrada uma visualização do mapa em que um único documento composto de todos os tópicos no mapa é mostrado.

O modo de Visualização oferece as seguintes funcionalidades:

- [Exibir conteúdo com base em filtros condicionais](#id2114BI00VXA)
- [Exibir as marcações de rastreamento de alterações](#id2114BJ00CE8)
- [Exportar um tópico como PDF](#id2114BL00B5U)

### Exibir conteúdo com base em filtros condicionais {#id2114BI00VXA}

Se você tiver usado as condições em seu tópico ou mapa, essas condições serão mostradas no painel Filtros . Por padrão, todas as condições são selecionadas e o conteúdo inteiro é exibido. Se você desmarcar uma condição, o conteúdo com essa condição será removido da visualização. Você também pode optar por destacar o conteúdo condicional.

A imagem a seguir mostra um tópico que usa duas condições. `Audience` e `Product`. O conteúdo condicional é realçado com plano de fundo amarelo.

![](images/preview-filters.png){width="800" align="left"}

### Exibir as marcações de rastreamento de alterações {#id2114BJ00CE8}

Se um documento contiver marcações de rastreamento de alterações \(ou dicas visuais\), você também poderá visualizar o documento com ou sem essas marcações. Ao visualizar um documento, o painel direito contém as opções de Filtros e Rastreamento.

![](images/preview-tracking_cs.png){width="400" align="left"}

Há três **Rastreamento** opções que podem ser escolhidas:

- **Sem Marcação**: Nesta exibição, todas as inserções e exclusões são aceitas e uma visualização simples do documento é apresentada. Nesta exibição, você não vê marcações de rastreamento de alterações.
- **Original**: Nesta exibição, todas as inserções são rejeitadas e todas as exclusões são restauradas e, em seguida, uma visualização é mostrada. Basta obter o formulário original do documento antes de habilitar o modo de rastreamento de alterações.
- **Mostrar Marcação**: Nesta visualização, você obtém todas as marcações para conteúdo inserido e excluído.

   A imagem a seguir mostra a pré-visualização de um arquivo de mapa com marcações:

   ![](images/preview-map-with-track-changes.PNG){width="800" align="left"}


### Exportar um tópico como PDF {#id2114BL00B5U}

O PDF é um dos formatos de saída mais comuns usados em cada estágio possível do ciclo de desenvolvimento de documento. AEM Guias fornece a flexibilidade para gerar a PDF de um tópico individual ou de um arquivo de mapa inteiro. O recurso Exportar como PDF permite que o Autor, o Editor ou um Administrador gere facilmente a saída do PDF para um tópico individual. Ele usa as configurações DITA-OT salvas no perfil de nível de pasta para gerar o PDF.

Esse recurso suporta as seguintes funcionalidades:

- Gere o PDF da cópia de trabalho atualmente ativa de um tópico.
- Aceite o nome da transformação DITA-OT e os argumentos da linha de comando para gerar o PDF.
- Salve a saída gerada no sistema local.
- Resolva as referências de chave e conteúdo usadas no tópico antes de gerar a saída.

Para exportar um tópico como PDF, siga estas etapas:

1. Abra o tópico no modo de Visualização.

1. Clique no botão **Exportar como PDF** \(![](images/export-as-pdf-icon.svg)\).

   A caixa de diálogo Exportar como PDF é exibida.

   ![](images/export-as-pdf-dialog.png){width="350" align="left"}

1. *\(Opcional\)* Especifique o nome da transformação DITA-OT e quaisquer argumentos de linha de comando que deseja usar.

1. Clique em **Baixar**.

   >[!NOTE]
   >
   > Certifique-se de ter ativado a janela pop-up na configuração do navegador; caso contrário, o PDF não será baixado.

   O PDF é gerado e aberto em uma nova guia ou é exibida uma caixa de diálogo para salvar o PDF no sistema local.


**Tópico principal:**[ Trabalhar com o editor da Web](web-editor.md)

