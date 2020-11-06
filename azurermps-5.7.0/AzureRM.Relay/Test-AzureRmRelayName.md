---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548024"
---
# Test-AzureRmRelayName

## STRESZCZENIe
Sprawdza dostępność danej nazwy obszaru nazw.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **test-AzureRmRelayName** sprawdza dostępność nazwy przestrzeni nazw.

## Przykłady

### Przykład 1
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### Przykład 2
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### Przykład 3
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

Zwraca stan dostępności nazwy przestrzeni nazw.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Nazwa obszaru nazw przekaźnika.

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

### [Microsoft. Azure. Commands. Relay. models. CheckNameAvailabilityResultAttributes, Microsoft. Azure. Commands

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

