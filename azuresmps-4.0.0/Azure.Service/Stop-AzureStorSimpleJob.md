---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A1E143A8-70F2-4158-9A10-F2082AD62A73
online version: ''
schema: 2.0.0
ms.openlocfilehash: 371291f4bd33809bc2f5880e4380c448219ed37a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054978"
---
# Stop-AzureStorSimpleJob

## STRESZCZENIe
Zatrzymuje zadanie programu StorSimple.

## POLECENIA

```
Stop-AzureStorSimpleJob -InstanceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **stop-AzureStorSimpleJob** zatrzymuje bieżące zadanie StorSimple.
Możesz określić zadania, podając identyfikator wystąpienia lub nazwę zadania.

## Przykłady

### Przykład 1: zatrzymywanie zadań dla urządzenia
```
PS C:\>Get-AzureStorSimpleJob -DeviceName "Device07" | Stop-AzureStorSimpleJob -Force
```

To polecenie pobiera zadania dla urządzenia o nazwie Device07 przy użyciu polecenia cmdlet **Get-AzureStorSimpleJob** .
Polecenie przekazuje zadania do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet zatrzymuje wszystkie zadania przekazywane do tego polecenia.
Polecenie określa parametr *Force* , a więc nie monituje o potwierdzenie przed zatrzymaniem zadania.

### Przykład 2: zatrzymywanie określonego zadania
```
PS C:\>Stop-AzureStorSimpleJob -InstanceId "574f47e0-44e9-495c-b8a5-0203c57ebf6d" -Force
```

To polecenie zatrzymuje zadanie o określonym IDENTYFIKATORze wystąpienia.

## PARAMETRÓW

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

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

### -InstanceId
Określa identyfikator zadania urządzenia, które ma zostać zatrzymane.

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
Określa Profil platformy Azure.

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

### Znaleziono

## WYSYŁA

### DeviceJobDetails
To polecenie cmdlet pobiera szczegóły **DeviceJob** , które zostanie zatrzymane przez to polecenie cmdlet.

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


