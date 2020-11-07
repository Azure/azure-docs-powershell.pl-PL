---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePortsLocation.md
ms.openlocfilehash: 5d077991e42da0709019df1dccdd83f03659ca49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719092"
---
# Get-AzureRmExpressRoutePortsLocation

## STRESZCZENIe
Pobiera lokalizacje, w których ExpressRoutePort są dostępne zasoby.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmExpressRoutePortsLocation** służy do pobierania lokalizacji, w których zasoby ExpressRoutePort są dostępne. W przypadku konkretnych lokalizacji jako danych wejściowych polecenie cmdlet wyświetla szczegóły tej lokalizacji, czyli listę dostępnych przepustowości w tej lokalizacji.


## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation
```

Wyświetla listę lokalizacji, w których ExpressRoutePort są dostępne zasoby.

### Przykład 2
```powershell
PS C:\> Get-AzureRmExpressRoutePortsLocation -LocationName $loc
```

Wyświetla listę dostępnych ExpressRoutePortych przepustowości w lokalizacji $loc.

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

### -LocationName
Nazwa lokalizacji.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSExpressRoutePortsLocation

## INFORMACYJN

## LINKI POKREWNE
