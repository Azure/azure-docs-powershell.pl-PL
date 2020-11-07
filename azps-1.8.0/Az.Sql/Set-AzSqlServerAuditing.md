---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: 44db866488459382a3b66f77328b5cbc9259754b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707724"
---
# <span data-ttu-id="68440-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="68440-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="68440-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="68440-102">SYNOPSIS</span></span>
<span data-ttu-id="68440-103">Zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68440-103">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="68440-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="68440-104">SYNTAX</span></span>

### <span data-ttu-id="68440-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="68440-105">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68440-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="68440-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68440-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="68440-107">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68440-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="68440-108">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68440-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="68440-109">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68440-110">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="68440-110">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68440-111">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="68440-111">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68440-112">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="68440-112">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68440-113">Opis</span><span class="sxs-lookup"><span data-stu-id="68440-113">DESCRIPTION</span></span>
<span data-ttu-id="68440-114">Polecenie cmdlet **Set-AzSqlServerAuditing** zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="68440-114">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="68440-115">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="68440-115">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="68440-116">Miejsce docelowe dzienników inspekcji jest określane przez określenie jednego z następujących parametrów przełącznika: BlobStorage, LogAnalytics lub EventHub (jeśli nie jest określona, wartość domyślna to BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="68440-116">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="68440-117">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="68440-117">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="68440-118">Gdy miejsce docelowe dziennika inspekcji jest miejscem docelowym, określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* , aby zdefiniować klucze magazynowania.</span><span class="sxs-lookup"><span data-stu-id="68440-118">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="68440-119">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="68440-119">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="68440-120">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt z opisem bieżących ustawień inspekcji oprócz identyfikatorów serwera.</span><span class="sxs-lookup"><span data-stu-id="68440-120">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="68440-121">Identyfikatory serwerów obejmują, ale nie są ograniczone do **ResourceGroupName** oraz **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="68440-121">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="68440-122">Przykłady</span><span class="sxs-lookup"><span data-stu-id="68440-122">EXAMPLES</span></span>

### <span data-ttu-id="68440-123">Przykład 1: Włączanie zasad inspekcji magazynu obiektów BLOB dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-123">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="68440-124">Przykład 2: wyłączenie zasad inspekcji magazynu obiektów BLOB dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-124">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="68440-125">Przykład 3: Włączanie zasad inspekcji magazynu obiektów BLOB dla programu Azure SQL Server przy użyciu konta magazynu z innej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="68440-125">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="68440-126">Przykład 4: Włączanie zasad inspekcji magazynu obiektów BLOB programu Azure SQL Server za pomocą funkcji filtrowania zaawansowanego przy użyciu predykatu T-SQL</span><span class="sxs-lookup"><span data-stu-id="68440-126">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="68440-127">Przykład 5: usuwanie ustawień filtrowania zaawansowanego z zasad przechowywania inspekcji obiektów BLOB w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-127">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="68440-128">Przykład 6: Włączanie zasad inspekcji centrum zdarzeń programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-128">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="68440-129">Przykład 7: wyłączanie zasad inspekcji centrum zdarzeń programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-129">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="68440-130">Przykład 8: Włączanie zasad inspekcji analizy dzienników programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-130">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="68440-131">Przykład 9: wyłączenie zasad inspekcji analizy dzienników programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-131">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="68440-132">Przykład 10: wyłączanie, za pośrednictwem rurociągu, zasady inspekcji analizy dzienników w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="68440-132">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="68440-133">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="68440-133">PARAMETERS</span></span>

### <span data-ttu-id="68440-134">-AsJob</span><span class="sxs-lookup"><span data-stu-id="68440-134">-AsJob</span></span>
<span data-ttu-id="68440-135">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="68440-135">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="68440-136">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="68440-136">-AuditActionGroup</span></span>
<span data-ttu-id="68440-137">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="68440-137">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="68440-138">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="68440-138">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="68440-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="68440-139">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="68440-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="68440-140">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="68440-141">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="68440-141">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="68440-142">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="68440-142">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="68440-143">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="68440-143">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="68440-144">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="68440-144">-BlobStorage</span></span>
<span data-ttu-id="68440-145">Określa, że miejsce docelowe dziennika inspekcji jest magazynem obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="68440-145">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="68440-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68440-146">-DefaultProfile</span></span>
<span data-ttu-id="68440-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="68440-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68440-148">— EventHub</span><span class="sxs-lookup"><span data-stu-id="68440-148">-EventHub</span></span>
<span data-ttu-id="68440-149">Określa, że miejscem docelowym dziennika inspekcji jest centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="68440-149">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="68440-150">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="68440-150">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="68440-151">Identyfikator zasobu dla reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="68440-151">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="68440-152">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="68440-152">-EventHubName</span></span>
<span data-ttu-id="68440-153">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="68440-153">The name of the event hub.</span></span> <span data-ttu-id="68440-154">Jeśli w trakcie dostarczania EventHubAuthorizationRuleResourceId zostanie wybrana opcja Brak, zostanie wybrany domyślny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="68440-154">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="68440-155">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="68440-155">-InputObject</span></span>
<span data-ttu-id="68440-156">Obiekt serwera do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="68440-156">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, StorageAccountSubscriptionIdByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68440-157">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="68440-157">-LogAnalytics</span></span>
<span data-ttu-id="68440-158">Określa, że miejscem docelowym dziennika inspekcji jest Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="68440-158">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="68440-159">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68440-159">-PassThru</span></span>
<span data-ttu-id="68440-160">Określa, czy ma być wyprowadzana zasada inspekcji na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68440-160">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="68440-161">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="68440-161">-PredicateExpression</span></span>
<span data-ttu-id="68440-162">Predykat T-SQL (klauzula WHERE) służący do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="68440-162">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="68440-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68440-163">-ResourceGroupName</span></span>
<span data-ttu-id="68440-164">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="68440-164">The name of the resource group.</span></span>

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

### <span data-ttu-id="68440-165">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="68440-165">-RetentionInDays</span></span>
<span data-ttu-id="68440-166">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="68440-166">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="68440-167">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="68440-167">-ServerName</span></span>
<span data-ttu-id="68440-168">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="68440-168">SQL server name.</span></span>

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

### <span data-ttu-id="68440-169">-State</span><span class="sxs-lookup"><span data-stu-id="68440-169">-State</span></span>
<span data-ttu-id="68440-170">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="68440-170">The state of the policy.</span></span>

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

### <span data-ttu-id="68440-171">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="68440-171">-StorageAccountName</span></span>
<span data-ttu-id="68440-172">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="68440-172">The name of the storage account.</span></span>

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

### <span data-ttu-id="68440-173">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="68440-173">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="68440-174">Identyfikator subskrypcji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="68440-174">The storage account subscription id</span></span>

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

### <span data-ttu-id="68440-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="68440-175">-StorageKeyType</span></span>
<span data-ttu-id="68440-176">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="68440-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="68440-177">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="68440-177">-WorkspaceResourceId</span></span>
<span data-ttu-id="68440-178">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analizy dzienników) dla obszaru roboczego analizy dzienników, do którego mają być wysyłane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="68440-178">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="68440-179">Przykład:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="68440-179">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="68440-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="68440-180">-Confirm</span></span>
<span data-ttu-id="68440-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68440-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68440-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68440-182">-WhatIf</span></span>
<span data-ttu-id="68440-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68440-183">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68440-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="68440-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68440-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68440-185">CommonParameters</span></span>
<span data-ttu-id="68440-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68440-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68440-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68440-187">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68440-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="68440-188">INPUTS</span></span>

### <span data-ttu-id="68440-189">System. String</span><span class="sxs-lookup"><span data-stu-id="68440-189">System.String</span></span>

### <span data-ttu-id="68440-190">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="68440-190">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="68440-191">Microsoft. Azure. Commands. SQL. Audit. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="68440-191">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="68440-192">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="68440-192">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="68440-193">System. GUID</span><span class="sxs-lookup"><span data-stu-id="68440-193">System.Guid</span></span>

### <span data-ttu-id="68440-194">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="68440-194">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="68440-195">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="68440-195">OUTPUTS</span></span>

### <span data-ttu-id="68440-196">Microsoft. Azure. Commands. SQL. Audit. model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="68440-196">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="68440-197">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="68440-197">NOTES</span></span>

## <span data-ttu-id="68440-198">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="68440-198">RELATED LINKS</span></span>
