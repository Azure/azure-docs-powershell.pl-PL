---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719089"
---
# Get-AzureRmFirewall

## STRESZCZENIe
Pobiera zaporę Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmFirewall umożliwia pobranie** co najmniej jednej zapory w grupie zasobów.

## Przykłady

### 1: pobieranie wszystkich zapór w grupie zasobów
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

W tym przykładzie są pobierane wszystkie zapory w grupie zasobów "rgName".

### 2: pobieranie zapory za pomocą nazwy
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

W tym przykładzie jest pobierana Zapora o nazwie "azFw" w grupie zasobów "rgName".

### 3: pobieranie zapory, a następnie dodawanie kolekcji reguł aplikacji do zapory
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

W tym przykładzie jest pobierana Zapora, a następnie do zapory jest dodawana Kolekcja reguł aplikacji przez połączenie metody AddApplicationRuleCollection.

### 4: pobieranie zapory, a następnie dodawanie kolekcji reguł sieci do zapory
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

W tym przykładzie jest pobierana Zapora, a następnie do zapory jest dodawana Kolekcja reguł sieci przez połączenie metody AddNetworkRuleCollection.

### 5: pobieranie zapory, a następnie pobieranie kolekcji reguł aplikacji według nazwy z zapory
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

W tym przykładzie jest pobierana Zapora, a następnie pobierana jest kolekcja reguł według nazwy, która jest wywoływana przy użyciu metody GetApplicationRuleCollectionByName na obiekcie firewall. W nazwie kolekcji reguł dla metody GetApplicationRuleCollectionByName nie jest rozróżniana wielkość liter.

### 6: pobieranie zapory, a następnie pobieranie kolekcji reguł sieci według nazwy z zapory
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

W tym przykładzie jest pobierana Zapora, a następnie pobierana jest kolekcja reguł według nazwy, która jest wywoływana przy użyciu metody GetNetworkRuleCollectionByName na obiekcie firewall. W nazwie kolekcji reguł dla metody GetNetworkRuleCollectionByName nie jest rozróżniana wielkość liter.

### 7: pobieranie zapory, a następnie Usuwanie kolekcji reguł aplikacji według nazwy z zapory
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

W tym przykładzie jest pobierana Zapora, a następnie usuwana jest kolekcja reguł według nazwy, która jest wywoływana przez metodę RemoveApplicationRuleCollectionByName na obiekcie firewall. W nazwie kolekcji reguł dla metody RemoveApplicationRuleCollectionByName nie jest rozróżniana wielkość liter.

### 8: pobieranie zapory, a następnie Usuwanie kolekcji reguł sieci według nazwy z zapory
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

W tym przykładzie jest pobierana Zapora, a następnie usuwana jest kolekcja reguł według nazwy, która jest wywoływana przez metodę RemoveNetworkRuleCollectionByName na obiekcie firewall. W nazwie kolekcji reguł dla metody RemoveNetworkRuleCollectionByName nie jest rozróżniana wielkość liter.

### 9: pobieranie zapory, a następnie przydzielenie zapory
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

W tym przykładzie jest pobierana Zapora i połączenia przydzielone na zaporze w celu uruchomienia usługi firewall przy użyciu konfiguracji (aplikacji i kolekcji reguł sieci) skojarzonych z zaporą.

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

### -Name (nazwa)
Określa nazwę zapory, która jest pobierana przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której należy Zapora.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSAzureFirewall

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)

[Set-AzureRmFirewall](./Set-AzureRmFirewall.md)
