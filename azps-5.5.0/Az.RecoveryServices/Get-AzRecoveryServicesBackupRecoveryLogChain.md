---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackuprecoverylogchain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupRecoveryLogChain.md
ms.openlocfilehash: ba82e1ddf8385f74b271feb9119280d48fc1b859
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178994"
---
# Get-AzRecoveryServicesBackupRecoveryLogChain

## SYNOPSIS
To polecenie zawiera listę punktów startowych i końcowych nieprzerwanego łańcucha dziennika danego elementu kopii zapasowej. Za jego pomocą można określić, czy punkt w czasie, do którego użytkownik chce przywrócić db, jest prawidłowy, czy nie.

## SKŁADNIA

### NoFilterParameterSet (ustawienie domyślne)
```
Get-AzRecoveryServicesBackupRecoveryLogChain [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DateTimeFilter
```
Get-AzRecoveryServicesBackupRecoveryLogChain [[-StartDate] <DateTime>] [[-EndDate] <DateTime>]
 [-Item] <ItemBase> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzRecoveryServicesBackupRecoveryLogChain** pobiera punkty odzyskiwania zakresu czasu w czasie dla kopii zapasowej elementu kopii zapasowej usługi Azure.
Po zakończeniu kopii zapasowej elementu obiekt **AzRecoveryServicesBackupRecoveryLogChain** ma co najmniej jeden zakres czasu odzyskiwania.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> $StartDate = (Get-Date).AddDays(-7) 
PS C:\> $EndDate = Get-Date 
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureWorkload -Status Registered
PS C:\> $RP = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType MSSQL | Get-AzRecoveryServicesBackupRecoveryLogChain -StartDate $Startdate.ToUniversalTime() -EndDate $Enddate.ToUniversalTime()
```

Pierwsze polecenie pobiera datę z siedmiu dni temu, a następnie przechowuje ją w $StartDate zmienną.
Drugie polecenie pobiera dzisiejszą datę, a następnie przechowuje je w $EndDate zmienną.
Trzecie polecenie pobiera kontenery kopii zapasowej azureWorkload i przechowuje je w $Container danych.
Czwarte polecenie pobiera element kopii zapasowej, a następnie udostępnia go w potokowym poleceniu cmdlet jako obiekt elementu kopii zapasowej.
Ostatnie polecenie pobiera tablicę zakresów czasu punktów odzyskiwania dla elementu w programie $BackupItem, a następnie przechowuje je w $RP zmienną.

### Przykład 2

To polecenie zawiera listę punktów startowych i końcowych nieprzerwanego łańcucha dziennika danego elementu kopii zapasowej. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupRecoveryLogChain -Item $Item -VaultId $vault.ID
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

### -EndDate
Czas zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — element
Obiekt Elementu chronionego, dla którego należy pobrać punkt odzyskiwania

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### - StartDate
Godzina rozpoczęcia zakresu czasu, dla którego należy pobrać punkt odzyskiwania

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: DateTimeFilter
Aliases:

Required: False
Position: 0
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

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase
System.String

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RecoveryPointBase

## NOTATKI

## LINKI POKREWNE
