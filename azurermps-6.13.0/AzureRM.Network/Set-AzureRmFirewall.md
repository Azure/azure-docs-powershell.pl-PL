---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524378"
---
# Set-AzureRmFirewall

## STRESZCZENIe
Umożliwia zapisanie zmodyfikowanej zapory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmFirewall** aktualizuje zaporę platformy Azure.

## Przykłady

### 1: priorytet aktualizacji kolekcji reguł aplikacji zapory
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

W tym przykładzie Zaktualizowano priorytet istniejącej kolekcji reguł w zaporze platformy Azure.
Zakładając, że Zapora platformy Azure "AzureFirewall" w grupie zasobów "RG" zawiera kolekcję reguł aplikacji o nazwie "ruleCollectionName", powyższe polecenia zmienią priorytet kolekcji reguł, a następnie zaktualizują zaporę systemu Azure później. Bez polecenia Set-AzureRmFirewall wszystkie operacje wykonywane na lokalnym obiekcie $azFw nie są odzwierciedlane na serwerze.

### 2: Tworzenie zapory na platformie Azure i Konfigurowanie kolekcji reguł aplikacji później
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

W tym przykładzie Zapora jest tworzona jako pierwsza bez żadnych kolekcji reguł aplikacji. Po utworzeniu zestawu reguł aplikacji i kolekcji reguł aplikacji obiekt firewall jest modyfikowany w pamięci bez wpływu na rzeczywistą konfigurację w chmurze. Aby zmiany zostały odzwierciedlone w chmurze, należy najpierw wywołać Set-AzureRmFirewall.

## PARAMETRÓW

### -AsJob
Uruchom polecenie cmdlet w tle

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

### -AzureFirewall
AzureFirewall

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSAzureFirewall
Parametr "AzureFirewall" akceptuje wartość typu "PSAzureFirewall" z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSAzureFirewall

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmFirewall](./Get-AzureRmFirewall.md)

[Nowe — AzureRmFirewall](./New-AzureRmFirewall.md)

[Remove-AzureRmFirewall](./Remove-AzureRmFirewall.md)
