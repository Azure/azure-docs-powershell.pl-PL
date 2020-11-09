---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azfirewallpolicyrulecollectiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyRuleCollectionGroup.md
ms.openlocfilehash: 8d60b8f7ff28e6c2a4f5a177f5cad222b1a3014c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309240"
---
# New-AzFirewallPolicyRuleCollectionGroup

## STRESZCZENIe
Tworzenie nowej grupy kolekcji reguł zasad zapory platformy Azure

## POLECENIA

### SetByInputObjectParameterSet
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyObject <PSAzureFirewallPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNameParameterSet
```
New-AzFirewallPolicyRuleCollectionGroup -Name <String> -Priority <UInt32>
 -RuleCollection <PSAzureFirewallPolicyBaseRuleCollection[]> -ResourceGroupName <String>
 -FirewallPolicyName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzFirewallPolicyRuleCollectionGroup** tworzy grupę kolekcji reguł w zasadach zapory platformy Azure.

## Przykłady

### Przykład 1
```powershell
PS C:\> New-AzFirewallPolicyRuleCollectionGroup -Name rg1 -ResourceGroupName TestRg -Location westus -Priority 200 -RuleCollection $filterRule1 -AzureFirewallPolicy $fp
```

W tym przykładzie przedstawiono tworzenie grupy kolekcji reguł w $fp zasad zapory

### Przykład 2

Utwórz nową grupę kolekcji reguł zasad zapory platformy Azure. (autogenerowana)

<!-- Aladdin Generated Example -->
```powershell
New-AzFirewallPolicyRuleCollectionGroup -FirewallPolicyName <String> -Name rg1 -Priority 200 -ResourceGroupName TestRg
```

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

### -FirewallPolicyName
Nazwa zasad zapory

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FirewallPolicyObject
Zasady zapory.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa grupy reguł

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority (priorytet)
Priorytet grupy reguł

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleCollection
Lista reguł

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyBaseRuleCollection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicy

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSAzureFirewallPolicyRuleCollectionGroup

## INFORMACYJN

## LINKI POKREWNE
