---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184643"
---
# Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## SYNOPSIS
To polecenie commandlet pobiera zasoby połączeń, markę urządzenia VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracji, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach VPN. Skrypt będzie postępować zgodnie ze składnią wybranego urządzenia i wypełnij niezbędne parametry, takie jak publiczne adresy IP bramy Azure, prefiksy wirtualnych adresów sieciowych, wstępnie udostępniony klucz podpowiązków VPN, itd., aby klienci mogą po prostu kopiować-wklejać do swoich konfiguracji urządzeń VPN.

## SKŁADNIA

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
To polecenie commandlet pobiera zasoby połączeń, markę urządzenia VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracji, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach VPN. Skrypt będzie postępować zgodnie ze składnią wybranego urządzenia i wypełnij niezbędne parametry, takie jak publiczne adresy IP bramy Azure, prefiksy wirtualnych adresów sieciowych, wstępnie udostępniony klucz podpowiązków VPN, itd., aby klienci mogą po prostu kopiować-wklejać do swoich konfiguracji urządzeń VPN.

## PRZYKŁADY

### Przykład 1
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

W powyższym przykładzie Get-AzVirtualNetworkGatewaySupportedVpnDevice do uzyskania obsługiwanych marek urządzeń VPN, modeli i wersji oprogramowania układowego.
Następnie używa jednego z zwracanych modeli w celu wygenerowania skryptu konfiguracji urządzenia VPN dla funkcji VirtualNetworkGatewayConnection "TestConnection". Urządzenie użyte w tym przykładzie ma deviceFamily "IOS-Test", DeviceVendor "Cisco-Test" i FirmwareVersion 20.

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

### — DeviceFamily
Nazwa modelu/rodziny urządzeń VPN.

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

### - DeviceVendor
Nazwa dostawcy urządzenia SIECI VPN.

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

### - FirmwareVersion
Wersja oprogramowania układowego urządzenia VPN.

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

### — Nazwa
Nazwa zasobu połączenia, dla którego ma zostać wygenerowana konfiguracja.

```yaml
Type: System.String
Parameter Sets: (All)
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
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### System.String

## NOTATKI

## LINKI POKREWNE
