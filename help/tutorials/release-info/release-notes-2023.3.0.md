---
title: Notas de versão | Adobe Experience Manager Guides as a Cloud Service, versão de março de 2023
description: Lançamento de março do Adobe Experience Manager Guides as a Cloud Service
exl-id: b3fe7cc8-1654-467a-ab18-6e6912855ecc
source-git-commit: 8073716bccacbe8d6a158b44d5106b083e3a5dcd
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Lançamento de março do Adobe Experience Manager Guides as a Cloud Service

## Atualização para a versão de março

Atualize seus Guias do Adobe Experience Manager atuais as a Cloud Service (mais tarde chamados de *Guias de AEM as a Cloud Service*), executando as seguintes etapas:
1. Confira o código Git do Cloud Services e alterne para a ramificação configurada no pipeline Cloud Services correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade no `/dox/dox.installer/pom.xml` arquivo do seu código Git Cloud Services para 2023.3.242.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de março do AEM Guides as a Cloud Service.

## Etapas para indexar o conteúdo existente (somente se você estiver em uma versão anterior à versão de setembro do AEM Guides as a Cloud Service)

Execute as seguintes etapas para indexar o conteúdo existente e usar o novo texto de localização e substituição no nível do mapa:

* Execute uma solicitação POST no servidor (com a autenticação correta) - `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: é possível passar caminhos específicos dos mapas para indexá-los; por padrão, todos os mapas serão indexados || Exemplo: `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com id de trabalho para o mesmo ponto de extremidade - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por exemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Quando o trabalho for concluído, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados nos logs do servidor.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade dos aplicativos de software compatíveis com os Guias do AEM as a Cloud Service na versão de março de 2023.

### FrameMaker e FrameMaker Publishing Server

| Versão do AEM Guides as a Cloud | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | Não compatível | 2022 ou superior |
|  |  |  |


### Conector de oxigênio

| Versão do AEM Guides as a Cloud | Janelas do conector Oxygen | Conector Oxygen Mac | Editar no Oxygen Windows | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Novos recursos e melhorias

O AEM Guides as a Cloud Service fornece melhorias e novos recursos na versão de março de 2023:

### Abrir e reproduzir arquivos de vídeo ou áudio no Editor da Web

O AEM Guides agora fornece o recurso para abrir e reproduzir os arquivos de áudio ou vídeo no Editor da Web. Você pode alterar o volume ou a visualização do vídeo. No menu de atalho, você também tem as opções para **Baixar**, alterar **Velocidade de reprodução**, ou exibir **Picture in Picture**.

<img src="assets/video-web-editor.png" alt="reproduzir vídeo" width="600">


## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* O processo de PDF de download não está funcionando adequadamente no Editor da Web. (11496)
* Saída JSON | Mapear metadados com o valor de propriedade como `"value in spaces and double quotes"` leva a um erro de publicação. (11438)
* A inserção para arquivos multimídia de áudio e vídeo falha no formato YouTube na **Inserir multimídia** ícone. (11320)
* O erro de validação ocorre quando um mapa é criado usando o modelo que tem um elemento de título especializado. (11212)
* PDF nativo | a nota de rodapé presente no cabeçalho da tabela leva a negrito e texto alinhado ao centro no rodapé da página correspondente na saída do PDF. (10610)
>[!NOTE]
>
>Para refletir a alteração do PDF nativo, exclua a pasta PDF localizada em /content/dam/dita-templates e atualize para a build mais recente. (10610)

### Problema conhecido com a solução alternativa

A Adobe identificou o seguinte problema conhecido para os Guias AEM as a Cloud Service na versão de março de 2023.

* Os usuários não podem salvar ou criar a versão de um ativo duplicado.

**Solução alternativa**: antes de fazer qualquer alteração no ativo duplicado, reprocesse-o na interface do usuário do Assets.
