---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: abaaaf7d9f430bd1b7850f3141b651ac02821257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527846"
---
# Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript

## STRESZCZENIe
Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN. Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Ta unifiedgroup pobiera zasób połączenia, markę urządzenia sieci VPN, model, wersję oprogramowania układowego i zwraca odpowiedni skrypt konfiguracyjny, który klienci mogą stosować bezpośrednio na swoich lokalnych urządzeniach sieci VPN. Skrypt będzie śledzić składnię wybranego urządzenia i wprowadzić wymagane parametry, takie jak publiczne adresy IP bramy platformy Azure, prefiksy adresów sieci wirtualnej, klucz wstępny tunelu VPN itd., aby klienci mogli po prostu kopiować do swoich konfiguracji urządzeń VPN.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

W powyższym przykładzie użyto Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice, aby uzyskać obsługiwane marki, modele i wersje oprogramowania wewnętrznego urządzenia sieci VPN.
Następnie używa jednej ze zwróconych informacji o modelach w celu wygenerowania skryptu konfiguracji urządzenia sieci VPN dla VirtualNetworkGatewayConnection "TestConnection". Urządzenie używane w tym przykładzie ma DeviceFamily "IOS-test", DeviceVendor "Cisco-test" i FirmwareVersion 20.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceFamily
Nazwa modelu/rodziny urządzenia sieci VPN.

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

### -DeviceVendor
Nazwa dostawcy urządzenia sieci VPN.

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

### -FirmwareVersion
Wersja oprogramowania układowego urządzenia sieci VPN.

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

### -Name (nazwa)
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE
