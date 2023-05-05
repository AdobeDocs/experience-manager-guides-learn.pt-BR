---
title: Criar mapas com base em modelos personalizados
description: Saiba como criar mapas com base em modelos personalizados
exl-id: 02513148-3876-4549-962a-9984f619030f
source-git-commit: 3bca42f0954afc2362ab24f369e698113324dbc3
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 0%

---

# Criar mapas com base em modelos personalizados {#id225VF0808MP}

Você pode criar modelos de mapa personalizados e usá-los para criar mapas DITA junto com os modelos de tópico e modelos de mapa referenciados no modelo de mapa

Você pode consultar outros modelos de mapa e modelos de tópico do modelo de mapa personalizado. Os modelos de mapa referenciados podem se referir a vários modelos de mapa, modelos de tópico, tópicos, mapas, imagens, vídeos e outros ativos. O modelo de mapa personalizado pode ajudar você a replicar facilmente os modelos de mapa e toda a estrutura de pasta referenciada. Esses modelos personalizados são especialmente úteis para criar e recriar vários mapas que têm estruturas e referências recursivas.

>[!NOTE]
>
> Os modelos de tópico não são criados recursivamente. Somente os modelos de tópico que estão diretamente no modelo de mapa são gerados e qualquer modelo de tópico dentro de um modelo de tópico é simplesmente referenciado diretamente no principal.

## Criar modelos personalizados

AEM Guias permite criar mapas e tópicos personalizados a partir da pasta de modelos dita. Você pode usar esses modelos personalizados para criar seu mapa e tópico. Você também pode compartilhar esses modelos com seus autores e eles podem usá-los para criar seus arquivos. Com esses modelos, é possível permitir que os autores mantenham cópias separadas de determinados recursos que estão dentro da pasta de modelos.

>[!NOTE]
>
> Todos os recursos que devem ser mencionados e mantidos somente na pasta templates devem ser mantidos fora dela.

**Modelo de tópico**

Execute as seguintes etapas para criar um modelo de tópico:

1. No **Interface do usuário do Assets**, navegue até a pasta de templates.

   ![](images/dita-templates.png){width="800" align="left"}

1. Clique em **tópicos** pasta para abri-la.Clique **Criar \> Modelo DITA**.
1. Na página Blueprint, selecione **Tópico** e, em seguida, clique em **Próximo.**
1. Na página Propriedades, especifique o modelo de tópico **Título**.
1. Especificar o arquivo **Nome**

   >[!NOTE]
   >
   > O nome do arquivo deve ter a extensão .dita .

1. \(Opcional\) Adicione uma descrição.
1. Clique em **Criar**. A mensagem de modelo de tópico criado é exibida. Em seguida, você pode abrir o modelo de tópico e editá-lo.

**Modelo de mapa**

Execute as seguintes etapas para criar um modelo de mapa:

1. No **Interface do usuário do Assets**, navegue até a pasta de templates.
1. Clique em **mapas** para abri-la.
1. Clique em **Crie \> Modelo DITA.**

   ![](images/create-dita-template.png){width="300" align="left"}

1. Na página Blueprint, selecione **Mapa** e clique em **Próximo**.
1. Na página Propriedades , especifique o modelo de mapa **Título**.
1. Especificar o arquivo **Nome**.

   >[!NOTE]
   >
   > O nome do arquivo deve ter a extensão .ditamap .

1. (Opcional\) Adicione uma descrição. Clique em **Criar**. A mensagem do modelo de mapa criado é exibida. Em seguida, você pode abrir o modelo de mapa e editá-lo. É possível adicionar as referências dos modelos de tópico, modelos de mapa e também outros ativos no modelo de mapa.

## Transmite o título definido nos modelos

Se você quiser transmitir o título do tópico ou mapa usado em seu modelo para os mapas DITA criados usando esse modelo, use colchetes ao redor do título.

Exemplo

```XML
<pubtitle>
   <mainpubtitle outputclass="booktitle">
   {title}
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>

The resultant DITA map with title "Rootmap1" will look like as follows:
<pubtitle>
   <mainpubtitle outputclass="booktitle">Rootmap1
   </mainpubtitle>
   <subtitle>Subtitle</subtitle>
</pubtitle>
```

>[!NOTE]
> Somente a primeira ocorrência de chaves será substituída por título.

Se você não usar colchetes ao redor do título, o mapa DITA resultante somente o primeiro elemento será escolhido e o aninhamento do título não será separado do modelo e terá a seguinte aparência:

```XML
<pubtitle> Rootmap1 </pubtitle>
```

>[!NOTE]
> Você também pode usar os colchetes ao redor do texto para passar sua estrutura aninhada dos modelos personalizados para seus mapas DITA.

Exemplo

```XML
<title>    
    <sub>        
        <b>{title}</b>    
    </sub>
</title>
```

## Usar o modelo de mapa para criar novos mapas

>[!NOTE]
>
> O modelo de mapa deve ser configurado e disponibilizado para criação pelo administrador. Para obter mais detalhes, consulte *Configurar modelos de criação* na seção Instalar e configurar os guias do Adobe Experience Manager as a Cloud Service.

Execute as seguintes etapas para criar um mapa usando o modelo de mapa personalizado:

1. No **Interface do usuário do Assets,** navegue até a pasta onde deseja criar o mapa.
1. Clique em **Criar \> Mapa DITA**.
1. Na página Blueprint, selecione o modelo de mapa que deseja usar e clique em **Próximo**. Por exemplo, se você criou um modelo de mapa &quot;modelo de teste&quot;, selecione-o.
1. Na página Propriedades , especifique o mapa **Título**.
1. Especificar o arquivo **Nome**.

   >[!NOTE]
   >
   > O nome do arquivo deve ter a extensão .ditamap .

1. Clique em **Criar**. A mensagem de mapa criado é exibida.


O mapa gera todos os ativos que são referenciados dentro da pasta de modelo. Alguns tipos de ativos que são referenciados em um mapa podem ser os seguintes:

- Se o mapa contiver a referência a um modelo de tópico, uma cópia dele será criada dentro da pasta, na mesma hierarquia que na pasta de tópicos na `dita-templates` pasta.
- Se o mapa contiver a referência a um modelo de mapa, uma cópia dele será criada dentro da pasta, na mesma hierarquia que na pasta de mapas na `dita-templates` pasta.
- Se o mapa contiver a referência genérica a um tópico ou mapa fora do `dita-templates/topics` ou `dita-templates/maps` , o mesmo é mencionado apenas e nenhuma cópia é criada.

   >[!NOTE]
   >
   > `dita-templates/topics` e `dita-templates/maps` são os caminhos padrão em Guias e são configuráveis.


   Se houver uma definição de chave do modelo de tópico dentro do modelo de mapa, uma nova chave \(portanto, novo tópico\) será criada e mencionada no mapa.

- Se outro mapa ou tópico for criado no mesmo nível na pasta, os nomes dos ativos recém-criados serão anexados com 0,1,2 e assim por diante. Você pode optar por abrir o mapa para editar ou salvar o arquivo de mapa no repositório.

**Tópico principal:**[ Trabalhar com o Editor de Mapa](map-editor.md)
