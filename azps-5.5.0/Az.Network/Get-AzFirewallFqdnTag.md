---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallFqdnTag.md
ms.openlocfilehash: 84d42e18e1946b96a2102a51f71af7e879867d57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193867"
---
# Get-AzFirewallFqdnTag

## SYNOPSIS
Pobiera dostępne tagi Fqdn zapory platformy Azure.

## SKŁADNIA

```
Get-AzFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzFirewallFqdnTag** pobiera listę tagów FQDN, których można używać w regułach aplikacji zapory platformy Azure

## PRZYKŁADY

### 1. Pobieranie wszystkich dostępnych tagów FQDN
```
Get-AzFirewallFqdnTag
```

W tym przykładzie są pobierane wszystkie dostępne tagi FQDN.

### 2. Używanie pierwszego dostępnego tagu FQDN w witrynie application Rule
```
$fqdnTags = Get-AzFirewallFqdnTag
New-AzFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

W tym przykładzie jest tworzenie reguły aplikacji zapory przy użyciu pierwszego dostępnego tagu FQDN

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag

### System.Collections.generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag, Microsoft.Azure.PowerShell.Cmdlet.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]

## NOTATKI

## LINKI POKREWNE

[New-AzFirewallApplicationRule](./New-AzFirewallApplicationRule.md)

[New-AzFirewall](./New-AzFirewall.md)
