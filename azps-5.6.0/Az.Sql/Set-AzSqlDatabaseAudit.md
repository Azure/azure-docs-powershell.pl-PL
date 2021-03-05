---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlDatabaseAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAudit.md
ms.openlocfilehash: 6e3c5c935f6703f5c4f29b2a4ae793fc48e9b16f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995009"
---
# <span data-ttu-id="e9bd8-101">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="e9bd8-101">Set-AzSqlDatabaseAudit</span></span>

## <span data-ttu-id="e9bd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9bd8-102">SYNOPSIS</span></span>
<span data-ttu-id="e9bd8-103">Zmienia ustawienia inspekcji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-103">Changes the auditing settings for an Azure SQL database.</span></span>

## <span data-ttu-id="e9bd8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9bd8-104">SYNTAX</span></span>

### <span data-ttu-id="e9bd8-105">DatabaseParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e9bd8-105">DatabaseParameterSet (Default)</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9bd8-106">DatabaseObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9bd8-106">DatabaseObjectParameterSet</span></span>
```
Set-AzSqlDatabaseAudit [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-EventHubTargetState <String>]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -DatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9bd8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9bd8-107">DESCRIPTION</span></span>
<span data-ttu-id="e9bd8-108">Polecenie **cmdlet Set-AzSqlDatabaseAudit** zmienia ustawienia inspekcji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-108">The **Set-AzSqlDatabaseAudit** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="e9bd8-109">Aby użyć polecenia cmdlet, określ bazę danych za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName.*</span><span class="sxs-lookup"><span data-stu-id="e9bd8-109">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e9bd8-110">Gdy magazyn obiektów blob jest miejscem docelowym dzienników inspekcji, określ parametr *StorageAccountResourceId* w celu określenia konta magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynu.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="e9bd8-111">Można również zdefiniować przechowywanie dla dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="e9bd8-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9bd8-112">EXAMPLES</span></span>

### <span data-ttu-id="e9bd8-113">Przykład 1. Włączanie zasad inspekcji magazynu obiektów blob w bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-113">Example 1: Enable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled  -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="e9bd8-114">Przykład 2. Wyłączenie zasad inspekcji magazynu obiektów blob w bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-114">Example 2: Disable the blob storage auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="e9bd8-115">Przykład 3. Włączanie zasad inspekcji magazynu obiektów blob w bazie danych Azure SQL za pomocą filtrowania przy użyciu predykatu T-SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-115">Example 3: Enable the blob storage auditing policy of an Azure SQL database with filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression "schema_name <> 'sys''" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="e9bd8-116">Przykład 4. Usuwanie filtrowania z zasad inspekcji bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-116">Example 4: Remove the filtering from the auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -PredicateExpression ""
```

### <span data-ttu-id="e9bd8-117">Przykład 5. Włączanie zasad inspekcji centrum zdarzeń w bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-117">Example 5: Enable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="e9bd8-118">Przykład 6. Wyłączenie zasad inspekcji centrum zdarzeń w bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-118">Example 6: Disable the event hub auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHubTargetState Disabled
```

### <span data-ttu-id="e9bd8-119">Przykład 7. Włączanie zasad inspekcji analizy dziennika w bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-119">Example 7: Enable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="e9bd8-120">Przykład 8. Wyłączenie zasad inspekcji analizy dziennika w bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-120">Example 8: Disable the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="e9bd8-121">Przykład 9. Wyłączanie za pośrednictwem potoku zasad inspekcji analizy dziennika w bazie danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e9bd8-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL database</span></span>
```powershell
PS C:\>Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Set-AzSqlDatabaseAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="e9bd8-122">Przykład 10. Wyłącz wysyłanie rekordów inspekcji bazy danych Azure SQL do magazynu obiektów blob i włącz wysyłanie ich do analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-122">Example 10: Disable sending audit records of an Azure SQL database to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="e9bd8-123">Przykład 11. Włączanie wysyłania rekordów inspekcji bazy danych Azure SQL do magazynu obiektów blob, centrum zdarzeń i analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-123">Example 11: Enable sending audit records of an Azure SQL database to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="e9bd8-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9bd8-124">PARAMETERS</span></span>

### <span data-ttu-id="e9bd8-125">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="e9bd8-125">-AuditAction</span></span>
<span data-ttu-id="e9bd8-126">Zestaw akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-126">The set of audit actions.</span></span>  
<span data-ttu-id="e9bd8-127">Obsługiwane akcje do inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="e9bd8-127">The supported actions to audit are:</span></span>  
<span data-ttu-id="e9bd8-128">SELECT</span><span class="sxs-lookup"><span data-stu-id="e9bd8-128">SELECT</span></span>  
<span data-ttu-id="e9bd8-129">UPDATE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-129">UPDATE</span></span>  
<span data-ttu-id="e9bd8-130">INSERT</span><span class="sxs-lookup"><span data-stu-id="e9bd8-130">INSERT</span></span>  
<span data-ttu-id="e9bd8-131">DELETE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-131">DELETE</span></span>  
<span data-ttu-id="e9bd8-132">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-132">EXECUTE</span></span>  
<span data-ttu-id="e9bd8-133">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-133">RECEIVE</span></span>  
<span data-ttu-id="e9bd8-134">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="e9bd8-134">REFERENCES</span></span>  
<span data-ttu-id="e9bd8-135">Ogólnym formularzem definiującym akcję, która ma być poddana inspekcji, jest: [akcja] ON [obiekt] BY [podmiot] Zauważ, że [obiekt] w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok lub procedura składowana, albo do całej bazy danych lub schematu.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-135">The general form for defining an action to be audited is: [action] ON [object] BY [principal] Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="e9bd8-136">W innych przypadkach używane są odpowiednio formularze DATABASE::[nazwa_bazy danych] i SCHEMA::[nazwa_schematu].</span><span class="sxs-lookup"><span data-stu-id="e9bd8-136">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>
<span data-ttu-id="e9bd8-137">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="e9bd8-137">For example:</span></span>  
<span data-ttu-id="e9bd8-138">SELECT on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="e9bd8-138">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="e9bd8-139">Select on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="e9bd8-139">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="e9bd8-140">SELECT w schemacie::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="e9bd8-140">SELECT on SCHEMA::mySchema by public</span></span>  
<span data-ttu-id="e9bd8-141">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="e9bd8-141">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-142">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="e9bd8-142">-AuditActionGroup</span></span>
<span data-ttu-id="e9bd8-143">Zalecany zestaw grup akcji do użycia to następująca kombinacja — spowoduje to inspekcję wszystkich zapytań i procedur przechowywanych wykonywanych w bazie danych, a także pomyślnych i nieudanych logowania:</span><span class="sxs-lookup"><span data-stu-id="e9bd8-143">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="e9bd8-144">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e9bd8-144">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="e9bd8-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="e9bd8-145">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="e9bd8-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="e9bd8-146">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="e9bd8-147">Ta kombinacja jest również skonfigurowanym domyślnie zestawem.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-147">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="e9bd8-148">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w bazie danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to zduplikowane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-148">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="e9bd8-149">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="e9bd8-149">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-150">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="e9bd8-150">-BlobStorageTargetState</span></span>
<span data-ttu-id="e9bd8-151">Wskazuje, czy magazyn obiektów blob jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-151">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-152">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e9bd8-152">-DatabaseName</span></span>
<span data-ttu-id="e9bd8-153">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-153">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-154">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e9bd8-154">-DatabaseObject</span></span>
<span data-ttu-id="e9bd8-155">Obiekt bazy danych do zarządzania jego zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-155">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9bd8-156">-DefaultProfile</span></span>
<span data-ttu-id="e9bd8-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9bd8-158">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="e9bd8-158">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="e9bd8-159">Identyfikator zasobu reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="e9bd8-159">The resource Id for the event hub authorization rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-160">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="e9bd8-160">-EventHubName</span></span>
<span data-ttu-id="e9bd8-161">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-161">The name of the event hub.</span></span> <span data-ttu-id="e9bd8-162">Jeśli podczas dostarczania wartości EventHubAuthorizationRuleResourceId nie zostanie określone żadne, zostanie wybrane domyślne centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-162">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-163">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="e9bd8-163">-EventHubTargetState</span></span>
<span data-ttu-id="e9bd8-164">Wskazuje, czy centrum zdarzeń jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-164">Indicates whether event hub is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-165">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="e9bd8-165">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="e9bd8-166">Wskazuje, czy analiza dziennika jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-166">Indicates whether log analytics is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-167">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9bd8-167">-PassThru</span></span>
<span data-ttu-id="e9bd8-168">Określa, czy zasady inspekcji mają być wyprowadzone na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-168">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="e9bd8-169">-PreddicateExpression</span><span class="sxs-lookup"><span data-stu-id="e9bd8-169">-PredicateExpression</span></span>
<span data-ttu-id="e9bd8-170">Predykat T-SQL (klauzula WHERE) używany do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-170">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-171">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9bd8-171">-ResourceGroupName</span></span>
<span data-ttu-id="e9bd8-172">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-172">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-173">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e9bd8-173">-RetentionInDays</span></span>
<span data-ttu-id="e9bd8-174">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-174">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-175">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e9bd8-175">-ServerName</span></span>
<span data-ttu-id="e9bd8-176">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-176">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-177">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="e9bd8-177">-StorageAccountResourceId</span></span>
<span data-ttu-id="e9bd8-178">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="e9bd8-178">The storage account resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-179">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="e9bd8-179">-StorageKeyType</span></span>
<span data-ttu-id="e9bd8-180">Określa, których kluczy dostępu do magazynu należy użyć.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-180">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-181">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="e9bd8-181">-WorkspaceResourceId</span></span>
<span data-ttu-id="e9bd8-182">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analizy dziennika) dla obszaru roboczego analizy dziennika, do którego chcesz wysłać dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-182">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="e9bd8-183">Przykład: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="e9bd8-183">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9bd8-184">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9bd8-184">-Confirm</span></span>
<span data-ttu-id="e9bd8-185">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-185">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9bd8-186">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9bd8-186">-WhatIf</span></span>
<span data-ttu-id="e9bd8-187">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-187">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9bd8-188">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-188">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9bd8-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9bd8-189">CommonParameters</span></span>
<span data-ttu-id="e9bd8-190">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9bd8-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9bd8-191">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9bd8-191">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9bd8-192">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-192">INPUTS</span></span>

### <span data-ttu-id="e9bd8-193">System.String</span><span class="sxs-lookup"><span data-stu-id="e9bd8-193">System.String</span></span>

### <span data-ttu-id="e9bd8-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e9bd8-194">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="e9bd8-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="e9bd8-195">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="e9bd8-196">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e9bd8-196">System.String[]</span></span>

### <span data-ttu-id="e9bd8-197">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e9bd8-197">System.Guid</span></span>

### <span data-ttu-id="e9bd8-198">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e9bd8-198">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e9bd8-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span><span class="sxs-lookup"><span data-stu-id="e9bd8-199">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditModel</span></span>

## <span data-ttu-id="e9bd8-200">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-200">OUTPUTS</span></span>

### <span data-ttu-id="e9bd8-201">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e9bd8-201">System.Boolean</span></span>

## <span data-ttu-id="e9bd8-202">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9bd8-202">NOTES</span></span>

## <span data-ttu-id="e9bd8-203">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9bd8-203">RELATED LINKS</span></span>
