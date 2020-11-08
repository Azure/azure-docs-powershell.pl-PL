---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054518"
---
# Get-AzureStorSimpleTask

## STRESZCZENIe
Pobiera stan zadania na urządzeniu StorSimple.

## POLECENIA

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleTask** Pobiera stan zadania, które jest uruchamiane asynchronicznie na urządzeniu usługi Azure StorSimple.

Gdy zarządzasz urządzeniem StorSimple, większość akcji tworzenia, czytania, aktualizowania i usuwania może być wykonywany asynchronicznie.
Program Windows PowerShell zwraca wartość **TaskID**.
Użyj identyfikatora, aby uzyskać bieżący stan zadania.

## Przykłady

### Przykład 1. Pobieranie stanu zadania
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

To polecenie uzyskuje stan zadania o określonym IDENTYFIKATORze.
Wyniki wskazują, że zadanie ma stan ukończone i wynik pozytywny.

## PARAMETRÓW

### -InstanceId
Określa identyfikator zadania, dla którego ten aplet polecenia śledzi stan.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
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

### Znaleziono

## WYSYŁA

### JobStatusInfo
To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , który zawiera następujące pola: 

- **Błąd**.
**ErrorDetails** , który zawiera **kod** i **wiadomość**.
- **TaskID**.
**String**.
Identyfikator zadania, dla którego jest zwracany stan.
- **TaskSteps**.
**IList \<TaskStep\>**.
Każdy obiekt **TaskStep** zawiera **Informacje o szczegółach** , **kodzie błędu** , **komunikacie** , **wyniku** i **stanie**.
- **Wynik**.
**TaskResult** , który zawiera ogólny wynik zadania.
Prawidłowe wartości to: niepowodzenie, udane, PartialSuccess, anulowane i nieprawidłowe.
- **Status**.
**TaskStatus** , który zawiera całkowity stan uruchomienia zadania.
Prawidłowe wartości to: w trakcie, nieprawidłowe i wykonane.
- **TaskResult**.
**TaskResult** wartość obliczona na podstawie **wyniku** i **stanu**.
Prawidłowe wartości to: niepowodzenie, powiodło się, stan, PartialSuccess, anulowane i nieprawidłowe.

## INFORMACYJN

## LINKI POKREWNE

