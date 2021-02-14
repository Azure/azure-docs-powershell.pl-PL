---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183818"
---
# Wait-AzRecoveryServicesBackupJob

## SYNOPSIS

Czeka na zakończenie zadania kopii zapasowej.

## SKŁADNIA

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS

Polecenie cmdlet **Wait-AzRecoveryServicesBackupJob** czeka na ukończenie zadania kopii zapasowej platformy Azure.
Tworzenie zadań kopii zapasowej może zająć dużo czasu.
Jeśli uruchamiasz zadanie kopii zapasowej w ramach skryptu, może być konieczne wymusienie na skryptie czekania na ukończenie zadania przed kontynuowaniem wykonywania innych zadań.
Skrypt, który zawiera to polecenie cmdlet, może być prostszy niż skrypt, który przeszuka usługę kopii zapasowej na temat stanu zadania.
Ustaw kontekst magazynu przy użyciu parametru -VaultId.

## PRZYKŁADY

### Przykład 1. Oczekiwanie na zakończenie zadania

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

Ten skrypt ankietuje pierwsze zadanie, które obecnie trwa do czasu jego ukończenia lub wygaśnięcia limitu czasu 1 godziny.

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

### — Zadanie

Określa zadanie do oczekiwania.
Aby uzyskać obiekt **BackupJob,** użyj polecenia cmdlet **Get-AzRecoveryServicesBackupJob.**

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Limit czasu

Określa maksymalny czas (w sekundach), przez który to polecenie cmdlet oczekuje na ukończenie zadania.
Zalecane jest określenie wartości przec.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
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

### System.Object

### System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase

## NOTATKI

## LINKI POKREWNE

[Get-AzRecoveryServicesBackupJob](./Get-AzRecoveryServicesBackupJob.md)
