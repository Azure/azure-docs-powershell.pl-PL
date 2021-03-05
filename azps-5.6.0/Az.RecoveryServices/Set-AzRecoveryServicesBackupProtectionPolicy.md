---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: D614B509-82DD-42FB-B975-D72CD3355E3E
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c71dcc24947070a6d57aa617d121c1b5fcc3e923
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997410"
---
# Set-AzRecoveryServicesBackupProtectionPolicy

## SYNOPSIS
Modyfikuje zasady ochrony kopii zapasowej.

## SKŁADNIA

### ModifyPolicyParamSet
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [[-RetentionPolicy] <RetentionPolicyBase>]
 [[-SchedulePolicy] <SchedulePolicyBase>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### FixPolicyParamSet
```
Set-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-FixForInconsistentItems]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzRecoveryServicesBackupProtectionPolicy** modyfikuje istniejące zasady ochrony usługi Azure Backup.
Można modyfikować składniki harmonogramu i zasad przechowywania kopii zapasowej.
Wszelkie wprowadzone zmiany wpływają na tworzenie kopii zapasowej i przechowywanie elementów skojarzonych z zasadami.
Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.

## PRZYKŁADY

### Przykład 1. Modyfikowanie zasad ochrony kopii zapasowej
```
PS C:\> $SchPol = Get-AzRecoveryServicesBackupSchedulePolicyObject -WorkloadType "AzureVM" 
PS C:\> $SchPol.ScheduleRunTimes.Clear()
PS C:\> $Time = Get-Date
PS C:\> $Time1 = Get-Date -Year $Time.Year -Month $Time.Month -Day $Time.Day -Hour $Time.Hour -Minute 0 -Second 0 -Millisecond 0
PS C:\> $Time1 = $Time1.ToUniversalTime()
PS C:\> $SchPol.ScheduleRunTimes.Add($Time1)
PS C:\> $SchPol.ScheduleRunFrequency.Clear
PS C:\> $SchPol.ScheduleRunDays.Add("Monday")
PS C:\> $SchPol.ScheduleRunFrequency="Weekly"
PS C:\> $RetPol = Get-AzRecoveryServicesBackupRetentionPolicyObject -WorkloadType "AzureVM" 
PS C:\> $RetPol.IsDailyScheduleEnabled=$false
PS C:\> $RetPol.DailySchedule.DurationCountInDays = 0
PS C:\> $RetPol.IsWeeklyScheduleEnabled=$true 
PS C:\> $RetPol.WeeklySchedule.DaysOfTheWeek.Add("Monday")
PS C:\> $RetPol.WeeklySchedule.DurationCountInWeeks = 365
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "azurefiles" -Name "azurefilesvault"
PS C:\> $Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "TestPolicy" -VaultId $vault.ID
PS C:\> $Pol.SnapshotRetentionInDays=5
PS C:\> Set-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol -SchedulePolicy $SchPol -RetentionPolicy $RetPol
```

Oto szczegółowy opis czynności, które należy wykonać w celu zmodyfikowania zasad ochrony: 
1.  Uzyskaj podstawową grafikę SchedulePolicyObject i podstawową wartość RetentionPolicyObject. Przechowuj je w zmiennej.
2.  Ustaw różne parametry obiektu zasad harmonogramu i przechowywania zgodnie z wymaganiami. Na przykład w powyższym przykładowym skrypcie próbujemy ustawić tygodniowe zasady ochrony. Dlatego zmieniliśmy częstotliwość harmonogramu na "Tygodniowy", a także zaktualizowaliśmy czas uruchamiania harmonogramu. W obiekcie zasad przechowywania zaktualizowaliśmy tygodniowy czas trwania przechowywania i ustawiliśmy poprawną flagę "Włączony harmonogram tygodniowy". Jeśli chcesz ustawić zasady dzienne, ustaw flagę "Harmonogram dzienny włączony" na prawda i przypisz odpowiednie wartości dla innych parametrów obiektu.
3.  Uzyskaj zasady ochrony kopii zapasowej, które chcesz zmodyfikować i przechowywać w zmiennej. W powyższym przykładzie pobrano zasady kopii zapasowej o nazwie "TestPolicy", którą chcemy zmodyfikować.
4.  Modyfikowanie zasad ochrony kopii zapasowej pobranych w kroku 3 przy użyciu obiektu zmodyfikowanych zasad harmonogramu i obiektu zasad przechowywania.

## PARAMETERS

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

### -FixForInconsistentItems
Przełącz parametr wskazujący, czy chcesz ponowić aktualizację zasad dla elementów, których niepowodzenie nie powiodło się.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FixPolicyParamSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zasady
Określa zasady ochrony kopii zapasowej, które to polecenie cmdlet modyfikuje.
Aby uzyskać obiekt **BackupProtectionPolicy,** użyj Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
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
Aby uzyskać obiekt **RetentionPolicy,** użyj Get-AzRecoveryServicesBackupRetentionPolicyObject cmdlet.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RetentionPolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SchedulePolicy
Określa obiekt zasad harmonogramu podstawowego.
Aby uzyskać obiekt **SchedulePolicy,** użyj Get-AzRecoveryServicesBackupSchedulePolicyObject obiekt.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.SchedulePolicyBase
Parameter Sets: ModifyPolicyParamSet
Aliases:

Required: False
Position: 3
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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.PolicyBase

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase

## NOTATKI

## LINKI POKREWNE

[Get-AzRecoveryServicesBackupProtectionPolicy](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[Get-AzRecoveryServicesBackupRetentionPolicyObject](./Get-AzRecoveryServicesBackupRetentionPolicyObject.md)

[New-AzRecoveryServicesBackupProtectionPolicy](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[Remove-AzRecoveryServicesBackupProtectionPolicy](./Remove-AzRecoveryServicesBackupProtectionPolicy.md)


