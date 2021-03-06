---
title: Bancos de dados na memória
ms.date: 12/13/2019
description: Saiba como usar bancos de dados do SQLite na memória.
ms.openlocfilehash: 408c81f538e27dcfffad20db74b7809912b7905f
ms.sourcegitcommit: a9b8945630426a575ab0a332e568edc807666d1b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/30/2020
ms.locfileid: "80391202"
---
# <a name="in-memory-databases"></a>Bancos de dados na memória

Os bancos de dados na memória do SQLite são bancos de dados armazenados inteiramente na memória, não no disco. Use o nome de arquivo `:memory:` de fonte de dados especial para criar um banco de dado na memória. Quando a conexão é fechada, o banco de dados é excluído. Ao usar `:memory:`o, cada conexão cria seu próprio banco de dados.

```ConnectionString
Data Source=:memory:
```

## <a name="shareable-in-memory-databases"></a>Bancos de dados compartilhados na memória

Os bancos de dados na memória podem ser compartilhados entre várias conexões usando `Mode=Memory` e `Cache=Shared` na cadeia de conexão. A `Data Source` palavra-chave é usada para fornecer um nome ao banco de dados na memória. As cadeias de conexão que usam o mesmo nome acessarão o mesmo banco de dados na memória. O banco de dados persiste, desde que pelo menos uma conexão permaneça aberta. Um [exemplo](https://github.com/dotnet/docs/blob/master/samples/snippets/standard/data/sqlite/InMemorySample/Program.cs) que demonstra isso está disponível no github.

```ConnectionString
Data Source=InMemorySample;Mode=Memory;Cache=Shared
```
