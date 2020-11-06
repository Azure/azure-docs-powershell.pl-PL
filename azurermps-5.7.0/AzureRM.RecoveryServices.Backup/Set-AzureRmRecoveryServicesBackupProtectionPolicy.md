---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/set-azurermrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Set-AzureRmRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 5a60320736e65fae83547bbf9b2825979f73601e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526677"
---
# Set-AzureRmRecoveryServicesBackupProtectionPolicy

## STRESZCZENIe
Modyfikuje zasady ochrony kopii zapasowej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase>
 [[-RetentionPolicy] <RetentionPolicyBase>] [[-SchedulePolicy] <SchedulePolicyBase>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmBackupProtectionPolicy** modyfikuje istniejące zasady ochrony kopii zapasowych platformy Azure.
Można modyfikować składniki Harmonogram kopii zapasowych i zasady przechowywania.

Wszelkie wprowadzone zmiany mają wpływ na wykonywanie kopii zapasowych i zachowywanie elementów skojarzonych z tymi zasadami.

Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.

## Przykłady

### Przykład 1. modyfikacja zasad ochrony kopii zapasowych
```
PS C:\>$SchPol = Get-AzureRmRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.RemoveAll()
PS C:\> $DT = Get-Date
PS C:\> $SchPol.ScheduleRunTimes.Add($DT.ToUniversalTime())
PS C:\> $RetPol = Get-AzureRmRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 365
PS C:\> $Pol = Get-AzureRmRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Set-AzureRmRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

Pierwsze polecenie uzyskuje podstawowy obiekt SchedulePolicy, a następnie zapisuje go w zmiennej $SchPol.

Drugie polecenie usuwa wszystkie zaplanowane godziny wykonania z zasad harmonogramu w $SchPol.

W trzecim poleceniu użyto polecenia cmdlet Get-Date, aby uzyskać bieżącą datę i godzinę, a następnie przechowywać ją w zmiennej $DT.

Czwarte polecenie umożliwia dodanie daty i godziny w $DT do harmonogramu czasu uruchomienia zasad harmonogramu.

W piątym poleceniu jest pobierany podstawowy obiekt zasady przechowywania, a następnie jest on przechowywany w zmiennej $RetPol.

Szóste polecenie ustawia czas trwania przechowywania na 365 dni.

Po siódmym poleceniu otrzymano zasady ochrony kopii zapasowej o nazwie NewPolicy, a następnie zapisuje je w zmiennej $Pol.

Polecenie ostatnie modyfikuje zasady ochrony kopii zapasowej w $Pol przy użyciu zasad harmonogramu w $SchPol i zasad przechowywania w $RetPol.

## PARAMETRÓW

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

### -Policy
Określa zasady ochrony kopii zapasowej, które modyfikuje to polecenie cmdlet.
Aby uzyskać obiekt **BackupProtectionPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupProtectionPolicy.

```yaml
Type: PolicyBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RetentionPolicy
Określa podstawowe zasady przechowywania.
Aby uzyskać obiekt **RetentionPolicy** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.

```yaml
Type: RetentionPolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
Określa obiekt zasad dotyczących harmonogramu podstawowego.
Aby uzyskać obiekt **SchedulePolicy** , użyj obiektu Get-AzureRmRecoveryServicesBackupSchedulePolicyObject.

```yaml
Type: SchedulePolicyBase
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
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

### PolicyBase
Parametr "Policy" przyjmuje wartość typu "PolicyBase" z rurociągu

## WYSYŁA

### System. Collections. Generic. list "1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. JobBase]

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmRecoveryServicesBackupProtectionPolicy](./Get-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Get-AzureRmRecoveryServicesBackupRetentionPolicyObject](./Get-AzureRmRecoveryServicesBackupRetentionPolicyObject.md)

[Nowe — AzureRmRecoveryServicesBackupProtectionPolicy](./New-AzureRmRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzureRmRecoveryServicesBackupProtectionPolicy](./Remove-AzureRmRecoveryServicesBackupProtectionPolicy.md)


