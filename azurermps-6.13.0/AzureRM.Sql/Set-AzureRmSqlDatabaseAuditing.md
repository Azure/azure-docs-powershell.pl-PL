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
# <span data-ttu-id="cac5c-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="cac5c-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="cac5c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cac5c-102">SYNOPSIS</span></span>
<span data-ttu-id="cac5c-103">Zmienia ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cac5c-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cac5c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cac5c-104">SYNTAX</span></span>

### <span data-ttu-id="cac5c-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cac5c-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cac5c-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="cac5c-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cac5c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cac5c-107">DESCRIPTION</span></span>
<span data-ttu-id="cac5c-108">Polecenie cmdlet **Set-AzureRmSqlDatabaseAuditing** zmienia ustawienia inspekcji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="cac5c-108">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="cac5c-109">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cac5c-109">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="cac5c-110">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="cac5c-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="cac5c-111">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="cac5c-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="cac5c-112">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cac5c-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="cac5c-113">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja bazy danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="cac5c-113">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="cac5c-114">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji obiektu BLOB oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="cac5c-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="cac5c-115">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="cac5c-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="cac5c-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cac5c-116">EXAMPLES</span></span>

### <span data-ttu-id="cac5c-117">Przykład 1. Włączanie zasad inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="cac5c-117">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="cac5c-118">Przykład 2: wyłączanie zasad inspekcji obiektu BLOB bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="cac5c-118">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="cac5c-119">Przykład 3: Włączanie zasad inspekcji bazy danych usługi Azure SQL przy użyciu konta magazynu z innej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cac5c-119">Example 3: Enable the auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="cac5c-120">Przykład 4: Włączanie rozszerzonych zasad inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="cac5c-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="cac5c-121">Przykład 5: usuwanie zasad inspekcji rozszerzonej bazy danych usługi Azure SQL i Ustawianie zasad inspekcji zamiast tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="cac5c-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="cac5c-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cac5c-122">PARAMETERS</span></span>

### <span data-ttu-id="cac5c-123">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="cac5c-123">-AuditAction</span></span>
<span data-ttu-id="cac5c-124">Zestaw akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cac5c-124">The set of audit actions.</span></span>
<span data-ttu-id="cac5c-125">Obsługiwane działania podlegające inspekcji są następujące: wybierz pozycję Aktualizuj Wstawianie, wykonywanie Odbierz odwołują się do formularza ogólnego definiującego akcję, która ma być poddana inspekcji, to: [Action] ([Object] (obiekt]) należy pamiętać, że [obiekt] w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok lub procedura składowana albo cała baza danych lub schemat.</span><span class="sxs-lookup"><span data-stu-id="cac5c-125">The supported actions to audit are: SELECT UPDATE INSERT DELETE EXECUTE RECEIVE REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="cac5c-126">W tych przypadkach baza danych formularze: [dbname] i schemat:: [SchemaName] są używane odpowiednio.</span><span class="sxs-lookup"><span data-stu-id="cac5c-126">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="cac5c-127">Na przykład: wybierz pozycję w witrynie dbo. myTable według publicznej wybierz pozycję w bazie danych:: Moja baza danych przez publiczną wybierz pozycję w SCHEMAcie:: moje schematy według opinii publicznej Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="cac5c-127">For example: SELECT on dbo.myTable by public SELECT on DATABASE::myDatabase by public SELECT on SCHEMA::mySchema by public For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="cac5c-128">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="cac5c-128">-AuditActionGroup</span></span>
<span data-ttu-id="cac5c-129">Zalecany zestaw grup akcji, który ma być używany, to następująca kombinacja — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Ta powyższa kombinacja jest również skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="cac5c-129">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="cac5c-130">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cac5c-130">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="cac5c-131">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="cac5c-131">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="cac5c-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cac5c-132">-DatabaseName</span></span>
<span data-ttu-id="cac5c-133">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="cac5c-133">SQL Database name.</span></span>

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

### <span data-ttu-id="cac5c-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac5c-134">-DefaultProfile</span></span>
<span data-ttu-id="cac5c-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cac5c-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac5c-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cac5c-136">-PassThru</span></span>
<span data-ttu-id="cac5c-137">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="cac5c-137">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="cac5c-138">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="cac5c-138">-PredicateExpression</span></span>
<span data-ttu-id="cac5c-139">Instrukcja klauzuli WHERE użytej do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cac5c-139">The statement of the Where Clause used to filter audit logs.</span></span>

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

### <span data-ttu-id="cac5c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac5c-140">-ResourceGroupName</span></span>
<span data-ttu-id="cac5c-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cac5c-141">The name of the resource group.</span></span>

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

### <span data-ttu-id="cac5c-142">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cac5c-142">-RetentionInDays</span></span>
<span data-ttu-id="cac5c-143">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cac5c-143">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="cac5c-144">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="cac5c-144">-ServerName</span></span>
<span data-ttu-id="cac5c-145">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="cac5c-145">SQL Database server name.</span></span>

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

### <span data-ttu-id="cac5c-146">-State</span><span class="sxs-lookup"><span data-stu-id="cac5c-146">-State</span></span>
<span data-ttu-id="cac5c-147">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="cac5c-147">The state of the policy.</span></span>

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

### <span data-ttu-id="cac5c-148">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="cac5c-148">-StorageAccountName</span></span>
<span data-ttu-id="cac5c-149">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="cac5c-149">The name of the storage account.</span></span> <span data-ttu-id="cac5c-150">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="cac5c-150">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="cac5c-151">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="cac5c-151">This parameter is not required.</span></span>
<span data-ttu-id="cac5c-152">Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cac5c-152">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="cac5c-153">Jeśli zasady inspekcji są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="cac5c-153">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="cac5c-154">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cac5c-154">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="cac5c-155">Określa identyfikator subskrypcji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="cac5c-155">Specifies storage account subscription id</span></span>

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

### <span data-ttu-id="cac5c-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="cac5c-156">-StorageKeyType</span></span>
<span data-ttu-id="cac5c-157">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="cac5c-157">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="cac5c-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cac5c-158">-Confirm</span></span>
<span data-ttu-id="cac5c-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cac5c-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cac5c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cac5c-160">-WhatIf</span></span>
<span data-ttu-id="cac5c-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cac5c-161">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cac5c-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cac5c-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cac5c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac5c-163">CommonParameters</span></span>
<span data-ttu-id="cac5c-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cac5c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac5c-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac5c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac5c-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cac5c-166">INPUTS</span></span>

## <span data-ttu-id="cac5c-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cac5c-167">OUTPUTS</span></span>

## <span data-ttu-id="cac5c-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cac5c-168">NOTES</span></span>

## <span data-ttu-id="cac5c-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cac5c-169">RELATED LINKS</span></span>
