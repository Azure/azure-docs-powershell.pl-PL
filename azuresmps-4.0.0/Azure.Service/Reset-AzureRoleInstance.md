---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054446"
---
# Reset-AzureRoleInstance

## STRESZCZENIe
Żąda ponownego uruchomienia lub odobrazowania pojedynczego wystąpienia roli lub wszystkich wystąpień ról określonej roli.

## POLECENIA

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Reseting-AzureRoleInstance** żąda ponownego uruchomienia lub ponownego obrazu wystąpienia roli uruchomionego we wdrożeniu.
Ta operacja jest wykonywana synchronicznie.
Po ponownym uruchomieniu wystąpienia roli usługa Azure przejmuje wystąpienie w trybie offline, ponownie uruchamia system operacyjny dla tego wystąpienia i przełącza wystąpienie z powrotem do trybu online.
Wszystkie dane zapisywane na dysku lokalnym są zachowywane po ponownym uruchomieniu komputera.
Wszystkie dane, które są w pamięci, zostaną utracone.

Przetworzenie obrazów wystąpienia roli powoduje różne zachowanie w zależności od typu roli.
W przypadku roli sieci Web lub procesu roboczego po zakończeniu działania tej roli usługa Azure przełącza tę rolę do trybu offline i zapisuje nową instalację systemu operacyjnego gościa platformy Azure na maszynie wirtualnej.
Następnie rola jest przywracana w trybie online.
W przypadku roli maszyny wirtualnej, gdy rola zostanie ponownie utworzona, usługa Azure przełączy tę rolę w tryb offline, ponownie zastosuje obraz niestandardowy, który został przez Ciebie dostarczony, oraz przywraca tę rolę w trybie online.

Usługa Azure próbuje zachować dane w zasobach magazynu lokalnego, gdy rola zostanie przechowana. Jednak w przypadku przejściowego błędu sprzętowego zasób lokalnego magazynu może zostać utracony.
Jeśli aplikacja wymaga zachowywania danych, zalecane jest zapisywanie do trwałego źródła danych, takiego jak dysk Azure.
Wszystkie dane, które są zapisywane w katalogu lokalnym innym niż zdefiniowany przez zasób lokalnego magazynu, zostaną utracone po przekroczeniu roli.

## Przykłady

### Przykład 1: Ponowna rozruch wystąpienia roli
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

To polecenie powoduje ponowne uruchomienie wystąpienia roli o nazwie MyWebRole_IN_0 w rozmieszczeniu przemieszczania usługi MySvc01.

### Przykład 2: rezdjęcie wystąpienia roli
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

To polecenie powoduje ponowne zdjęcie wystąpień roli w ramach przemieszczania usługi w chmurze MySvc01.

### Przykład 3: odobrazowanie wszystkich wystąpień ról
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

To polecenie powoduje ponowne zdjęcie wszystkich wystąpień ról we wdrożeniu produkcji usługi MySvc01.

## PARAMETRÓW

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceName
Określa nazwę wystąpienia roli, które ma być ponownie podobrazem lub ponownym uruchomieniem.

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

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

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

### -Ponowne uruchamianie
Określa, że to polecenie cmdlet powoduje ponowne uruchomienie określonego wystąpienia roli lub, jeśli nie jest określone, wszystkie wystąpienia ról.
Musisz dodać parametr *ponownego rozruchu* lub ponownie *obrazu* , ale nie oba.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Reimage
Określa, że to polecenie cmdlet odnosi się do określonego wystąpienia roli lub jeśli nie określono żadnego wystąpienia roli.
Musisz dodać parametr *ponownego rozruchu* lub ponownie *obrazu* , ale nie oba.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Określa nazwę usługi.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
Określa środowisko wdrażania, w którym są uruchamiane wystąpienia roli.
Prawidłowe wartości: produkcja i przemieszczanie.
Możesz dodać parametr *deploymentname* lub *slot* , ale nie oba.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRole](./Set-AzureRole.md)


