---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzFirewallPolicy.md
ms.openlocfilehash: f53733976d946b61fc143e0a2b2e9be71017b7f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052317"
---
# Get-AzFirewallPolicy

## STRESZCZENIe
Pobiera zasady zapory platformy Azure

## POLECENIA

### GetByNameParameterSet (domyślny)
```
Get-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByResourceIdParameterSet
```
Get-AzFirewallPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzFirewallPolicy** pobiera co najmniej jedno okno zapory w grupie zasobów

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzFirewallPolicy -Name firwallPolicy -ResourceGroupName TestRg
```

W tym przykładzie otrzymano zasady zapory o nazwie "firewallPolicy" w grupie zasobów "TestRg".

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa zasobu.

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu.

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
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

### Microsoft. Azure. Commands. Network. models. PSAzureFirewall

### System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. models. PSAzureFirewall, Microsoft. Azure. PowerShell. PowerShell

## INFORMACYJN

## LINKI POKREWNE
