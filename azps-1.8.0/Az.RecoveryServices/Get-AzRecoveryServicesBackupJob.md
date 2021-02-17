---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 5dab5eaca48152dc573caf75f5d80737802bfcdf
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399825"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS
Otrzymuje zadania kopii zapasowej.

## SKŁADNIA

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej platformy Azure dla określonego magazynu.
Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich zadań w toku
```
PS C:\>$Joblist = Get-AzRecoveryservicesBackupJob -Status Inprogress
PS C:\> $Joblist[0]
WorkloadName     Operation            Status               StartTime                 EndTime                                             
------------     ---------            ------               ---------                 -------                                             
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Pierwsze polecenie otrzymuje stan zadania w toku jako tablicę, a następnie przechowuje je w $Joblist tablicy.
Drugie polecenie wyświetla pierwszy element w $Joblist tablicy.

### Przykład 2. Uzyskiwanie wszystkich zadań, których nie udało się uzyskać w ciągu ostatnich 7 dni
```
PS C:\>Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed
```

To polecenie pobiera zadania, których niepowodzenie zakończyło się w zeszłym tygodniu w magazynie.
Parametr *Od* określa czas siedmiu dni w przeszłości określonej w czasie UTC.
To polecenie nie określa wartości dla *parametru To.*
W związku z tym używana jest wartość domyślna bieżącego czasu.

### Przykład 3. Uzyskiwanie zadania w toku i oczekiwanie na ukończenie
```
PS C:\> 
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress
$Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $job = Get-AzBackAzureRmRecoveryServicesBackupJob  -Job $Job
    }
    Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

Ten skrypt ankietuje pierwsze zadanie, które jest obecnie w toku, do momentu jego ukończenia.

## PARAMETERS

### -BackupManagementType
Określa typ zarządzania kopią zapasową.
Obecnie jest obsługiwana tylko usługa AzureVM, AzureStorage.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

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

### — Od
Określa rozpoczęcie (jako obiekt **DateTime)** zakresu czasu dla zadań, które otrzymuje to polecenie cmdlet.
Aby uzyskać obiekt **DateTime,** użyj Get-Date cmdlet.
Aby uzyskać więcej informacji na **temat obiektów DateTime,** wpisz `Get-Help Get-Date` tekst.
Daty należy stosować w formacie UTC.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zadanie
Określa nazwę zadania kopii zapasowej do uzyskania.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - JobId
Określa identyfikator zadania, które otrzymuje to polecenie cmdlet.
Identyfikator jest właściwością InstanceId obiektu **AzureRmRecoveryServicesBackupJob.**
Aby uzyskać obiekt **AzureRmRecoveryServicesBackupJob,** użyj narzędzia Get-AzRecoveryServicesBackupJob.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Operacja
Określa operację zadań, które otrzymuje to polecenie cmdlet.
Dopuszczalne wartości dla tego parametru to:
- Kopia zapasowa
- ConfigureBackup
- DeleteBackupData
- Zarejestruj się
- Przywróć
- UnProtect
- Wyrejestruj

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobOperation]
Parameter Sets: (All)
Aliases:
Accepted values: Backup, Restore, ConfigureBackup, DisableBackup, DeleteBackupData

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Status
Określa stan zadań, które otrzymuje to polecenie cmdlet.
Dopuszczalne wartości dla tego parametru to:
- InProgress
- Niepowodzenie
- Anulowano
- Anulowanie
- Ukończono
- CompletedWithWarnings

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobStatus]
Parameter Sets: (All)
Aliases:
Accepted values: InProgress, Cancelling, Cancelled, Completed, CompletedWithWarnings, Failed

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Do
Określa koniec (jako obiekt **DateTime)** zakresu czasu dla zadań, które otrzymuje to polecenie cmdlet.
Wartość domyślna to bieżący czas systemowy.
Jeśli określisz ten parametr, musisz również określić parametr *Od.*
Daty należy stosować w formacie UTC.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultId
ARM identyfikatora magazynu usług odzyskiwania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase

## NOTATKI

## LINKI POKREWNE


[Stop-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)


