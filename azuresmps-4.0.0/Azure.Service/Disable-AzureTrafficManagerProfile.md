---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054659"
---
# Disable-AzureTrafficManagerProfile

## STRESZCZENIe
Wyłącza profil w usłudze Traffic Manager.

## POLECENIA

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **disable-AzureTrafficManagerProfile** wyłącza profil usługi Microsoft Azure Traffic Manager.
Za pomocą parametru *PassThru* można wyświetlać, czy operacja kończy się powodzeniem.

## Przykłady

### Przykład 1: wyłączenie profilu usługi Traffic Manager i wyświetlenie wyników
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

To polecenie wyłącza profil usługi Traffic Manager o nazwie Moja profil.
To polecenie określa parametr *PassThru* , który ma być wyświetlany, gdy polecenie zostało pomyślnie zakończone.

### Przykład 2: wyłączenie profilu w usłudze Traffic Manager i wyświetlenie brakujących wyników
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

To polecenie wyłącza profil usługi Traffic Manager o nazwie Moja profil, ale nie wyświetla tego, czy polecenie zostało pomyślnie zakończone.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę profilu usługi Traffic Manager, który ma zostać wyłączony.

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
Jeśli operacja kończy się powodzeniem, a jeśli określisz parametr *PassThru* , to polecenie cmdlet zwróci wartość $true.

## INFORMACYJN

## LINKI POKREWNE

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[Nowe — AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


