---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 28a7fa45c8c6dc291f5e0c2a54c9fcf5fb5242dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709530"
---
# Get-AzFirewallFqdnTag

## STRESZCZENIe
Pobiera dostępne znaczniki FQDN zapory platformy Azure.

## POLECENIA

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzFirewallFqdnTag** pobiera listę tagów FQDN, których można użyć w regułach aplikacji Zapora platformy Azure

## Przykłady

### 1: pobieranie wszystkich dostępnych tagów FQDN
```
Get-AzFirewallFqdnTag
```

W tym przykładzie są pobierane wszystkie dostępne znaczniki FQDN.

### 2: używanie znacznika pierwszy dostępny numer FQDN w regule aplikacji
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

W tym przykładzie przedstawiono tworzenie reguły aplikacji zapory przy użyciu pierwszego dostępnego tagu FQDN

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSAzureFirewallFqdnTag

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. models. PSAzureFirewallFqdnTag, Microsoft. Azure. PowerShell. PowerShell

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[Nowe — AzFirewall](./New-AzFirewall.md)
