---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 28136DC3-520B-4134-8736-93D86EEABAE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: bf9fd7b67b63ce2bddb762c7006722b6035ffe87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054502"
---
# Get-AzureTrafficManagerProfile

## STRESZCZENIe
Pobiera szczegóły profilu usługi Traffic Manager.

## POLECENIA

```
Get-AzureTrafficManagerProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureTrafficManagerProfile** pobiera szczegóły profilu Microsoft Azure Traffic Manager.
Jeśli parametr *name* nie jest określony, polecenie cmdlet wyświetla listę profilów usługi Traffic managera w bieżącej subskrypcji.

## Przykłady

### Przykład 1: uzyskiwanie listy profilów usługi Traffic managera w ramach abonamentu
```
PS C:\>Get-AzureTrafficManagerProfile
```

To polecenie pobiera listę profilów usługi Traffic managera w ramach abonamentu.

### Przykład 2: uzyskiwanie profilu w usłudze Traffic Manager
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile"
```

To polecenie pobiera profil usługi Traffic Manager o nazwie Moja profil.

### Przykład 3: Dodawanie punktu końcowego do profilu usługi Traffic Manager
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Add-AzureTrafficManagerEndpoint -DomainName "Myapp2.cloudapp.net" -TrafficManagerProfile $MyTrafficManagerProfile -Type "CloudService" -Status "Enabled" | Set-AzureTrafficManagerProfile
```

To polecenie dodaje punkt końcowy do profilu usługi Traffic Manager, a następnie zapisuje profil.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę profilu usługi Traffic Manager, który ma zostać wyświetlony.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet. Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Utilities.. modele. IProfileWithDefinition
To polecenie cmdlet generuje obiekt lub obiekty profilu Menedżera ruchu.

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureTrafficManagerEndpoint](./Add-AzureTrafficManagerEndpoint.md)

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Nowe — AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


