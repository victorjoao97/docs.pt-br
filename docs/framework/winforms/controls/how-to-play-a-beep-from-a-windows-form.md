---
title: 'Como: Reproduzir um aviso sonoro de um Windows Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], beep
- Windows Forms, sounds
- sounds [Windows Forms], playing
- forms [Windows Forms], sounds
- examples [Windows Forms], sounds
ms.assetid: 7ea5cded-4888-4f35-8f28-5cab1a55c973
ms.openlocfilehash: 7fecc5d5b7259b743926713f87d9303596803582
ms.sourcegitcommit: 121ab70c1ebedba41d276e436dd2b1502748a49f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2019
ms.locfileid: "70015817"
---
# <a name="how-to-play-a-beep-from-a-windows-form"></a>Como: Reproduzir um aviso sonoro de um Windows Form
Este exemplo reproduz um aviso sonoro no tempo de execução.

## <a name="example"></a>Exemplo

```vb
Public Sub OnePing()
    Beep()
End Sub
```

```csharp
public void onePing()
{
    SystemSounds.Beep.Play();
}
```

> [!NOTE]
> O som tocado no exemplo C# de código é determinado pela configuração <xref:System.Media.SystemSounds.Beep%2A> de som do sistema. Para obter mais informações, consulte <xref:System.Media.SystemSounds>.

## <a name="compiling-the-code"></a>Compilando o código
 Para C#, este exemplo requer uma referência ao <xref:System.Media?displayProperty=nameWithType> namespace.

## <a name="see-also"></a>Consulte também

- <xref:Microsoft.VisualBasic.Interaction.Beep%2A>
- <xref:System.Media.SoundPlayer>
- [Como: Reproduzir um som do sistema de um Windows Form](how-to-play-a-system-sound-from-a-windows-form.md)
- [Como: Tocar um som de um formulário do Windows](how-to-play-a-sound-from-a-windows-form.md)
