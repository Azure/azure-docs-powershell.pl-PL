---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Tags.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 07c6e327-05f4-4279-a5fb-d4e860c897d4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-aztag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzTag.md
ms.openlocfilehash: df34b529a64e1c773c95a5234fd995944e8caac8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308700"
---
# Update-AzTag

## STRESZCZENIe

Selektywne Aktualizowanie zestawu znaczników zasobu lub abonamentu.

## POLECENIA

```powershell
Update-AzTag
   -ResourceId <String>
   -Operation <TagPatchOpeation>
   -Tag <Hashtable>
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]

```

## Opis

Polecenie cmdlet **Update-AzTag** z identyfikatorem **zasobu umożliwia selektywne** Aktualizowanie zestawu tagów w zasobie lub subskrypcji.
Ta operacja umożliwia zamianę, scalanie lub selektywne usuwanie tagów określonego zasobu lub abonamentu. Na końcu operacji określona encja może zawierać maksymalnie 50 tagów. Opcja "Zamień" powoduje zastąpienie całego zestawu istniejących znaczników nowym zestawem. Opcja "Scal" umożliwia dodawanie tagów przy użyciu nowych nazw i aktualizowanie wartości znaczników przy użyciu istniejących nazw. Opcja "Usuń" umożliwia wybiórcze Usuwanie tagów na podstawie podanych nazw lub par nazw/wartości.

## Przykłady

### Przykład 1. selektywne Aktualizowanie zestawu znaczników w subskrypcji za pomocą operacji scalania

```powershell
PS C:\>$mergedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $mergedTags -Operation Merge

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key2     value2
             key3     value3
```

To polecenie Scala zestaw tagów w subskrypcji z aplikacją {subId}.

### Przykład 2: selektywne Aktualizowanie zestawu znaczników w subskrypcji przy użyciu operacji zamieniania

```powershell
PS C:\>$replacedTags = @{"key1"="value1"; "key3"="value3";}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $replacedTags -Operation Replace

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key1     value1
             key3     value3
```

To polecenie Repalces zestaw tagów w subskrypcji przy użyciu funkcji {subId}.

### Przykład 3: selektywne Aktualizowanie zestawu znaczników w subskrypcji za pomocą operacji usuwania

```powershell
PS C:\>$deletedTags = @{"key1"="value1"}
PS C:\>Update-AzTag -ResourceId /subscriptions/{subId} -Tag $deletedTags -Operation Delete

Id         : {Id}
Name       : {Name}
Type       : {Type}
Properties :
             Name     Value
             =======  =========
             key3     value3
```

To polecenie usuwa zestaw tagów w subskrypcji przy użyciu programu {subId}.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu oznakowanej jednostki. Zasób, Grupa zasobów lub abonament mogą być oznakowane.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Zestaw tagów, które mają być używane do aktualizacji.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Operation
Operacja aktualizowania. Opcje są scalane, zamieniane i usuwane.

```yaml
Type: Microsoft.Azure.Commands.Tags.Model.TagPatchOpeation
Parameter Sets: (All)
Aliases:
Accepted values: Merge, Replace, Delete

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Tags. model. TagPatchOpeation

### System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Commands. Tags. model. PSTagResource

## INFORMACYJN

## LINKI POKREWNE

[Get-AzTag](./Get-AzTag.md)

[Nowe — AzTag](./New-AzTag.md)

[Remove-AzTag](./Remove-AzTag.md)