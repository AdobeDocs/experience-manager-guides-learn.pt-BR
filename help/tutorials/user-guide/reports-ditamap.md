---
title: Relatório de mapa DITA no painel de mapa
description: Saiba como criar um relatório de mapa DITA no painel de mapa
source-git-commit: 8a104cfe17778a71915e3700f49fc6892493ccd0
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---


# Relatório de mapa DITA no painel de mapa {#id205BB800EEN}

AEM Guias fornece aos administradores os recursos de relatório para verificar a integridade geral da documentação antes que ela seja colocada em funcionamento ou disponibilizada aos usuários finais. O relatório de mapa DITA do painel de mapa nos Guias AEM fornece informações valiosas como tópicos ausentes, tópicos com elementos ausentes, UUID de tópicos referenciados e arquivos de mídia e status de revisão de cada tópico. Um relatório detalhado de nível de tópico individual também fornece informações relacionadas ao conteúdo do DITA, como referências de conteúdo e imagens ausentes ou referências cruzadas.

>[!NOTE]
>
> Os Guias AEM atualizam este relatório em cada evento que resulta em uma alteração no arquivo de mapa ou quando qualquer referência no arquivo de tópico é atualizada.

Execute as seguintes etapas para visualizar o relatório do mapa DITA:

1. Na interface do usuário do Assets, navegue até o arquivo de mapa DITA no qual deseja exibir o relatório e clique nele.

1. Clique em **Relatórios**.

   ![](images/reports-page-uuid.png)

   A página Relatórios é dividida em duas partes:

   - **Resumo do tópico:**

      Lista o resumo geral do arquivo de mapa selecionado. Ao analisar o Resumo, é possível conhecer rapidamente o número total de tópicos no mapa, faltando tópicos, o número de tópicos que têm elementos ausentes, o estado dos tópicos — Em rascunho, Em revisão ou no estado Revisado.

   - **Detalhes:**

      Quando você clica em um tópico, um relatório detalhado do tópico selecionado é exibido.

      ![](images/detailed-report-uuid.png)

      Itens destacados em **A**, **B**, **C** e **D** são descritos abaixo:

      - **Tópico**: O título do tópico especificado no mapa DITA. Passar o ponteiro do mouse sobre o título do tópico exibe o caminho completo do tópico. Se houver problemas no tópico, como ausência de referências ou imagens, um ponto vermelho será exibido antes do título do tópico.

      - **Nome do arquivo**: Nome do arquivo.

      - **UUID**: O identificador universal exclusivo \(UUID\) do arquivo.

      - **Autor**: Usuário que trabalhou por último neste tópico.

      - **Estado do documento**: O estado atual do documento - Rascunho, Em revisão ou Revisado.

      - **Tópicos ausentes \(B\)**: Se houver tópicos com referências quebradas, esses tópicos serão listados na lista Tópicos ausentes.

      - **Elementos ausentes**: Lista o número de imagens ausentes ou referências cruzadas quebradas, se houver.

      - **Abrir no Editor \(D\)**: Clicar nesse ícone abre o tópico no Editor da Web.

   Itens destacados em **E** são descritos abaixo:

   - **Multimídia**: O caminho das imagens usadas no tópico é mostrado junto com sua UUID. Se você clicar no caminho da imagem, a imagem correspondente será aberta em uma janela pop-up. Os links de imagem quebrados são listados em cor vermelha.

   - **Referências de conteúdo**: O caminho do conteúdo referenciado no tópico é mostrado junto com sua UUID. Se você clicar no título do conteúdo referenciado, o tópico correspondente será aberto no modo de Visualização.

   - **Referência cruzada**: O caminho do conteúdo referenciado é exibido junto com a UUID. Se você clicar no título do conteúdo referenciado, o tópico correspondente será aberto no modo de Visualização. Referências cruzadas quebradas são listadas em cor vermelha.

   - **Revisão**: Mostra o status da tarefa de revisão do tópico. Você pode ver o status \(abrir ou fechar\), a data de vencimento e o destinatário do tópico em revisão. Se você clicar no link do tópico, ele abrirá o tópico no modo de revisão.

   - **Usado em**: Mostra uma lista de outros tópicos ou mapas em que o tópico é usado. A UUID de todos esses tópicos e mapas também está listada.



Além do relatório de cada tópico individual, os administradores também têm acesso a informações como o histórico de publicação de um mapa DITA. Para obter mais informações sobre o histórico de saídas geradas, consulte [Exibir o status da tarefa de geração de saída](generate-output-for-a-dita-map.md#viewing_output_history).

## Gerar o CSV do relatório de mapa DITA

Você pode baixar e exportar o CSV de um relatório de mapa DITA. O CSV contém o relatório detalhado do mapa DITA.

Execute as seguintes etapas para gerar o CSV de um relatório de mapa DITA:

1. Clique em **Gerar relatório** no canto superior esquerdo para gerar o relatório de mapa DITA.

   ![](images/generate-DITA-map-report.png)

1. Você receberá uma notificação quando o relatório estiver pronto para download. Clique em **Baixar** para baixar o CSV do relatório gerado.

   ![](images/download-report-dialog.png)


   Você também pode baixar o CSV do relatório gerado posteriormente a partir da Caixa de entrada da notificação de AEM.

   Clique no relatório gerado na Caixa de entrada para baixar o relatório.

   ![](images/report-inbox--notification.png)

Depois que o relatório for baixado na Caixa de entrada, você também poderá selecionar o relatório e usar o ícone Abrir na parte superior para abrir o relatório selecionado.

**Tópico principal:**[ Relatórios](reports-intro.md)

