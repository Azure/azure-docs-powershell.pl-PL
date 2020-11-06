---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 9f551b5b334f6151b42faebf8b60d2939a0680d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542179"
---
# Set-AzureRmSqlDatabaseAuditingPolicy

## STRESZCZENIe
Ustawia zasady inspekcji dla bazy danych.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmSqlDatabaseAuditingPolicy** powoduje zmianę zasad inspekcji bazy danych Azure SQL.
Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.
Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.

Możesz również zdefiniować przechowywanie w tabeli Dziennik inspekcji, ustawiając wartość parametrów *RetentionInDays* i *TableIdentifier* , aby zdefiniować okres i materiał siewny dla nazw tabel dziennika inspekcji.
Określ parametr *EventType* definiujący typy zdarzeń do inspekcji.

Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja bazy danych jest włączona.
W przypadku inspekcji tabeli Jeśli baza danych korzystała z zasad serwera w celu prowadzenia inspekcji przed uruchomieniem tego polecenia cmdlet, inspekcja przestanie działać przy użyciu tych zasad. W przypadku inspekcji obiektu BLOB, jeśli baza danych korzystała z zasad serwera w celu prowadzenia inspekcji przed uruchomieniem tego polecenia cmdlet, obie zasady inspekcji będą istnieć obok siebie.
Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji oprócz identyfikatorów bazy danych.
Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.

To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.

## Przykłady

### Przykład 1: Ustawianie zasad inspekcji bazy danych w celu korzystania z inspekcji tabeli
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01 w celu użycia konta magazynu o nazwie Storage31.

### Przykład 2: Ustawianie klucza konta magazynu istniejących zasad inspekcji bazy danych
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01, aby nadal korzystać z tej samej nazwy konta magazynu, a następnie używać klucza pomocniczego.

### Przykład 3: Ustawianie zasad inspekcji bazy danych w celu używania określonego typu zdarzenia
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### Przykład 4: Ustawianie zasad inspekcji bazy danych w celu używania inspekcji obiektów BLOB
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01.
Zasady rejestrują typ zdarzenia Login_Failure.
Polecenie nie powoduje zmiany ustawień miejsca do magazynowania.

## PARAMETRÓW

### -AuditAction
Określ co najmniej jedno działanie inspekcji.
Ten parametr dotyczy tylko inspekcji obiektu BLOB.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditActionGroup
Określanie jednej lub kilku grup akcji inspekcji.
Ten parametr dotyczy tylko inspekcji obiektu BLOB.

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Audittype
```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DatabaseName
Określa nazwę bazy danych.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -EventType
Określa typy zdarzeń do inspekcji.
Ten parametr dotyczy tylko inspekcji tabeli.

Możesz określić kilka typów zdarzeń.
Możesz określić, czy wszystkie typy zdarzeń mają być poddawane inspekcji, czy żadne zdarzenia nie będą poddawane inspekcji.
W przypadku jednoczesnego określenia wszystkich lub brakujących poleceń nie można uruchomić polecenia cmdlet.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów, do której jest przypisana baza danych.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Określa liczbę dni przechowywania w tabeli Dziennik inspekcji.
Wartość zero (0) oznacza, że tabela nie jest zachowywana.
Wartość domyślna to zero.
Jeśli określisz wartość większą niż zero, musisz określić wartość parametru *TableIdentifer* .

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Nazwa_serwera
Określa nazwę serwera, na którym jest przechowywana baza danych.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Określa nazwę konta magazynu do inspekcji bazy danych.
Znaki wieloznaczne są niedozwolone.
Ten parametr nie jest wymagany.
Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji bazy danych.
Jeśli zasady inspekcji bazy danych są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKeyType
Określa, który z kluczy dostępu do magazynowania ma być używany.
Dopuszczalne wartości tego parametru to:

- Początkowe
- Dodatkowej

Wartość domyślna to Primary (podstawowy).

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableIdentifier
Określa nazwę tabeli dzienników inspekcji.
Określ tę wartość, jeśli dla parametru *RetentionInDays* określono wartość większą niż zero.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
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

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. SQL. Security. model. DatabaseAuditingPolicyModel

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmSqlDatabaseAuditingPolicy](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[Remove-AzureRmSqlDatabaseAuditing](./Remove-AzureRmSqlDatabaseAuditing.md)

[Dokumentacja bazy danych SQL](https://docs.microsoft.com/azure/sql-database/)


