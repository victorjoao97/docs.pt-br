---
ms.openlocfilehash: 2359dafb9042c13ae75e644d4ea655f53c14e95e
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "67804366"
---
### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>Associação do WCF com o modo de segurança TransportWithMessageCredential

|   |   |
|---|---|
|Detalhes|Começando com o .NET Framework 4.6.1, a associação do WCF que usar o modo de segurança TransportWithMessageCredential poderá ser configurada para receber mensagens com cabeçalhos &quot;to&quot; não assinados para chaves de segurança assimétricas. Por padrão, os cabeçalhos &quot;to&quot; não assinados continuarão a ser rejeitados no NET Framework 4.6.1. Eles só serão aceitos se o aplicativo aceitar esse novo modo de operação usando a opção de configuração Switch.System.ServiceModel.AllowUnsignedToHeader.|
|Sugestão|Como esse é um recurso de aceitação, ele não deve afetar o comportamento dos aplicativos existentes.<br/>Para controlar se o novo comportamento está sendo usado ou não, use a seguinte configuração:<pre><code class="lang-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Escopo|Transparente|
|Versão|4.6.1|
|Type|Redirecionando|
|APIs afetadas|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|
