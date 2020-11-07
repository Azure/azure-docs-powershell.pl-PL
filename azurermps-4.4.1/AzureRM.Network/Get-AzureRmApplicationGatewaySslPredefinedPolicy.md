---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewaySslPredefinedPolicy.md
ms.openlocfilehash: 03d47278681cbba23895c00b124cc3a2fc2cc6e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719628"
---
# Get-AzureRmApplicationGatewaySslPredefinedPolicy

## STRESZCZENIe
Pobiera wstępnie zdefiniowane zasady SSL udostępnione przez bramę Application Gateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmApplicationGatewaySslPredefinedPolicy [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmApplicationGatewaySslPredefinedPolicy** umożliwia pobieranie wstępnie zdefiniowanych zasad SSL udostępnionych przez bramkę Application Gateway.

## Przykłady

### Przykład 1
```
PS C:\>$policies = Get-AzureRmApplicationGatewaySslPredefinedPolicy
```

To polecenie zwraca wszystkie wstępnie zdefiniowane zasady SSL.

### Przykład 2
```
PS C:\>$policy = Get-AzureRmApplicationGatewaySslPredefinedPolicy -Name AppGwSslPolicy20170401
```

To polecenie zwraca wstępnie zdefiniowane zasady z nazwą AppGwSslPolicy20170401.

## PARAMETRÓW

### -Name (nazwa)
Nazwa wstępnie zdefiniowanych zasad SSL

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySslPredefinedPolicy
System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewaySslPredefinedPolicy, Microsoft. Azure. Commands, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMACYJN

## LINKI POKREWNE

