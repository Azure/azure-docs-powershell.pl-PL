---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 71650d36c319536db5ad96aa142e2712e229d712
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872664"
---
# Get-AzRecoveryServicesBackupSchedulePolicyObject

## STRESZCZENIe
Pobiera obiekt zasad dotyczących harmonogramu podstawowego.

## POLECENIA

```
Get-AzRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzRecoveryServicesBackupSchedulePolicyObject** pobiera **AzureRMRecoveryServicesSchedulePolicyObject** bazowy.
Ten obiekt nie jest utrwalony w systemie.
Jest to obiekt tymczasowy, który można manipulować i używać z poleceniem cmdlet New-AzRecoveryServicesBackupProtectionPolicy, aby utworzyć nowe zasady ochrony kopii zapasowych.

## Przykłady

### Przykład 1. Ustaw częstotliwość harmonogramu na co tydzień
```
PS C:\>$RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Pierwsze polecenie pobiera obiekt zasady przechowywania, a następnie zapisuje go w zmiennej $RetPol.
Drugie polecenie pobiera obiekt zasad harmonogramu, a następnie zapisuje go w zmiennej $SchPol.
Trzecia zmiana częstotliwości dla zasad harmonogramu na co tydzień.
Ostatnie polecenie tworzy zasady ochrony kopii zapasowej ze zaktualizowanym harmonogramem.

### Przykład 2: Ustawianie czasu wykonywania kopii zapasowej
```
PS C:\>$SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Pierwsze polecenie powoduje wyświetlenie obiektu zasad harmonogramu, a następnie zapisanie go w zmiennej $SchPol.
Drugie polecenie usuwa wszystkie zaplanowane czasy uruchamiania z $SchPol.
W trzecim poleceniu jest pobierana aktualna Data i godzina, a następnie jest ona przechowywana w zmiennej $DT.
Czwarte polecenie zamienia zaplanowane czasy uruchamiania na bieżącą godzinę.
Kopię zapasową można wykonać tylko raz dziennie, aby zresetować czas wykonywania kopii zapasowej, zastępując oryginalny harmonogram.
Ostatnie polecenie tworzy zasady ochrony kopii zapasowych przy użyciu nowego harmonogramu.

## PARAMETRÓW

### -BackupManagementType
Określa typ zarządzania kopią zapasową.
Dopuszczalne wartości tego parametru to:
- AzureVM 
- AzureSQLDatabase
- AzureStorage

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: False
Position: 1
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

### -Obciążenia
Określa typ obciążenia pracą.
Dopuszczalne wartości tego parametru to:
- AzureVM 
- AzureSQLDatabase
- AzureFiles

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. SchedulePolicyBase

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Set-AzRecoveryServicesBackupProtectionPolicy](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


