---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176979"
---
# Get-AzSqlDatabaseGeoBackup

## SYNOPSIS
Pobiera nadmiarową geograficznie kopię zapasową bazy danych.

## SKŁADNIA

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzSqlDatabaseGeoBackup** pobiera określoną geograficznie nadmiarową kopię zapasową bazy danych SQL lub wszystkie dostępne geograficznie nadmiarowe kopie zapasowe na określonym serwerze.
Geograficznie nadmiarowa kopia zapasowa to zasób, który można przywrócić, używając plików danych z oddzielnej lokalizacji geograficznej.
Za pomocą programu Geo-Restore można przywrócić geograficznie nadmiarową kopię zapasową w przypadku 30-65-65-65-855 000 w celu odzyskania bazy danych w nowym regionie.
To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych na serwerze
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe na określonym serwerze.

### Przykład 2. Uzyskiwanie określonej nadmiarowej geograficznej kopii zapasowej
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

To polecenie pobiera geograficznie nadmiarową kopię zapasową bazy danych o nazwie ContosoDatabase.

### Przykład 3. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych na serwerze przy użyciu filtrowania
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe na określonym serwerze, których nazwa rozpoczyna się od "Contoso".

## PARAMETERS

### -DatabaseName
Określa nazwę bazy danych do uzyskania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisany serwer bazy danych SQL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Określa nazwę serwera hostatora kopii zapasowej do przywrócenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

## OUTPUTS

### Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel

## NOTATKI

## LINKI POKREWNE

[Omówienie: zapewnianie ciągłości działania i odzyskiwanie baz danych w chmurze za pomocą usługi SQL Database](http://go.microsoft.com/fwlink/?LinkId=746881)

[Odzyskiwanie bazy danych Azure SQL Database po 30-55 dniach](http://go.microsoft.com/fwlink/?LinkId=746882)

[Restore-AzSqlDatabase](./Restore-AzSqlDatabase.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)
