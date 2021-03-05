---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3efb6270-f908-4734-bdb1-6c7e4e4eb382
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 6561037b9174fd732d616f425324c164529e6367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967818"
---
# Get-AzExpressRouteCrossConnection

## SYNOPSIS
Pobiera połączenie krzyżowe usługi Azure ExpressRoute z platformy Azure.

## SKŁADNIA

```
Get-AzExpressRouteCrossConnection [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzExpressRouteCrossConnection** służy do pobierania obiektu połączenia krzyżowego usługi ExpressRoute z subskrypcji.
AzureRmExpressRouteCrossConnection

## PRZYKŁADY

### Przykład 1. Uzyskiwanie połączenia krzyżowego expressRoute
```
Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
```

### Przykład 2. Lista połączeń krzyżowych usługi ExpressRoute przy użyciu filtru
```
Get-AzExpressRouteCrossConnection -Name test*
```

To polecenie cmdlet spowoduje listę wszystkich połączeń krzyżowych expressRoute, które zaczynają się od "testu".

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

### — Nazwa
Nazwa połączenia krzyżowego expressRoute.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -ResourceGroupName
Nazwa grupy zasobów zawierającej połączenie krzyżowe expressRoute.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Brak
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection

## NOTATKI

## LINKI POKREWNE

[Set-AzExpressRouteCrossConnection](Set-AzExpressRouteCrossConnection.md)