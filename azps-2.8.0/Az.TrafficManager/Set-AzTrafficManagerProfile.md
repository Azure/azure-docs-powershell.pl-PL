---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888474"
---
# Set-AzTrafficManagerProfile

## STRESZCZENIe
Aktualizuje profil w usłudze Traffic Manager.

## POLECENIA

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzTrafficManagerProfile** aktualizuje profil usługi Azure Traffic Manager.
To polecenie cmdlet umożliwia zaktualizowanie ustawień profilu z obiektu profilu lokalnego.
Obiekt profile można określić przy użyciu parametru *TrafficManagerProfile* lub za pomocą potoku.

Obiekt lokalny przedstawiający profil można uzyskać przy użyciu Get-AzTrafficManagerProfile polecenia cmdlet.
Zmodyfikuj obiekt lokalnie, a następnie użyj **Ustawienia Set-AzTrafficManagerProfile** w celu zatwierdzenia zmian.

## Przykłady

### Przykład 1: aktualizowanie profilu
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

Pierwsze polecenie pobiera profil usługi Azure Traffic Manager przy użyciu polecenia cmdlet Get-AzTrafficManagerProfile.
Polecenie zapisuje profil lokalnie w zmiennej $TrafficManagerProfile.

Drugie polecenie powoduje zmianę lokalnego profilu.
To polecenie wyłącza profil.

Trzecie polecenie aktualizuje profil usługi Traffic Manager o nazwie ContosoProfile, aby odpowiadał wartości lokalnej w $TrafficManagerProfile.

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

### -TrafficManagerProfile
Określa lokalny obiekt **TrafficManagerProfile** .
To polecenie cmdlet umożliwia zaktualizowanie Menedżera ruchu w celu dopasowania go do tego obiektu lokalnego.

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

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile

## WYSYŁA

### Microsoft. Azure. Commands. Trafficmanager. modele. TrafficManagerProfile

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[Get-AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[Nowe — AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[Remove-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[Remove-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)


