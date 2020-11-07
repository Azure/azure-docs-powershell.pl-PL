---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718695"
---
# Test-AzureRmServiceBusName

## STRESZCZENIe
Sprawdza dostępność danej nazwy obszaru nazw.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## Opis
Polecenie cmdlet **test-AzureRmServiceBusName** sprawdza dostępność nazwy przestrzeni nazw.

## Przykłady

### Przykład 1
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### Przykład 2
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### Przykład 3
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

Zwraca stan dostępności nazwy przestrzeni nazw.

## PARAMETRÓW

### -Namespace
Nazwa przestrzeni nazw ServiceBus.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### -Namespace
 System. String

## WYSYŁA

### [Microsoft. Azure. Commands. ServiceBus. modele. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]

### Przykład 1
Komunikat o przyczynach NameAvailable
------------- ------ -------
         True   None

### Przykład 2
Komunikat o przyczynach NameAvailable
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### Przykład 3
Komunikat o przyczynach NameAvailable
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## INFORMACYJN

## LINKI POKREWNE
