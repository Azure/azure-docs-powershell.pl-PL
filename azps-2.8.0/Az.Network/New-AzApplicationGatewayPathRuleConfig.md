---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A1F949A9-7AEF-41C1-B757-114421B79493
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaypathruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPathRuleConfig.md
ms.openlocfilehash: 6592f79291c069ade40b30277461f5e0e218b937
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407050"
---
# New-AzApplicationGatewayPathRuleConfig

## SYNOPSIS
Tworzy regułę ścieżki bramy aplikacji.

## SKŁADNIA

### SetByResourceId
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]> [-BackendAddressPoolId <String>]
 [-BackendHttpSettingsId <String>] [-RewriteRuleSetId <String>] [-RedirectConfigurationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
New-AzApplicationGatewayPathRuleConfig -Name <String> -Paths <String[]>
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-RewriteRuleSet <PSApplicationGatewayRewriteRuleSet>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzApplicationGatewayPathRuleConfig** tworzy regułę ścieżki bramy aplikacji.
Reguły utworzone za pomocą tego polecenia cmdlet można dodać do zbioru ustawień konfiguracji mapy ścieżki adresu URL, a następnie przypisać do bramy.
Ustawienia konfiguracji mapy ścieżki są używane do równoważenia obciążenia bramy aplikacji.

## PRZYKŁADY

### Przykład 1
```
PS C:\>$Gateway = Get-AzApplicationGateway -Name "ContosoApplicationGateway"
PS C:\> $AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"
PS C:\> $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled"
PS C:\> $PathRuleConfig = New-AzApplicationGatewayPathRuleConfig -Name "base" -Paths "/base" -BackendAddressPool $AddressPool -BackendHttpSettings $HttpSettings
PS C:\> Add-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $Gateway -Name "ContosoUrlPathMap" -PathRules $PathRuleConfig -DefaultBackendAddressPool $AddressPool -DefaultBackendHttpSettings $HttpSettings
```

Te polecenia tworzą nową regułę ścieżki bramy aplikacji, a następnie przypisz ją do bramy aplikacji za pomocą polecenia cmdlet **Add-AzApplicationGatewayUrlPathMapConfig.**
W tym celu pierwsze polecenie tworzy odwołanie do obiektu bramy ContosoApplicationGateway.
To odwołanie do obiektu jest przechowywane w zmiennej o nazwie $Gateway.
Następne dwa polecenia tworzą pulę adresów zaplecza i obiekt ustawień protokołu HTTP zaplecza. te obiekty (przechowywane w zmiennych $AddressPool i $HttpSettings) są potrzebne do utworzenia obiektu reguły ścieżki.
Czwarte polecenie tworzy obiekt reguły ścieżki i jest przechowywany w zmiennej o nazwie $PathRuleConfig.
Piąte polecenie korzysta z polecenia **Add-AzApplicationGatewayUrlPathMapConfig** w celu dodania ustawień konfiguracji i nowej reguły ścieżki zawartej w tych ustawieniach do aplikacji ContosoApplicationGateway.

## PARAMETERS

### -BackendAddressPool
Określa odwołanie do obiektu do kolekcji ustawień puli adresów zaplecza, które mają zostać dodane do ustawień konfiguracji reguł ścieżki bramy.
To odwołanie do obiektu można utworzyć przy użyciu polecenia cmdlet New-AzApplicationGatewayBackendAddressPool składni podobnej do tej: `$AddressPool = New-AzApplicationGatewayBackendAddressPool -Name "ContosoAddressPool" -BackendIPAddresses "192.168.1.1", "192.168.1.2"`
Poprzednie polecenie dodaje dwa adresy IP (192.16.1.1 i 192.168.1.2) do puli adresów.
Zwróć uwagę, że adres IP jest ujęty w cudzysłów i oddzielony przecinkami.
Następnie można użyć $AddressPool jako wartości parametru *parametru DefaultBackendAddressPool.*
Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.
Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.
W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendAddressPoolId* w tym samym poleceniu.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendAddressPoolId
Określa identyfikator istniejącej puli adresów zaplecza, którą można dodać do ustawień konfiguracji reguły ścieżki bramy.
Identyfikatory puli adresów można zwrócić za pomocą Get-AzApplicationGatewayBackendAddressPool cmdlet.
Po tym identyfikatorze można użyć parametru *DefaultBackendAddressPoolId* zamiast *parametru DefaultBackendAddressPool.*
Na przykład: -DefaultBackendAddressPoolId "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10//resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendAddressPools/ContosoAddressPools" Pula adresów zaplecza reprezentuje adresy IP na serwerach zaplecza.
Te adresy IP powinny należeć do podsieci sieci wirtualnej lub powinny być publicznymi adresami IP.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackendHttpSettings
Określa odwołanie do obiektu do zbioru ustawień http zaplecza, które mają zostać dodane do ustawień konfiguracji reguły ścieżki bramy.
To odwołanie do obiektu można utworzyć przy użyciu polecenia cmdlet New-AzApplicationGatewayBackendHttpSettings o składni podobnej do tej: $HttpSettings = New-AzApplicationGatewayBackendHttpSettings -Name "ContosoHttpSettings" -Port 80 -Protocol "Http" -CookieBasedAffinity "Disabled" Zmienna wynikowa. $HttpSettings następnie może być używana jako wartość parametru *parametru DefaultBackendAddressPool:* -DefaultBackendHttpSettings $HttpSettings Ustawienia protokołu HTTP zaplecza konfigurują właściwości, takie jak port, protokół i chowalność oparta na plikach cookie puli zaplecza.
W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendHttpSettingsId* w tym samym poleceniu.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
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
Identyfikatory ustawień protokołu HTTP można zwrócić za pomocą Get-AzApplicationGatewayBackendHttpSettings cmdlet.
Po wytyczaniu identyfikatora można użyć parametru *DefaultBackendHttpSettingsId* zamiast parametru *DefaultBackendHttpSettings.*
Na przykład: -DefaultBackendSettings Id "/subscriptions/39c54063-01d3-4abf-8f4c-234777bc1f10//resourceGroups/appgw-rg/providers/Microsoft.Network/applicationGateway/appgwtest/backendHttpSettingsCollection/ContosoHttpSettings" Ustawienia protokołu HTTP zaplecza konfigurują właściwości, takie jak port, protokół, i powiążność opartą na plikach cookie dla puli zaplecza.
W przypadku użycia tego parametru nie można użyć *parametru DefaultBackendHttpSettings* w tym samym poleceniu.

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### — Nazwa
Określa nazwę konfiguracji reguły ścieżki, którą tworzy to polecenie cmdlet.

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

### — Ścieżki
Określa co najmniej jedną regułę ścieżki bramy aplikacji.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfiguration
RedirectConfiguration bramy aplikacji

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RedirectConfigurationId
Identyfikator konfiguracji przekierowywania przez bramę aplikacji

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSet
Application gateway RewriteRuleSet

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRewriteRuleSet
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RewriteRuleSetId
Identyfikator bramy aplikacji RewriteRuleSet

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule

## NOTATKI

## LINKI POKREWNE

[Add-AzApplicationGatewayUrlPathMapConfig](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[Get-AzApplicationGateway](./Get-AzApplicationGateway.md)

[Get-AzApplicationGatewayUrlPathMapConfig](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[New-AzApplicationGatewayBackendAddressPool](./New-AzApplicationGatewayBackendAddressPool.md)


[New-AzApplicationGatewayPathRuleConfig](./New-AzApplicationGatewayPathRuleConfig.md)

[New-AzApplicationGatewayUrlPathMapConfig](./New-AzApplicationGatewayUrlPathMapConfig.md)

[Remove-AzApplicationGatewayUrlPathMapConfig](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[Set-AzApplicationGatewayUrlPathMapConfig](./Set-AzApplicationGatewayUrlPathMapConfig.md)


