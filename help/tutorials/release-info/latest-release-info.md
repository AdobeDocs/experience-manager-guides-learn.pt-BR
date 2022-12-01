---
title: Versões dos Guias AEM
description: Versões mais recentes dos Guias de AEM e versões AEM pré-requisitos
exl-id: 780697a9-bdc6-40c2-b258-64639fe30f88
source-git-commit: f693ebb6a96ed9898050a754e10a74db235299fe
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---

# [!DNL AEM Guides] Versões

[!DNL Adobe Experience Manager Guides] é um aplicativo implantado em AEM. É uma poderosa solução de gerenciamento de conteúdo de componentes (CCMS) de nível empresarial que permite o suporte ao DITA nativo no Adobe Experience Manager, permitindo AEM para lidar com a criação e o delivery de conteúdo baseado em DITA.

AEM Os pacotes de guias estão disponíveis em duas variantes - build UUID e builds não UUID.

## Criações de UUID e não UUID

As principais diferenças entre as builds UUID e Non-UUID são as seguintes:

|  | Build UUID | Build não UUID |
|---|---|---|
| **Identificação do ativo** | Todos os ativos são identificados usando o caminho do ativo no repositório. | Todos os ativos são identificados usando sua UUID (ID exclusiva gerada pelo sistema quando o ativo foi carregado pela primeira vez). |
| **Criação de referência** | Todas as referências de conteúdo são criadas com base em seus caminhos. | Todas as referências de conteúdo são criadas com base em sua UUID. |

### Benefícios da build de UUID

* A instalação do UUID tem mais desempenho:
   * As referências são independentes de caminho: O sistema de gerenciamento de referência está ciente dos links à medida que as referências são criadas com base em UUIDs e não nos caminhos.
   * As operações de movimentação/atualização são eficientes: Os UUIDs permanecem os mesmos mesmo se os ativos forem movidos para outro caminho no repositório. Portanto, nenhum processamento é necessário para corrigir as referências entre os ativos em operações de movimentação/atualização.
* A criação de UUID é voltada para o futuro, já que estamos usando essa estrutura para a configuração em nuvem dos Guias de AEM também.


### Escolha entre as duas criações

* Se você for um novo cliente, recomendamos que você use a build de UUID.
* Se você for um cliente existente, poderá optar por migrar para a build de UUID, já que a migração da build de Non-UUID para UUID agora é possível. Para obter mais detalhes, consulte a *Migração de conteúdo não UUID para UUID* na seção **Instale e configure os Guias do Adobe Experience Manager.**

>[!NOTE]
>
>* Os clientes precisarão decidir entre o UUID e o modo não UUID no momento da primeira configuração (caso precise de ajuda, conecte-se com o Gerente de sucesso do cliente para ajudá-lo a tomar a decisão com base no seu caso de uso).
>* Ao atualizar de uma versão dos Guias de AEM para uma versão mais recente, os clientes precisarão garantir que escolham o mesmo modo (UUID / não UUID) para corresponder ao modo existente. Uma build que não seja UUID não deve ser atualizada diretamente para uma build UUID. A migração da build não UUID para a build UUID precisaria da migração de conteúdo.


**Atualização das criações**

Ao atualizar de uma versão mais antiga para uma versão mais recente de [!DNL AEM Guides], talvez seja necessário executar scripts de migração. Consulte as Notas de versão e a documentação específica da versão para obter instruções de atualização.

Nem todos os caminhos de atualização são suportados diretamente. Por exemplo, a atualização direta para a versão 4.0 é possível somente a partir da versão 3.8. Se você estiver em uma versão anterior à 3.8, consulte a documentação específica da versão para obter instruções de atualização [Arquivo de ajuda](https://helpx.adobe.com/xml-documentation-for-experience-manager/archive.html).
Entre em contato com o gerente de sucesso do cliente para validar o caminho de atualização.

**[!DNL AEM Guides]Builds**

A lista a seguir contém os mais recentes [!DNL AEM Guides] pacotes disponíveis para instalação no AMS ou no local, versões de AEM correspondentes (pré-requisitos), links de download de pacotes e outras informações úteis. É recomendável usar somente a build mais recente de [!DNL AEM Guides]. Se, por algum motivo, você precisar acessar criações mais antigas, conecte-se com o Gerente de sucesso do cliente de sua conta.

>[!NOTE]
>
>Entre em contato com o Gerente de sucesso do cliente para obter acesso a [!DNL AEM Guides] cria para AEM as a Cloud Service.

| [!DNL AEM Guides]Versão  | Notas de versão | Pré-requisitos AEM | Criar links de download |
|---|---|---|---|
| **Guias de AEM 4.1** | [Notas de versão 4.1.x](https://experienceleague.adobe.com/docs/experience-manager-guides-learn/tutorials/release-info/release-notes/on-prem-release-notes/release-notes-4.1.html) | **Não UUID e UUID 4.1.2**<br><br> AEM 6.5 SP13, SP12, SP11 ou SP10 <br>Java: 11 ou 8 <br><br>**Não UUID e UUID 4.1**<br><br> AEM 6.5 SP13, SP12, SP11 ou SP10 | **Não UUID**: <br> **AEM 6.5** <br>[4.1.](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-non-uuid%2Fcom.adobe.fmdita-6.5-4.1.159.zip)<br>[4.1.2.](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-2%2F4-1-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.1.2.11.zip)<br>[4.1.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-3%2F4-1-3-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.1.3.2.zip)<br><br> **UUID** <br>**AEM 6.5** <br>[4.1.](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1%2F4-1-uuid%2Fcom.adobe.fmdita-6.5-uuid-4.1.159.zip)<br>[4.1.2.](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-2%2F4-1-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.1.2.11.zip)<br>[4.1.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-1-3%2F4-1-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.1.3.2.zip) |
| **Guias de AEM 4.0** | [Notas de versão 4.0.x](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-4-0.html) | **Não UUID e UUID 4.0.3**<br> AEM 6.5 SP12, SP11, SP10 ou SP9 <br>Java: 11 ou 8 <br><br> <br>**Não UUID e UUID 4.0.2** <br> AEM 6.5 SP12, SP11, SP10 ou SP9 <br>Java: 11 ou 8 <br><br> **Não UUID e UUID 4.0** <br> AEM 6.5 SP11, SP10 ou SP9 | **Não UUID**: <br> **AEM 6.5** <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-hotfix-4.0.3.1.zip)<br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-non-uuid%2Fcom.adobe.fmdita-6.5-sp-4.0.2.10.zip)  <br> [4,0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-non-uuid/com.adobe.fmdita-6.5-4.0.70.zip)  <br><br> **UUID** <br>**AEM 6.5**  <br>[4.0.3](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-3%2F4-0-3-uuid%2Fcom.adobe.fmdita.uuid-6.5-hotfix-4.0.3.1.zip) <br>[4.0.2](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=%2Fcontent%2Fsoftware-distribution%2Fen%2Fdetails.html%2Fcontent%2Fdam%2Faem%2Fpublic%2Faemdox%2F4-0-2%2F4-0-2-uuid%2Fcom.adobe.fmdita.uuid-6.5-sp-4.0.2.10.zip)<br> [4,0](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/4-0/4-0-uuid/com.adobe.fmdita-6.5-uuid-4.0.70.zip) |
| **Guias de AEM 3.8.5** <br> O 3.8.5 é uma versão do SP além do 3.8. <br>A versão 3.8 não deve ser instalada independente, pois o SP 3.8.5 contém uma correção crítica. <br>Os clientes devem primeiro instalar o 3.8 e depois o SP 3.8.5. | [Notas de versão 3.8.x](https://helpx.adobe.com/xml-documentation-for-experience-manager/release-note/release-notes-xml-documentation-solution-3-8.html) | **Não UUID** <br> AEM 6.5 SP9 ou SP8 <br> AEM 6.4 SP8 <br> AEM 6.3 SP3 <br><br> **UUID** <br> AEM 6.5 SP9 ou SP8 | **Não UUID**: <br> **AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.5-hotfix-3.8.5.2.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.5-3.8.166.zip)<br> **AEM 6.4** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.4-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.4-3.8.166.zip) <br> **AEM 6.3** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5/com.adobe.fmdita-6.3-hotfix-3.8.5.1.zip) <br>[3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8/com.adobe.fmdita-6.3-3.8.166.zip) <br><br> **UUID** <br>**AEM 6.5** <br> [3.8.5 SP](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8-5uuid/com.adobe.fmdita.uuid-6.5-hotfix-3.8.5.2.zip) <br> [3,8](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/aemdox/3-8uuid/com.adobe.fmdita.uuid-6.5-3.8.168.zip) |
