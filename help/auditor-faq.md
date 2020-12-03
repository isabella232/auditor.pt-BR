---
description: Perguntas e respostas comuns sobre o Adobe Experience Platform Auditor
seo-description: Perguntas e respostas comuns sobre o Adobe Experience Platform Auditor
seo-title: Perguntas frequentes sobre o Adobe Experience Platform Auditor
title: Perguntas frequentes sobre o Adobe Experience Platform Auditor
uuid: 4db0781a-b288-4ec2-97ff-410a8241a61d
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '990'
ht-degree: 100%

---


# Perguntas frequentes sobre o Adobe Experience Platform Auditor {#auditor-faq}

Este artigo contém as respostas às perguntas frequentes sobre o Adobe Experience Platform Auditor.

* [O que é o Adobe Experience Platform Auditor?](auditor-faq.md#section-c4a9bc8d8eef41598c27e0951a2518e4)
* [Minha empresa está qualificada para usar o Platform Auditor?](auditor-faq.md#section-f90094050d1e44929066a942833435cf)
* [Quais tecnologias da Adobe o Platform Auditor avalia? ](auditor-faq.md#section-52833b71c05448aaae508e6070a387f5)
* [Quantas auditorias posso fazer?](auditor-faq.md#section-caac1e50ce1249aeba76308f3ef03fa0)
* [O que está rastreado para uma auditoria?](auditor-faq.md#section-6d068ed69ece4a1bb6d0c34454550c45)
* [Quanto tempo leva uma auditoria?](auditor-faq.md#section-5086ae27ef1f4671a9d951348654633a)
* [Que informações são fornecidas num relatório?](auditor-faq.md#section-752d6b82f6744a3182c4ce16ea6b5d3f)
* [Como essa informação é acionável?](auditor-faq.md#section-9308c1ea882048b781087ae6d2eee9f0)
* [O Platform Auditor pode auditar tecnologias não pertencentes à Adobe?](auditor-faq.md#section-f6e73c56083b4815bbf901296038bcd4)
* [Posso aprovar meus endereços IP para permitir a digitalização de páginas...](auditor-faq.md#section-011e4f54c58140ffb93bedeb0745b6cc)
* [O Platform Auditor utiliza os mesmos intervalos IP que o Observepoint?](auditor-faq.md#section-39512b156e194787981bdd572ff5b5a9)

## O que é o Adobe Experience Platform Auditor? {#section-c4a9bc8d8eef41598c27e0951a2518e4}

O Platform Auditor é um serviço da Adobe Experience Cloud, que foi desenvolvido em conjunto com o ObservePoint, especialistas na validação de implementações digitais.

Com o Platform Auditor, os clientes podem digitalizar até 500 páginas da Web de cada vez e receber um relatório que mostra como melhorar suas implementações da Adobe Experience Cloud para que eles recebam o valor total do investimento da Adobe.

## Posso usar o Platform Auditor? {#section-f90094050d1e44929066a942833435cf}

Todas as organizações de clientes da Adobe Experience Cloud recebem acesso gratuito ao Platform Auditor (desde 1º de maio de 2018). Cada usuário deve consentir nos termos de uso do Adobe/ObservePoint na interface do usuário da Adobe Experience Cloud antes de acessar a funcionalidade. Para excluir os termos, entre em contato com seu Gerente de conta.

## Como faço para acessar o Platform Auditor? {#section-531ff85f94384831a89cbb4109549daf}

Depois de fazer logon em [https://experiencecloud.adobe.com](https://experiencecloud.adobe.com), é possível encontrar o Platform Auditor clicando em **[!UICONTROL Ativação]** na navegação superior. Também pode ir diretamente para [https://auditor.adobe.com](https://auditor.adobe.com).

## Quais tecnologias da Adobe o Platform Auditor avalia? {#section-52833b71c05448aaae508e6070a387f5}

* Advertising Cloud DSP
* Pesquisa na Advertising Cloud
* Analytics
* DTM
* Serviço da Experience Cloud ID (antigo serviço da Marketing Cloud ID)
* Target

As soluções da Adobe a seguir não estão incluídas na estrutura de teste. O suporte para essas soluções está planejado para atualizações futuras.

* Advertising Cloud Creative
* Audience Manager
* Campaign
* Adobe Experience Platform Launch

## Quantas auditorias posso fazer? {#section-caac1e50ce1249aeba76308f3ef03fa0}

Não há limite para o número de auditorias que você pode executar. Os usuários estão limitados a uma auditoria executada de cada vez. Ocorre um erro se você tentar iniciar uma auditoria com as mesmas configurações que a que está sendo executada.

## O que está rastreado para uma auditoria? {#section-6d068ed69ece4a1bb6d0c34454550c45}

Atualmente, a tecnologia do ObservePoint rastreia URLs encontrados em links de documentos. Links encontrados em botões, widgets de paginação e outros elementos semelhantes da página não são rastreados.

## Como sugiro novos critérios para os testes do Platform Auditor? {#section-926e6ef9225b4f0bb19c2927d634cd77}

Envie sugestões de teste por meio da Comunidade do Platform Auditor clicando em **[!UICONTROL Compartilhar feedback]** nesta página: [https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor](https://forums.adobe.com/community/experience-cloud/platform/core-services/activation-service/auditor)

## Quanto tempo leva uma auditoria? {#section-5086ae27ef1f4671a9d951348654633a}

Há muitos fatores que contribuem para o tempo necessário para a conclusão de uma auditoria, incluindo:

* Tempo do carregamento da página

   O mecanismo de ObservePoint carrega cada página da auditoria em um navegador. Quanto mais rapidamente uma página for carregada, mais rapidamente a auditoria será concluída.
* Conexões simultâneas

   O Platform Auditor usa uma única conexão para visitar cada página. Contas completas do ObservePoint usam até 10 mecanismos de uma só vez.
* Silêncio da rede

   Depois que cada página é carregada, a auditoria aguarda um silêncio de rede de sete segundos antes de prosseguir para a próxima página. Se uma página enviar várias solicitações de rede que ocorrem depois que a página é carregada, o tempo limite de espera expirará após 60 segundos.
* Tentativas de página

   Se uma página ou tag não puder ser encontrada, a auditoria armazenará esse URL e retornará a ele mais tarde na auditoria. A auditoria visitará uma página até três vezes para verificar se o erro não foi causado por um problema transitório.
* Processamento

   Depois que uma auditoria é executada, todos os dados coletados são processados e filtrados pelas regras. Esse tempo de processamento é significativo, embora não leve tanto tempo quanto a própria verificação.

>[!NOTE]
>
>O Platform Auditor executa uma única verificação por vez. Contas completas do ObservePoint podem executar muitas auditorias consecutivamente.

## Que informações são fornecidas num relatório? {#section-752d6b82f6744a3182c4ce16ea6b5d3f}

Cada varredura gera um relatório que mostra quais URLs foram digitalizados, problemas encontrados nessas páginas e recomendações sobre como corrigir os problemas encontrados.

Os resultados das verificações são divididos em três categorias:

* Configuração
* Consistência de tags
* Presença de tag

Além dessas três categorias, o relatório fornece alertas contendo informações que você deve conhecer, mas que não exigem necessariamente uma ação imediata.

As recomendações incluídas nestas categorias são então divididas em três categorias adicionais:

* Altamente recomendado
* Recomendado
* Aprovado

## Como essa informação é acionável? {#section-9308c1ea882048b781087ae6d2eee9f0}

Todas as recomendações fornecidas por meio do Platform Auditor têm como objetivo ajudar você a tomar medidas para corrigir um problema com a implementação das soluções da Adobe Experience Cloud, como o DTM ou o Target. A fim de facilitar esta tarefa, a equipe do Platform Auditor trabalhou de forma exaustiva para fornecer instruções muito pormenorizadas sobre o que deve ser feito onde quer que seja. É possível exportar uma planilha de todos os URLs digitalizados e todos os resultados do teste para que você possa identificar as áreas problemáticas facilmente. Este é um exemplo de uma recomendação para uma implementação do DTM:

<table id="table_EE67775088344BDAA5126268072D6089"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>pageBottom calback last</b> </p> <p>Uma função _satellite.pageBottom() é necessária para uma implementação correta do DTM. Adicione o script em linha imediatamente antes da tag de fechamento &lt;/body&gt; para garantir a funcionalidade adequada do DTM. </p> </td> 
  </tr> 
 </tbody> 
</table>

## O Platform Auditor pode auditar tecnologias não pertencentes à Adobe? {#section-f6e73c56083b4815bbf901296038bcd4}

Não. No entanto, a oferta completa da ObservePoint permite que os clientes auditem e monitorem todas as suas tags e tecnologias de marketing. Como cliente da Adobe, você tem acesso a uma conta de avaliação complementar. Para acessar sua conta de avaliação, acesse a [página Platform Auditor do ObservePoint](https://www.observepoint.com/adobe-auditor/?utm_source=Adobe&amp;utm_medium=Auditor&amp;utm_campaign=Premium).

## Posso aprovar meus endereços IP para permitir a digitalização de páginas protegidas por um login? {#section-011e4f54c58140ffb93bedeb0745b6cc}

No momento, essa funcionalidade não é suportada sem a oferta completa do ObservePoint.

## O Platform Auditor utiliza os mesmos intervalos IP que o ObservePoint? {#section-39512b156e194787981bdd572ff5b5a9}

O rastreamento é executado pelo ObservePoint, portanto, os mesmos endereços IP são usados.

Consulte a [documentação do ObservePoint](https://help.observepoint.com/articles/2312494-observepoint-whitelisting-and-proxy-list) para obter mais detalhes.
