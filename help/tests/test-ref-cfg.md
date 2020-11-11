---
description: Esta referência fornece mais informações sobre os testes que o Adobe Experience Platform Auditor realiza para configuração.
seo-description: Esta referência fornece mais informações sobre os testes que o Adobe Experience Platform Auditor realiza para configuração.
seo-title: Configuração
title: Configuração
uuid: d40d815c-edfe-48b9-921f-cea1b0b54a0a
translation-type: tm+mt
source-git-commit: 00d184c1fa1eece9eec8f27896bfbf72fa32bfb6
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 89%

---


# Configuração

Esta referência fornece mais informações sobre os testes que o Adobe Experience Platform Auditor realiza para configuração.

Os testes de configuração verificam configurações, valores ou possíveis conflitos na implementação. O Platform Auditor avalia as tags em relação a outras regras e práticas recomendadas.

<table id="table_A8A1FC360482447185C8460A18426638"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Teste </th> 
   <th colname="col2" class="entry"> Critérios </th> 
   <th colname="col3" class="entry"> Recomendação </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Os nomes de conversão usam somente caracteres alfanuméricos</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p>O parâmetro <span class="codeph"> ev_conversion_property_name</span> deve conter apenas valores numéricos e decimais, EXCETO para o parâmetro "<span class="codeph"> ev_transid</span>" (o valor <span class="codeph"> ev_transid</span> pode conter valores de texto ou numéricos) </p> <p>Procure por pixels <span class="codeph"> everesttech.net</span> que contenham um parâmetro de URL que comece com <span class="codeph"> ev_</span>. </p> <p>Exemplo: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue=$12&amp;ev_transid=1hf74i47 </span> </p> </td> 
   <td colname="col3"> <p> Certifique-se de que seus parâmetros de propriedade de transação contenham apenas valores numéricos e decimais. </p> <p> <p>Aviso:  Qualquer outro tipo de valor pode causar perda de dados. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - Os nomes de conversão usam caracteres com segurança de URL</b> </p> <p>Peso: 3 </p> </td> 
   <td colname="col2"> <p> Os nomes de propriedades de conversão não devem conter um E comercial (&amp;) ou um ponto de interrogação. </p> <p> Exemplo: </p> <p><span class="codeph">http://pixel.everesttech.net/1180/t?ev_revenue&amp;order=12&amp;ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>Verifique se os parâmetros de propriedade de transação não contêm um E comercial (&amp;) não codificado ou um ponto de interrogação. Elas quebram o formato do URL. </p> <p> <p>Aviso: Parâmetros de propriedade que contêm um E comercial (&amp;) não codificado ou um ponto de interrogação (por exemplo: <span class="codeph"> ev_formComplete?=1</span> ou <span class="codeph"> ev_formComplete&amp;Submit=1</span>), pode resultar em perda de dados. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Advertising Cloud - ID de transação implementada corretamente</b> </p> <p>Peso: 1 </p> </td> 
   <td colname="col2"> <p> O nome da propriedade <span class="codeph"> ev_transid=</span> não deve estar vazio. </p> <p>Exemplo: </p> <p> <span class="codeph">http://pixel.everesttech.net/1180/t?ev_page_load=1&amp;ev_revenue= 12&amp; ev_transid=</span> </p> </td> 
   <td colname="col3"> <p>O nome da propriedade <span class="codeph"> ev_transid=</span> não deve ser deixado sem um valor (<span class="codeph"> ev_transid=</span>). Se isso for deixado sem um valor, pode haver perda de dados de transação. Atribua um valor a <span class="codeph"> ev_transid=</span> ou remova o parâmetro do pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Instanciado no DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/analytics/implementation/home.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> O código do Adobe Analytics não está instalado ou não está sendo executado. Retorna 0 quando nenhum código de análise for encontrado na página da Web. </p> </td> 
   <td colname="col3"> <p>Verifique se a tag do Analytics está implementada na página e se não está bloqueada por atividades de script subsequentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Instanciado uma vez</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/analytics/implementation/home.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> O código do Adobe Analytics foi detectado mais de uma vez na página. . Retorna 0 quando nenhum código de análise for encontrado na página da Web. </p> </td> 
   <td colname="col3"> <p>Verifique se há apenas uma tag do Analytics na página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Analytics - Versão mais recente</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/analytics/implementation/appmeasurement-updates.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> Suas páginas não estão executando a versão mais recente da biblioteca de códigos do Analytics. As bibliotecas de código que alimentam as tecnologias da Experience Cloud estão sendo constantemente atualizadas e aprimoradas para aproveitar as melhorias de desempenho e fornecer os recursos mais recentes. Retorna 0 quando nenhum código de análise for encontrado na página da Web. </p> </td> 
   <td colname="col3"> <p>Instale a última versão da biblioteca Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>DTM - tags de terceiros são carregadas de forma assíncrona após DOM pronto</b> </p> <p>Peso: 3 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/resources/load-order.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p>Para obter um equilíbrio entre uma boa experiência do usuário e a coleta de dados precisos, as tags de terceiros devem ser acionadas no DOM pronto. Isso garantirá que esses scripts de rastreamento sejam executados sem afetar a funcionalidade do site. </p> </td> 
   <td colname="col3"> <p>Resolva esse problema ajustando todas as regras que executam pixels de terceiros para serem acionados no DOM Ready. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Serviço da Experience Cloud ID - Versão mais recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/tools/macid.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> Suas páginas não estão executando a versão mais recente da biblioteca de códigos do Serviço de ID de visitante, <span class="codeph"> visitorAPI.js</span>. As bibliotecas de código que alimentam as tecnologias da Experience Cloud estão sendo constantemente atualizadas e aprimoradas para aproveitar as melhorias de desempenho e fornecer os recursos mais recentes. </p> </td> 
   <td colname="col3"> <p>Instale a versão mais recente da biblioteca do serviço de ID de visitante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Launch - Versão mais recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p>Essas páginas não estão executando a versão mais recente da biblioteca de códigos do Platform Launch (Turbine). As bibliotecas de código que alimentam as tecnologias da Experience Cloud estão sendo constantemente atualizadas e aprimoradas para aproveitar as melhorias de desempenho e fornecer os recursos mais recentes. </p> </td> 
   <td colname="col3"> <p> Atualize a biblioteca do Platform Launch recriando e publicando a biblioteca do Platform Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - Versão mais recente</b> </p> <p>Peso: 2 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/dtm/implementing/target/update-target-tool.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> Suas páginas não estão executando a versão mais recente da biblioteca de códigos do Target. As bibliotecas de código que alimentam as tecnologias da Experience Cloud estão sendo constantemente atualizadas e aprimoradas para aproveitar as melhorias de desempenho e fornecer os recursos mais recentes. </p> </td> 
   <td colname="col3"> <p>Instale a última versão da biblioteca Target. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - mboxDefault precede mboxCreate </b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/target/using/implement-target/client-side/mbox-implement/mbox-download.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p>O uso correto de <span class="codeph"> mboxCreate</span> é semelhante a: </p> <p> <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;!-Conteúdo do cliente—&gt;&lt;/div&gt;&lt;script&gt;mboxCreate('myMboxName')&lt;/script&gt;</span> </p> </td> 
   <td colname="col3"> <p>Certifique-se de incluir uma tag <span class="codeph"> &lt;div class="mboxDefault"&gt;&lt;/div&gt;</span> antes de chamar <span class="codeph"> mboxCreate()</span>. O at.js não adicionará um para você. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <!--
      1.0.1 
    --> <p><b>Target - DOCTYPE válido</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/help/pt-BR/target/using/implement-target/client-side/faq-at-js/target-atjs-faq.html#what-html-doctype-does-atjs-require" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> Um DOCTYPE inválido foi detectado. Nenhuma mbox será acionada neste cenário. </p> <p>Para at.js, DOCTYPE deve estar no modo Padrões ou o Target não funcionará. </p> </td> 
   <td colname="col3"> <p>Atualize o DOCTYPE na página. </p> </td> 
  </tr> 
 </tbody> 
</table>

