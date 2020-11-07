---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719088"
---
# Get-AzureRmFirewallFqdnTag

## STRESZCZENIe
Pobiera dostępne znaczniki FQDN zapory platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmFirewallFqdnTag** pobiera listę tagów FQDN, których można użyć w regułach aplikacji Zapora platformy Azure

## Przykłady

### 1: pobieranie wszystkich dostępnych tagów FQDN
```
Get-AzureRmFirewallFqdnTag
```

W tym przykładzie są pobierane wszystkie dostępne znaczniki FQDN.

### 2: używanie znacznika pierwszy dostępny numer FQDN w regule aplikacji
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

W tym przykładzie przedstawiono tworzenie reguły aplikacji zapory przy użyciu pierwszego dostępnego tagu FQDN

## PARAMETRÓW

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
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSAzureFirewallFqdnTag

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmFirewallApplicationRule](./New-AzureRmFirewallApplicationRule.md)

[Nowe — AzureRmFirewall](./New-AzureRmFirewall.md)
