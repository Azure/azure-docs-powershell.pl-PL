---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 4795e89013acaadcc08477370441ff5acdded85a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051231"
---
# Remove-AzTrafficManagerEndpointConfig

## STRESZCZENIe
Usuwa punkt końcowy z obiektu profilu lokalnego zarządzania ruchem.

## POLECENIA

```
Remove-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzTrafficManagerEndpointConfig** umożliwia usunięcie punktu końcowego z obiektu profilu lokalnego usługi Azure Endpoint Manager.
Możesz uzyskać profil przy użyciu Get-AzTrafficManagerProfile polecenia cmdlet.

To polecenie cmdlet działa na obiekcie profilu lokalnego.
Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzTrafficManagerProfile.
Aby usunąć punkt końcowy i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzTrafficManagerEndpoint.

## Przykłady

### Przykład 1: Usuwanie punktu końcowego
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzTrafficManagerProfile** .
Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.

Drugie polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu przechowywanego w $TrafficManagerProfile.
To polecenie powoduje zmianę tylko obiektu lokalnego.

Ostatnie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.

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

### -EndpointName
Określa nazwę punktu końcowego usługi Traffic Managera, który jest usuwany przez to polecenie cmdlet.

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
Określa lokalny obiekt **TrafficManagerProfile** .
To polecenie cmdlet modyfikuje ten obiekt lokalny.
Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzTrafficManagerProfile.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile

## WYSYŁA

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpoint](./Remove-AzTrafficManagerEndpoint.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


