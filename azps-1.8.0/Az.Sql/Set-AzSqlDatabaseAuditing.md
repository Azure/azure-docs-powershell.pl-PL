---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 511207be4094dae96f8d138124021ce2f8ed3913
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707769"
---
# <span data-ttu-id="61151-101">Set-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="61151-101">Set-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="61151-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="61151-102">SYNOPSIS</span></span>
<span data-ttu-id="61151-103">Zmienia ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="61151-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="61151-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="61151-104">SYNTAX</span></span>

### <span data-ttu-id="61151-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="61151-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] [-StorageAccountName <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61151-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="61151-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-BlobStorage] -StorageAccountName <String>
 -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61151-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="61151-107">EventHubSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-EventHub] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61151-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="61151-108">LogAnalyticsSet</span></span>
```
Set-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-AsJob] [-WorkspaceResourceId <String>] [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61151-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="61151-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61151-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="61151-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-BlobStorage] -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="61151-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="61151-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61151-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="61151-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> -State <String> [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61151-113">Opis</span><span class="sxs-lookup"><span data-stu-id="61151-113">DESCRIPTION</span></span>
<span data-ttu-id="61151-114">Polecenie cmdlet **Set-AzSqlDatabaseAuditing** zmienia ustawienia inspekcji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="61151-114">The **Set-AzSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="61151-115">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="61151-115">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="61151-116">Miejsce docelowe dzienników inspekcji jest określane przez określenie jednego z następujących parametrów przełącznika: BlobStorage, LogAnalytics lub EventHub (jeśli nie jest określona, wartość domyślna to BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="61151-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="61151-117">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="61151-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="61151-118">Gdy miejsce docelowe dziennika inspekcji jest miejscem docelowym, określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* , aby zdefiniować klucze magazynowania.</span><span class="sxs-lookup"><span data-stu-id="61151-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="61151-119">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="61151-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="61151-120">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt z opisem bieżących ustawień inspekcji oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="61151-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the database identifiers.</span></span>
<span data-ttu-id="61151-121">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="61151-121">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="61151-122">Przykłady</span><span class="sxs-lookup"><span data-stu-id="61151-122">EXAMPLES</span></span>

### <span data-ttu-id="61151-123">Przykład 1. Włączanie zasad inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-123">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="61151-124">Przykład 2: wyłączanie zasad inspekcji magazynu obiektów BLOB bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-124">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

### <span data-ttu-id="61151-125">Przykład 3: Włączanie zasad inspekcji magazynu obiektów BLOB dla bazy danych Azure SQL Database przy użyciu konta magazynu z innej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="61151-125">Example 3: Enable the blob storage auditing policy of an Azure SQL database using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="61151-126">Przykład 4: Włączanie zasad inspekcji magazynu obiektów BLOB bazy danych Azure SQL z filtrowaniem zaawansowanymi przy użyciu predykatu T-SQL</span><span class="sxs-lookup"><span data-stu-id="61151-126">Example 4: Enable the blob storage auditing policy of an Azure SQL database with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="61151-127">Przykład 5: usuwanie ustawień filtrowania zaawansowanego z zasad inspekcji magazynu obiektów BLOB bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-127">Example 5: Remove the advanced filtering setting from the blob storage auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="61151-128">Przykład 6: Włączanie zasad inspekcji centrum zdarzeń bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-128">Example 6: Enable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="61151-129">Przykład 7: wyłączanie zasad inspekcji centrum zdarzeń bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-129">Example 7: Disable the event hub auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHub
```

### <span data-ttu-id="61151-130">Przykład 8: Włączanie zasad inspekcji analizy dzienników bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-130">Example 8: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="61151-131">Przykład 9: wyłączenie zasad inspekcji analizy dzienników bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-131">Example 9: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
```

### <span data-ttu-id="61151-132">Przykład 10: wyłączanie, za pośrednictwem rurociągu, zasady inspekcji analizy dzienników bazy danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="61151-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="61151-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61151-133">PARAMETERS</span></span>

### <span data-ttu-id="61151-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61151-134">-AsJob</span></span>
<span data-ttu-id="61151-135">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="61151-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61151-136">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="61151-136">-AuditAction</span></span>
<span data-ttu-id="61151-137">Zestaw akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="61151-137">The set of audit actions.</span></span>  
<span data-ttu-id="61151-138">Obsługiwane działania podlegające inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="61151-138">The supported actions to audit are:</span></span>  
<span data-ttu-id="61151-139">ZAZNACZYSZ</span><span class="sxs-lookup"><span data-stu-id="61151-139">SELECT</span></span>  
<span data-ttu-id="61151-140">AKTUALIZOWANE</span><span class="sxs-lookup"><span data-stu-id="61151-140">UPDATE</span></span>  
<span data-ttu-id="61151-141">STAW</span><span class="sxs-lookup"><span data-stu-id="61151-141">INSERT</span></span>  
<span data-ttu-id="61151-142">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="61151-142">DELETE</span></span>  
<span data-ttu-id="61151-143">URUCHOMIĆ</span><span class="sxs-lookup"><span data-stu-id="61151-143">EXECUTE</span></span>  
<span data-ttu-id="61151-144">OTRZYMA</span><span class="sxs-lookup"><span data-stu-id="61151-144">RECEIVE</span></span>  
<span data-ttu-id="61151-145">Odwołuje się do formularza ogólnego definiującego akcję, która ma zostać poddana inspekcji, to: [Action] (obiekt [Object]) należy pamiętać, że [obiekt] w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok lub procedura składowana albo cała baza danych lub schemat.</span><span class="sxs-lookup"><span data-stu-id="61151-145">REFERENCES The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="61151-146">W tych przypadkach baza danych formularze: [dbname] i schemat:: [SchemaName] są używane odpowiednio.</span><span class="sxs-lookup"><span data-stu-id="61151-146">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="61151-147">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="61151-147">For example:</span></span>  
<span data-ttu-id="61151-148">Wybierz pozycję na dbo. myTable według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="61151-148">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="61151-149">Wybierz w bazie danych:: Moja baza danych przez publiczną</span><span class="sxs-lookup"><span data-stu-id="61151-149">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="61151-150">Wybierz pozycję w SCHEMAcie:: moje schematy według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="61151-150">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="61151-151">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="61151-151">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="61151-152">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="61151-152">-AuditActionGroup</span></span>
<span data-ttu-id="61151-153">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="61151-153">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="61151-154">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="61151-154">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="61151-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="61151-155">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="61151-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="61151-156">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="61151-157">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="61151-157">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="61151-158">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="61151-158">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="61151-159">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="61151-159">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="61151-160">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="61151-160">-BlobStorage</span></span>
<span data-ttu-id="61151-161">Określa, że miejsce docelowe dziennika inspekcji jest magazynem obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="61151-161">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="61151-162">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="61151-162">-DatabaseName</span></span>
<span data-ttu-id="61151-163">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="61151-163">SQL Database name.</span></span>

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

### <span data-ttu-id="61151-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61151-164">-DefaultProfile</span></span>
<span data-ttu-id="61151-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="61151-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61151-166">— EventHub</span><span class="sxs-lookup"><span data-stu-id="61151-166">-EventHub</span></span>
<span data-ttu-id="61151-167">Określa, że miejscem docelowym dziennika inspekcji jest centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="61151-167">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="61151-168">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="61151-168">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="61151-169">Identyfikator zasobu dla reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="61151-169">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="61151-170">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="61151-170">-EventHubName</span></span>
<span data-ttu-id="61151-171">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="61151-171">The name of the event hub.</span></span> <span data-ttu-id="61151-172">Jeśli w trakcie dostarczania EventHubAuthorizationRuleResourceId zostanie wybrana opcja Brak, zostanie wybrany domyślny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="61151-172">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="61151-173">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="61151-173">-InputObject</span></span>
<span data-ttu-id="61151-174">Obiekt bazy danych do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="61151-174">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="61151-175">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="61151-175">-LogAnalytics</span></span>
<span data-ttu-id="61151-176">Określa, że miejscem docelowym dziennika inspekcji jest Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="61151-176">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="61151-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61151-177">-PassThru</span></span>
<span data-ttu-id="61151-178">Określa, czy ma być wyprowadzana zasada inspekcji na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61151-178">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="61151-179">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="61151-179">-PredicateExpression</span></span>
<span data-ttu-id="61151-180">Predykat T-SQL (klauzula WHERE) służący do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="61151-180">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="61151-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61151-181">-ResourceGroupName</span></span>
<span data-ttu-id="61151-182">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61151-182">The name of the resource group.</span></span>

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

### <span data-ttu-id="61151-183">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="61151-183">-RetentionInDays</span></span>
<span data-ttu-id="61151-184">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="61151-184">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="61151-185">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="61151-185">-ServerName</span></span>
<span data-ttu-id="61151-186">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="61151-186">SQL server name.</span></span>

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

### <span data-ttu-id="61151-187">-State</span><span class="sxs-lookup"><span data-stu-id="61151-187">-State</span></span>
<span data-ttu-id="61151-188">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="61151-188">The state of the policy.</span></span>

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

### <span data-ttu-id="61151-189">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="61151-189">-StorageAccountName</span></span>
<span data-ttu-id="61151-190">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="61151-190">The name of the storage account.</span></span>

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

### <span data-ttu-id="61151-191">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61151-191">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="61151-192">Identyfikator subskrypcji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="61151-192">The storage account subscription id</span></span>

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

### <span data-ttu-id="61151-193">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="61151-193">-StorageKeyType</span></span>
<span data-ttu-id="61151-194">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="61151-194">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="61151-195">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="61151-195">-WorkspaceResourceId</span></span>
<span data-ttu-id="61151-196">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analizy dzienników) dla obszaru roboczego analizy dzienników, do którego mają być wysyłane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="61151-196">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="61151-197">Przykład:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="61151-197">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="61151-198">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="61151-198">-Confirm</span></span>
<span data-ttu-id="61151-199">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61151-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61151-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61151-200">-WhatIf</span></span>
<span data-ttu-id="61151-201">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61151-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61151-202">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="61151-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="61151-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61151-203">CommonParameters</span></span>
<span data-ttu-id="61151-204">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61151-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61151-205">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61151-205">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61151-206">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61151-206">INPUTS</span></span>

### <span data-ttu-id="61151-207">System. String</span><span class="sxs-lookup"><span data-stu-id="61151-207">System.String</span></span>

### <span data-ttu-id="61151-208">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="61151-208">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="61151-209">Microsoft. Azure. Commands. SQL. Audit. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="61151-209">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="61151-210">System. String []</span><span class="sxs-lookup"><span data-stu-id="61151-210">System.String[]</span></span>

### <span data-ttu-id="61151-211">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="61151-211">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="61151-212">System. GUID</span><span class="sxs-lookup"><span data-stu-id="61151-212">System.Guid</span></span>

### <span data-ttu-id="61151-213">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="61151-213">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="61151-214">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="61151-214">OUTPUTS</span></span>

### <span data-ttu-id="61151-215">Microsoft. Azure. Commands. SQL. Audit. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="61151-215">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="61151-216">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="61151-216">NOTES</span></span>

## <span data-ttu-id="61151-217">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61151-217">RELATED LINKS</span></span>
