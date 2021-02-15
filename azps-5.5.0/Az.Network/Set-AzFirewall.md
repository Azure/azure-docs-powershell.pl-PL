---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzFirewall.md
ms.openlocfilehash: 1ab3d82b494d5598081ea229a7ae50d486b8ca20
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189522"
---
# Set-AzFirewall

## SYNOPSIS
Umożliwia zapisanie zmodyfikowanej zapory.

## SKŁADNIA

```
Set-AzFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzFirewall** aktualizuje Zaporę platformy Azure.

## PRZYKŁADY

### 1. Aktualizowanie priorytetu zbioru reguł aplikacji zapory
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzFirewall -AzureFirewall $azFw
```

W tym przykładzie priorytet istniejącej kolekcji reguł zapory platformy Azure jest aktualizowany.
Zakładając, że zapora platformy Azure "AzureFirewall" w grupie zasobów "rg" zawiera kolekcję reguł aplikacji o nazwie "ruleCollectionName", powyższe polecenia później zmienią priorytet tego zbioru reguł i zaktualizują Zaporę platformy Azure. Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.

### 2. Tworzenie Zapory platformy Azure i ustawianie zbioru reguł aplikacji później
```
$azFw = New-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzFirewall
```

W tym przykładzie Zapora jest tworzona najpierw bez żadnych kolekcji reguł aplikacji. Później są tworzone reguły aplikacji i zbiór reguł aplikacji, a następnie obiekt Zapory jest modyfikowany w pamięci, bez wpływu na rzeczywistą konfigurację w chmurze. Aby zmiany mają być odzwierciedlane w chmurze, Set-AzFirewall musi zostać wywołana.

### 3. Aktualizowanie trybu operacji "Threat Intel" zapory platformy Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ThreatIntelMode = "Deny"
Set-AzFirewall -Firewall $azFw
```

W tym przykładzie aktualizacja trybu operacji Threat Intel zapory platformy Azure "AzureFirewall" w grupie zasobów "rg".
Bez polecenia Set-AzFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.

### 4. Przydzielanie transakcji i przydzielanie zapory
```
$firewall=Get-AzFirewall -ResourceGroupName rgName -Name azFw
$firewall.Deallocate()
$firewall | Set-AzFirewall

$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$firewall.Allocate($vnet, $pip)
$firewall | Set-AzFirewall
```
W tym przykładzie jest pobierana Zapora, lokalizuje zaporę i zapisuje ją. Polecenie Deallocate usuwa uruchamianą usługę, ale zachowuje konfigurację zapory. Aby zmiany mają być odzwierciedlane w chmurze, Set-AzFirewall musi zostać wywołana.
Jeśli użytkownik chce ponownie uruchomić usługę, należy uruchomić metodę Allocate w zaporze.
Nowy adres VNet i publiczny adres IP muszą znajdować się w tej samej grupie zasobów co zapora. Również w celu odzwierciedlenia zmian w chmurze Set-AzFirewall musi zostać wywołana.

### 5. Przydzielanie przy użyciu publicznego adresu IP zarządzania na scenariusze wymuszonego rozdzielania
```
$vnet = Get-AzVirtualNetwork -ResourceGroupName rgName -Name anotherVNetName
$pip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name publicIpName
$mgmtPip = Get-AzPublicIpAddress -ResourceGroupName rgName -Name MgmtPublicIpName
$firewall.Allocate($vnet, $pip, $mgmtPip)
$firewall | Set-AzFirewall
```
W tym przykładzie zapora z publicznym adresem IP zarządzania i podsiecią zarządzania jest przydzielana w scenariuszach z wymuszonym podcięciem. Sieć VNet musi zawierać podsieci o nazwie "AzureFirewallManagementSubnet".

### 6. Dodawanie publicznego adresu IP do Zapory platformy Azure
```
$pip = New-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AddPublicIpAddress($pip)

$azFw | Set-AzFirewall
```

W tym przykładzie publiczny adres IP "azFwPublicIp1" dołączony do zapory.

### 7. Usuwanie publicznego adresu IP z Zapory platformy Azure
```
$pip = Get-AzPublicIpAddress -Name "azFwPublicIp1" -ResourceGroupName "rg"
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.RemovePublicIpAddress($pip)

$azFw | Set-AzFirewall
```

W tym przykładzie publiczny adres IP "azFwPublicIp1" odłączony od Zapory.

### 8. Zmienianie publicznego adresu IP zarządzania w Zaporze platformy Azure
```
$newMgmtPip = New-AzPublicIpAddress -Name "azFwMgmtPublicIp2" -ResourceGroupName "rg" -Sku "Standard" -Location "centralus" -AllocationMethod Static
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.ManagementIpConfiguration.PublicIpAddress = $newMgmtPip

$azFw | Set-AzFirewall
```

W tym przykładzie publiczny adres IP zarządzania zapory zostanie zmieniony na "AzFwMgmtPublicIp2".

### 9. Dodawanie konfiguracji systemu DNS do zapory platformy Azure
```
$dnsServers = @("10.10.10.1", "20.20.20.2")
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.DNSEnableProxy = $true
$azFw.DNSServer = $dnsServers

$azFw | Set-AzFirewall
```

W tym przykładzie konfiguracja serwera proxy DNS i serwera DNS jest dołączona do zapory.

### 10. Aktualizowanie miejsca docelowego istniejącej reguły w zbiorze reguł aplikacji zapory
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetNetworkRuleCollectionByName("ruleCollectionName")
$rule=$ruleCollection.GetRuleByName("ruleName")
$rule.DestinationAddresses = "10.10.10.10"
Set-AzFirewall -AzureFirewall $azFw
```

W tym przykładzie jest aktualizowana docelowa istniejąca reguła w zbiorze reguł zapory platformy Azure. Dzięki temu można automatycznie aktualizować reguły, gdy adresy IP zmieniają się dynamicznie.

### 11. Zezwalanie na aktywne protokół FTP w zaporze platformy Azure
```
$azFw = Get-AzFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$azFw.AllowActiveFTP = $true

$azFw | Set-AzFirewall
```

W tym przykładzie aktywny protokół FTP jest dozwolony na zaporze.

## PARAMETERS

### — AsJob
Uruchamianie polecenia cmdlet w tle

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — AzureFirewall
The AzureFirewall

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSAzureFirewall

## NOTATKI

## LINKI POKREWNE

[Get-AzFirewall](./Get-AzFirewall.md)

[New-AzFirewall](./New-AzFirewall.md)

[Remove-AzFirewall](./Remove-AzFirewall.md)
