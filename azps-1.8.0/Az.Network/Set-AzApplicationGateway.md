---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 34f3de9e2dafe3cfb9b15aad1dda7d75bab67c20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709039"
---
# Set-AzApplicationGateway

## STRESZCZENIe
Umożliwia zaktualizowanie bramy aplikacji.

## POLECENIA

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzApplicationGateway** umożliwia zaktualizowanie bramy aplikacji platformy Azure.

## Przykłady

### Przykład 1: aktualizowanie bramy aplikacji
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

To polecenie aktualizuje bramę aplikacji za pomocą ustawień w zmiennej $AppGw i przechowuje zaktualizowaną bramę w zmiennej $UpdatedAppGw.

## PARAMETRÓW

### -ApplicationGateway
Określa obiekt bramy aplikacji reprezentujący stan, w którym należy ustawić bramę aplikacji.

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AsJob
Uruchom polecenie cmdlet w tle

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

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSApplicationGateway

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSApplicationGateway

## INFORMACYJN

## LINKI POKREWNE

[Start — AzApplicationGateway](./Start-AzApplicationGateway.md)


