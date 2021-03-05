---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 5287D4DB-2709-4A3C-97D5-DB494CEEFD18
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 8f8ba0297ac0302e50dfdfdc25ddc3941fb10e34
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987239"
---
# Set-AzTrafficManagerEndpoint

## SYNOPSIS
Aktualizuje punkt końcowy Menedżera ruchu.

## SKŁADNIA

```
Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzTrafficManagerEndpoint** aktualizuje punkt końcowy w usłudze Azure Traffic Manager.
To polecenie cmdlet aktualizuje ustawienia z lokalnego obiektu punktu końcowego.
Obiekt punktu końcowego można określić za pomocą *parametru TrafficManagerEndpoint* lub potoku.

Za pomocą polecenia cmdlet można uzyskać obiekt lokalny reprezentujący punkt Get-AzTrafficManagerEndpoint cmdlet.
Zmodyfikuj obiekt lokalnie, a następnie **użyj ustawienia Set-AzTrafficManagerEndpoint,** aby zatwierdzić zmiany.

## PRZYKŁADY

### Przykład 1. Aktualizowanie punktu końcowego
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "endpoint1" -Type AzureEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> $TrafficManagerEndpoint.Weight = 20
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

Pierwsze polecenie uzyskuje punkt końcowy usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerEndpoint.**
Polecenie przechowuje punkt końcowy lokalnie w $TrafficManagerEndpoint zmienną.

Drugie polecenie zmienia ten punkt końcowy lokalnie.
To polecenie zmienia wagę punktu końcowego na 20.

Trzecie polecenie aktualizuje punkt końcowy w Menedżerze ruchu, aby dopasować wartość lokalną w $TrafficManagerEndpoint.

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

### -TrafficManagerEndpoint
Określa lokalny obiekt **TrafficManagerEndpoint.**
To polecenie cmdlet aktualizuje Menedżera ruchu w celu dopasowania tego obiektu lokalnego.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint

## NOTATKI

## LINKI POKREWNE
