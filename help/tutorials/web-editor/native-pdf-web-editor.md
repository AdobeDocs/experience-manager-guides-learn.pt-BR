---
title: PDF nativo | Produção de PDF
description: Gerar saída do PDF nos Guias do Adobe Experience Manager as a Cloud Service
exl-id: ec3d59b7-1dda-4fd1-848e-21d8a36ff5e4
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '2171'
ht-degree: 0%

---

# Publicar uma saída do PDF

Com a solução Guias de AEM, você pode gerar PDF de tópicos individuais ou um arquivo de mapa inteiro. Você pode publicar seu conteúdo em um formato PDF usando um dos três métodos abaixo:

* **DITA-OT**

Use esse método para gerar uma saída PDF para um mapa no painel de mapa. Você pode definir propriedades de publicação antes de gerar o PDF criando uma predefinição de saída para o mapa que está aberto no painel de mapa. Para criar ou editar uma predefinição de saída, o *Noções básicas das predefinições de saída* na seção [Guia do AEM Guia do usuário as a Cloud Service](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf).

Para obter mais informações sobre como gerar um PDF usando o método DITA-OT, consulte [Gerar o PDF usando DITA-OT](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-pdf.html).

* **Servidor de publicação do FrameMaker (FMPS)**

Use esse método para gerar uma saída do PDF não apenas do conteúdo DITA, mas também dos documentos do FrameMaker (.book e .fm) disponíveis no repositório AEM. O PDF pode ser criado configurando-se uma predefinição de saída e publicado usando o FrameMaker Publishing Server (FMPS). Você pode projetar e configurar a aparência da saída para o PDF e outros formatos e armazenar o mesmo em um arquivo de configuração (.sts). Esse arquivo de configuração é então usado pelo FMPS para gerar saída para um mapa DITA ou arquivo .book. Para criar ou editar uma predefinição de saída, consulte o  *Noções básicas das predefinições de saída* na seção [Guia do AEM Guia do usuário as a Cloud Service](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/cs-apr-22/XML-Documentation-for-Adobe-Experience-Manager_CS_User-Guide_EN.pdf).

Para obter mais informações sobre como configurar o FMPS, consulte [Gerar saída de documentos do FrameMaker](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Ffm-output-generatation.html).

* **Publicação PDF nativa**

Use esse método para gerar uma saída PDF rica em recursos com base nos padrões de mídia paginada W3C CSS3 e CSS. Com a publicação do PDF nativo, você pode usar modelos para definir o layout e o estilo do seu conteúdo e aplicar várias configurações para ajustar o PDF. Além disso, você pode modificar e criar seus próprios modelos com o editor de modelos.

Para obter mais informações sobre a publicação do PDF nativo, consulte [Uso da publicação nativa do PDF](#native-pdf-publishing).


## Uso da publicação do PDF nativo {#native-pdf-publishing}

Ao criar conteúdo, é essencial garantir que o conteúdo seja otimizado para exibição, edição e impressão. Usando padrões como o W3C CSS3 para estilo de conteúdo e padrões de mídia paginada CSS para propriedades de definição de página, como tamanho, margens, orientação, quebras de página, cabeçalhos, rodapés e numeração de página, você pode definir a exibição e o layout para o documento do PDF, garantindo consistência e usabilidade. O recurso de publicação PDF nativo usa esses padrões para gerar um PDF.

Com a publicação no PDF nativo, você pode usar modelos predefinidos para garantir a consistência no layout e na estrutura do conteúdo, aplicar folhas de estilos para alterar a aparência e comportamento da saída, otimizar o PDF, definir marcas de impressora, permitir suporte ao leitor de tela, definir a conformidade do PDF, incorporar fontes e muito mais.

Gerar um PDF usando a publicação de PDF nativo tem dois aspectos:

* Use modelos para aplicar estilo ao conteúdo, definir layouts de página e várias configurações para ajustar o PDF. Os autores podem optar por usar/modificar os modelos de amostra fornecidos ou criar modelos personalizados e definir opções de configuração avançadas usadas por editores e desenvolvedores.

* Crie ou configure uma predefinição de saída do PDF para controlar as configurações do PDF. Depois de criar uma predefinição de saída do PDF, você pode gerar o PDF.

Para obter mais informações, consulte [Gerar uma saída PDF](#generate-pdf-output).

## Criar uma predefinição de saída do PDF {#create-output-preset}

A primeira etapa na geração de uma saída PDF é criar uma predefinição de saída PDF, que é uma coleção de propriedades de publicação atribuídas a um mapa. Você pode criar uma predefinição de saída para qualquer mapa que esteja aberto no painel Exibição de mapa ou configurar uma predefinição existente para gerar rapidamente um PDF para o mesmo mapa.

Na predefinição de saída do PDF, você pode selecionar um modelo, aplicar condições, definir restrições para controlar como um usuário interage com seu PDF, definir configurações avançadas como compactação, conformidade e muito mais.

Para criar ou configurar uma predefinição de saída do PDF:

1. Na guia Saída , clique em **Predefinições** na barra lateral esquerda.
O painel Predefinição é aberto.
   ![painel predefinido](assets/preset-panel.png)
2. Na saída **Predefinições** , execute um dos seguintes procedimentos:
   * Clique duas vezes em uma predefinição de saída PDF predefinida para exibi-la.
   * Clique no ícone + em **Predefinições** para adicionar uma nova predefinição de saída de **Tipo: PDF**
3. Para definir as configurações de uma predefinição de PDF existente:
   * Clique no botão  **Opções** ![opções](assets/options.svg) ícone ao lado da Predefinição de saída desejada e selecione **Editar**.
Você pode usar as seguintes configurações no **Geral**, **Layout**, **Segurança** e **Avançado** guias para configurar uma predefinição de saída do PDF:

**Geral**

Use para especificar configurações básicas de saída, como especificar caminho de saída, nome de arquivo de PDF e muito mais.

| Configuração | Descrição |
| --- | --- |
| **Caminho de saída** | O caminho no repositório de AEM onde a saída do PDF é armazenada. Verifique se o caminho de saída não está localizado dentro da pasta do projeto. Se deixado em branco, a saída é gerada no local de saída padrão do mapa DITA. |
| **Arquivo PDF** | Especifique um nome de arquivo para salvar o PDF. Por padrão, o nome do arquivo PDF adiciona o nome do mapa DITA junto com o nome predefinido. Por exemplo, o ditamap é &quot;TestMap&quot; e o nome da predefinição é &quot;preset1&quot;, então o nome padrão do pdf será &quot;TestMap_preset1.pdf&quot;. |
| **Aplicar condições usando** | Para conteúdo condicional, escolha entre as opções abaixo para gerar uma saída PDF com base nessas condições: <br>* **Nenhum Aplicado** Selecione essa opção se não quiser aplicar nenhuma condição no mapa e no conteúdo de origem. <br> * **Arquivo Ditaval** Selecione um arquivo DITAVAL para gerar conteúdo condicional. Para selecionar, clique em Predefinição de condição e localize o arquivo. <br> * **Predefinição de condição** Selecione uma predefinição de condição no menu suspenso para aplicar uma condição enquanto publica a saída. Essa opção estará visível se você tiver adicionado uma condição para o arquivo de mapa DITA. As configurações condicionais estão disponíveis na guia Predefinições de condição do console de mapa DITA. Para saber mais sobre a predefinição de condição, consulte [Usar predefinições de condição](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-condition-presets.html). <br> |
| **Usar linha de base** | Se tiver criado uma Linha de base para o mapa DITA selecionado, selecione essa opção para especificar a versão que deseja publicar. Consulte [Trabalhar com linha de base](https://help.adobe.com/en_US/xml-documentation-for-adobe-experience-manager/index.html#t=DXML-master-map%2Fgenerate-output-use-baseline-for-publishing.html) para obter mais detalhes. |

**Layout**

Use para definir layouts de página e especificar opções de exibição de página para saída do PDF, como Exibição de página e definir níveis de Zoom.

| Configuração | Descrição |
| --- | --- |
| **Modelo PDF** | Os templates de PDF fornecem uma estrutura clara para definir layouts de página, estilo de conteúdo e aplicar várias configurações à saída do PDF. Selecione nas opções suspensas do modelo de PDF para escolher o modelo preferencial. |
| **Exibição de página** | Use a Exibição de página para exibição de página que mostra como o PDF é exibido quando ele é aberto. Selecione nas opções suspensas Exibição de página para escolher uma exibição preferencial. <br>* **Padrão**  Exibido de acordo com a configuração padrão do visualizador de PDF no computador de um usuário.  <br> * **Exibição de página única** Exibe uma página de cada vez.   <br> * **Rolagem de página única** Exibe uma única página em uma coluna vertical contínua.  <br> * **Exibição de duas páginas** Exibe páginas espelhadas lado a lado de duas páginas de cada vez. .<br> * **Rolagem de duas páginas** Exibe páginas espelhadas lado a lado com rolagem contínua. |
| **Zoom** | Selecione para redimensionar a visualização de página que mostra como o PDF é exibido quando ele é aberto.  <br>* **Padrão** É exibido de acordo com a configuração padrão do visualizador de PDF no computador de um usuário    <br> * **100%** Faz com que a página apareça em seu tamanho real.     <br> * **Ajustar página** Torna a largura e a altura da página ajustadas ao painel do documento. .<br> * **Ajustar a largura da página** Faz com que a largura da página preencha a largura do painel do documento.  <br> * **Ajustar altura da página** Faz com que a altura da página preencha a altura do painel do documento. |

**Segurança**

Protect o PDF, adicionando restrições para abrir e ler o arquivo. Use as opções abaixo para evitar acesso não autorizado.

| Configuração | Descrição |
| --- | --- |
| **Definir senha para abrir o documento** | Selecione para adicionar uma senha segura para ver o ficheiro PDF. Especifique uma senha no **Senha do usuário** campo. Os usuários só podem abrir o PDF inserindo a senha fornecida neste campo. |
| **Definir as restrições do documento** | Selecione para restringir como os usuários podem interagir com seu PDF. Especifique uma senha no **Senha do proprietário** para que as configurações de restrição abaixo funcionem.  <br>* **Impressão** Selecione para permitir que um usuário imprima o PDF. <br> * **Impressão de qualidade de rascunho** Selecione para permitir que um usuário imprima o PDF em uma resolução mais baixa.  <br> * **Cópia de conteúdo** Selecione para permitir que um usuário copie conteúdo do PDF.   <br> * **Anotações** Selecione para permitir que um usuário adicione uma observação ou um comentário no PDF.  <br> * **Modificações de conteúdo** Selecione para permitir que um usuário altere o conteúdo no PDF.  <br> * **Cópia de conteúdo para acessibilidade** Selecione para permitir que os leitores de tela leiam e naveguem pelo conteúdo no PDF.  <br> * **Conjunto de documentos** Selecione para permitir que os usuários insiram páginas no PDF.  <br> **Observação**: Os usuários precisam digitar a senha do proprietário para alterar quaisquer restrições de Arquivo > Propriedades no Adobe Acrobat. |

**Avançado**

Use as opções a seguir para especificar configurações avançadas para unir PDF, usar compactação, selecionar o padrão de conformidade e muito mais.

| Configuração | Descrição |
| --- | --- |
| **Criar PDF acessível (marcado)** | Selecione essa opção para gerar um PDF com tags. Um PDF marcado facilita a leitura e navegação de conteúdo, hiperlinks, marcadores e assim por diante para os leitores de tela. Por exemplo, se uma tabela estiver marcada, o leitor de tela saberá que está lendo a tabela e não apenas linhas e texto. |
| **Mesclar PDF incluídos no sumário** | Selecione esta opção para unir PDF existentes à saída adicionando-os ao Índice. Os PDF serão inseridos no local representado no sumário e as páginas serão incrementadas de acordo. |
| **Incorporar fontes usadas** | Selecione esta opção ao usar fontes que podem não ser instaladas na máquina do usuário final. Com essa opção selecionada, as fontes usadas são incorporadas no PDF, garantindo que o usuário possa ver o PDF como pretendido, mesmo que as fontes não estejam instaladas em sua máquina. <br> **Observação**: Uma fonte só pode ser incorporada se contiver uma configuração pelo fornecedor da fonte que permita sua incorporação. Certifique-se de ter a configuração ou licença necessária antes de incorporar uma fonte. |
| **Usar separação automática de sílabas** | Com a separação automática de sílabas ativada, as palavras no final das linhas são quebradas em lugares gramaticalmente corretos com um hífen. |
| **Habilitar JavaScript** | Ative essa opção se você tiver um código JavaScript que deseja usar para transformar seu conteúdo dinamicamente antes de gerar um PDF. |
| **Incorporar arquivos multimídia** | Selecione essa opção para incluir qualquer áudio, vídeo e qualquer conteúdo interativo no PDF. |
| **Use a compactação completa para otimizar o tamanho do PDF** | Selecione esta opção se quiser compactar/reduzir o tamanho de um PDF grande. Lembre-se, compactar o PDF pode reduzir a qualidade do arquivo. |
| **Use a compactação de imagem para otimizar o tamanho do PDF** | Selecione esta opção se desejar compactar/reduzir o tamanho das imagens usadas no PDF. Lembre-se, compactar uma imagem pode reduzir a qualidade da imagem. |
| **Usar resolução personalizada (pixels por polegada)** | É a resolução de exibição da página em pixels por polegada. Insira um valor preferencial no campo exibido quando essa opção é selecionada. O valor padrão é 96 pixels por polegada. Defina um valor maior para ajustar mais conteúdo em uma polegada e vice-versa, se você definir um valor menor. |
| **Mostrar marca d&#39;água** | Selecione essa opção para renderizar as equações de MathML presentes no seu conteúdo. Caso contrário, as equações serão ignoradas. |
| **Ativar equações de MathML** | Selecione essa opção para renderizar as equações de MathML presentes no seu conteúdo. Caso contrário, as equações serão ignoradas por padrão. |
| **Conformidade com PDF** | É o padrão ao qual você pretende salvar o PDF para garantir sua conformidade. Selecione na lista suspensa para escolher na lista de padrões de PDF disponíveis. Para obter mais detalhes sobre os padrões compatíveis, consulte [Sobre os padrões PDF](https://helpx.adobe.com/acrobat/using/pdf-conversion-settings.html#about_pdf_x_pdf_e_and_pdf_a_standards). |

## Gerar uma saída PDF {#generate-pdf-output}

Depois de configurar a predefinição de saída, você pode gerar a saída do painel Predefinições usando o **Gerar predefinição** recurso.

1. Em **Autor** selecione a guia **Repositório** Exibir.\
   Isso abre o painel Repositório.

2. No painel Repositório, abra o arquivo de mapa DITA em **Exibição do mapa**.

3. No **Saída** clique em **Predefinições** para exibir o painel Predefinição .
Para criar ou configurar uma predefinição de saída, consulte [Criar uma predefinição de saída do PDF](#create-output-preset).
4. Para salvar suas configurações, clique no botão **Salvar tudo** ![salvar tudo](assets/SaveFloppy_icon.svg) ícone no canto superior esquerdo da barra de ferramentas padrão na exibição Saída.
5. Clique no botão **Gerar predefinição** ![gerar predefinição](assets/generate-output.svg) na barra superior.
Você pode exibir uma barra de progresso ao lado da predefinição de saída selecionada no painel Predefinições de saída.
6. Quando a geração de saída estiver concluída, clique em  **Exibir saída** ![exibir saída](assets/view-output.svg) na barra superior para visualizar a saída.\
   A **Sucesso** é visível no canto inferior direito da tela.
Se uma saída não for bem-sucedida, a mensagem de erro abaixo será exibida.
   ![log de erros](assets/error-log.png)

Para exibir o log de erros, clique em **Dismiss**, passe o mouse sobre a guia predefinida selecionada e clique em ![opções](assets/options.svg) **Opções** > **Exibir registro**.
