---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8E12A392-A100-4814-9003-B2999150DCE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: 3468730caa727c7c8cde46ddbf431c374361b8fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525925"
---
# Remove-AzureRmTrafficManagerEndpointConfig

## STRESZCZENIe
Usuwa punkt końcowy z obiektu profilu lokalnego zarządzania ruchem.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmTrafficManagerEndpointConfig -EndpointName <String>
 -TrafficManagerProfile <TrafficManagerProfile> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmTrafficManagerEndpointConfig** umożliwia usunięcie punktu końcowego z obiektu profilu lokalnego usługi Azure Endpoint Manager.
Możesz uzyskać profil przy użyciu Get-AzureRmTrafficManagerProfile polecenia cmdlet.

To polecenie cmdlet działa na obiekcie profilu lokalnego.
Zatwierdź zmiany w profilu dla Menedżera ruchu, korzystając z polecenia cmdlet Set-AzureRmTrafficManagerProfile.
Aby usunąć punkt końcowy i przekazać zmiany w ramach jednej operacji, użyj polecenia cmdlet Remove-AzureRmTrafficManagerEndpoint.

## Przykłady

### Przykład 1: Usuwanie punktu końcowego
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Remove-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -TrafficManagerProfile $TrafficManagerProfile 
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet **Get-AzureRmTrafficManagerProfile** .
Polecenie zapisuje profil lokalny w zmiennej $TrafficManagerProfile.

Drugie polecenie usuwa punkt końcowy Azure o nazwie contoso z profilu przechowywanego w $TrafficManagerProfile.
To polecenie powoduje zmianę tylko obiektu lokalnego.

Ostatnie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.

## PARAMETRÓW

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
Aby uzyskać obiekt **TrafficManagerProfile** , użyj polecenia cmdlet Get-AzureRmTrafficManagerProfile.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
To polecenie cmdlet akceptuje obiekt **TrafficManagerProfile** do tego polecenia cmdlet.

## WYSYŁA

### Microsoft. Azure. Commands. Network. TrafficManagerProfile
To polecenie cmdlet zwraca zmodyfikowany obiekt TrafficManagerProfile.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureRmTrafficManagerEndpointConfig](./Add-AzureRmTrafficManagerEndpointConfig.md)

[Get-AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[Remove-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


