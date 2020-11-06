---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: e28295a5f743e1475075e93a52c21bba8bd83e08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527782"
---
# Set-AzureRmSqlDatabaseAuditing

## STRESZCZENIe
Zmienia ustawienia inspekcji bazy danych SQL Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### DefaultParameterSet (domyślny)
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### StorageAccountSubscriptionIdSet
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmSqlDatabaseAuditing** zmienia ustawienia inspekcji bazy danych Azure SQL Database.
Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.
Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.
Użyj parametru *State* , aby włączyć/wyłączyć zasady.
Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.
Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja bazy danych jest włączona.
Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji obiektu BLOB oprócz identyfikatorów bazy danych.
Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.

## Przykłady

### Przykład 1. Włączanie zasad inspekcji bazy danych Azure SQL Database
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### Przykład 2: wyłączanie zasad inspekcji obiektu BLOB bazy danych Azure SQL Database
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### Przykład 3: Włączanie zasad inspekcji bazy danych usługi Azure SQL przy użyciu konta magazynu z innej subskrypcji
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### Przykład 4: Włączanie rozszerzonych zasad inspekcji bazy danych Azure SQL Database
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### Przykład 5: usuwanie zasad inspekcji rozszerzonej bazy danych usługi Azure SQL i Ustawianie zasad inspekcji zamiast tej funkcji.
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## PARAMETRÓW

### -AuditAction
Zestaw akcji inspekcji.
Obsługiwane działania podlegające inspekcji są następujące: wybierz pozycję Aktualizuj Wstawianie, wykonywanie Odbierz odwołują się do formularza ogólnego definiującego akcję, która ma być poddana inspekcji, to: [Action] ([Object] (obiekt]) należy pamiętać, że [obiekt] w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok lub procedura składowana albo cała baza danych lub schemat. W tych przypadkach baza danych formularze: [dbname] i schemat:: [SchemaName] są używane odpowiednio.
Na przykład: wybierz pozycję w witrynie dbo. myTable według publicznej wybierz pozycję w bazie danych:: Moja baza danych przez publiczną wybierz pozycję w SCHEMAcie:: moje schematy według opinii publicznej Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditActionGroup
Zalecany zestaw grup akcji, który ma być używany, to następująca kombinacja — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Ta powyższa kombinacja jest również skonfigurowanym ustawieniem domyślnym. Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji. Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Nazwa bazy danych SQL.

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

### -PassThru
{{Fill PassThru Description}}

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -PredicateExpression
Instrukcja klauzuli WHERE użytej do filtrowania dzienników inspekcji.

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

### -RetentionInDays
Liczba dni przechowywania dzienników inspekcji.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nazwa_serwera
Nazwa serwera bazy danych SQL.

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

### -State
Stan zasad.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Nazwa konta magazynu. Znaki wieloznaczne są niedozwolone.
Ten parametr nie jest wymagany.
Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji.
Jeśli zasady inspekcji są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountSubscriptionId
Określa identyfikator subskrypcji konta magazynu

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
Określa, który z kluczy dostępu do magazynowania ma być używany.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE
