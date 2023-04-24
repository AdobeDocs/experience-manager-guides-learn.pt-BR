---
title: Personalizado
description: Saiba como usar a predefinição de saída personalizada
source-git-commit: 8b6294425c6e60d1c5b37d98e99114014a104ee6
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 2%

---


# Personalizado {#id205BEF00PX0}

As predefinições de saída Personalizadas estão disponíveis para plug-ins DITA-OT personalizados. Você pode criar uma predefinição de saída DITA-OT personalizada para publicar a saída usando o plug-in DITA-OT personalizado.

Você pode criar a predefinição Personalizada de duas maneiras:

**No Editor da Web:** No painel Repositório, abra o arquivo de mapa DITA na Visualização de mapa e, na guia Saída, selecione o ícone + para criar uma predefinição de saída e, em seguida, selecione Personalizado no menu suspenso do tipo na caixa de diálogo Adicionar predefinição.

No editor da Web, as configurações foram organizadas em guias Geral e Avançado :

**Geral**

O **Geral** contém as seguintes configurações:

- Argumentos da linha de comando DITA-OT
- Nome da transformação
- Nome do arquivo
- Caminho de saída
- Aplicar condições usando \(se as condições forem definidas para um mapa\)
- Usar Linha de Base \(Se uma linha de base for criada para um mapa\)
- Fluxo de trabalho de pós-geração

**Avançado**

A guia Advanced contém as seguintes configurações:

- Limpar arquivos temporários DITA-OT
- Propriedades

Para obter detalhes, consulte [Configuração personalizada](#id231KJA00REJ).

**No painel de mapa**

Para abrir predefinições de saída para o PDF, clique em um arquivo de mapa DITA na interface do usuário do Assets, em seguida, clique em Predefinições de saída e na opção HTML5 . No painel Mapa, clique em **Editar** na parte superior para atualizar as várias configurações e, em seguida, clique em **Salvar**.

**Configuração personalizada**

As seguintes opções estão disponíveis para a predefinição de saída Personalizada:

| Opções de saída personalizada | Descrição |
| --- | --- |
| Tipo de saída | O tipo de saída que você deseja gerar. Para gerar saída usando o plug-in personalizado DITA-OT, escolha a opção Personalizado . |
| Nome da configuração | Dê um nome descritivo para as configurações de saída que você está criando. Por exemplo, você pode especificar _Saída de clientes internos_ ou _saída de usuários finais_. |
| Argumentos da linha de comando DITA-OT | Especifique os argumentos adicionais que você deseja que o DITA-OT processe ao gerar a saída. Para obter detalhes sobre os argumentos da linha de comando suportados no DITA-OT, consulte [Documentação do DITA-OT](https://www.dita-ot.org/). |
| Nome da transformação | Especifique o tipo de saída que deseja gerar. Isso é necessário se você quiser gerar saída usando seu próprio plug-in personalizado, que está integrado ao plug-in DITA-OT. Por exemplo, se você deseja gerar a saída XHTML, especifique `xhtml`. Para obter uma lista de transformações disponíveis no DITA-OT, consulte [Transformações DITA-OT (formatos de saída)](http://www.dita-ot.org/2.3/user-guide/AvailableTransforms.html) no Guia do usuário do OASIS DITA-OT. |
| Nome do arquivo | Especifique o nome do arquivo com o qual deseja salvar a saída.<br><br>**Observação**: Se você não fornecer um nome de arquivo, o título do mapa DITA será usado para gerar o nome final do arquivo de saída. Se o mapa não tiver um título, o nome de arquivo do mapa DITA será usado para nomear a saída final. O nome do arquivo é limpo usando as regras configuradas no sistema para lidar com qualquer caractere inválido. |
| Aplicar condições usando | Selecione uma das seguintes opções:<br><br>* **Nenhum aplicado**: Selecione essa opção se não quiser aplicar nenhuma condição na saída publicada.<br>* **Arquivo DITAVal**: Selecione DITAVall file(s) para gerar conteúdo personalizado. Você pode selecionar vários arquivos DITAVal usando a caixa de diálogo Procurar ou digitando o caminho do arquivo. Use o ícone de cruz próximo ao nome do arquivo para removê-lo. Os arquivos DITAVal são avaliados na ordem especificada, de modo que as condições especificadas no primeiro arquivo têm prioridade sobre as condições correspondentes especificadas nos arquivos posteriores. Você pode manter a ordem dos arquivos adicionando ou excluindo arquivos. Se o arquivo DITAVal for movido para outro local ou excluído, ele não será excluído automaticamente do painel de mapa. Você precisa atualizar o local caso os arquivos sejam movidos ou excluídos. Você pode passar o mouse sobre o nome do arquivo para ver o caminho no repositório AEM onde o arquivo está armazenado. Você só poderá selecionar arquivos DITAVal e um erro será exibido se tiver selecionado qualquer outro tipo de arquivo.<br>* **Predefinição de condição**: Selecione uma predefinição de condição no menu suspenso para aplicar uma condição enquanto publica a saída. A opção estará visível se você tiver adicionado uma condição presente na guia Predefinições de condição do console de mapa DITA. Para saber mais sobre a predefinição de condição, consulte [Usar predefinições de condição](generate-output-use-condition-presets.md#id1825FL004PN). |
| Caminho de destino | O caminho no repositório de AEM onde a saída do EPUB é armazenada. |
| Limpar arquivos temporários DITA-OT | Selecione essa opção para limpar os arquivos temporários gerados pelo DITA-OT. O local onde o DITA-OT armazena arquivos temporários pode ser encontrado no log de geração de saída.<br><br>Se você estiver apresentando erros ao gerar saída por meio do DITA-OT, é possível desmarcar essa opção para reter os arquivos temporários. Em seguida, você pode usar esses arquivos para solucionar erros de geração de saída. |
| Executar fluxo de trabalho de pós-geração | Ao escolher essa opção, uma nova lista suspensa Fluxo de trabalho de pós-geração é exibida contendo todos os fluxos de trabalho configurados no AEM. Você deve selecionar um workflow que deseja executar após a conclusão do workflow de geração de saída.<br><br>**Observação**: Para obter mais informações sobre como criar um fluxo de trabalho de geração de pós-saída personalizado, consulte _Personalizar fluxo de trabalho de geração de pós-saída_ em Instalar e configurar os Guias do Adobe Experience Manager as a Cloud Service. |
| Usar linha de base | Se tiver criado uma Linha de base para o mapa DITA selecionado, selecione essa opção para especificar a versão que deseja publicar.<br><br>Consulte [Trabalhar com linha de base](generate-output-use-baseline-for-publishing.md#id1825FI0J0PF) para obter mais detalhes. |
| Propriedades | Selecione as propriedades que deseja processar como metadados. Essas propriedades são definidas na página Propriedades do mapa DITA ou do arquivo de mapa de favoritos. As propriedades selecionadas na lista suspensa são listadas abaixo do campo Propriedades e são removidas da lista suspensa. Depois de definidas, essas propriedades também são copiadas para os tópicos no mapa.<br><br>**Observação**: Você também pode transmitir os metadados para a saída usando a publicação DITA-OT. Para obter mais detalhes, consulte [Transmita os metadados para a saída usando DITA-OT](pass-metadata-dita-ot.md#id21BJ00QD0XA). |

**Tópico principal:**[ Noções básicas das predefinições de saída](generate-output-understand-presets.md)

