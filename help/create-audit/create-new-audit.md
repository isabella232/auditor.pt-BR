---
description: Criar uma nova auditoria no Auditor
seo-description: Criar uma nova auditoria no Auditor
seo-title: Criar uma nova auditoria no Auditor
title: Criar uma nova auditoria no Auditor
uuid: bd6798bb-3fab-4091-9e07-d3d1e5fdd087
translation-type: tm+mt
source-git-commit: c697f3d759ad1f086f16a39e03062431583ffd7f

---


# Create a new audit{#create-a-new-audit}

>[!NOTE]
>
>Os usuários estão limitados a uma auditoria executada de cada vez. Ocorre um erro se você tentar iniciar uma auditoria com as mesmas configurações que a que está sendo executada. Você pode usar o link na mensagem de erro se desejar cancelar a auditoria em execução no momento para criar um novo link.

Se desejar, use o link na parte inferior da página para acessar uma conta de avaliação gratuita e com recursos completos com o ObservePoint.

1. Na lista Auditor, clique em **[!UICONTROL Nova auditoria]**.

   The [!DNL New Audit] screen opens.

   ![](assets/config.png)

1. (Obrigatório) Nomear a auditoria.

   O nome pode ter até 250 caracteres.
1. (Obrigatório) Especifique o URL inicial.

   O protocolo é necessário ao especificar o URL inicial. O URL inicial é a página na qual a auditoria começa a rastrear. Depois de iniciado, o Auditor pesquisa até 500 páginas, seguindo os links que começam no URL inicial. Consulte [Incluir e excluir filtros](../create-audit/filters.md#concept-23531490bb124981ba807ed1806e3257) para obter mais informações. O URL inicial pode ter até 250 caracteres.

   >[!NOTE]
   >
   >Em alguns casos, pode levar até 48 horas para concluir uma verificação de 500 páginas.

1. Especifique um ou mais endereços de email para notificações sobre esta auditoria.

   É possível especificar vários emails separando cada endereço por vírgula. O solicitante é notificado por padrão. Os endereços de email são validados em tempo real. Se você digitar um endereço inválido, seu nome será notificado na tela.

   Cada email tem no máximo 250 caracteres, incluindo o fim do domínio (por exemplo, .com).
1. Especifique Incluir filtros.

   Esse campo pode conter URLs exatos, URLs parciais ou expressões regulares. Use este campo para os critérios que deseja que cada URL corresponda. Quaisquer URLs rastreados que não correspondem aos critérios de Incluir filtro não são incluídos nos resultados da auditoria.

   Você pode inserir diretórios que deseja que a auditoria verifique. Ou você pode executar auditoria entre domínios ou de automatização, onde é necessário iniciar a auditoria em um domínio e terminar em outro. Para fazer isso, digite os domínios que deseja navegar; para padrões complexos de URL, use uma expressão regular.

   >[!NOTE]
   >
   >Se você incluir uma página em seus filtros, mas ela não estiver conectada ao URL inicial, ou o Auditor verificar 500 páginas antes de chegar a essa página, a página não será digitalizada e não será incluída nos resultados do teste.

   Os filtros de inclusão são limitados a 1.000 caracteres por linha.

   Consulte [Incluir lista](../create-audit/filters.md#section-7626060a56a24b658f8c05f031ac3f5f) para obter mais informações.
1. Especifique Excluir filtros.

   A Lista de exclusões impede que os URLs sejam auditados. Use URLs exatos, URLs parciais ou expressões regulares, como faria na Lista de inclusão.

   Uma prática comum é excluir um link de logout se a auditoria tiver uma sessão de usuário (por exemplo: `/logout`, ou seja, qualquer URL que contenha a string `/logout`).

   Os filtros de exclusão são limitados a 1.000 caracteres por linha.

   Consulte [Excluir lista](../create-audit/filters.md#section-00aa5e10c878473b91ba0844bebe7ca9) para obter mais informações.
1. (Opcional) Se desejar, você pode testar os filtros incluir e excluir e testar seus URLs.

   Insira os filtros e URLs e clique em **[!UICONTROL Aplicar]** para executar o teste.

   ![](assets/test-advanced-filters.png)

1. Clique em **[!UICONTROL Executar relatório]**.
