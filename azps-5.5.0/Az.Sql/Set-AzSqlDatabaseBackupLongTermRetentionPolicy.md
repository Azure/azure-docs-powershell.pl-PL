---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188011"
---
# Set-AzSqlDatabaseBackupLongTermRetentionPolicy

## SYNOPSIS
Ustawia zasady przechowywania długoterminowego serwera.

## SKŁADNIA

### WeeklyRetentionRequired (domyślne)
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### RemovePolicy
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### MonthlyRetentionRequired
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### YearlyRetentionRequired
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** ustawia dla tej bazy danych zasady przechowywania przez długi czas.
Zasady są zasobem kopii zapasowej azure używanym do definiowania zasad przechowywania kopii zapasowych.

## PRZYKŁADY

### Przykład 1. Ustawianie tygodniowego przechowywania dla bieżącej wersji zasad przechowywania długoterminowego
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

Dzięki temu zasady przechowywania przez długi czas w bazie danych01 są zachowywane co tydzień z pełną kopią zapasową przez 2 tygodnie.

### Przykład 2. Ustawianie miesięcznego okresu przechowywania dla bieżącej wersji zasad przechowywania długoterminowego
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

W ten sposób są ustawiane zasady przechowywania danych przez długi czas w bazie danych01 w celu zapisywania pierwszej pełnej kopii zapasowej każdego miesiąca przez 5 lat.

### Przykład 3. Ustawianie przechowywania co rok dla bieżącej wersji zasad przechowywania długoterminowych
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

W ten sposób są ustawiane zasady przechowywania danych przez długi czas w bazie danych 01 w celu zapisania pełnej kopii zapasowej wykonanej w 26. tygodniu roku przez 10 lat.

### Przykład 4. Ustawianie każdego przechowywania dla bieżącej wersji zasad przechowywania długoterminowego
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

Dzięki temu zasady przechowywania przez długi czas w bazie danych01 są zachowywane przez 14 dni, pierwsza pełna kopia zapasowa każdego miesiąca przez 24 tygodnie i pełna kopia zapasowa 10 lat z 26. tygodnia roku.

### Przykład 5. Usuwanie długoterminowych zasad przechowywania
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

Usuwa zasady dla bazy danych 01, aby nie zapisywały już żadnych długoterminowych kopii zapasowych przechowywania.
Nie ma to wpływu na kopie zapasowe, które zostały już wykonane

### Przykład 6. Usuwanie długoterminowych zasad przechowywania
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

Jest to inny sposób usuwania zasad dla bazy danych 01, aby nie zapisywały już żadnych długoterminowych kopii zapasowych przechowywania.
Nie ma to wpływu na kopie zapasowe, które zostały już wykonane

## PARAMETERS

### -DatabaseName
Nazwa bazy danych Azure SQL Database, która ma być używania.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -MonthlyRetention
Miesięczne przechowywanie.
Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.
Maksymalna długość wynosi 7 dni i maksymalnie 10 lat.

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RemovePolicy
Jeśli zostanie to podane, zasady bazy danych zostaną usunięte.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

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
Nazwa serwera Azure SQL Server, w którym znajduje się baza danych.

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

### -WeeklyRetention
Tygodniowe przechowywanie.
Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.
Maksymalna długość wynosi 7 dni i maksymalnie 10 lat.

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - WeekOfYear
Tydzień roku, od 1 do 52, aby zapisać na przechowywanie co rok.

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - YearlyRetention
Przechowywanie co rok.
Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.
Maksymalna długość wynosi 7 dni i maksymalnie 10 lat.

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
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

### System.Int32

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel

## NOTATKI

## LINKI POKREWNE

[Get-AzSqlDatabaseBackupLongTermRetentionPolicy](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[Get-AzSqlDatabaseLongTermRetentionBackup](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[Remove-AzSqlDatabaseLongTermRetentionBackup](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)