---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 184e1291f134b52ee57a239327bb45da4a4481ff
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890750"
---
# Get-AzNetworkSecurityRuleConfig

## STRESZCZENIe
Uzyskaj konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci.

## POLECENIA

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzNetworkSecurityRuleConfig** Pobiera konfigurację reguły zabezpieczeń sieci dla grupy zabezpieczeń sieci Azure.

## Przykłady

### 1: Pobieranie konfiguracji reguł zabezpieczeń sieci
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

To polecenie pobiera domyślną regułę o nazwie "AllowInternetOutBound" z grupy zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1".

### 2: Pobieranie konfiguracji reguł zabezpieczeń sieci przy użyciu samej nazwy
```
Get-AzNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

To polecenie pobiera regułę zdefiniowaną przez użytkownika o nazwie "RDP-Rule" z grupy zabezpieczeń sieci Azure o nazwie "nsg1" w grupie zasobów "RG1".

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

### -DefaultRules
Wskazuje, czy to polecenie cmdlet umożliwia pobieranie konfiguracji reguły utworzonej przez użytkownika, czy domyślnej konfiguracji reguły.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę konfiguracji reguł zabezpieczeń sieci do pobrania.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkSecurityGroup
Określa obiekt **NetworkSecurityGroup** , który zawiera konfigurację reguły zabezpieczeń sieci do pobrania.

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSNetworkSecurityGroup
Parametr "NetworkSecurityGroup" akceptuje wartość typu "PSNetworkSecurityGroup" z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSSecurityRule

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzNetworkSecurityRuleConfig](./Add-AzNetworkSecurityRuleConfig.md)

[Nowe — AzNetworkSecurityRuleConfig](./New-AzNetworkSecurityRuleConfig.md)

[Remove-AzNetworkSecurityRuleConfig](./Remove-AzNetworkSecurityRuleConfig.md)

[Set-AzNetworkSecurityRuleConfig](./Set-AzNetworkSecurityRuleConfig.md)


