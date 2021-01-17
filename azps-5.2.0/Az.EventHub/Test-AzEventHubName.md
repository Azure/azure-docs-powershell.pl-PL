---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/test-azeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Test-AzEventHubName.md
ms.openlocfilehash: 8eb43982db0eddeb9127006e0cfa3336698eb7e3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345325"
---
# Test-AzEventHubName

## STRESZCZENIe
Sprawdza dostępność danej nazwy obszaru nazw lub aliasu (nazwy konfiguracji DR).

## POLECENIA

### NamespaceCheckNameAvailabilitySet (domyślny)
```
Test-AzEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### AliasCheckNameAvailabilitySet
```
Test-AzEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **test-AzEventhubName** sprawdza dostępność nazwy obszaru nazw lub aliasu (nazwy konfiguracji dr).

## Przykłady

### Przykład 1
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako prawda, jeśli jest dostępna.

### Przykład 2
```
PS C:\> Test-AzEventhubName -Namespace MyNameSapceName
```

Zwraca stan dostępności nazwy przestrzeni nazw "MyNameSapceName" jako FAŁSZ z powodu

### Przykład 3
```
PS C:\> Test-AzEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

Zwraca stan dostępności nazwy aliasu "aliasname" dla obszaru nazw "MyNameSapceName" jako prawda, jeśli jest dostępny.

## PARAMETRÓW

### -Aliasname
Nazwa konfiguracji DR — Nazwa aliasu

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### -Namespace
Nazwa obszaru nazw Eventhub

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów

```yaml
Type: System.String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. EventHub. modele. PSCheckNameAvailabilityResultAttributes

## INFORMACYJN

## LINKI POKREWNE
