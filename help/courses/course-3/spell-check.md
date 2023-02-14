---
title: Verificar ortografia e localizar/substituir
description: Uso da verificação ortográfica e localizar/substituir em Guias AEM
exl-id: 5f39618d-a919-4d3c-a4de-2896f2d1bf20
source-git-commit: 1c4d278a05f2612bc55ce277efb5da2e6a0fa9a9
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 1%

---

# Verificar ortografia e localizar/substituir

O Editor de guias de AEM tem recursos avançados de verificação ortográfica e localização e substituição.

>[!VIDEO](https://video.tv.adobe.com/v/342768?quality=12&learn=on)

Corrigir um erro ortográfico

1. Localize um erro em um tópico aberto, mostrado com um sublinhado vermelho.

2. Mantenha pressionada a tecla Ctrl + clique no botão secundário do mouse dentro da palavra.

3. Escolha a ortografia correta nas sugestões.

Se a ortografia correta não for sugerida, você sempre poderá editar a palavra manualmente.

## Mudar para AEM Verificação Ortográfica

Você pode usar uma ferramenta de verificação ortográfica diferente do dicionário padrão do navegador.

1. Navegar para **Configurações do editor**.

2. Selecione o **Geral** guia de configurações.

   ![Configuração de verificação ortográfica](images/lesson-11/configure-dictionary.png)

3. Existem duas opções disponíveis:

   - **Verificação ortográfica do navegador** — a configuração padrão em que a verificação ortográfica usa o dicionário interno do navegador.

   - **Verificação Ortográfica AEM** — use essa opção para criar uma lista de palavras personalizada usando AEM dicionário personalizado.

4. Choose **Verificação Ortográfica AEM**.

5. Clique em [!UICONTROL **Salvar**].

Configurar um dicionário personalizado

O Administrador pode alterar as configurações para que o dicionário de AEM reconheça palavras personalizadas, como nomes de empresas.

1. Navegue até o **Ferramentas** painel.

2. Faça logon em **CRXDE Lite**.

   ![Ícone de CRXDE Lite da interface do usuário do AEM](images/lesson-11/crxde-lite.png)

3. Navegue até o **_/apps/fmdita/config node_**.

   ![Nó de configuração CRXDE Lite](images/lesson-11/config-node.png)

4. Crie um novo arquivo.

   a. Clique com o botão direito do mouse na pasta de configuração.

   b. Choose **Criar > Criar arquivo**.

   ![Nova criação de arquivo de dicionário](images/lesson-11/new-dictionary-file.png)

   c. Nomeie o arquivo _**user_dictionary.txt**_.

   ![Texto do dicionário do usuário](images/lesson-11/user-dictionary.png)

   d. Clique em [!UICONTROL **OK**].

5. Abra o arquivo .

6. Adicione uma lista de palavras que você deseja incluir em seu dicionário personalizado.

7. Clique em [!UICONTROL **Salvar tudo**].

8. Feche o arquivo .

Os autores podem precisar reiniciar a sessão do Editor da Web para obter a lista de palavras personalizada atualizada no Dicionário de AEM.

## Localizar e substituir em um único arquivo

1. Clique no ícone Localizar e substituir na barra de ferramentas superior.

   ![Ícone Localizar Substituir](images/lesson-11/find-replace-icon.png)

2. Na barra de ferramentas inferior, digite uma palavra ou frase.

3. Clique em [!UICONTROL **Localizar**].

4. Se necessário, digite uma palavra para substituir a palavra encontrada.

5. Clique em [!UICONTROL **Substituir**].

## Localizar e substituir no repositório

1. Navegue até o **Repositório**.

2. Clique no botão [!UICONTROL **Localizar e substituir**] na parte inferior esquerda da tela.

3. Clique no botão [!UICONTROL **Mostrar configurações**] ícone .

4. Escolha um

   - **Arquivo de check-out antes de substituir** — se ativado por um Administrador, o check-out do arquivo será feito automaticamente antes da substituição dos termos de pesquisa.

   - **Somente palavra inteira** — restringe a pesquisa a retornar somente a palavra exata ou frase inserida.

   ![Localizar Substituir no Repositório](images/lesson-11/repository-find-replace.png)

5. Clique no botão [!UICONTROL **Aplicar filtro**] ícone para selecionar o caminho no Repositório onde deseja executar a pesquisa.

6. Insira os termos para Localizar e Substituir.

7. Se necessário, selecione **Criar nova versão após substituir**.

8. Clique em [!UICONTROL **Localizar**].

9. Abra o arquivo desejado e use as setas para navegar de um resultado encontrado para outro.

   ![Localizar e substituir interface de navegação](images/lesson-11/find-replace-navigation.png)
