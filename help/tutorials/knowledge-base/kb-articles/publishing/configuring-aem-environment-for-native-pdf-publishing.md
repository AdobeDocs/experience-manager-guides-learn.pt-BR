---
title: Configuração do ambiente AEM para publicação no Native PDF
description: Configuração do ambiente AEM para publicação no Native PDF
source-git-commit: f26b8f94e1d7a3c9dd0aaab2eb196a77119e47ac
workflow-type: tm+mt
source-wordcount: '797'
ht-degree: 1%

---


# Configuração do ambiente AEM para publicação no Native PDF

AEM Guias inclui um mecanismo de publicação de PDF nativo que permite que os usuários projetem, desenvolvam e publiquem o conteúdo no formato PDF.

Ele oferece a capacidade de criar diferentes layouts de página, modelos de CSS e projetar os templates do PDF em conjunto com os layouts de página e o CSS.

As etapas para configurar esse PDF nativo nos Guias de AEM diferem dependendo do sistema operacional. Use as etapas de configuração abaixo com base no sistema operacional no qual o AEM está instalado.

## Pré-requisitos

Requisitos mínimos para a configuração do PDF nativo:

- Plataforma Java instalada, Standard Edition 8 ou 11 JDK (Java SE Development Kit) e JRE (Java SE Runtime Environment)
- AEM 6.5 SP13, SP12, SP11 ou SP10
- Guias 4.1 e versões acima (não UUID ou UUID)

O mecanismo de publicação PDF nativo precisa do JDK do Oracle para gerar os módulos de nó na pasta AEM crx-quickstart. Por padrão, ele suporta os seguintes sistemas operacionais:

- Windows 10, windows 2019 server e superior.
- Linux - (RHEL 8 e superior, CentOS 7 e superior, Ubuntu 18 e versões acima)
- SO Mac (baseado na Intel)

## Etapas de configuração para Windows Server (JAVA 11/8)

1. Verifique se AEM servidor está inativo.
2. Na barra de tarefas do Windows, clique com o botão direito do mouse no ícone do Windows e selecione Sistema.
3. Na janela Configurações, em Configurações relacionadas, clique em Configurações avançadas do sistema.
4. Na guia Advanced , clique em Environment Variables.
5. Na seção variáveis do sistema, clique em &quot;_Novo_&quot; para criar uma nova variável de ambiente.
6. Insira o nome da variável como JAVA_HOME.
7. No campo de valor , forneça o caminho Instalação do Java e clique em Ok.

   Por exemplo:

   JAVA 11:

   C:\Program Files\JAVA\jdk-11.0.15.1

   JAVA 8:

   C:\Program Files\JAVA\ jdk1.8.0_144

8. Adicione selecione Caminho nas variáveis do sistema e clique em Editar.

9. Agora, dentro das variáveis Caminho , forneça o valor do caminho Servidor e clique em Ok.

   Por exemplo:

   JAVA 11:

   %JAVA_HOME%\bin\server\

   JAVA 8:

   %JAVA_HOME%\jre\bin\server\

10. Clique em &#39;OK&#39; novamente na caixa de diálogo Variáveis de ambiente .
11. Clique novamente em &#39;OK&#39; na caixa de diálogo Propriedades do sistema.
12. Agora, inicie o servidor AEM.
13. Gere PDF nativo a partir de predefinições no editor da Web.

## Etapas de configuração para servidor Linux (RHEL7/centOS 7)

1. Certifique-se de que AEM servidor está inativo
2. Verifique a variável JAVA_HOME fazendo eco em $JAVA_HOME
3. Se a variável JAVA_HOME não estiver definida, siga a etapa 4. Caso contrário, vá diretamente para a etapa 5.
4. Defina a variável JAVA_HOME usando os comandos abaixo com base na versão java instalada

   Por exemplo:

   JAVA 11:

   1. exportar JAVA\_HOME=/usr/lib/jvm/java-11.0.15.1
   2. exportar PATH=$PATH: $JAVA\_HOME/bin
   3. exportar LD\_LIBRARY\_PATH=/usr/lib/jvm/jdk-11.0.15.1/lib/server:/usr/java/jdk-11.0.15.1/lib/server

   JAVA 8:

   1. exportar JAVA\_HOME=/usr/lib/jvm/java-11.0.15.1
   2. exportar PATH=$PATH: $JAVA\_HOME/bin


5. Reiniciar o servidor AEM
6. Copie o &quot;_node_modules.zip_&quot; anexado na parte inferior deste artigo ao diretório crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166/ .
7. Abra o terminal em crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166/ location.
8. Excluir diretório node_modules usando o comando abaixo

   **rm -rf node_modules**

9. Descompacte node_modules.zip usando o comando abaixo

   **unzip node_modules.zip**

10. Se o comando unzip não estiver instalado/reconhecido, ele poderá ser instalado usando o seguinte comando

   **yum install unzip**

11. Instale o pacote fontconfig.
Comando: yum install fontconfig
12. Gere PDF nativo a partir de predefinições no editor da Web.

**OBSERVAÇÃO** : o pacote node_modules.zip pode ser baixado [here](https://acrobat.adobe.com/link/track?uri=urn:aaid:scds:US:295d8f03-41e1-429b-8465-2761ce3c2fb3).

A importação manual dos módulos de nó baixados para o sistema operacional Linux é uma solução alternativa para os usuários que estão nos Guias 4.1 ou versões anteriores.

## Etapas de configuração para a máquina Mac (JAVA 11/8)

1. Instale o Oracle JAVA 11 ou Oracle JAVA 8.
2. Defina a variável de ambiente JAVA_HOME para o diretório JAVA instalado.
3. Abra um shell Unix.
(Bash é usado aqui para configurar a configuração)

   Comando: nano ~/.bashrc

4. Defina a variável JAVA_HOME usando os comandos abaixo com base na versão java instalada

   Por exemplo:

   JAVA 11:

   exportar JAVA\_HOME= /Library/Java/JavaVirtualMachines/jdk-11.0.15.1.jdk/Contents/Home

5. Recarregar bashrc

   Comando: source ~/.bashrc.

6. Verifique se JAVA_HOME está definido usando o comando echo $JAVA_HOME

7. Execute os três comandos abaixo AEM caminho de instalação

   C:/{aem-installation-folder}/crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166

   i) encontre . -type d -exec chmod 0755 {} \; ii) encontrar . -type f -exec chmod 0755 {} \; iii) ./node-darwin/bin/node node-darwin/lib/node_modules/npm/bin/npm-cli.js —prefix . instalar —unsafe-perm —scripts-prepend-node-path

8. Verifique se o Java está instalado usando o comando abaixo

   i) Executar **./node-darwin/bin/node** comando da pasta /crx-quickstart/profiles/nodejs—b1aad0a7-9079-e56c-1ed8-6fcababe8166

   ![mac](../assets/publishing/mac.png)

   ii) a = require(&#39;java&#39;)

9. Instale o pacote fontconfig.
Comando: configurar fonte de instalação da apt

10. Gere PDF nativo a partir de predefinições no editor da Web.

## Resolução de problemas

Abaixo estão os erros comuns que podem ocorrer durante a Geração de PDF quando as variáveis de ambiente não são definidas corretamente.

### Ponteiro nulo Exceção no sistema operacional Windows/Mac

![exceção de ponteiro nulo](../assets/publishing/null-pointer-exception.png)

### Bibliotecas ausentes no sistema operacional Linux RHEL 7

![bibliotecas ausentes](../assets/publishing/missing-libraries.png)

Se encontrar problemas ao executar qualquer uma das etapas acima, poste sua pergunta na Comunidade de guias de AEM [fórum](https://experienceleaguecommunities.adobe.com/t5/experience-manager-guides/ct-p/aem-xml-documentation) para obter assistência.
