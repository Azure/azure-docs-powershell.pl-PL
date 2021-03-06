---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteportslocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePortsLocation.md
ms.openlocfilehash: 918ef18717cb09bad28ee10b91f635181dd5b3cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189786"
---
# Get-AzExpressRoutePortsLocation

## SYNOPSIS
Pobiera lokalizacje, w których są dostępne zasoby usługi ExpressRoutePort.

## SKŁADNIA

```
Get-AzExpressRoutePortsLocation [-LocationName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzExpressRoutePortsLocation** służy do pobierania lokalizacji, w których są dostępne zasoby usługi ExpressRoutePort. Gdy jako dane wejściowe jest podana konkletna lokalizacja, polecenie cmdlet wyświetla szczegóły tej lokalizacji, czyli listę dostępnych przepustowości w tej lokalizacji.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzExpressRoutePortsLocation
```

Lista lokalizacji, w których są dostępne zasoby usługi ExpressRoutePort.

### Przykład 2
```powershell
PS C:\> Get-AzExpressRoutePortsLocation -LocationName $loc
```

Zawiera informacje o przepustowości usługi ExpressRoutePort dostępnej w lokalizacji $loc.

## PARAMETERS

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Network.Models.PSExpressRoutePortsLocation

## NOTATKI

## LINKI POKREWNE
