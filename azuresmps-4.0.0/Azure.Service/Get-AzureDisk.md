---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055320"
---
# Get-AzureDisk

## STRESZCZENIe
Pobiera informacje o dyskach w repozytorium dysków Azure.

## POLECENIA

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureDisk** pobiera informacje o dyskach przechowywanych w repozytorium dysków Azure na potrzeby bieżącej subskrypcji.
To polecenie cmdlet zwraca listę informacji dla wszystkich dysków w repozytorium.
Aby wyświetlić informacje dotyczące określonego dysku, określ nazwę dysku.

## Przykłady

### Przykład 1: uzyskiwanie informacji o dysku
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

To polecenie pobiera dane dotyczące dysku o nazwie ContosoDataDisk z repozytorium dysków.

### Przykład 2: uzyskiwanie informacji o wszystkich dyskach
```
PS C:\> Get-AzureDisk
```

To polecenie pobiera informacje o wszystkich dyskach w repozytorium dysków.

### Przykład 3: uzyskiwanie informacji o dysku
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

To polecenie pobiera dane dla wszystkich dysków w repozytorium dysków, które nie są obecnie dołączone do maszyny wirtualnej.
Polecenie pobiera informacje o wszystkich dyskach i przekazuje poszczególne obiekty do polecenia cmdlet **WHERE-Object** .
Polecenie cmdlet powoduje porzucanie wszystkich dysków, które nie mają wartości $Null dla właściwości **AttachedTo** .
Polecenie umożliwia sformatowanie listy jako tabeli przy użyciu polecenia cmdlet **formatowanie tabeli** .

## PARAMETRÓW

### -Diskname
Określa nazwę dysku w repozytorium dysków, w którym ten aplet polecenia pobiera informacje.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureDisk](./Add-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


