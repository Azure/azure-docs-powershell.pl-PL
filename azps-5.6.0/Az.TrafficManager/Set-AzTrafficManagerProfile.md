---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: 4a4d09fb0e44dcb09781b2155e1bfe2d10a0cc80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987211"
---
# Set-AzTrafficManagerProfile

## SYNOPSIS
Aktualizuje profil Menedżera ruchu.

## SKŁADNIA

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzTrafficManagerProfile** aktualizuje profil usługi Azure Traffic Manager.
To polecenie cmdlet aktualizuje ustawienia profilu z lokalnego obiektu profilu.
Obiekt profilu można określić za pomocą parametru *TrafficManagerProfile* lub potoku.

Obiekt lokalny reprezentujący profil można uzyskać za pomocą Get-AzTrafficManagerProfile cmdlet.
Zmodyfikuj obiekt lokalnie, a następnie **użyj set-azTrafficManagerProfile,** aby zatwierdzić zmiany.

## PRZYKŁADY

### Przykład 1. Aktualizowanie profilu
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager przy użyciu Get-AzTrafficManagerProfile cmdlet.
Polecenie przechowuje profil lokalnie w $TrafficManagerProfile zmienną.

Drugie polecenie zmienia profil lokalnie.
To polecenie wyłącza profil.

Trzecie polecenie aktualizuje profil menedżera ruchu o nazwie ContosoProfile zgodnie z wartością lokalną w $TrafficManagerProfile.

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

### -TrafficManagerProfile
Określa lokalny obiekt **TrafficManagerProfile.**
To polecenie cmdlet aktualizuje Menedżera ruchu w celu dopasowania tego obiektu lokalnego.

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
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

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile

## NOTATKI

## LINKI POKREWNE

[Add-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[New-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)


