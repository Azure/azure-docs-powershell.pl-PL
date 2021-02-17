---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAudit.md
ms.openlocfilehash: ec88d8ff9f5a514a3b1b5dcd9ecb917ee348b900
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187994"
---
# <span data-ttu-id="4f8dc-101">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="4f8dc-101">Set-AzSqlServerAudit</span></span>

## <span data-ttu-id="4f8dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f8dc-102">SYNOPSIS</span></span>
<span data-ttu-id="4f8dc-103">Zmienia ustawienia inspekcji serwera Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="4f8dc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4f8dc-104">SYNTAX</span></span>

### <span data-ttu-id="4f8dc-105">ServerParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="4f8dc-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f8dc-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4f8dc-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerAudit [-AuditActionGroup <AuditActionGroups[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f8dc-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4f8dc-107">DESCRIPTION</span></span>
<span data-ttu-id="4f8dc-108">Polecenie **cmdlet Set-AzSqlServerAudit** zmienia ustawienia inspekcji serwera Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-108">The **Set-AzSqlServerAudit** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="4f8dc-109">Aby użyć polecenia cmdlet, określ serwer za pomocą parametrów *ResourceGroupName* i *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="4f8dc-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="4f8dc-110">Gdy magazyn obiektów blob jest miejscem docelowym dzienników inspekcji, określ parametr *StorageAccountResourceId* w celu określenia konta magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynu.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="4f8dc-111">Można również zdefiniować przechowywanie dla dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="4f8dc-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4f8dc-112">EXAMPLES</span></span>

### <span data-ttu-id="4f8dc-113">Przykład 1. Włączanie zasad inspekcji magazynu obiektów blob serwera Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-113">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="4f8dc-114">Przykład 2. Wyłączenie zasad inspekcji magazynu obiektów blob serwera Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="4f8dc-114">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="4f8dc-115">Przykład 3. Włączanie zasad inspekcji magazynu obiektów blob na serwerze Azure SQL z zaawansowanym filtrowaniem przy użyciu predykatu T-SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-115">Example 3: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="4f8dc-116">Przykład 4. Usunięcie zaawansowanego ustawienia filtrowania z zasad inspekcji serwera Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-116">Example 4: Remove the advanced filtering setting from the auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -PredicateExpression ""
```

### <span data-ttu-id="4f8dc-117">Przykład 5. Włączanie zasad inspekcji centrum zdarzeń serwera Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-117">Example 5: Enable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="4f8dc-118">Przykład 6. Wyłączenie zasad inspekcji centrum zdarzeń serwera Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-118">Example 6: Disable the event hub auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="4f8dc-119">Przykład 7. Włączanie zasad inspekcji analizy dziennika na serwerze Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-119">Example 7: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="4f8dc-120">Przykład 8. Wyłączenie zasad inspekcji analizy dziennika na serwerze Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-120">Example 8: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="4f8dc-121">Przykład 9. Wyłączanie w potoku zasad inspekcji analizy dziennika serwera Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f8dc-121">Example 9: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="4f8dc-122">Przykład 10. Wyłącz wysyłanie rekordów inspekcji serwera Azure SQL do magazynu obiektów blob i włącz wysyłanie ich do analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-122">Example 10: Disable sending audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="4f8dc-123">Przykład 11. Włączanie wysyłania rekordów inspekcji serwera Azure SQL do magazynu obiektów blob, centrum zdarzeń i analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-123">Example 11: Enable sending audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="4f8dc-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f8dc-124">PARAMETERS</span></span>

### <span data-ttu-id="4f8dc-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4f8dc-125">-AsJob</span></span>
<span data-ttu-id="4f8dc-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4f8dc-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4f8dc-127">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="4f8dc-127">-AuditActionGroup</span></span>
<span data-ttu-id="4f8dc-128">Zalecany zestaw grup akcji do użycia to następująca kombinacja — spowoduje to inspekcję wszystkich zapytań i procedur przechowywanych wykonywanych w bazie danych, a także pomyślnego i nieudanych logowania:</span><span class="sxs-lookup"><span data-stu-id="4f8dc-128">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="4f8dc-129">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="4f8dc-129">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="4f8dc-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="4f8dc-130">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="4f8dc-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="4f8dc-131">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="4f8dc-132">Ta kombinacja jest również skonfigurowanym domyślnie zestawem.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-132">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="4f8dc-133">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w bazie danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to zduplikowane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-133">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="4f8dc-134">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="4f8dc-134">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="4f8dc-135">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="4f8dc-135">-BlobStorageTargetState</span></span>
<span data-ttu-id="4f8dc-136">Wskazuje, czy magazyn obiektów blob jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-136">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="4f8dc-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f8dc-137">-DefaultProfile</span></span>
<span data-ttu-id="4f8dc-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f8dc-139">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="4f8dc-139">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="4f8dc-140">Identyfikator zasobu reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="4f8dc-140">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="4f8dc-141">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="4f8dc-141">-EventHubName</span></span>
<span data-ttu-id="4f8dc-142">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-142">The name of the event hub.</span></span> <span data-ttu-id="4f8dc-143">Jeśli podczas dostarczania wartości EventHubAuthorizationRuleResourceId nie zostanie określone żadne, zostanie wybrane domyślne centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-143">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="4f8dc-144">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="4f8dc-144">-EventHubTargetState</span></span>
<span data-ttu-id="4f8dc-145">Wskazuje, czy centrum zdarzeń jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-145">Indicates whether event hub is a destination for audit records.</span></span>

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

### <span data-ttu-id="4f8dc-146">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="4f8dc-146">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="4f8dc-147">Wskazuje, czy analiza dziennika jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-147">Indicates whether log analytics is a destination for audit records.</span></span>

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

### <span data-ttu-id="4f8dc-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f8dc-148">-PassThru</span></span>
<span data-ttu-id="4f8dc-149">Określa, czy zasady inspekcji mają być wyprowadzone na koniec wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-149">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="4f8dc-150">-PreddicateExpression</span><span class="sxs-lookup"><span data-stu-id="4f8dc-150">-PredicateExpression</span></span>
<span data-ttu-id="4f8dc-151">Predykat T-SQL (klauzula WHERE) używany do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-151">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="4f8dc-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f8dc-152">-ResourceGroupName</span></span>
<span data-ttu-id="4f8dc-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-153">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8dc-154">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4f8dc-154">-RetentionInDays</span></span>
<span data-ttu-id="4f8dc-155">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-155">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="4f8dc-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4f8dc-156">-ServerName</span></span>
<span data-ttu-id="4f8dc-157">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-157">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f8dc-158">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="4f8dc-158">-ServerObject</span></span>
<span data-ttu-id="4f8dc-159">Obiekt serwera do zarządzania jego zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-159">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: ServerObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f8dc-160">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4f8dc-160">-StorageAccountResourceId</span></span>
<span data-ttu-id="4f8dc-161">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="4f8dc-161">The storage account resource id</span></span>

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

### <span data-ttu-id="4f8dc-162">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="4f8dc-162">-StorageKeyType</span></span>
<span data-ttu-id="4f8dc-163">Określa, których kluczy dostępu magazynu należy użyć.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-163">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="4f8dc-164">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="4f8dc-164">-WorkspaceResourceId</span></span>
<span data-ttu-id="4f8dc-165">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analizy dziennika) dla obszaru roboczego analizy dziennika, do którego chcesz wysłać dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-165">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="4f8dc-166">Przykład: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="4f8dc-166">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="4f8dc-167">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4f8dc-167">-Confirm</span></span>
<span data-ttu-id="4f8dc-168">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f8dc-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f8dc-169">-WhatIf</span></span>
<span data-ttu-id="4f8dc-170">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4f8dc-171">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f8dc-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f8dc-172">CommonParameters</span></span>
<span data-ttu-id="4f8dc-173">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f8dc-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f8dc-174">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4f8dc-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f8dc-175">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f8dc-175">INPUTS</span></span>

### <span data-ttu-id="4f8dc-176">System.String</span><span class="sxs-lookup"><span data-stu-id="4f8dc-176">System.String</span></span>

### <span data-ttu-id="4f8dc-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="4f8dc-177">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="4f8dc-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span><span class="sxs-lookup"><span data-stu-id="4f8dc-178">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="4f8dc-179">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4f8dc-179">System.Guid</span></span>

### <span data-ttu-id="4f8dc-180">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4f8dc-180">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4f8dc-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span><span class="sxs-lookup"><span data-stu-id="4f8dc-181">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditModel</span></span>

## <span data-ttu-id="4f8dc-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4f8dc-182">OUTPUTS</span></span>

### <span data-ttu-id="4f8dc-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4f8dc-183">System.Boolean</span></span>

## <span data-ttu-id="4f8dc-184">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4f8dc-184">NOTES</span></span>

## <span data-ttu-id="4f8dc-185">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f8dc-185">RELATED LINKS</span></span>
