---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayredirectconfiguration
schema: 2.0.0
ms.openlocfilehash: 286afc05e9b7c825f183aabe7a78c965c790cb02
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899289"
---
# Get-AzureRmApplicationGatewayRedirectConfiguration

## STRESZCZENIe
Pobiera istniejącą konfigurację przekierowania od bramy aplikacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmApplicationGatewayRedirectConfiguration** pobiera istniejącą konfigurację przekierowania od bramy aplikacji.

## Przykłady

### Przykład 1
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzureRmApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 i zapisuje wynik w zmiennej o nazwie $AppGW.
Drugie polecenie pobiera konfigurację przekierowania o nazwie Redirect01 od bramy aplikacji przechowywanej w zmiennej o nazwie $AppGW.

## PARAMETRÓW

### -ApplicationGateway
ApplicationGateway

```yaml
Type: PSApplicationGateway
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

### -Name (nazwa)
Nazwa reguły rozsyłania żądań

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSApplicationGateway

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSApplicationGatewayRedirectConfiguration
System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. Network. MODELES. PSApplicationGatewayRedirectConfiguration, Microsoft. Azure. Commands, Version = 4.1.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMACYJN

## LINKI POKREWNE

