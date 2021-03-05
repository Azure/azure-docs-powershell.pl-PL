---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 1dac991645d6f57ba4fe30a82955531b7fdb3f5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987267"
---
# Remove-AzTrafficManagerEndpointConfig

## SYNOPSIS
Usuwa punkt końcowy z obiektu profilu lokalnego menedżera ruchu.

## SKŁADNIA

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzTrafficManagerEndpointConfig** usuwa punkt końcowy z lokalnego obiektu profilu usługi Azure Traffic Manager.
Profil możesz uzyskać za pomocą polecenia cmdlet Get-AzTrafficManagerProfile cmdlet.

To polecenie cmdlet działa na lokalnym obiekcie profilu.
Zatwierdzanie zmian w profilu menedżera ruchu za pomocą Set-AzTrafficManagerProfile cmdlet.
Aby usunąć punkt końcowy i zatwierdzić zmiany w jednej operacji, użyj Remove-AzTrafficManagerEndpoint cmdlet.

## PRZYKŁADY

### Przykład 1. Usuwanie punktu końcowego
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Pierwsze polecenie otrzymuje profil usługi Azure Traffic Manager za pomocą polecenia cmdlet **Get-AzTrafficManagerProfile.**
Polecenie przechowuje profil lokalny w $TrafficManagerProfile zmienną.

Drugie polecenie usuwa punkt końcowy platformy Azure o nazwie contoso z profilu przechowywanego w usłudze $TrafficManagerProfile.
To polecenie zmienia tylko obiekt lokalny.

Ostatnie polecenie aktualizuje profil menedżera ruchu o nazwie ContosoProfile, aby dopasować go do wartości lokalnej w $TrafficManagerProfile.

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

### -EndpointName
Określa nazwę punktu końcowego menedżera ruchu, który usuwa to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
Określa lokalny obiekt **TrafficManagerProfile.**
To polecenie cmdlet modyfikuje ten obiekt lokalny.
Aby uzyskać obiekt **TrafficManagerProfile,** użyj Get-AzTrafficManagerProfile cmdlet.

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

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


