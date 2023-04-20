---
title: Adicionar novo botão acionável personalizado na barra de ferramentas do editor
description: Saiba como adicionar um novo botão personalizado na barra de ferramentas do webeditor e chamar javascript para operá-lo personalizado.
source-git-commit: 26a6acde54953eab1d751f165d0f7769c7e790fe
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Adicionar novo botão acionável personalizado na barra de ferramentas do editor

Neste artigo, aprenderemos como adicionar um novo botão personalizado na barra de ferramentas do webeditor e chamar javascript para executar a operação personalizada desejada.

A adição de um botão acionável ao webeditor envolve as seguintes etapas:
- Adição do botão na *ui_config.json* na posição em que é necessário
- Registro do evento de botão ao clicar no editor da Web para o usuário executar uma ação ao clicar nela


## Implementar tomando um exemplo

Vamos entender isso com um exemplo em que um autor deseja adicionar uma referência jira a uma seção de perfil de tópico. A seção de prolog com a id de referência jira incorporada pode ser semelhante a abaixo:

![Seção Prolog com referência à ID JIRA](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-sample.png)

O elemento &quot;change-request-id&quot; que contém a ID JIRA deve ser recuperado da API (por exemplo, com base em uma consulta JIRA específica representada pelo aplicativo). Quando o usuário estiver criando a seção prolog, poderá clicar em um botão e inserir uma id de referência jira na barra de ferramentas do editor da Web, algo como:

![Seção Prolog - adicionar referência JIRA](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-insertjirareference.png)

E quando o usuário clica no botão, ele deve mostrar uma caixa de diálogo que deve extrair as opções possíveis e permitir que o usuário selecione a ID JIRA desejada, algo como:

![Caixa de diálogo Adicionar ID do JIRA da seção Prolog](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-insertjirareference-dialog.png)

que deve então adicionar o &quot;change-request-id&quot; ao prolog:

![Seção Prolog com referência à ID JIRA](../../../assets/authoring/webeditor-add-customtoolbarbutton-prolog-sample.png)



## Implementar


### Adicione o botão no webeditor configurando-o em *ui_config.json*

Use os perfis de pasta para verificar a variável *ui_config.json* na guia &quot;Configuração do editor XML&quot; e adicione o JSON de configuração de botão à seção desejada do grupo &quot;barra de ferramentas&quot;

```
{
    "on-click":"insertJIRARef",
    "icon":"linkCheck",
    "variant":"quiet",
    "type":"button",
    "title":"Insert JIRA Reference"
}
```

[use este link para saber mais sobre o perfil da pasta e configurar o ui_config.json](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/videos/advanced-user-guide/editor-configuration.html?lang=en)


### Gerenciar o evento de clique para o novo botão

    OBSERVAÇÃO: As etapas mencionadas abaixo estão disponíveis como pacote anexado nesta publicação


- Depois de salvar o perfil da pasta, crie um &quot;cq:ClientLibraryFolder&quot; em um diretório de projeto (pode estar em */apps*) e adicione as propriedades conforme mostrado na captura de tela abaixo:
   ![Configurações da biblioteca de clientes para o webeditor](../../../assets/authoring/webeditor-add-customtoolbarbutton-clientlibrarysettings.png)

```
This example uses "coralui3" library to show a dialog as it is used in the Javascript sample we presented.
You may use different library of your choice.
```

- Nesta pasta da biblioteca de clientes, crie dois arquivos, conforme mencionado abaixo:
   - *overrides.js*: que terá o código javascript para lidar com o evento on-click de &quot;insertJIRARef&quot; (use o pacote anexado para obter o conteúdo deste javascript)
   - *js.txt*: que incluirá &quot;overrides.js&quot; para ativar este javascript

- Salve as alterações e você deve estar pronto para testar.


### Testes

- Abrir editor da Web
- Nas preferências do usuário, escolha o perfil da pasta no qual você adicionou o *ui_config.json*. Se você a adicionou ao perfil Global, provavelmente já está usando isso.
- Abra um tópico e observe a barra de ferramentas com um novo botão &quot;Inserir referência de Jira&quot;
- Em seguida, você pode adicionar a seção prolog conforme fornecido abaixo ao tópico e tentar clicar no botão &quot;Inserir referência de Jira&quot; dentro do elemento prolog &quot;alterar-solicitação-referência&quot;

```
<prolog>
    <change-historylist>
        <change-item>
            <change-request-reference>
            </change-request-reference>
            <change-completed></change-completed>
            <change-summary></change-summary>
        </change-item>
    </change-historylist>
</prolog>
```

Consulte a captura de tela abaixo para saber como será:

![Testar novo botão](../../../assets/authoring/webeditor-add-customtoolbarbutton-testing.png)


### Anexos

- Exemplo de pacote clientlibs que instalará a biblioteca do cliente webeditor com código javascript para ação do botão da barra de ferramentas: [baixar usando este link](../../../assets/authoring/webeditor-addbuttonontoolbar-insertjira-clientlib.zip)
- Amostra *ui_config.json* que você pode fazer upload para um perfil de pasta: [baixar a amostra ui_config.json](../../../assets/authoring/sample_ui_config_Guides4.2-InsertJiraReference.json)

```
Please note this is compatible to AEM 6.5 and AEM Guides version 4.2.
If you are using a different version please add the toolbar button to the ui_config.json manually.
```
