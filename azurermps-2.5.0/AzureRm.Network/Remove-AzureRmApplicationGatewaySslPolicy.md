---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A308E4DD-49FA-4905-94A7-CEA3AAEC3959
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewaysslpolicy
schema: 2.0.0
ms.openlocfilehash: 383ad627ff7a633d508daccde70e3de395e4ad57
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897897"
---
# Remove-AzureRmApplicationGatewaySslPolicy

## STRESZCZENIe
Usuwa zasady SSL z bramy aplikacji platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway <PSApplicationGateway> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Remove-AzureRmApplicationGatewaySslPolicy usuwa zasady SSL z bramy aplikacji platformy Azure.

## Przykłady

### Przykład 1: usuwanie zasad SSL z bramy aplikacji
```
PS C:\>$AppGW = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGW = Remove-AzureRmApplicationGatewaySslPolicy -ApplicationGateway $AppGW
```

To polecenie usuwa zasady SSL z bramy Application Gateway o nazwie ApplicationGateway01.

## PARAMETRÓW

### -ApplicationGateway
Określa bramę aplikacji, z której to polecenie cmdlet usuwa zasady SSL.

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

### -Force
Nie pytaj o potwierdzenie.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

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

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSApplicationGateway

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking

## LINKI POKREWNE

[Set-AzureRmApplicationGatewaySslPolicy](./Set-AzureRmApplicationGatewaySslPolicy.md)

[Nowe — AzureRmApplicationGatewaySslPolicy](./New-AzureRmApplicationGatewaySslPolicy.md)

[Get-AzureRmApplicationGatewaySslPolicy](./Get-AzureRmApplicationGatewaySslPolicy.md)

