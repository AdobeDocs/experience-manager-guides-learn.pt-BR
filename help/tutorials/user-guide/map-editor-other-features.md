---
title: Outros recursos nos editores de mapa
description: Saiba como acessar Outros recursos nos editores de mapa
source-git-commit: 7cd719921e68ac1763d09d9665d912e3697e5849
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# Outros recursos nos editores de mapa {#id1942D0T0HUI}

Alguns recursos comuns nos Editores de mapa básico e avançado são:

## Resolver referências de chave {#id176GD01H05Z}

Uma referência de chave de conteúdo DITA ou `conkeyref` é um mecanismo para inserir uma parte do conteúdo de um tópico em outro. Esse mecanismo usa a chave para localizar o conteúdo a ser reutilizado, em vez do mecanismo de referência de conteúdo direto. Para obter mais informações sobre referência direta e indireta no DITA, consulte *Endereçamento DITA* em Especificação de Idioma DITA OASIS.

Se o tópico DITA tiver referências-chave associadas, elas precisarão ser resolvidas antes de visualizar, editar ou revisar um tópico.

As referências principais são resolvidas com base no mapa raiz definido na seguinte ordem de prioridade:

1. Preferências de usuário
1. Painel Visualização de mapa
1. Perfil da pasta

O mapa raiz selecionado nas Preferências do usuário tem a maior precedência para resolver as referências de chave seguidas pelo painel Visualização de mapa e pelo mapa raiz do Perfil da pasta . Portanto, se nenhum mapa estiver definido nas Preferências do usuário, o mapa aberto no painel Exibição do mapa será usado. Se nenhum mapa for aberto no painel Exibição de mapa, o mapa definido nos Perfis de pasta será usado para resolver as referências de chave.

As referências de chave podem ser armazenadas em um arquivo de mapa DITA ou em um arquivo DITA separado. Em Guias AEM, você pode especificar referências-chave no nível do projeto ou em um nível de sessão. Se um mapa raiz já estiver definido para a sessão do usuário, ele será usado para resolver as chaves. Caso contrário, o mapa raiz padrão para essa pasta será usado. Caso um mapa raiz padrão não esteja configurado, as referências de chave ausentes serão realçadas para o usuário.

Há várias maneiras de resolver referências principais em um tópico DITA, definindo o mapa DITA a ser usado nos seguintes locais:

**Propriedades do projeto** - Você pode definir um mapa-raiz para resolver referências-chave ao criar um Projeto na seção Propriedades do Projeto.

Esse mapa-raiz será aplicável para todos os ativos \(pastas e subpastas\) associados a esse projeto. Para conteúdo referenciado em vários projetos, uma lista alfabética de projetos é mantida e o mapa raiz padrão associado ao primeiro projeto é usado. Você também pode escolher o mapa DITA a ser usado na lista para resolver referências de chave.

**Visualização do tópico** - No modo de visualização do tópico, clique no ícone Resolução da chave na barra de ferramentas e selecione o arquivo DITA a ser usado para referências da chave.

**Exibição de edição de tópico** - Clique no ícone Resolução da chave ao editar um tópico DITA e selecione o arquivo DITA a ser usado para resolver as referências da chave.

**Tópico principal:**[ Trabalhar com o Editor de Mapa](map-editor.md)

