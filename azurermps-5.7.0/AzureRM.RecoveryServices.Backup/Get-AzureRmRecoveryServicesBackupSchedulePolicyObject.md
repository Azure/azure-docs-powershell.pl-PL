---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: E247C6DF-B53D-487E-AAA2-551FCBFD77E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupschedulepolicyobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md
ms.openlocfilehash: 4a3602363436c396b0706d9c195569874a35fdf3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526690"
---
# Get-AzureRmRecoveryServicesBackupSchedulePolicyObject

## STRESZCZENIe
Pobiera obiekt zasad dotyczących harmonogramu podstawowego.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmRecoveryServicesBackupSchedulePolicyObject [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupSchedulePolicyObject** pobiera **AzureRMRecoveryServicesSchedulePolicyObject** bazowy.
Ten obiekt nie jest utrwalony w systemie.
Jest to obiekt tymczasowy, który można manipulować i używać z poleceniem cmdlet New-AzureRmRecoveryServicesBackupProtectionPolicy, aby utworzyć nowe zasady ochrony kopii zapasowych.

## Przykłady

### Przykład 1. Ustaw częstotliwość harmonogramu na co tydzień
```
PS C:\>$RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunFrequency = "Weekly"
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Pierwsze polecenie pobiera obiekt zasady przechowywania, a następnie zapisuje go w zmiennej $RetPol.

Drugie polecenie pobiera obiekt zasad harmonogramu, a następnie zapisuje go w zmiennej $SchPol.

Trzecia zmiana częstotliwości dla zasad harmonogramu na co tydzień.

Ostatnie polecenie tworzy zasady ochrony kopii zapasowej ze zaktualizowanym harmonogramem.

### Przykład 2: Ustawianie czasu wykonywania kopii zapasowej
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
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

```yaml
Type: BackupManagementType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

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
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. SchedulePolicyBase

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


