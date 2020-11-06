---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 72E0E558-74D7-4A50-A975-FA7D0C0B301E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Restore-AzureRmSqlDatabase.md
ms.openlocfilehash: 61f66a61d14738da034644fc3dfef865c8719181
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542831"
---
# Restore-AzureRmSqlDatabase

## STRESZCZENIe
Przywraca bazę danych SQL.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### FromPointInTimeBackup
```
Restore-AzureRmSqlDatabase [-FromPointInTimeBackup] -PointInTime <DateTime> -ResourceId <String>
 -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromDeletedDatabaseBackup
```
Restore-AzureRmSqlDatabase [-FromDeletedDatabaseBackup] [-PointInTime <DateTime>] -DeletionDate <DateTime>
 -ResourceId <String> -ServerName <String> -TargetDatabaseName <String> [-Edition <DatabaseEdition>]
 [-ServiceObjectiveName <String>] [-ElasticPoolName <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FromGeoBackup
```
Restore-AzureRmSqlDatabase [-FromGeoBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### FromLongTermRetentionBackup
```
Restore-AzureRmSqlDatabase [-FromLongTermRetentionBackup] -ResourceId <String> -ServerName <String>
 -TargetDatabaseName <String> [-Edition <DatabaseEdition>] [-ServiceObjectiveName <String>]
 [-ElasticPoolName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Restore-AzureRmSqlDatabase** przywraca bazę danych SQL z kopii zapasowej Geo-rezerwowej, kopii zapasowej usuniętej bazy danych, kopii zapasowej długotrwałego przechowywania lub punktu w czasie w bazie danych na żywo.
Przywrócona baza danych zostanie utworzona jako nowa baza danych.

Można utworzyć elastyczną bazę danych SQL, ustawiając parametr *ElasticPoolName* na istniejącą pulę elastyczną.

## Przykłady

### Przykład 1: Przywracanie bazy danych z punktu w czasie
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -Edition "Standard" -ServiceObjectiveName "S2"
```

Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w zmiennej $Database.

Drugie polecenie przywraca bazę danych w $Database z określonego momentu kopii zapasowej do bazy danych o nazwie RestoredDatabase.

### Przykład 2: Przywracanie bazy danych od punktu w czasie do puli elastycznej
```
PS C:\>$Database = Get-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromPointInTimeBackup -PointInTime UTCDateTime -ResourceGroupName $Database.ResourceGroupName -ServerName $Database.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $Database.ResourceID -ElasticPoolName "ElasticPool01"
```

Pierwsze polecenie pobiera bazę danych SQL o nazwie Database01, a następnie zapisuje ją w zmiennej $Database.

Drugie polecenie przywraca bazę danych w $Database z określonego momentu kopii zapasowej bazy danych SQL o nazwie RestoredDatabase w elastycznej puli o nazwie elasticpool01.

### Przykład 3: Przywracanie usuniętej bazy danych
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -Edition "Standard" -ServiceObjectiveName "S2" -PointInTime UTCDateTime
```

Pierwsze polecenie powoduje pobranie usuniętej kopii zapasowej bazy danych, która ma zostać przywrócona przy użyciu polecenia [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).
Drugie polecenie rozpoczyna przywracanie z usuniętej kopii zapasowej bazy danych przy użyciu polecenia cmdlet [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md) . Jeśli nie określono parametru-PointInTime, baza danych zostanie przywrócona do godziny usunięcia.

### Przykład 4: Przywracanie usuniętej bazy danych do puli elastycznej
```
PS C:\>$DeletedDatabase = Get-AzureRmSqlDeletedDatabaseBackup -ResourceGroupName $resourceGroupName -ServerName $sqlServerName -DatabaseName 'DatabaseToRestore'
PS C:\> Restore-AzureRmSqlDatabase -FromDeletedDatabaseBackup -DeletionDate $DeletedDatabase.DeletionDate -ResourceGroupName $DeletedDatabase.ResourceGroupName -ServerName $DeletedDatabase.ServerName -TargetDatabaseName "RestoredDatabase" -ResourceId $DeletedDatabase.ResourceID -ElasticPoolName "elasticpool01" -PointInTime UTCDateTime
```

Pierwsze polecenie powoduje pobranie usuniętej kopii zapasowej bazy danych, która ma zostać przywrócona przy użyciu polecenia [Get-AzureRmSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md).
Drugie polecenie rozpoczyna przywracanie z usuniętej kopii zapasowej bazy danych za pomocą polecenia [Restore-AzureRmSqlDatabase](./Restore-AzureRmSqlDatabase.md). Jeśli nie określono parametru-PointInTime, baza danych zostanie przywrócona do godziny usunięcia.

### Przykład 5: Geo-Restore bazy danych
```
PS C:\>$GeoBackup = Get-AzureRmSqlDatabaseGeoBackup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\> Restore-AzureRmSqlDatabase -FromGeoBackup -ResourceGroupName "TargetResourceGroup" -ServerName "TargetServer" -TargetDatabaseName "RestoredDatabase" -ResourceId $GeoBackup.ResourceID -Edition "Standard" -RequestedServiceObjectiveName "S2"
```

Pierwsze polecenie pobiera kopię zapasową Geo-nadmiarową bazy danych o nazwie Database01, a następnie zapisuje ją w zmiennej $GeoBackup.

Drugie polecenie przywraca kopię zapasową w $GeoBackup bazie danych SQL o nazwie RestoredDatabase.

## PARAMETRÓW

### -DeletionDate
Określa datę usunięcia jako obiekt **DateTime** .
Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Edition
Określa wersję bazy danych SQL.
Dopuszczalne wartości tego parametru to:

- Znaleziono
- Ubezpieczeni
- Podstawowym
- Standard
- DataWarehouse
- Niezależnych

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ElasticPoolName
Określa nazwę puli elastycznej, w której ma zostać umieszczona baza danych SQL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FromDeletedDatabaseBackup
Wskazuje, że to polecenie cmdlet przywraca bazę danych z kopii zapasowej usuniętej bazy danych SQL.
Możesz użyć polecenia cmdlet Get-AzureRMSqlDeletedDatabaseBackup, aby pobrać kopię zapasową usuniętej bazy danych SQL.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromGeoBackup
Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z kopii zapasowej Geo-nadmiarowej.
Możesz użyć polecenia cmdlet Get-AzureRMSqlDatabaseGeoBackup, aby uzyskać kopię zapasową Geo-nadmiarową.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromGeoBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromLongTermRetentionBackup
Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL po długim czasie przechowywania kopii zapasowej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromLongTermRetentionBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FromPointInTimeBackup
Wskazuje, że to polecenie cmdlet przywraca bazę danych SQL z kopii zapasowej w czasie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PointInTime
Określa punkt w postaci obiektu **DateTime** , na który ma być przywracana baza danych SQL.
Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .

Ten parametr jest używany razem z parametrem *FromPointInTimeBackup* .

```yaml
Type: System.DateTime
Parameter Sets: FromPointInTimeBackup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: FromDeletedDatabaseBackup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, z którą to polecenie cmdlet przypisuje bazę danych SQL.

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

### -ResourceId
Określa identyfikator zasobu do przywrócenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera bazy danych SQL.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Servicecelname
Określa nazwę celu usługi.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetDatabaseName
Określa nazwę bazy danych, do której ma zostać przywrócona operacja.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel

## INFORMACYJN

## LINKI POKREWNE

[Odzyskiwanie bazy danych SQL Azure z awarii](https://go.microsoft.com/fwlink/?LinkId=746882)

[Odzyskiwanie bazy danych SQL Azure przy użyciu błędu użytkownika](https://go.microsoft.com/fwlink/?LinkId=746944)

[Get-AzureRmSqlDatabase](./Get-AzureRmSqlDatabase.md)

[Get-AzureRMSqlDatabaseGeoBackup](./Get-AzureRMSqlDatabaseGeoBackup.md)

[Get-AzureRMSqlDeletedDatabaseBackup](./Get-AzureRMSqlDeletedDatabaseBackup.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)

