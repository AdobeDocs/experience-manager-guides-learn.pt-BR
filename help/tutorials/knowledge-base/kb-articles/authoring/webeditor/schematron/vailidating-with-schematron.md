---
title: Suporte a schema no webeditor
description: Trabalhar com Schematron no webeditor
source-git-commit: 2a036ec628424f0dedfdb69a5e860906ca100cc6
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 0%

---


# Controle da qualidade do conteúdo no editor da Web

Este artigo fornece uma visão geral das possibilidades de validação no editor da Web dos Guias AEM.
Por design, o editor da Web aproveita a configuração de esquema DITA no sistema para impor aos usuários a criação de conteúdo compatível com DITA. Com isso, todo o conteúdo armazenado no sistema é estruturado, reutilizável e um conteúdo DITA válido.

Além do suporte para regras DITA, o editor da Web também oferece suporte à validação de conteúdo com base em &quot;*Schematron*&quot;.

&quot;*Schematron*&quot; refere-se a uma linguagem de validação baseada em regras usada para definir testes para um arquivo XML. Você pode importar os arquivos do Schematron e também editá-los no Editor da Web. Usando um arquivo &quot;Schematron&quot;, você pode definir determinadas regras e validá-las para um tópico DITA ou um mapa. As regras de schema podem garantir a consistência da estrutura XML impondo restrições definidas como regras. Estas restrições são impostas por PME que detêm a qualidade e a coerência do conteúdo.

    OBSERVAÇÃO: O editor da Web oferece suporte ao Esquema ISO.


## Saiba como o &quot;Schematron&quot; funciona no editor da Web

### Configuração de regras do Schematron

Consulte a seção &quot;Suporte para arquivos Schematron&quot; no [Guia do usuário](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=148)


### Impor regras de validação no salvamento do arquivo

As configurações do editor permitem que os usuários avançados configurem regras/arquivos de esquema que serão executados sempre que um usuário atualizar o conteúdo. Para obter mais detalhes, consulte a seção &quot;Validação&quot; em [Guia do usuário](https://helpx.adobe.com/content/dam/help/en/xml-documentation-solution/4-2/Adobe-Experience-Manager-Guides_UUID_User-Guide_EN.pdf#page=58)

![Definir regras das configurações do editor da Web](../../../assets/authoring/schematron-editorsettings-validation-tab.png)


### Você pode executar a validação manualmente?

Sim, como autor/usuário ao criar o conteúdo, você pode usar o painel Schematron no webeditor para carregar um arquivo de schematron e executar validações no arquivo aberto no editor.

    Para que isso funcione, o administrador do perfil da pasta deve permitir que todos os usuários adicionem arquivos Schemtron no painel Validação. Consulte as configurações do editor (captura de tela fornecida acima)

![Escolher arquivo de Schematron](../../../assets/authoring/schematron-rightpanel-validation-addsch.png)
![Executar validação](../../../assets/authoring/schematron-rightpanel-validation-runsch.png)


### Regras compatíveis

A versão atual dos Guias de AEM suporta a validação usando somente as regras baseadas em &quot;Asserção&quot;. (consulte [ativo vs relatório](https://schematron.com/document/205.html)) Qualquer regra baseada em &quot;Relatórios&quot; ainda não é suportada.


### Exemplos e mais ajuda sobre regras do Schematron

#### Casos de uso de exemplo

- Verifique se um link é externo e se ele tem escopo &quot;externo&quot;

   ```
   <sch:pattern>
       <sch:rule context="xref[contains(@href, 'http') or contains(@href, 'https')]">
           <sch:assert test="@scope = 'external' and @format = 'html'">
               All external xref links must be with scope='external' and format='html'
           </sch:assert>
       </sch:rule>
   </sch:pattern>
   ```

- Verifique se há pelo menos um &quot;topicref&quot; em um mapa ou pelo menos um &quot;li&quot; sob um &quot;ul&quot;

   ```
   <sch:pattern>
       <sch:rule context="map">
           <sch:assert test="count(topicref) > 0">
               There should be atleast one topicref in map
           </sch:assert>
       </sch:rule>
   
       <sch:rule context="ul">
           <sch:assert test="count(li) > 1" >
               A list must have more than one item.
           </sch:assert>
       </sch:rule>
   </sch:pattern>
   ```

- O elemento &quot;indextm&quot; deve estar sempre presente em um &quot;prolog&quot;

   ```
   <sch:pattern>
       <sch:rule context="*[contains(@class, ' topic/indexterm ')]">
           <sch:assert test="ancestor::node()/local-name() = 'prolog'">
               The indexterm element should be in a prolog.
           </sch:assert>
       </sch:rule>
   </sch:pattern>
   ```

#### Recursos

- Noções básicas  [Noções básicas sobre esquematria](https://da2022.xatapult.com/#what-is-schematron)
- Mais informações sobre [Regras de asserção no Schematron](https://www.xml.com/pub/a/2003/11/12/schematron.html#Assertions)
- [Arquivo Schematron de exemplo](../../../assets/authoring/sample_schematron.sch)