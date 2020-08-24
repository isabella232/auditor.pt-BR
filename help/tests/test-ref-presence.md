---
description: Esta referência fornece mais informações sobre os testes que o Auditor realiza para a presença de tags.
seo-description: Esta referência fornece mais informações sobre os testes que o Auditor realiza para a presença de tags.
seo-title: Presença de tag
title: Presença de tag
uuid: 91aa355b-7022-431c-9837-e108b5ce604d
translation-type: ht
source-git-commit: a76ecb232c29d83ef82b14be460d9ce60f5e8662
workflow-type: ht
source-wordcount: '943'
ht-degree: 100%

---


# Presença de tag

Esta referência fornece mais informações sobre os testes que o Auditor realiza para a presença de tags.

O Auditor avalia se a tag existe e se está no lugar certo no código da sua página.

<table id="table_98A2E3F7B3154EEFA76D0CAE2FE97CAB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Teste </th> 
   <th colname="col2" class="entry"> Critérios </th> 
   <th colname="col3" class="entry"> Recomendação </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Presença de código</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> A tag da Advertising Cloud não está disponível no DOM. </p> </td> 
   <td colname="col3"> <p>Implemente a tag da Advertising Cloud usando a Extensão Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Advertising Cloud - Pixel de segmento implementado</b> </p> <p>Peso: 5 </p> </td> 
   <td colname="col2"> <p> Atualize seus pixels de segmento da Advertising Cloud para as novas tags somente de imagem da Advertising Cloud. O uso de tags de segmento AMO obsoletas pode resultar em perda de dados. </p> </td> 
   <td colname="col3"> <p>Implemente o pixel do segmento da Advertising Cloud usando a Extensão Advertising Cloud Launch. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Analytics - Carregado no DOM</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/analytics/implementation/home.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> A tag do Adobe Analytics não foi detectada. </p> </td> 
   <td colname="col3"> <p>Instale a versão mais recente do Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Biblioteca carregada</b> </p> <p>Peso: 5 </p> <p>Informações adicionais: </p> <p> 
     <ul id="ul_7E706EBC2E4649A69732E6982E116E22"> 
      <li id="li_9AF0257E39C347A9AE6D8D8FFBD66B38"><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/admin/c-troubleshooting.html" format="html" scope="external"> Solução de problemas do DTM</a> </li> 
      <li id="li_7B422BCCD2654B0A9059799FB5276BE8"><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Adicionar o código do cabeçalho e do rodapé</a> </li> 
     </ul> </p> </td> 
   <td colname="col2"> <p> Um objeto _satellite global não foi encontrado no DOM. O Dynamic Tag Management não está instalado ou não está sendo executado. </p> </td> 
   <td colname="col3"> <p>Verifique se a biblioteca do DTM está implementada na página e se não está bloqueada por atividades de script subsequentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> DTM - Um código incorporado</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/client-side/code.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> Os sites de produção devem carregar apenas uma biblioteca do DTM. </p> </td> 
   <td colname="col3"> <p>Verifique se apenas a biblioteca de produção está sendo carregada na página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - o retorno de chamada pageBottom existe em &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> O retorno de chamada <span class="codeph"> _satellite.pageBottom()</span> não foi encontrado dentro do <span class="codeph"> &lt;body&gt;</span> da página, que é exigido pelo Dynamic Tag Management. </p> <p>Esse teste falhará se a <span class="codeph"> chamada </span>pageBottom não for encontrada na página, ou se estiver na tag <span class="codeph"> &lt;head&gt;</span> (ou em algum outro local inesperado). Ele só passará se <span class="codeph"> pageBottom</span> for encontrado em algum lugar dentro da tag <span class="codeph"> &lt;body&gt;</span>. Se não estiver na página, não funcionará e os outros dois testes <span class="codeph"> pageBottom</span> também falharão. </p> </td> 
   <td colname="col3"> <p>Adicione o script em linha imediatamente antes da tag de fechamento <span class="codeph"> &lt;/body&gt;</span> para garantir a funcionalidade adequada do DTM. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>DTM - tag pageBottom ativada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/client-side/t-add-header-fooder-code.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> A tag <code> pageBottom</code> do DTM não foi detectada. </p> <p>Isso pode ocorrer se a chamada estiver em uma <code> if</code> declaração que resulta em algo semelhante a <code> if (false) {_satellite.pageBottom()}</code>. Então, embora possa existir e estar corretamente colocada, a tag ainda pode não disparar. </p> </td> 
   <td colname="col3"> <p>Instale a chamada do DTM <code> pageBottom</code> em cada página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Serviço da Experience Cloud ID - Presença do código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/id-service/using/intro/overview.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p>O código do Serviço da Experience Cloud ID não foi encontrado. A Experience Cloud ID (MCID) é altamente recomendada para garantir que você obtenha o máximo de valor das soluções da Experience Cloud e seja essencial para o gerenciamento de ID nas soluções da Experience Cloud. </p> </td> 
   <td colname="col3"> <p> Instale a versão mais recente da MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Cookie do serviço da Experience Cloud ID</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/dtm/using/tools/macid.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> O cookie <span class="codeph"> AMCV_</span> não foi encontrado. É necessário instanciar um objeto de visitante do código <span class="codeph"> VisitorAPI.js</span>. </p> </td> 
   <td colname="col3"> <p> Se esta for uma implementação do DTM, verifique se a AdobeOrg ID foi inserida corretamente na ferramenta MCID. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b>Serviço da Experience Cloud ID - valor da MID presente</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/id-service/using/intro/cookies.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> O valor MID não foi encontrado no cookie <span class="codeph"> AMCV_</span>. </p> </td> 
   <td colname="col3"> <p>Teste novamente para verificar se há latência de API MCID. Se a condição persistir, entre em contato com o Atendimento ao cliente da Adobe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b> Launch - Biblioteca carregada</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> Um objeto _satellite global não foi encontrado no DOM. O Launch não está instalado ou não está sendo executado. </p> </td> 
   <td colname="col3"> <p>Verifique se a biblioteca do Launch está implementada na página e não está bloqueada pelas atividades subsequentes de script. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - Não tem vários scripts incorporados</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p>Não deve haver vários scripts incorporados carregados na página. Os sites de produção devem carregar apenas uma biblioteca do Launch. </p> </td> 
   <td colname="col3"> <p>Verifique se apenas a biblioteca de produção está sendo carregada na página. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - o retorno de chamada pageBottom existe em &lt;body&gt;</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> O retorno de chamada <span class="codeph"> _satellite.pageBottom()</span> não foi encontrado dentro do <span class="codeph"> &lt;body&gt;</span> da página, que é exigido pelo Launch. </p> <p>Esse teste falhará se a <span class="codeph"> chamada </span>pageBottom não for encontrada na página, ou se estiver na tag <span class="codeph"> &lt;head&gt;</span> (ou em algum outro local inesperado). Ele só passará se <span class="codeph"> pageBottom</span> for encontrado em algum lugar dentro da tag <span class="codeph"> &lt;body&gt;</span>. Se não estiver na página, não funcionará e os outros dois testes <span class="codeph"> pageBottom</span> também falharão. </p> </td> 
   <td colname="col3"> <p>Adicione o script em linha imediatamente antes da tag de fechamento <span class="codeph"> &lt;/body&gt;</span> para garantir a funcionalidade do Launch correta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.5 
    </draft-comment> <p><b>Launch - o retorno de chamada pageBottom não deve existir quando implantado de forma assíncrona</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/launch/using/intro/get-started/quick-start.html" format="https" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p>O retorno de chamada <span class="codeph"> _satellite.pageBottom()</span> foi encontrado na página, o que não deve ocorrer quando o Launch é implantado de forma assíncrona. </p> </td> 
   <td colname="col3"> <p>Remova o script<span class="codeph"> _satellite.pageBottom()</span> para ativar a funcionalidade do Launch correta. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <draft-comment>
      1.0.1 
    </draft-comment> <p><b> Target - Presença de código</b> </p> <p>Peso: 5 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p>O Target deve ser definido no DOM. </p> </td> 
   <td colname="col3"> <p>Instale a versão mais recente do Target (at.js). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b> Target - Biblioteca carregada em &lt;head&gt;</b> </p> <p>Peso: 4 </p> <p><a href="https://docs.adobe.com/content/help/pt-BR/target/using/implement-target/implementing-target.html" format="html" scope="external"> Informações adicionais</a> </p> </td> 
   <td colname="col2"> <p> A biblioteca do Target deve ser carregada na tag <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
   <td colname="col3"> <p> Verifique se a biblioteca do Target está carregada na tag <span class="codeph"> &lt;head&gt;</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>
