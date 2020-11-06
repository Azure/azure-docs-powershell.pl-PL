---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistenercustomerror
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListenerCustomError.md
ms.openlocfilehash: d0f26991498d8efc88eaacf9d01ed7e95d92e2cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527833"
---
# Remove-AzureRmApplicationGatewayHttpListenerCustomError

## STRESZCZENIe
Usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmApplicationGatewayHttpListenerCustomError -StatusCode <String>
 -HttpListener <PSApplicationGatewayHttpListener> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmApplicationGatewayCustomError** usuwa błąd niestandardowy z odbiornika http bramy Application Gateway.

## Przykłady

### Przykład 1. usuwa błąd niestandardowy z odbiornika http
```powershell
PS C:\> $updatedlistener = Remove-AzureRmApplicationGatewayCustomError -HttpListener $listener01 -StatusCode HttpStatus502
```

To polecenie powoduje usunięcie niestandardowego błędu kodu stanu HTTP 502 z odbiornika http $listener 01 i zwrócenie zaktualizowanego odbiornika.

## PARAMETRÓW

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

### -HttpListener
Odbiornik http bramy Application Gateway

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusCode
Kod stanu błędu klienta bramy aplikacji.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.
Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener

## INFORMACYJN

## LINKI POKREWNE
