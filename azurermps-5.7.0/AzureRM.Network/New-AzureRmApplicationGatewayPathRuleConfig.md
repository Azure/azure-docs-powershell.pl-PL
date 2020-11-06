---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 209986a25882415a68df86611d10559612a8ec04
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549660"
---
# New-AzureRmApplicationGatewayPathRuleConfig

## STRESZCZENIe
Tworzy regułę ścieżki bramy Application Gateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### SetByResourceId
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzureRmApplicationGatewayPathRuleConfig -Name <String>
 -Paths <System.Collections.Generic.List`1[System.String]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmApplicationGatewayPathRuleConfig** tworzy regułę ścieżki bramy Application Gateway.
Reguły utworzone przez to polecenie cmdlet można dodać do kolekcji ustawień konfiguracji mapowania ścieżki URL, a następnie przypisywać je do bramy.

Ustawienia konfiguracji mapy ścieżki są używane w równoważeniu obciążenia bramy aplikacji.

## Przykłady

### Przykład 1
```
PS C:\>$Gateway = Get-AzureRmApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings -Name "ContosoHttpSetings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzureRmApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Te polecenia umożliwiają utworzenie nowej reguły ścieżki bramy Application Gateway, a następnie użycie polecenia cmdlet **Add-AzureRmApplicationGatewayUrlPathMapConfig** w celu przypisania tej reguły do bramy aplikacji.
W tym celu pierwsze polecenie tworzy odwołanie do obiektu bramy ContosoApplicationGateway.
Odwołanie do tego obiektu jest przechowywane w zmiennej o nazwie $Gateway.

Następne dwa polecenia tworzą pulę adresów zaplecza i obiekt ustawienia HTTP zaplecza; te obiekty (przechowywane w zmiennych $AddressPool i $HttpSettings) są potrzebne w celu utworzenia obiektu reguły ścieżki.

Czwarte polecenie tworzy obiekt reguły ścieżki i jest przechowywany w zmiennej o nazwie $PathRuleConfig.

W piątym poleceniu użyto polecenia **Add-AzureRmApplicationGatewayUrlPathMapConfig** w celu dodania ustawień konfiguracji i nowej reguły ścieżki zawartych w tych ustawieniach do ContosoApplicationGateway.

## PARAMETRÓW

### -BackendAddressPool
Określa odwołanie obiektu do kolekcji ustawień puli adresów zaplecza, które mają zostać dodane do ustawień konfiguracji reguł ścieżki bramy.
To odwołanie do obiektu można utworzyć przy użyciu New-AzureRmApplicationGatewayBackendAddressPool polecenia cmdlet i składni podobnej do następującej:

`$AddressPool = New-AzureRmApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`

W powyższym poleceniu są dodawane dwa adresy IP (192.16.1.1 i 192.168.1.2) do puli adresów.
Należy zauważyć, że adres IP jest ujęty w cudzysłów i oddzielony średnikami.

Zmienna wynikowa $AddressPool może być używana jako wartość parametru parametru *DefaultBackendAddressPool* .

Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.
Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.
W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendAddressPoolId* w tym samym poleceniu.

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Określa identyfikator istniejącej puli adresów zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.
Identyfikatory puli adresów można zwracać przy użyciu polecenia cmdlet Get-AzureRmApplicationGatewayBackendAddressPool.
Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendAddressPoolId* zamiast parametru *DefaultBackendAddressPool* .
Na przykład:

-DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendAddressPools/ContosoAddressPool"

Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.
Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
Określa odwołanie obiektu do kolekcji ustawień protokołu HTTP zaplecza, które mają zostać dodane do ustawień konfiguracji reguły ścieżki bramy.
To odwołanie do obiektu można utworzyć przy użyciu New-AzureRmApplicationGatewayBackendHttpSettings polecenia cmdlet i składni podobnej do następującej:

$HttpSettings = New-AzureRmApplicationGatewayBackendHttpSettings-Name "ContosoHttpSetings"-port 80-protokół "http"-CookieBasedAffinity "Disabled"

Zmienna wynikowa $HttpSettings może być używana jako wartość parametru parametru *DefaultBackendAddressPool* :

-DefaultBackendHttpSettings $HttpSettings

Ustawienia HTTP zaplecza konfigurują właściwości, takie jak port, protokół oraz koligacja oparta na plikach cookie dla puli wewnętrznej bazy danych.
W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettingsId* w tym samym poleceniu.

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettingsId
Określa identyfikator istniejącej kolekcji ustawień protokołu HTTP zaplecza, który można dodać do ustawień konfiguracji reguły ścieżki bramy.
Identyfikatory ustawień HTTP można zwrócić przy użyciu Get-AzureRmApplicationGatewayBackendHttpSettings polecenia cmdlet.
Po uzyskaniu identyfikatora możesz użyć parametru *DefaultBackendHttpSettingsId* zamiast parametru *DefaultBackendHttpSettings* .
Na przykład:

-DefaultBackendSettings ID "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10/resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateways/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings"

Ustawienia HTTP zaplecza konfigurują właściwości, takie jak port, protokół oraz koligacja oparta na plikach cookie dla puli wewnętrznej bazy danych.
W przypadku użycia tego parametru nie można użyć parametru *DefaultBackendHttpSettings* w tym samym poleceniu.

```yaml
Type: String
Parameter Sets: SetByResourceId
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
Określa nazwę konfiguracji reguły ścieżki, którą to polecenie cmdlet tworzy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ścieżki
Określa co najmniej jeden Regulamin ścieżki bramy aplikacji.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
Aplikacja Application Gateway RedirectConfiguration

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
Identyfikator bramy Application RedirectConfiguration

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

###  
Funkcja **New-AzureRmApplicationGatewayPathRuleConfig** nie akceptuje danych wejściowych rurociągu.

## WYSYŁA

###  
**Nowe — AzureRmApplicationGatewayPathRuleConfig** tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSApplicationGatewayPathRule** .

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmApplicationGatewayUrlPathMapConfig](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Get-AzureRmApplicationGateway](./Get-AzureRmApplicationGateway.md)

[Get-AzureRmApplicationGatewayUrlPathMapConfig](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Nowe — AzureRmApplicationGatewayBackendAddressPool](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[Nowe — AzureRmApplicationGatewayBackendHttpSettings](./New-AzureRmApplicationGatewayBackendHttpSettings.md)

[Nowe — AzureRmApplicationGatewayPathRuleConfig](./New-AzureRmApplicationGatewayPathRuleConfig.md)

[Nowe — AzureRmApplicationGatewayUrlPathMapConfig](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Remove-AzureRmApplicationGatewayUrlPathMapConfig](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[Set-AzureRmApplicationGatewayUrlPathMapConfig](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


