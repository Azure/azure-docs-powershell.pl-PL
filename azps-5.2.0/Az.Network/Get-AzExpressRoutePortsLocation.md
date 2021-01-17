---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337786"
---
# Get-AzExpressRoutePortsLocation

## STRESZCZENIe
Pobiera lokalizacje, w których ExpressRoutePort są dostępne zasoby.

## POLECENIA

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzExpressRoutePortsLocation** służy do pobierania lokalizacji, w których zasoby ExpressRoutePort są dostępne. W przypadku konkretnych lokalizacji jako danych wejściowych polecenie cmdlet wyświetla szczegóły tej lokalizacji, czyli listę dostępnych przepustowości w tej lokalizacji.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Wyświetla listę lokalizacji, w których ExpressRoutePort są dostępne zasoby.

### Przykład 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

Wyświetla listę dostępnych ExpressRoutePortych przepustowości w lokalizacji $loc.

## PARAMETRÓW

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

### -LocationName
Nazwa lokalizacji.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Network. models. PSExpressRoutePortsLocation

## INFORMACYJN

## LINKI POKREWNE
