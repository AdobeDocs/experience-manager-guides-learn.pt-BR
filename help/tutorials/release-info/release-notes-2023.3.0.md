---
title: Notas de versão | Guias do Adobe Experience Manager as a Cloud Service, versão de março de 2023
description: Versão de março do Adobe Experience Manager Guias as a Cloud Service
source-git-commit: d762cccc4a8f89eb91a1a8eb2c1410a7e0358b85
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Versão de março do Adobe Experience Manager Guias as a Cloud Service

## Atualize para a versão de março

Atualizar seus Guias atuais do Adobe Experience Manager as a Cloud Service (mais tarde, como *Guias de AEM as a Cloud Service*) configurando executando as seguintes etapas:
1. Verifique o código GKS do Cloud Services e alterne para a ramificação configurada no pipeline correspondente ao ambiente que você deseja atualizar.
2. Atualizar `<dox.version>` propriedade em `/dox/dox.installer/pom.xml` arquivo do código Git do Cloud Services para 2023.3.242.
3. Confirme as alterações e execute o pipeline do Cloud Services para atualizar para a versão de março AEM Guias as a Cloud Service.

## Etapas para indexar o conteúdo existente (somente se você estiver em uma versão anterior à versão de setembro AEM Guias as a Cloud Service)

Execute as seguintes etapas para indexar o conteúdo existente e usar o novo texto localizar e substituir no nível de mapa:

* Execute uma solicitação de POST para o servidor (com autenticação correta) - `http://<server:port>/bin/guides/map-find/indexing`.
(Opcional: Você pode passar caminhos específicos dos mapas para indexá-los, por padrão, todos os mapas serão indexados || Exemplo : `https://<Server:port>/bin/guides/map-find/indexing?paths=<map_path_in_repository>`)

* A API retornará um jobId. Para verificar o status do trabalho, você pode enviar uma solicitação de GET com ID do trabalho para o mesmo ponto final - `http://<server:port>/bin/guides/map-find/indexing?jobId={jobId}`
(Por exemplo: http://&lt;
_localhost:8080_>/bin/guides/map-find/indexing?jobId=2022/9/15/7/27/7dfa1271-981e-4617-b5a4-c18379f11c42_678)

* Quando a tarefa for concluída, a solicitação do GET acima responderá com sucesso e mencionará se algum mapa falhou. Os mapas indexados com êxito podem ser confirmados dos logs do servidor.

## Matriz de compatibilidade

Esta seção lista a matriz de compatibilidade para os aplicativos de software suportados pelos Guias de AEM as a Cloud Service, versão de março de 2023.

### Servidor de publicação do FrameMaker e do FrameMaker

| AEM Guias das a Cloud Release | FMPS | FrameMaker |
| --- | --- | --- |
| 2023.03.0 | Não compatível | 2022 ou superior |
|  |  |  |


### Conector de oxigênio

| AEM Guias das a Cloud Release | Janelas do conector de oxigênio | Conector de oxigênio Mac | Editar no Windows Oxygen | Editar no Oxygen Mac |
| --- | --- | --- | --- | --- |
| 2023.03.0 | 2.9-uuid-2 | 2.9-uuid-2 | 2.3 | 2.3 |
|  |  |  |  |


## Novos recursos e melhorias

AEM Guias as a Cloud Service fornecem melhorias e novos recursos na versão de março de 2023:

### Abrir e reproduzir arquivos de vídeo ou áudio no Editor da Web

AEM Guias agora fornece o recurso para abrir e reproduzir arquivos de áudio ou vídeo no Editor da Web. Você pode alterar o volume ou a visualização do vídeo. No menu de atalho, você também tem as opções para **Baixar**, alterar **Velocidade de reprodução** ou exibir **Picture in Picture**.

<img src="assets/video-web-editor.png" alt="reproduzir vídeo" width="600">


## Problemas corrigidos

Os bugs corrigidos em várias áreas estão listados abaixo:

* O processo de PDF de download não está funcionando adequadamente no Editor da Web. (11496)
* Saída JSON | Mapear metadados com valor de propriedade como `"value in spaces and double quotes"` resulta em um erro de publicação. (11438)
* A inserção de arquivos de multimídia de áudio e vídeo falha no formato YouTube na guia **Inserir multimídia** ícone . (11320)
* O erro de validação ocorre quando um mapa é criado usando o modelo que tem um elemento de título especializado. (11212)
* PDF nativo | a nota de rodapé presente no cabeçalho da tabela leva ao texto em negrito e alinhado no rodapé da página correspondente na saída do PDF. (10610)
>[!NOTE]
>
>Para refletir a alteração de PDF nativo, exclua a pasta PDF localizada em /content/dam/dita-templates e atualize para a build mais recente. (10610)

### Problema conhecido com solução alternativa

O Adobe identificou o seguinte problema conhecido para a versão dos Guias de AEM as a Cloud Service em março de 2023.

* Os usuários não podem salvar ou criar a versão de um ativo duplicado.

**Solução alternativa**: Antes de fazer alterações no ativo duplicado, reprocesse-o da interface do usuário do Assets.

