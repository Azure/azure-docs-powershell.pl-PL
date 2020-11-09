---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 12F8A120-7282-4844-90E0-1C3393336E8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 623acc7d96fc6c3dc4f1496f42a53bf276f8e778
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308982"
---
# Get-AzRecoveryServicesBackupJob

## STRESZCZENIe

Pobiera zadania kopii zapasowej.

## POLECENIA

```
Get-AzRecoveryServicesBackupJob [[-Status] <JobStatus>] [[-Operation] <JobOperation>] [[-From] <DateTime>]
 [[-To] <DateTime>] [[-JobId] <String>] [[-Job] <JobBase>] [-BackupManagementType <BackupManagementType>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis

Polecenie cmdlet **Get-AzRecoveryServicesBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.
Ustaw kontekst magazynu przy użyciu parametru-VaultId.

## Przykłady

### Przykład 1: uzyskiwanie wszystkich zadań w trakcie wykonywania

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Joblist = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> $Joblist[0]

WorkloadName     Operation            Status               StartTime                 EndTime
------------     ---------            ------               ---------                 -------
V2VM             Backup               InProgress           4/23/2016 5:00:30 PM      1/1/2001 12:00:00
```

Pierwsze polecenie pobiera stan zadań w trakcie wykonywania jako tablicę, a następnie zapisuje je w zmiennej $Joblist.
Drugie polecenie wyświetla pierwszy element tablicy $Joblist.

### Przykład 2: pobieranie wszystkich zadań zakończonych niepowodzeniem w ciągu ostatnich 7 dni

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupJob -From (Get-Date).AddDays(-7).ToUniversalTime() -Status Failed -VaultId $vault.ID
```

To polecenie pobiera nieudane zadania z ostatniego tygodnia w magazynie.
Parametr *from* określa godzinę określoną w ubiegłym ciągu siedem dni (UTC).
W poleceniu nie określono *wartości parametru to* .
W związku z tym używana jest wartość domyślna bieżącego czasu.

### Przykład 3: uzyskiwanie zadania w trakcie wykonywania i oczekiwanie na ukończenie

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

Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.

Uwaga: możesz poczekać na zakończenie zadania kopii zapasowej Azure zamiast pętli while za pomocą polecenia cmdlet **wait-AzRecoveryServicesBackupJob** .

### Przykład 4: pobieranie wszystkich zadań AzureVM w ciągu ostatnich 2 dni, które zakończyły się powodzeniem

```powershell
$vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
$Jobs = Get-AzRecoveryServicesBackupJob  -VaultId $vault.ID  -Status Completed -From (Get-Date).AddDays(-2).ToUniversalTime() -BackupManagementType AzureVM
```
Pierwsze polecenie cmdlet pobiera obiekt magazynu. Drugie polecenie cmdlet przechowuje wszystkie zadania AzureVM w danym magazynie, które zostały ukończone w ciągu ostatnich 2 dni w celu $jobs. Zmień wartość parametru BackupManagementType na MAB w celu pobrania zadań agenta MAB.

## PARAMETRÓW

### -BackupManagementType

Klasa zasobów chronionych. Obecnie obsługiwane są wartości dla tego polecenia cmdlet to AzureVM, AzureStorage, AzureWorkload, MAB.

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

Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Od

Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.
Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .
Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .
Użyj formatu UTC dla dat.

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

Określa zadanie do pobrania.

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

### -JobId

Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.
Identyfikator jest właściwością JobId obiektu **Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase** .

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

### -Operation

Określa działanie zadań, które są pobierane przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:

- Wykonania
- ConfigureBackup
- DeleteBackupData
- DisableBackup
- Przywrócenie
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

### -Status

Określa stan zadań pobieranych przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:

- W trakcie
- Nie powiodło się
- Anulowania
- Anulowanie
- Zakończyć
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

### -To

Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.
Wartością domyślną jest bieżąca godzina systemowa.
W przypadku określenia tego parametru należy również określić parametr **-from** .
Użyj formatu UTC dla dat.

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

Identyfikator ARM magazynu usług Recovery Services.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase

## INFORMACYJN

## LINKI POKREWNE

[Get-AzRecoveryServicesBackupJobDetail](./Get-AzRecoveryServicesBackupJobDetail.md)

[Zatrzymaj — AzRecoveryServicesBackupJob](./Stop-AzRecoveryServicesBackupJob.md)

[Wait-AzRecoveryServicesBackupJob](./Wait-AzRecoveryServicesBackupJob.md)
