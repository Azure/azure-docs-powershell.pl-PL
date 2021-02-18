---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayprivatelinkconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayPrivateLinkConfiguration.md
ms.openlocfilehash: df616c0b8e6d2fdb7de3567c921714251093fd60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240914"
---
# New-AzApplicationGatewayPrivateLinkConfiguration

## SYNOPSIS
Tworzy konfigurację prywatnego linku dla bramy aplikacji

## SKŁADNIA

```
New-AzApplicationGatewayPrivateLinkConfiguration -Name <String>
 -IpConfiguration <PSApplicationGatewayPrivateLinkIpConfiguration[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzApplicationGatewayPrivateLinkConfiguration** tworzy konfigurację PrivateLink dla bramy aplikacji Azure.
Konfiguracja łącza prywatnego musi być skojarzona z konfiguracją frontonu ip, aby włączyć funkcję prywatnego linku.
Jedna konfiguracja łącza prywatnego może być co najwyżej skojarzona tylko z jedną konfiguracją frontonu ip w bramie aplikacji.

## PRZYKŁADY

### Przykład 1. Tworzenie konfiguracji linku prywatnego przy użyciu pojedynczej konfiguracji adresu IP
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1
```

To polecenie tworzy konfigurację privateLink o nazwie "privateLinkConfig01" i przechowuje wynik w zmiennej o nazwie $PrivateLinkConfiguration.

### Przykład 2. Tworzenie konfiguracji linku prywatnego z wieloma konfiguracjami adresów IP
```powershell
PS C:\> $PrivateLinkConfiguration = New-AzApplicationGatewayPrivateLinkConfiguration -Name "privateLinkConfig01" -IpConfiguration $privateLinkIpConfiguration1, $privateLinkIpConfiguration2
```

To polecenie tworzy konfigurację privateLink o nazwie "privateLinkConfig01" z dwoma konfiguracjami ipConfigurations i przechowuje wynik w zmiennej o nazwie $PrivateLinkConfiguration. 

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### -IpConfiguration
Lista konfiguracji ip

```yaml
Type: PSApplicationGatewayPrivateLinkIpConfiguration[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Nazwa konfiguracji privateLink

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkIpConfiguration[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPrivateLinkConfiguration

## NOTATKI

## LINKI POKREWNE

[Get-AzApplicationGatewayPrivateLinkConfiguration](./Get-AzApplicationGatewayPrivateLinkConfiguration.md)

[Add-AzApplicationGatewayPrivateLinkConfiguration](./Add-AzApplicationGatewayPrivateLinkConfiguration.md)

[Remove-AzApplicationGatewayPrivateLinkConfiguration](./Remove-AzApplicationGatewayPrivateLinkConfiguration.md)

[Set-AzApplicationGatewayPrivateLinkConfiguration](./Set-AzApplicationGatewayPrivateLinkConfiguration.md)
