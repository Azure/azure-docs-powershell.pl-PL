---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 39ce61f4a1e973dfdac8104a6364bdd3d8b9151a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899095"
---
# Remove-AzureRmApplicationGatewayProbeConfig

## STRESZCZENIe
Usuwa badanie kondycji z istniejącej bramy aplikacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Remove-AzureRmApplicationGatewayProbeConfig usuwa z istniejącej bramy aplikacji sondę Heath.

## Przykłady

### Przykład 1: usuwanie sondy kondycji z istniejącej bramy aplikacji
```
PS C:\>$Gateway = Remove-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

To polecenie usuwa badanie kondycji o nazwie Probe04 z bramy Application Gateway o nazwie Gateway.

## PARAMETRÓW

### -ApplicationGateway
Określa bramę aplikacji, z którą to polecenie cmdlet usuwa sondę.

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
Określa nazwę sondy, dla której zostanie usunięte to polecenie cmdlet.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### PSApplicationGateway
Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSApplicationGateway

## INFORMACYJN

## LINKI POKREWNE

[Usuwanie sondy z istniejącej bramy aplikacji](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[Dodaj-AzureRmApplicationGatewayProbeConfig]()

[Get-AzureRmApplicationGatewayProbeConfig]()

[Nowe — AzureRmApplicationGatewayProbeConfig]()

[Set-AzureRmApplicationGatewayProbeConfig]()

