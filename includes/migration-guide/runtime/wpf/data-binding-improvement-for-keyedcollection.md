---
ms.openlocfilehash: 8aae403e3f23d3bfc755140b2ac29d757f10f753
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2020
ms.locfileid: "74451590"
---
### <a name="data-binding-improvement-for-keyedcollection"></a>Melhoria de Associação de Dados para KeyedCollection

|   |   |
|---|---|
|Detalhes|Corrigimos <xref:System.Windows.Data.Binding> o uso incorreto do indexador IList quando o objeto de origem&lt;declara um indexador personalizado com a mesma assinatura (por exemplo, KeyedCollection int,TItem&gt;).|
|Sugestão|Para que um aplicativo que tenha como alvo uma versão mais antiga se beneficie dessa alteração, ele deve ser executado no .NET Framework <code>&lt;runtime&gt;</code> 4.8 ou posterior, e <code>false</code>deve optar pela alteração adicionando o seguinte [interruptor AppContext](https://docs.microsoft.com/dotnet/framework/configure-apps/file-schema/runtime/appcontextswitchoverrides-element) à seção do arquivo de configuração do aplicativo e definindo-o como :<pre><code class="lang-xml">&lt;?xml version=&quot;1.0&quot; encoding=&quot;utf-8&quot;?&gt;&#13;&#10;&lt;configuration&gt;&#13;&#10;&lt;startup&gt;&#13;&#10;&lt;supportedRuntime version=&quot;v4.0&quot; sku=&quot;.NETFramework,Version=v4.7&quot;/&gt;&#13;&#10;&lt;/startup&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;!-- AppContextSwitchOverrides value attribute is in the form of &#39;key1=true/false;key2=true/false  --&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.Windows.Data.Binding.IListIndexerHidesCustomIndexer=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Escopo|Principal|
|Versão|4.8|
|Type|Runtime|
