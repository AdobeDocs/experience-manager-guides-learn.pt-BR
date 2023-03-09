---
title: Guias FMPS e AEM
description: Publicação com o FMPS usando guias do AEM
source-git-commit: 82f010a97d0ed0e3c6351e6411e5955c79e0b01f
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---


# Guias do FrameMaker Publishing Server (FMPS) e do AEM

**A integração do AEM Guides com o FrameMaker Publishing Server pode ser a sua solução se você estiver procurando uma publicação automatizada de alta qualidade.\
O artigo abaixo ajudará você a configurar e executar o FMPS com Guias AEM.**

## Compatibilidade do FMPS com o Guia AEM:

- Compatibilidade com Guias AEM 4.1: [Link](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html?lang=en/#compatibility-matrix)
- Compatibilidade com guias de AEM 4.0: [Link](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html/#Compatibility%20matrix)
- Versão futura: [Link](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/latest-release-info.html?lang=en)

## Instalação:

### Guias do AEM:

Instalação e configuração consulte: [Link](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf)

### FMPS:

Para a instalação do FMPS, você pode consultar [Link de vídeo](https://www.youtube.com/watch?v=2deelyM5VA8&amp;t) ou [Documentação](https://help.adobe.com/en_US/framemaker/server/index.html#t=fmps-user-guide%2Finstall_config_fmps.html%23install_config_fmps&amp;rhtocid=_2)

## Configurações necessárias:

Seu conteúdo DITA pode ser emitido usando o FrameMaker Publishing Server (FMPS). Você pode criar saída em qualquer um dos muitos formatos compatíveis com o FMPS. No Console da Web, modifique as seguintes propriedades do pacote com.adobe.fmdita.config.ConfigManager para configurar Guias do AEM para usar o FMPS.

Para abrir o Console da Web, acesse o URL Access http://\&lt;server name=&quot;&quot;>:\&lt;port>/system/console/configMgr

**Propriedades de configuração e sua descrição:** [Link](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-1-2/Adobe-Experience-Manager-Guides_Installation-Configuration-Guide_EN.pdf#page=89)

## Executando teste:

Usando o FMPS, você pode publicar automaticamente **PDF, HTML responsivo5**, e **Epub** para seus ativos DITA e FM.

No menu &quot;Generate PDF using&quot;, escolha FrameMaker Publishing Server.

O usuário pode fornecer &quot;settings File(.sts)&quot; e &quot;ditaval. A filtragem será feita usando ditaval com base nas condições fornecidas.

- **arquivo de configuração**: Configuração FrameMaker /FMPS Publish que contém todas as configurações que você deseja que o FMPS aceite durante a publicação. Por exemplo: Gerando saída com o modelo personalizado, Gerando marcas e sangramentos (PDF), Gerando PDF com índice, índice etc.
- **Predefinição FMPS:** Combinação predefinida de arquivos ditaval e de configurações, em vez de fornecer arquivos ditaval e de configurações separados, o usuário pode pré-criar a predefinição FMPS que pode ser reutilizada para necessidades de publicação.

**Nota:** Se você não selecionar nenhuma das configurações ou predefinição FMPS, o FMPS publicará com a configuração padrão do sistema.

Se você selecionou a predefinição FMPS e também forneceu configurações/arquivo ditaval do AEM, isso entrará em conflito e a predefinição FMPS terá prioridade sobre configurações personalizadas/arquivo ditaval.

### Publicação de linha de base usando FMPS:

Você pode Publicar suas linhas de base já criadas com o FMPS2020.0.2 ou versão superior.

**Exemplo de arquivo de configurações FMPS (arquivo .sts) para começar:** [Link](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:ef750752-7a7e-4e51-923e-6b7d9861ed54) (descompacte este arquivo)

## Perguntas frequentes e solução de problemas:

- Falha na publicação do FMPS com &quot;Exceção de tempo limite&quot;.

Verifique e aumente o valor de &quot;Tempo limite do FMPS&quot; (Segundos) em /system/console/configMgr/com.adobe.fmdita.config.ConfigManager&quot;

- Não é possível obter a predefinição FMPS na lista suspensa.

Verifique se você tem uma predefinição de FMPS predefinida criada no Servidor e se as configurações de conexão estão corretas.

- Estou recebendo PDF em branco ao publicar.

Se estiver usando UUID, verifique se a opção &quot;Usar referência baseada em UUID&quot; está marcada em Preferências de edição do FrameMaker e vice-versa para guias AEM não UUID.

- Minhas configurações/edição não estão sendo aplicadas na saída final publicada.

Verifique se você não está selecionando o arquivo de configuração/edição e a predefinição FMPS simultaneamente. Verifique a saída manualmente usando o FrameMaker.

- A linha de base não está sendo publicada do FMPS.

A publicação de linha de base é compatível com o FMPS2020.0.2 ou versão superior.\
Verifique se a Linha de base foi criada corretamente. Para verificar, vá para Mapa de download de tópico do painel e selecione &quot;Usar linha de base&quot;.

- Tarefas de Publicação do FMPS levam mais tempo do que outros Mecanismos.

Haverá um cabeçalho fixo ideal de aprox. 3-4 min apenas durante a publicação a partir de FMPS do que outros motores, se você acha que é mais do que isso, verifique com o seu administrador de FMPS ou Entre em contato com o Suporte Adobe.

## Outros recursos:

[Aprendizagem e suporte do FMPS](https://helpx.adobe.com/support/framemaker-publishing-server.html)

[Aprendizagem e suporte do AEM](https://helpx.adobe.com/in/support/xml-documentation-for-experience-manager.html)

[FrameMaker e comunidade FMPS](https://community.adobe.com/t5/framemaker/ct-p/ct-framemaker?page=1&amp;sort=latest_replies&amp;lang=all&amp;tabid=all)

[Comunidade de guias do AEM](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation)
