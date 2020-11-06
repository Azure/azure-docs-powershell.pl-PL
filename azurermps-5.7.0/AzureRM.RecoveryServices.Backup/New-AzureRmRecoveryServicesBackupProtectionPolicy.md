---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/new-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/New-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: e9834236a72a68f64cc9b19d6576e56102f96b13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526681"
---
# New-AzureRmRecoveryServicesBackupProtectionPolicy

## STRESZCZENIe
Tworzy zasady ochrony kopii zapasowych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmRecoveryServicesBackupProtectionPolicy [-Name] <String> [-WorkloadType] <WorkloadType>
 [[-BackupManagementType] <BackupManagementType>] [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** tworzy zasady ochrony kopii zapasowych w magazynie.
Zasady ochrony są skojarzone z co najmniej jednym zasadami przechowywania.
Zasady przechowywania definiują czas przechowywania punktu odzyskiwania w usłudze Kopia zapasowa Azure.

Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać domyślne zasady przechowywania.
Możesz też użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać domyślne zasady dotyczące harmonogramu.
Obiekty **SchedulePolicy** i **RetentionPolicy** są używane jako dane wejściowe polecenia cmdlet **New-AzureRmRecoveryServicesBackupProtectionPolicy** .

Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.

## Przykłady

### Przykład 1. Tworzenie zasad ochrony kopii zapasowych
```
PS C:\> $SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Dt = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($Dt.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> New-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy" -WorkloadType AzureVM -RetentionPolicy $RetPol -SchedulePolicy $SchPol
```

Pierwsze polecenie uzyskuje podstawowy **SchedulePolicyObject** , a następnie zapisuje go w zmiennej $SchPol.

Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.

W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę.

Czwarte polecenie dodaje bieżącą datę i godzinę w $Dt jako zaplanowany czas wykonania do zasad harmonogramu.

Piąte polecenie uzyskuje podstawowy obiekt **RetentionPolicy** , a następnie zapisuje go w zmiennej $RetPol.

Szóste polecenie ustawia zasady czasu trwania retencji na 365 dni.

Polecenie ostatnie tworzy obiekt **BackupProtectionPolicy** na podstawie zasad harmonogramu i przechowywania utworzonych za pomocą poprzednich poleceń.

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
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Name (nazwa)
Określa nazwę zasady.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetentionPolicy
Określa podstawowy obiekt **RetentionPolicy** .
Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject, aby uzyskać obiekt **RetentionPolicy** .

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SchedulePolicy
Określa podstawowy obiekt **SchedulePolicy** .
Możesz użyć polecenia cmdlet Get-AzureRmRecoveryServicesBackupSchedulePolicyObject, aby uzyskać obiekt **SchedulePolicy** .

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. PolicyBase

## INFORMACYJN

## LINKI POKREWNE

[Enable-AzureRmRecoveryServicesBackupProtection](./Enable-AzureRmRecoveryServicesBackupProtection.md)

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[Get-AzureRmRecoveryServicesBackupSchedulePolicyObject](./Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Set-AzureRmRecoveryServicesBackupProtectionPolicy](./Set-AzureRmRecoveryServicesBackupProtectionPolicy.md)


