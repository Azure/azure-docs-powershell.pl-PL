---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 706C918B-1D1A-476C-BB74-EBB4EE72AC0C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayAuthenticationCertificate.md
ms.openlocfilehash: 846cdf57e78ca1d3bacb7673d23fd16d460e4400
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527477"
---
# Get-AzureRmApplicationGatewayAuthenticationCertificate

## STRESZCZENIe
Pobiera certyfikat uwierzytelniania dla bramy aplikacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmApplicationGatewayAuthenticationCertificate [-Name <String>]
 -ApplicationGateway <PSApplicationGateway> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmApplicationGatewayAuthenticationCertificate** pobiera certyfikat uwierzytelniania dla bramy aplikacji platformy Azure.

## Przykłady

## PARAMETRÓW

### -ApplicationGateway
Określa nazwę bramy aplikacji, dla której to polecenie cmdlet pobiera certyfikat uwierzytelniania.

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

### -Name (nazwa)
Określa nazwę certyfikatu uwierzytelniania, który ma być pobierany przez to polecenie cmdlet.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft. Azure. Commands. Network. models. PSApplicationGatewayAuthenticationCertificate

## INFORMACYJN
* Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking

## LINKI POKREWNE

[Dodaj-AzureRmApplicationGatewayAuthenticationCertificate](./Add-AzureRmApplicationGatewayAuthenticationCertificate.md)

[Nowe — AzureRmApplicationGatewayAuthenticationCertificate](./New-AzureRmApplicationGatewayAuthenticationCertificate.md)

[Remove-AzureRmApplicationGatewayAuthenticationCertificate](./Remove-AzureRmApplicationGatewayAuthenticationCertificate.md)

[Set-AzureRmApplicationGatewayAuthenticationCertificate](./Set-AzureRmApplicationGatewayAuthenticationCertificate.md)


