---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de abril de 2022
description: Versão de abril dos Guias do Adobe Experience Manager as a Cloud Service
exl-id: c735ba24-a803-454b-8723-57dacf90061b
source-git-commit: b5e64512956f0a7f33c2021bc431d69239f2a088
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 3%

---

# Versão de abril dos Guias do Adobe Experience Manager as a Cloud Service

## Atualize para a versão de abril

Atualize seu [!DNL Adobe Experience Manager Guides] as a Cloud Service (mais tarde conhecido como *[!DNL AEM Guides]as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação do Cloud Services configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2022.4.133.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de abril de [!DNL AEM Guides] as a Cloud Service.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software suportados por [!DNL AEM Guides] Versão as a Cloud Service de abril de 2022.

### Servidor de publicação do FrameMaker e do FrameMaker

| FMPS | FrameMaker |
| --- | --- |
| Não compatível | Atualização 4 e superior de 2020 |
|  |  |


### Conector de oxigênio

| Versão da nuvem dos guias de AEM | Janelas do conector de oxigênio | Conector de oxigênio Mac |
| --- | --- | --- |
| 2022.4.0 | 2.5.6 | 2.5.6 |
|  |  |  |

*A linha de base e as condições criadas em AEM são suportadas em versões FMPS a partir de 2020.2.

## Novos recursos e melhorias

Muitos aprimoramentos e novos recursos foram adicionados ao Editor da Web:

### Resolução de chave aprimorada

Uma referência de chave de conteúdo DITA insere uma parte do conteúdo de um tópico em outro. Ele usa uma chave para localizar o conteúdo. As referências principais associadas a um tópico DITA precisam ser resolvidas. O mapa-raiz selecionado tem a maior precedência para resolver referências-chave.

![caixa de diálogo preferências do usuário](assets/user-preferences.png)

Agora, as referências principais são resolvidas com base no mapa raiz definido na seguinte ordem de prioridade:

1. Preferências do usuário
2. Painel Visualização de mapa
3. Perfil da pasta

Para obter mais detalhes, consulte *Resolver referências de chave* no Guia do usuário.

### Adicionar um painel personalizado no painel esquerdo

Agora é possível adicionar um painel personalizado no painel esquerdo do Editor da Web. Você pode usar um painel personalizado para vários propósitos, como fornecer ajuda ou fazer o teste de um projeto. Se um painel personalizado tiver sido configurado, ele também aparecerá na lista de painéis dentro do **Configurações do editor**. Você pode alternar o switch para mostrar ou ocultar o painel personalizado.

### Capacidade de alterar o estado dos tópicos do documento em um mapa DITA

Agora é possível alterar facilmente o estado do documento de tópicos selecionados em um mapa DITA. Também é possível abrir e editar as propriedades dos tópicos selecionados em um mapa DITA no **Mais opções** na parte inferior do painel Visualização de mapa.

![propriedades de tópico selecionadas](assets/map-view-properties.png)

### Informações da versão exibidas no modo de Visualização

O Editor da Web ajuda você a gerenciar suas versões. Agora você também pode ver a versão do tópico ativo ou mapa DITA no canto superior direito da guia do arquivo do tópico no modo de Visualização de um tópico.

![versão de visualização](assets/preview-version.png)

## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* Os novos rótulos não são refletidos automaticamente na lista suspensa Adicionar/remover rótulo. Em vez disso, é necessária uma atualização da linha de base. (9249)
* Não é possível editar o título da linha de base se uma linha de base for criada por critérios de etiqueta. (9171)
* O trabalho de publicação usando uma linha de base fica preso no estado de &quot;espera&quot; se o status da linha de base for alterado para &quot;falha&quot;. (9194)
* Remover rótulos em referências diretas também remove os rótulos de referências indiretas. (9257)
* Pesquisar à medida que você digita causa solicitações de pesquisa indesejadas na exibição Repositório. (9307)
* Problemas ocorrem quando qualquer palavra-chave é usada no título da guia . (9318)
* A linha de base falha ao adicionar um rótulo com espaços. (9362)
* AEM saída do site não exibe o elemento glossage corretamente. (8936)
* O erro do console ocorre ao abrir o **Saída** no Editor da Web. (8715)
* A mensagem de erro exibida ao publicar um tipo de registro manual pelo Salesforce não é intuitiva. (8952)
* A configuração Validar com atributos de condição não é aberta imediatamente, em vez disso, o usuário precisa reabrir o arquivo para ver as validações. (9300)
* Os metadados não podem ser removidos uma vez que um mapa DITA é publicado com metadados.  (9178)
* O painel Tradução fica visível mesmo ao abrir o mapa DITA no Editor de mapa. (9053)
* O DTD personalizado definido pelo usuário não tem precedência sobre o DTD DITA padrão incorporado no DITA-OT. (9104)
* No recurso PDF nativo, o upload nos modelos falha para arquivos não-DITA e não-imagem. (9070)
* O mecanismo de autorização executa dois queries em vez de um, em alguns cenários especializados. (9221)
* A publicação da saída do site AEM falha ao usar o DTD personalizado. (9243)
* A nota de rodapé de uso por referência não é rolada para a seção de nota de rodapé AEM saída do site. (9234)

## Problemas conhecidos

O Adobe identificou o seguinte problema conhecido na [!DNL AEM Guides] Versão as a Cloud Service de abril.

* O Editor da Web não informa um erro quando duas ou mais linhas de base são criadas com o mesmo nome, mas têm diferenças de espaço ou maiúsculas e minúsculas. Por exemplo, &quot;adobe&quot; e &quot;Adobe&quot; ou &quot;Adobe&quot;.
* O conector de oxigênio trava intermitentemente durante a execução frequente de logon ou logout ou alternância entre diferentes tipos de autenticação.
