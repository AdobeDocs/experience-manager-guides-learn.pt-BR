---
title: JSON
description: Saiba como usar JSON
exl-id: 0a938cc2-1a6f-4ee4-ad7e-f94ad2a0cf94
source-git-commit: c74badebbcb4733fb9caa79c646b1d1e5c8bfe8e
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 1%

---

# JSON {#id231KK0180T4}

Você pode criar a predefinição JSON no Editor da Web:

No painel Repositório, abra o arquivo de mapa DITA na Visualização de mapa e, na guia Saída, selecione o ícone + para criar uma predefinição de saída e selecione JSON no menu suspenso do tipo na caixa de diálogo Adicionar predefinição.

No editor da Web, as seguintes configurações foram organizadas no **Geral** guia :

- Caminho de saída
- Arquivo de índice
- Aplicar condições usando \(se as condições forem definidas para um mapa\)
- Usar Linha de Base \(Se uma linha de base for criada para um mapa\)
- Propriedades a serem propagadas na saída
- Fluxo de trabalho de pós-geração

Para obter detalhes, consulte [Configuração JSON](#id231KJA00REJ).

**No painel de mapa**

Para abrir predefinições de saída para o PDF, clique em um arquivo de mapa DITA na interface do usuário do Assets, em seguida, clique em Predefinições de saída e na opção HTML5 . No painel Mapa, clique em **Editar** na parte superior para atualizar as várias configurações e, em seguida, clique em **Salvar**.

**Configuração JSON**

As seguintes opções estão disponíveis para a predefinição JSON:

>[!NOTE]
>
> Também é possível editar o arquivo JSON no Editor da Web.

| Opções JSON | Descrição |
| --- | --- |
| Caminho de saída | O caminho no repositório de AEM onde a saída JSON é armazenada. |
| Arquivo de índice | Você pode dar um nome para o arquivo de índice que está criando para a saída JSON. Por padrão, ele escolhe o nome de arquivo do mapa DITA e adiciona um sufixo (como `map_filename_index.json`).<br><br>Você também pode usar variáveis ao definir o Arquivo de índice. Para obter mais detalhes sobre o uso de variáveis, consulte [Use variáveis para definir as opções Caminho de destino, Nome do site ou Nome do arquivo](generate-output-use-variables.md#id18BUG70K05Z). |
| Aplicar condições usando | Selecione uma das seguintes opções:<br><br>* **Nenhum aplicado**: Selecione essa opção se não quiser aplicar nenhuma condição na saída publicada.<br>* **Arquivo DITAVAL**: Selecione DITAVAL file(s) para gerar conteúdo personalizado. Você pode selecionar vários arquivos DITAVAL usando a caixa de diálogo Procurar ou digitando o caminho do arquivo. Use o ícone de cruz próximo ao nome do arquivo para removê-lo. Os arquivos DITAVAL são avaliados na ordem especificada, de modo que as condições especificadas no primeiro arquivo têm prioridade sobre as condições correspondentes especificadas nos arquivos posteriores. Você pode manter a ordem dos arquivos adicionando ou excluindo arquivos. Se o arquivo DISAVAL for movido para outro local ou for excluído, ele não será automaticamente excluído do painel de mapa. Você precisa atualizar o local caso os arquivos sejam movidos ou excluídos. Você pode passar o mouse sobre o nome do arquivo para ver o caminho no repositório AEM onde o arquivo está armazenado. Você só poderá selecionar arquivos DISAVAL e um erro será exibido se tiver selecionado qualquer outro tipo de arquivo.<br>* **Predefinição de condição**: Selecione uma predefinição de condição no menu suspenso para aplicar uma condição enquanto publica a saída. A opção estará visível se você tiver adicionado uma condição presente na guia Predefinições de condição do console de mapa DITA. Para saber mais sobre a predefinição de condição, consulte [Usar predefinições de condição](generate-output-use-condition-presets.md#id1825FL004PN). |
| Usar linha de base | Se tiver criado uma Linha de base para o mapa DITA selecionado, selecione essa opção para especificar a versão que deseja publicar.<br><br>Consulte [Trabalhar com linha de base](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) para obter mais detalhes. |
| Propriedades a serem propagadas na saída | Selecione as propriedades que deseja processar como metadados. Essas propriedades são definidas na página Propriedades do mapa DITA ou do arquivo de mapa de favoritos. As propriedades selecionadas na lista suspensa são listadas abaixo do campo Propriedades .<br><br>**Observação**: Você também pode definir propriedades personalizadas e transmitir os metadados para a saída usando a publicação DITA-OT. Para obter mais detalhes, consulte [Trabalhar com metadados](metadata-dita.md#id21BJ00QD0XA). |
| Fluxo de trabalho de pós-geração | Ao escolher essa opção, uma nova lista suspensa Fluxo de trabalho de pós-geração é exibida contendo todos os fluxos de trabalho configurados no AEM. Você deve selecionar um workflow que deseja executar após a conclusão do workflow de geração de saída.<br><br>**Observação**: Para obter mais informações sobre como criar um fluxo de trabalho de geração de pós-saída personalizado, consulte _Personalizar fluxo de trabalho de geração de pós-saída_ no guia as a Cloud Service Instalar e configurar os guias do Adobe Experience Manager. |

**Tópico principal:**[ Noções básicas das predefinições de saída](generate-output-understand-presets.md)
