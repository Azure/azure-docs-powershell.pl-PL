---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055341"
---
# Enable-AzureTrafficManagerProfile

## STRESZCZENIe
Włącza profil w usłudze Traffic Manager.

## POLECENIA

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **enable-AzureTrafficManagerProfile** umożliwia profilowi Microsoft Azure Traffic Manager.
Określ parametr *PassThru* , aby wyświetlić, czy operacja powiodła się.

## Przykłady

### Przykład 1: Włączanie profilu w usłudze Traffic Manager
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

To polecenie włącza profil usługi Traffic Manager o nazwie Moja profil.

### Przykład 2: Włączanie profilu usługi Traffic Manager i wyświetlanie wyników
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

To polecenie umożliwia włączenie profilu usługi Traffic Manager o nazwie Moja profil i wyświetlenie tego, czy polecenie zostało pomyślnie zakończone.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę profilu usługi Traffic Manager, który ma zostać włączony.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca $True, jeśli operacja zakończyła się pomyślnie; w przeciwnym razie $False.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

```yaml
Type: SwitchParameter
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

### System. Boolean
To polecenie cmdlet generuje $True lub $False.
Jeśli operacja powiedzie się i określisz parametr *PassThru* , to polecenie cmdlet zwróci wartość $true.

## INFORMACYJN

## LINKI POKREWNE

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Nowe — AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


