---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: A0293D80-5935-4D2C-AF11-2837FEC95760
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsJob.md
ms.openlocfilehash: 73a9325ea4f1bc45eaaf2fb81796d526c7b95fea
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705887"
---
# Get-AzDataLakeAnalyticsJob

## STRESZCZENIe
Pobiera zadanie Data Lake Analytics.

## POLECENIA

### GetAllInResourceGroupAndAccount (domyślny)
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [[-Name] <String>] [[-Submitter] <String>]
 [[-SubmittedAfter] <DateTimeOffset>] [[-SubmittedBefore] <DateTimeOffset>] [[-State] <JobState[]>]
 [[-Result] <JobResult[]>] [-Top <Int32>] [-PipelineId <Guid>] [-RecurrenceId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetBySpecificJobInformation
```
Get-AzDataLakeAnalyticsJob [-Account] <String> [-JobId] <Guid> [[-Include] <ExtendedJobData>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzDataLakeAnalyticsJob** pobiera zadanie usługi Azure Data Lake Analytics.
Jeśli nie podano zadania, to polecenie cmdlet umożliwia pobieranie wszystkich zadań.

## Przykłady

### Przykład 1: pobieranie określonego zadania
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -JobId $JobID01
```

To polecenie pobiera zadanie z określonym IDENTYFIKATORem.

### Przykład 2: pobieranie zadań przesłanych w ubiegłym tygodniu
```
PS C:\>Get-AzDataLakeAnalyticsJob -Account "contosoadla" -SubmittedAfter (Get-Date).AddDays(-7)
```

To polecenie pobiera zadania przesłane w ubiegłym tygodniu.

## PARAMETRÓW

### — Konto
Określa nazwę konta usługi Data Lake Analytics.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Include
Określa opcje wskazujące typ dodatkowych informacji do pobrania dla zadania.
Dopuszczalne wartości tego parametru to:
- Znaleziono
- DebugInfo
- Celów
- Cały

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+ExtendedJobData
Parameter Sets: GetBySpecificJobInformation
Aliases:
Accepted values: None, All, DebugInfo, Statistics

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -JobId
Określa identyfikator zadania do pobrania.

```yaml
Type: System.Guid
Parameter Sets: GetBySpecificJobInformation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę, która ma być używana do filtrowania wyników listy zadań.
Dopuszczalne wartości tego parametru to:
- Znaleziono
- DebugInfo
- Celów
- Cały

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PipelineId
Identyfikator opcjonalny, który wskazuje tylko część zadań określonego potoku, należy zwrócić.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RecurrenceId
Identyfikator opcjonalny, który wskazuje tylko część zadań określonego cyklu, należy zwrócić.

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wynik
Określa filtr wyników zadania.
Dopuszczalne wartości tego parametru to:
- Znaleziono
- Anulowania
- Nie powiodło się
- Doszło

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobResult[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: None, Succeeded, Cancelled, Failed

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Określa filtr stanu dla wyników zadania.
Dopuszczalne wartości tego parametru to:
- Twierdzona
- Nowy
- Kompilowania
- Nich
- Oczekuje
- Czynając
- Wstrzymana
- Wykonywania
- Zakończona

```yaml
Type: Microsoft.Azure.Management.DataLake.Analytics.Models.JobState[]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:
Accepted values: Accepted, Compiling, Ended, New, Queued, Running, Scheduling, Starting, Paused, WaitingForCapacity

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedAfter
Określa filtr daty.
Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane po określonej dacie.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubmittedBefore
Określa filtr daty.
Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane przed określoną datą.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Osoba przesyłająca
Określa adres e-mail użytkownika.
Ten parametr służy do filtrowania wyników listy zadań na zadania przesłane przez określonego użytkownika.

```yaml
Type: System.String
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Początek
Wartość opcjonalna wskazująca liczbę zadań do zwrócenia. Wartość domyślna to 500

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: GetAllInResourceGroupAndAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. GUID

### Microsoft. Azure. Commands. DataLakeAnalytics. models. DataLakeAnalyticsEnums + ExtendedJobData

### System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Management. datalake. Analytics. modele. JobState []

### Microsoft. Azure. Management. datalake. Analytics. modele. JobResult []

### System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

## WYSYŁA

### Microsoft. Azure. Management. datalake. Analytics. modele. JobInformation

## INFORMACYJN

## LINKI POKREWNE

[Zatrzymaj — AzDataLakeAnalyticsJob](./Stop-AzDataLakeAnalyticsJob.md)

[Prześlij — AzDataLakeAnalyticsJob](./Submit-AzDataLakeAnalyticsJob.md)

[Wait-AzDataLakeAnalyticsJob](./Wait-AzDataLakeAnalyticsJob.md)


