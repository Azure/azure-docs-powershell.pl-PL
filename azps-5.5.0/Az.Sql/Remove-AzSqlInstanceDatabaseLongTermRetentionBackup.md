---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlinstancedatabaselongtermretentionbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceDatabaseLongTermRetentionBackup.md
ms.openlocfilehash: 3dbcbed2466f9bb6b229a6dcfa710d6745a72eac
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188026"
---
# Remove-AzSqlInstanceDatabaseLongTermRetentionBackup

## SYNOPSIS
Usuwa długookresową kopię zapasową przechowywania.

## SKŁADNIA

### RemoveBackupDefault (Domyślne)
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-Location] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-BackupName] <String> [-ResourceGroupName <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBackupByInputObject
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup
 [-InputObject] <AzureSqlManagedDatabaseLongTermRetentionBackupModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBackupByResourceId
```
Remove-AzSqlInstanceDatabaseLongTermRetentionBackup [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Remove-AzSqlInstanceDatabaseLongTermRetentionBackup** usuwa określoną kopię zapasową.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Remove-AzSqlInstanceDatabaseLongTermRetentionBackup -Location southeastasia -ResourceGroupName testResourceGroup -InstanceName testInstance -DatabaseName test -BackupName 15be823c-7e2c-49d8-819f-a3fdcad92215;132268250550000000
```

Usuwa kopię zapasową o nazwie 15be823c-7e2c-49d8-819f-a3fdcad92215;13226825055000000

## PARAMETERS

### -BackupName
Nazwa kopii zapasowej.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Nazwa zarządzanej bazy danych, z których pochodzi kopia zapasowa.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 2
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

### — Wymuszanie
Pomiń komunikat potwierdzenia wykonania akcji

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Obiekt długookresowej kopii zapasowej przechowywania bazy danych do usunięcia.

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel
Parameter Sets: RemoveBackupByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstanceName
Nazwa zarządzanego wystąpienia kopii zapasowej znajduje się poniżej.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja źródłowego wystąpienia zarządzanego kopii zapasowych.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: RemoveBackupDefault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu kopii zapasowej przechowywania długoterminowego bazy danych do usunięcia.

```yaml
Type: System.String
Parameter Sets: RemoveBackupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Polecenie cmdlet nie zostanie uruchomione.

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

### Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseLongTermRetentionBackupModel

## NOTATKI

## LINKI POKREWNE

[Get-AzSqlInstanceDatabaseLongTermRetentionBackup](./Get-AzSqlInstanceDatabaseLongTermRetentionBackup.md)

[Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy](./Get-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy](./Set-AzSqlInstanceDatabaseBackupLongTermRetentionPolicy.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)