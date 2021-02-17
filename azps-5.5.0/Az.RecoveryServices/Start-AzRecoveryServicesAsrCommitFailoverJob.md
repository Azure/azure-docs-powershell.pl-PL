---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrcommitfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrCommitFailoverJob.md
ms.openlocfilehash: 7b6e70e13175eb54fbb50e6412165270a7194166
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191267"
---
# Start-AzRecoveryServicesAsrCommitFailoverJob

## SYNOPSIS
Rozpoczyna akcję zatwierdzania trybu failover dla obiektu Odzyskiwanie witryny.

## SKŁADNIA

### ByRPIObject (domyślne)
```
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByRPObject
```
Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Start-AzRecoveryServicesAsrCommitFailoverJob** uruchamia proces zatwierdzania trybu failover dla obiektu Azure Site Recovery po operacji trybu failover.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> $currentJob = Start-AzRecoveryServicesAsrCommitFailoverJob -RecoveryPlan $RP
```

Rozpoczyna zatwierdzanie trybu failover dla określonego planu odzyskiwania i zwraca zadanie asr służące do śledzenia operacji.

### Przykład 2

Rozpoczyna akcję zatwierdzania trybu failover dla obiektu odzyskiwanie witryny. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
Start-AzRecoveryServicesAsrCommitFailoverJob -ReplicationProtectedItem $ReplicationProtectedItem
```

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

### -RecoveryPlan
Określa obiekt planu odzyskiwania asr odpowiadający planowi odzyskiwania w trybie failover.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
Określa obiekt elementu chronionego replikacją asr, odpowiadający elementowi chronionego replikacją, który ma zostać trybu failover.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem

## OUTPUTS

### Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob

## NOTATKI

## LINKI POKREWNE
