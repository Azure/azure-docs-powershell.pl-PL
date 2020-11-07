---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: f8a31171309a9c869d29078ff09ce8903288e8bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93886734"
---
# <span data-ttu-id="8a6d1-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="8a6d1-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="8a6d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a6d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a6d1-103">**Ważne: to polecenie cmdlet jest przestarzałe, funkcja [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) zamienia je.**</span><span class="sxs-lookup"><span data-stu-id="8a6d1-103">**Important: This cmdlet is deprecated, [Set-AzSqlDatabaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="8a6d1-104">Zmienia ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-104">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="8a6d1-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a6d1-105">SYNTAX</span></span>

### <span data-ttu-id="8a6d1-106">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a6d1-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6d1-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="8a6d1-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6d1-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="8a6d1-108">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6d1-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="8a6d1-109">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6d1-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8a6d1-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6d1-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8a6d1-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a6d1-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8a6d1-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a6d1-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="8a6d1-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a6d1-114">Opis</span><span class="sxs-lookup"><span data-stu-id="8a6d1-114">DESCRIPTION</span></span>
<span data-ttu-id="8a6d1-115">Polecenie cmdlet **Set-AzSqlDatabaseAuditing** zmienia ustawienia inspekcji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-115">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="8a6d1-116">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-116">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="8a6d1-117">Miejsce docelowe dzienników inspekcji jest określane przez określenie jednego z następujących parametrów przełącznika: BlobStorage, LogAnalytics lub EventHub (jeśli nie jest określona, wartość domyślna to BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="8a6d1-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="8a6d1-118">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="8a6d1-119">Gdy miejsce docelowe dziennika inspekcji jest miejscem docelowym, określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* , aby zdefiniować klucze magazynowania.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="8a6d1-120">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="8a6d1-121">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt z opisem bieżących ustawień inspekcji oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="8a6d1-122">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-122">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="8a6d1-123">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a6d1-123">EXAMPLES</span></span>

### <span data-ttu-id="8a6d1-124">Przykład 1. Włączanie zasad inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-124">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="8a6d1-125">Przykład 2: wyłączanie zasad inspekcji magazynu obiektów BLOB bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-125">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="8a6d1-126">Przykład 3: Włączanie zasad inspekcji magazynu obiektów BLOB dla bazy danych Azure SQL Database przy użyciu konta magazynu z innej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8a6d1-126">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="8a6d1-127">Przykład 4: Włączanie zasad inspekcji magazynu obiektów BLOB bazy danych Azure SQL z filtrowaniem zaawansowanymi przy użyciu predykatu T-SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-127">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="8a6d1-128">Przykład 5: usuwanie ustawień filtrowania zaawansowanego z zasad inspekcji magazynu obiektów BLOB bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-128">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="8a6d1-129">Przykład 6: Włączanie zasad inspekcji centrum zdarzeń bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-129">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="8a6d1-130">Przykład 7: wyłączanie zasad inspekcji centrum zdarzeń bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-130">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="8a6d1-131">Przykład 8: Włączanie zasad inspekcji analizy dzienników bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-131">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="8a6d1-132">Przykład 9: wyłączenie zasad inspekcji analizy dzienników bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-132">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="8a6d1-133">Przykład 10: wyłączanie, za pośrednictwem rurociągu, zasady inspekcji analizy dzienników bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="8a6d1-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="8a6d1-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a6d1-134">PARAMETERS</span></span>

### <span data-ttu-id="8a6d1-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a6d1-135">-AsJob</span></span>
<span data-ttu-id="8a6d1-136">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8a6d1-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a6d1-137">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="8a6d1-137">-AuditAction</span></span>
<span data-ttu-id="8a6d1-138">Zestaw akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-138">The set of audit actions.</span></span>  
<span data-ttu-id="8a6d1-139">Obsługiwane działania podlegające inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="8a6d1-139">The supported actions to audit are:</span></span>  
<span data-ttu-id="8a6d1-140">ZAZNACZYSZ</span><span class="sxs-lookup"><span data-stu-id="8a6d1-140">SELECT</span></span>  
<span data-ttu-id="8a6d1-141">AKTUALIZOWANE</span><span class="sxs-lookup"><span data-stu-id="8a6d1-141">UPDATE</span></span>  
<span data-ttu-id="8a6d1-142">STAW</span><span class="sxs-lookup"><span data-stu-id="8a6d1-142">INSERT</span></span>  
<span data-ttu-id="8a6d1-143">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="8a6d1-143">DELETE</span></span>  
<span data-ttu-id="8a6d1-144">URUCHOMIĆ</span><span class="sxs-lookup"><span data-stu-id="8a6d1-144">EXECUTE</span></span>  
<span data-ttu-id="8a6d1-145">OTRZYMA</span><span class="sxs-lookup"><span data-stu-id="8a6d1-145">RECEIVE</span></span>  
<span data-ttu-id="8a6d1-146">Odwołuje się do formularza ogólnego definiującego akcję, która ma zostać poddana inspekcji, to: [Action] (obiekt [Object]) należy pamiętać, że [obiekt] w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok lub procedura składowana albo cała baza danych lub schemat.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-146">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="8a6d1-147">W tych przypadkach baza danych formularze: [dbname] i schemat:: [SchemaName] są używane odpowiednio.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-147">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="8a6d1-148">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="8a6d1-148">For example:</span></span>  
<span data-ttu-id="8a6d1-149">Wybierz pozycję na dbo. myTable według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="8a6d1-149">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="8a6d1-150">Wybierz w bazie danych:: Moja baza danych przez publiczną</span><span class="sxs-lookup"><span data-stu-id="8a6d1-150">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="8a6d1-151">Wybierz pozycję w SCHEMAcie:: moje schematy według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="8a6d1-151">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="8a6d1-152">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="8a6d1-152">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="8a6d1-153">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="8a6d1-153">-AuditActionGroup</span></span>
<span data-ttu-id="8a6d1-154">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="8a6d1-154">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="8a6d1-155">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8a6d1-155">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="8a6d1-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="8a6d1-156">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="8a6d1-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="8a6d1-157">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="8a6d1-158">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-158">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="8a6d1-159">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-159">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="8a6d1-160">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="8a6d1-160">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-161">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="8a6d1-161">-BlobStorage</span></span>
<span data-ttu-id="8a6d1-162">Określa, że miejsce docelowe dziennika inspekcji jest magazynem obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="8a6d1-162">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-163">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a6d1-163">-DatabaseName</span></span>
<span data-ttu-id="8a6d1-164">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-164">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-165">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a6d1-165">-DefaultProfile</span></span>
<span data-ttu-id="8a6d1-166">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-166">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a6d1-167">— EventHub</span><span class="sxs-lookup"><span data-stu-id="8a6d1-167">-EventHub</span></span>
<span data-ttu-id="8a6d1-168">Określa, że miejscem docelowym dziennika inspekcji jest centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="8a6d1-168">Specifies that audit logs destination is event hub</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-169">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6d1-169">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="8a6d1-170">Identyfikator zasobu dla reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="8a6d1-170">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-171">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="8a6d1-171">-EventHubName</span></span>
<span data-ttu-id="8a6d1-172">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-172">The name of the event hub.</span></span> <span data-ttu-id="8a6d1-173">Jeśli w trakcie dostarczania EventHubAuthorizationRuleResourceId zostanie wybrana opcja Brak, zostanie wybrany domyślny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-173">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHubSet, EventHubByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-174">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a6d1-174">-InputObject</span></span>
<span data-ttu-id="8a6d1-175">Obiekt bazy danych do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-175">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-176">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="8a6d1-176">-LogAnalytics</span></span>
<span data-ttu-id="8a6d1-177">Określa, że miejscem docelowym dziennika inspekcji jest Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="8a6d1-177">Specifies that audit logs destination is log analytics</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-178">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a6d1-178">-PassThru</span></span>
<span data-ttu-id="8a6d1-179">Określa, czy ma być wyprowadzana zasada inspekcji na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-179">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="8a6d1-180">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="8a6d1-180">-PredicateExpression</span></span>
<span data-ttu-id="8a6d1-181">Predykat T-SQL (klauzula WHERE) służący do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-181">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="8a6d1-182">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a6d1-182">-ResourceGroupName</span></span>
<span data-ttu-id="8a6d1-183">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-183">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-184">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="8a6d1-184">-RetentionInDays</span></span>
<span data-ttu-id="8a6d1-185">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-185">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-186">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="8a6d1-186">-ServerName</span></span>
<span data-ttu-id="8a6d1-187">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-187">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-188">-State</span><span class="sxs-lookup"><span data-stu-id="8a6d1-188">-State</span></span>
<span data-ttu-id="8a6d1-189">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-189">The state of the policy.</span></span>

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

### <span data-ttu-id="8a6d1-190">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8a6d1-190">-StorageAccountName</span></span>
<span data-ttu-id="8a6d1-191">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-191">The name of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-192">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a6d1-192">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="8a6d1-193">Identyfikator subskrypcji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="8a6d1-193">The storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-194">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="8a6d1-194">-StorageKeyType</span></span>
<span data-ttu-id="8a6d1-195">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-195">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, StorageAccountSubscriptionIdSet, BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-196">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="8a6d1-196">-WorkspaceResourceId</span></span>
<span data-ttu-id="8a6d1-197">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analizy dzienników) dla obszaru roboczego analizy dzienników, do którego mają być wysyłane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-197">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="8a6d1-198">Przykład:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="8a6d1-198">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: LogAnalyticsSet, LogAnalyticsByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a6d1-199">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a6d1-199">-Confirm</span></span>
<span data-ttu-id="8a6d1-200">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a6d1-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a6d1-201">-WhatIf</span></span>
<span data-ttu-id="8a6d1-202">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a6d1-203">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a6d1-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a6d1-204">CommonParameters</span></span>
<span data-ttu-id="8a6d1-205">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a6d1-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a6d1-206">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a6d1-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a6d1-207">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a6d1-207">INPUTS</span></span>

### <span data-ttu-id="8a6d1-208">System. String</span><span class="sxs-lookup"><span data-stu-id="8a6d1-208">System.String</span></span>

### <span data-ttu-id="8a6d1-209">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8a6d1-209">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="8a6d1-210">Microsoft. Azure. Commands. SQL. Audit. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="8a6d1-210">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="8a6d1-211">System. String []</span><span class="sxs-lookup"><span data-stu-id="8a6d1-211">System.String[]</span></span>

### <span data-ttu-id="8a6d1-212">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a6d1-212">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8a6d1-213">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8a6d1-213">System.Guid</span></span>

### <span data-ttu-id="8a6d1-214">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="8a6d1-214">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="8a6d1-215">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a6d1-215">OUTPUTS</span></span>

### <span data-ttu-id="8a6d1-216">Microsoft. Azure. Commands. SQL. Audit. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="8a6d1-216">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="8a6d1-217">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a6d1-217">NOTES</span></span>

## <span data-ttu-id="8a6d1-218">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a6d1-218">RELATED LINKS</span></span>
