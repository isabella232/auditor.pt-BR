---
description: Esta referência fornece mais informações sobre os testes que o Adobe Experience Platform Auditor realiza.
seo-description: Esta referência fornece mais informações sobre os testes que o Adobe Experience Platform Auditor realiza.
seo-title: Referência do teste
title: Referência do teste
uuid: f1d0769e-a2bd-4cec-acd1-146793644895
exl-id: b368bf43-2007-4f98-a965-ed8fc07c0fdf
translation-type: ht
source-git-commit: 286a857b2ff08345499edca2e0eb6b35ecf02332
workflow-type: ht
source-wordcount: '293'
ht-degree: 100%

---

# Referência do teste {#test-reference}

Esta referência fornece mais informações sobre os testes que o Adobe Experience Platform Auditor realiza.

**Versão atual da rubrica de teste:** 1.0.5

Cada teste é ponderado. Sua pontuação de teste é igual ao peso atribuído. Se você passar em um teste com um peso de cinco, você receberá cinco pontos.

* 0: Alerta sobre problemas que você deve estar ciente, mas que não afetam sua pontuação.
* 1: Recomenda uma otimização. Nenhum impacto na precisão dos dados.
* 2: Se esse teste falhar, você não terá acesso aos recursos e correções mais recentes na Experience Cloud.
* 3: Testes de eficiência e se a implementação segue as práticas recomendadas.
* 4: Falha significa que você pode estar coletando dados não confiáveis.
* 5: Falha significa que você pode ver perda de dados.

Os testes são bem-sucedidos. Eles testam a conformidade ou não conformidade com as condições de teste, de modo que não há pontuações parciais para a conformidade parcial. Por exemplo, se o teste verificar a versão mais recente de uma solução da Adobe e você estiver somente atrasado em uma versão, você obterá a mesma pontuação se estiver com cinco versões de volta. As versões mais recentes incluem melhorias de desempenho e correções de erros, portanto, é recomendável que esteja na versão mais recente.

É **altamente recomendável** que você corrija quaisquer resultados de nível 4 ou 5.

É **recomendável** que você corrija quaisquer resultados de nível 1 a 3.

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
