---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489821"
---
# Get-AzEventGridTopicType

## STRESZCZENIe
Pobiera szczegóły dotyczące typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.

## POLECENIA

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Pobiera szczegóły typów tematów obsługiwanych przez siatkę zdarzeń platformy Azure.
Jeśli podano nazwę typu tematu, zostaną zwrócone szczegóły dotyczące tego typu tematu.
Jeśli nie podano nazwy typu tematu, zwracane są szczegóły dotyczące wszystkich typów tematów.
Jeśli IncludeEventTypes jest określony, w odpowiedzi jest uwzględniana informacja o typach zdarzeń obsługiwanych przez poszczególne typy tematów.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

Pobiera listę typów tematów.

### Przykład 2
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

Pobiera informacje o typie tematu StorageAccounts.

### Przykład 3
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Pobiera informacje o typie tematu StorageAccounts, w tym o typach zdarzeń obsługiwanych przez StorageAccounts.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -IncludeEventTypeData
Jeśli ta wartość jest określona, odpowiedź będzie zawierać typy zdarzeń obsługiwane przez typ tematu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa typu tematu EventGrid.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. EventGrid. models. PSTopicTypeInfoListInstance

### Microsoft. Azure. Commands. EventGrid. models. PSTopicTypeInfo

## INFORMACYJN

## LINKI POKREWNE
