---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 011b27cfff166173d485636a1e8890d917484651
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984241"
---
# Get-AzRecoveryServicesBackupJob

## SYNOPSIS

Otrzymuje zadania kopii zapasowej.

## SKŁADNIA

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
  [-UseSecondaryRegion] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS

Polecenie **cmdlet Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej platformy Azure dla określonego magazynu.
Ustaw kontekst magazynu przy użyciu parametru -VaultId.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich zadań w toku

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Pierwsze polecenie otrzymuje stan zadań w toku jako tablicę, a następnie przechowuje je w $Joblist tablicy.
Drugie polecenie wyświetla pierwszy element w $Joblist tablicy.

### Przykład 2. Uzyskiwanie wszystkich zadań, których nie udało się uzyskać w ciągu ostatnich 7 dni

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

To polecenie pobiera zadania, których niepowodzenie zakończyło się w zeszłym tygodniu w magazynie.
Parametr *From* określa czas siedmiu dni w przeszłości określonej w czasie UTC.
To polecenie nie określa wartości dla *parametru To.*
W związku z tym używana jest wartość domyślna bieżącego czasu.

### Przykład 3. Uzyskiwanie zadania w toku i oczekiwanie na ukończenie

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
$Job = $Jobs[0]
While ( $Job.Status -ne Completed ) {
    Write-Host -Object "Waiting for completion..."
    Start-Sleep -Seconds 10
    $Job = Get-AzRecoveryServicesBackupJob -Job $Job -VaultId $vault.ID
}
Write-Host -Object "Done!"

Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Ten skrypt ankietuje pierwsze zadanie, które jest obecnie w toku, do momentu jego ukończenia.

Uwaga: Możesz użyć polecenia cmdlet **Wait-AzRecoveryServicesBackupJob,** aby zaczekać na ukończenie zadania kopii zapasowej platformy Azure, zamiast podczas pętli.

### Przykład 4. Uzyskiwanie wszystkich zadań AzureVM w ciągu ostatnich 2 dni, które zakończyły się pomyślnie

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
Pierwsze polecenie cmdlet pobiera obiekt magazynu. Drugie polecenie cmdlet przechowuje wszystkie zadania AzureVM w danym magazynie, które zostały ukończone w ciągu ostatnich 2 dni w celu $jobs. Zmień wartość parametru BackupManagementType na mab w celu zdalnego dostępu do zadań agenta MAB.

## PARAMETERS

### -BackupManagementType

Klasa zasobów, które są chronione. Obecnie wartości obsługiwane dla tego polecenia cmdlet to: AzureVM, AzureStorage, AzureWorkload, MAB.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureStorage, AzureWorkload, MAB

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
Aby uzyskać obiekt **DateTime,** użyj polecenia cmdlet **Get-Date.**
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

Określa zadanie do uzyskania.

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
Identyfikator jest właściwością JobId obiektu **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase.**

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
- DisableBackup
- Przywróć
- BackupDataMove

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
Jeśli określisz ten parametr, musisz także określić parametr **-From.**
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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase

## NOTATKI

## LINKI POKREWNE

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Stop-AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
