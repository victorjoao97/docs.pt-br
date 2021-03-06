---
title: -target:library (opções do compilador C#)
ms.date: 07/20/2015
f1_keywords:
- /dll
helpviewer_keywords:
- -target compiler options [C#], /target:library
- target compiler options [C#], /target:library
- /target compiler options [C#], /target:library
ms.assetid: c5670e88-2126-47c1-8d1c-217923837d17
ms.openlocfilehash: c947b2015c19d0809cab4535e989ee83ebf17fd9
ms.sourcegitcommit: 7588136e355e10cbc2582f389c90c127363c02a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/14/2020
ms.locfileid: "69606400"
---
# <a name="-targetlibrary-c-compiler-options"></a>-target:library (opções do compilador C#)
A opção **-target:library** faz com que o compilador crie uma DLL (biblioteca de vínculo dinâmico) em vez de um EXE (arquivo executável).  
  
## <a name="syntax"></a>Sintaxe  
  
```console  
-target:library  
```  
  
## <a name="remarks"></a>Comentários  
 A DLL será criada com a extensão .dll.  
  
 A menos que seja especificado de outra forma com a opção [-out](./out-compiler-option.md), o nome do arquivo de saída usa o nome do primeiro arquivo de entrada.  
  
 Quando especificado na linha de comando, todos os arquivos até a próxima opção **-out** ou **-target:module** são usados para criar o arquivo .dll.  
  
 Ao criar um arquivo .dll, um método [Main](../../programming-guide/main-and-command-args/index.md) não é necessário.  
  
### <a name="to-set-this-compiler-option-in-the-visual-studio-development-environment"></a>Para definir esta opção do compilador no ambiente de desenvolvimento do Visual Studio  
  
1. Abra a página **Propriedades** do projeto.  
  
2. Clique na página de propriedades do **Aplicativo**.  
  
3. Modifique a propriedade **Tipo de saída**.  
  
 Para obter informações sobre como definir essa opção do compilador programaticamente, consulte <xref:VSLangProj80.ProjectProperties3.OutputType%2A>.  
  
## <a name="example"></a>Exemplo  
 Compile `in.cs`, criando `in.dll`:  
  
```console  
csc -target:library in.cs  
```  
  
## <a name="see-also"></a>Confira também

- [-destino (C# Opções de compilador)](./target-compiler-option.md)
- [C# Opções de compilador](./index.md)
