---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 974e30d9a287d18293515c019b0032bf36f15b51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184138"
---
# Start-AzApplicationGateway

## SYNOPSIS
Pozwala na rozpoczęcie pracy z bramą aplikacji.

## SKŁADNIA

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Start-AzApplicationGateway** umożliwia uruchomienie bramy aplikacji platformy Azure

## PRZYKŁADY

### Przykład1. Uruchamianie bramy aplikacji
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

To polecenie uruchamia bramę aplikacji przechowywaną w $AppGw aplikacji.

## PARAMETERS

### - ApplicationGateway
Określa bramę aplikacji uruchamianą przez to polecenie cmdlet.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSApplicationGateway

## NOTATKI

## LINKI POKREWNE

[Stop-AzApplicationGateway](./Stop-AzApplicationGateway.md)


