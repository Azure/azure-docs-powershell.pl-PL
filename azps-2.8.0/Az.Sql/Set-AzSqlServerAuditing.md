---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerAuditing.md
ms.openlocfilehash: e9d3e7ca009a756526bc0cb150ebdb6c124df032
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887213"
---
# <span data-ttu-id="41fc1-101">Set-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="41fc1-101">Set-AzSqlServerAuditing</span></span>

## <span data-ttu-id="41fc1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="41fc1-103">**Ważne: to polecenie cmdlet jest przestarzałe, funkcja [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) zamienia je.**</span><span class="sxs-lookup"><span data-stu-id="41fc1-103">**Important: This cmdlet is deprecated, [Set-AzSqlServerAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserveraudit) is replacing it.**</span></span>

<span data-ttu-id="41fc1-104">Zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="41fc1-104">Changes the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="41fc1-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41fc1-105">SYNTAX</span></span>

### <span data-ttu-id="41fc1-106">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41fc1-106">DefaultParameterSet (Default)</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fc1-107">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="41fc1-107">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41fc1-108">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="41fc1-108">EventHubSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fc1-109">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="41fc1-109">LogAnalyticsSet</span></span>
```
Set-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fc1-110">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="41fc1-110">BlobStorageByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fc1-111">StorageAccountSubscriptionIdByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="41fc1-111">StorageAccountSubscriptionIdByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob] [-BlobStorage]
 -StorageAccountName <String> -StorageAccountSubscriptionId <Guid> [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="41fc1-112">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="41fc1-112">EventHubByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>] [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41fc1-113">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="41fc1-113">LogAnalyticsByParentResourceSet</span></span>
```
Set-AzSqlServerAuditing -InputObject <AzureSqlServerModel> -State <String>
 [-AuditActionGroup <AuditActionGroups[]>] [-PassThru] [-PredicateExpression <String>] [-AsJob]
 [-WorkspaceResourceId <String>] [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41fc1-114">Opis</span><span class="sxs-lookup"><span data-stu-id="41fc1-114">DESCRIPTION</span></span>
<span data-ttu-id="41fc1-115">Polecenie cmdlet **Set-AzSqlServerAuditing** zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="41fc1-115">The **Set-AzSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="41fc1-116">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="41fc1-116">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="41fc1-117">Miejsce docelowe dzienników inspekcji jest określane przez określenie jednego z następujących parametrów przełącznika: BlobStorage, LogAnalytics lub EventHub (jeśli nie jest określona, wartość domyślna to BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="41fc1-117">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>
<span data-ttu-id="41fc1-118">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="41fc1-118">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="41fc1-119">Gdy miejsce docelowe dziennika inspekcji jest miejscem docelowym, określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* , aby zdefiniować klucze magazynowania.</span><span class="sxs-lookup"><span data-stu-id="41fc1-119">When audit logs destination is blob storage, specify the *StorageAccountName* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="41fc1-120">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="41fc1-120">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="41fc1-121">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt z opisem bieżących ustawień inspekcji oprócz identyfikatorów serwera.</span><span class="sxs-lookup"><span data-stu-id="41fc1-121">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing settings in addition to the server identifiers.</span></span>
<span data-ttu-id="41fc1-122">Identyfikatory serwerów obejmują, ale nie są ograniczone do **ResourceGroupName** oraz **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="41fc1-122">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="41fc1-123">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41fc1-123">EXAMPLES</span></span>

### <span data-ttu-id="41fc1-124">Przykład 1: Włączanie zasad inspekcji magazynu obiektów BLOB dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-124">Example 1: Enable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="41fc1-125">Przykład 2: wyłączenie zasad inspekcji magazynu obiektów BLOB dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-125">Example 2: Disable the blob storage auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="41fc1-126">Przykład 3: Włączanie zasad inspekcji magazynu obiektów BLOB dla programu Azure SQL Server przy użyciu konta magazynu z innej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="41fc1-126">Example 3: Enable the blob storage auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="41fc1-127">Przykład 4: Włączanie zasad inspekcji magazynu obiektów BLOB programu Azure SQL Server za pomocą funkcji filtrowania zaawansowanego przy użyciu predykatu T-SQL</span><span class="sxs-lookup"><span data-stu-id="41fc1-127">Example 4: Enable the blob storage auditing policy of an Azure SQL server with advanced filtering using a T-SQL predicate</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="41fc1-128">Przykład 5: usuwanie ustawień filtrowania zaawansowanego z zasad przechowywania inspekcji obiektów BLOB w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-128">Example 5: Remove the advanced filtering setting from the blob auditing storage policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -PredicateExpression ""
```

### <span data-ttu-id="41fc1-129">Przykład 6: Włączanie zasad inspekcji centrum zdarzeń programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-129">Example 6: Enable the event hub auditing policy of an Azure SQL server</span></span>
```
$EventHubAuthorizationRule = Get-AzEventHubAuthorizationRule `
    -ResourceGroupName "ResourceGroup01" `
    -Namespace "EventHubName" `
    -Name "SharedAccessPoliceName" 

Set-AzSqlServerAuditing `
    -State Enabled `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -EventHub `
    -EventHubName "EventHubName" `
    -EventHubAuthorizationRuleResourceId $EventHubAuthorizationRule.Id
```

### <span data-ttu-id="41fc1-130">Przykład 7: wyłączanie zasad inspekcji centrum zdarzeń programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-130">Example 7: Disable the event hub auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubName
```

### <span data-ttu-id="41fc1-131">Przykład 8: Włączanie zasad inspekcji analizy dzienników programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-131">Example 8: Enable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="41fc1-132">Przykład 9: wyłączenie zasad inspekcji analizy dzienników programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-132">Example 9: Disable the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalytics
```

### <span data-ttu-id="41fc1-133">Przykład 10: wyłączanie, za pośrednictwem rurociągu, zasady inspekcji analizy dzienników w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="41fc1-133">Example 10: Disable, through pipeline, the log analytics auditing policy of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerAuditing -LogAnalytics -State Disabled
```

## <span data-ttu-id="41fc1-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41fc1-134">PARAMETERS</span></span>

### <span data-ttu-id="41fc1-135">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41fc1-135">-AsJob</span></span>
<span data-ttu-id="41fc1-136">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="41fc1-136">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41fc1-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="41fc1-137">-AuditActionGroup</span></span>
<span data-ttu-id="41fc1-138">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="41fc1-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="41fc1-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="41fc1-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="41fc1-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="41fc1-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="41fc1-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="41fc1-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  
<span data-ttu-id="41fc1-142">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="41fc1-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="41fc1-143">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="41fc1-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="41fc1-144">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="41fc1-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="41fc1-145">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="41fc1-145">-BlobStorage</span></span>
<span data-ttu-id="41fc1-146">Określa, że miejsce docelowe dziennika inspekcji jest magazynem obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="41fc1-146">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="41fc1-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41fc1-147">-DefaultProfile</span></span>
<span data-ttu-id="41fc1-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41fc1-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41fc1-149">— EventHub</span><span class="sxs-lookup"><span data-stu-id="41fc1-149">-EventHub</span></span>
<span data-ttu-id="41fc1-150">Określa, że miejscem docelowym dziennika inspekcji jest centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="41fc1-150">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="41fc1-151">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="41fc1-151">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="41fc1-152">Identyfikator zasobu dla reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="41fc1-152">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="41fc1-153">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="41fc1-153">-EventHubName</span></span>
<span data-ttu-id="41fc1-154">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="41fc1-154">The name of the event hub.</span></span> <span data-ttu-id="41fc1-155">Jeśli w trakcie dostarczania EventHubAuthorizationRuleResourceId zostanie wybrana opcja Brak, zostanie wybrany domyślny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="41fc1-155">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="41fc1-156">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41fc1-156">-InputObject</span></span>
<span data-ttu-id="41fc1-157">Obiekt serwera do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="41fc1-157">The server object to manage its audit policy.</span></span>

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

### <span data-ttu-id="41fc1-158">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="41fc1-158">-LogAnalytics</span></span>
<span data-ttu-id="41fc1-159">Określa, że miejscem docelowym dziennika inspekcji jest Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="41fc1-159">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="41fc1-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41fc1-160">-PassThru</span></span>
<span data-ttu-id="41fc1-161">Określa, czy ma być wyprowadzana zasada inspekcji na końcu wykonania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41fc1-161">Specifies whether to output the auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="41fc1-162">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="41fc1-162">-PredicateExpression</span></span>
<span data-ttu-id="41fc1-163">Predykat T-SQL (klauzula WHERE) służący do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="41fc1-163">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="41fc1-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41fc1-164">-ResourceGroupName</span></span>
<span data-ttu-id="41fc1-165">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="41fc1-165">The name of the resource group.</span></span>

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

### <span data-ttu-id="41fc1-166">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="41fc1-166">-RetentionInDays</span></span>
<span data-ttu-id="41fc1-167">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="41fc1-167">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="41fc1-168">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="41fc1-168">-ServerName</span></span>
<span data-ttu-id="41fc1-169">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="41fc1-169">SQL server name.</span></span>

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

### <span data-ttu-id="41fc1-170">-State</span><span class="sxs-lookup"><span data-stu-id="41fc1-170">-State</span></span>
<span data-ttu-id="41fc1-171">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="41fc1-171">The state of the policy.</span></span>

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

### <span data-ttu-id="41fc1-172">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="41fc1-172">-StorageAccountName</span></span>
<span data-ttu-id="41fc1-173">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="41fc1-173">The name of the storage account.</span></span>

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

### <span data-ttu-id="41fc1-174">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41fc1-174">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="41fc1-175">Identyfikator subskrypcji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="41fc1-175">The storage account subscription id</span></span>

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

### <span data-ttu-id="41fc1-176">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="41fc1-176">-StorageKeyType</span></span>
<span data-ttu-id="41fc1-177">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="41fc1-177">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="41fc1-178">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="41fc1-178">-WorkspaceResourceId</span></span>
<span data-ttu-id="41fc1-179">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analizy dzienników) dla obszaru roboczego analizy dzienników, do którego mają być wysyłane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="41fc1-179">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Audit Logs.</span></span> <span data-ttu-id="41fc1-180">Przykład:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="41fc1-180">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="41fc1-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41fc1-181">-Confirm</span></span>
<span data-ttu-id="41fc1-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41fc1-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41fc1-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41fc1-183">-WhatIf</span></span>
<span data-ttu-id="41fc1-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41fc1-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="41fc1-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41fc1-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41fc1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41fc1-186">CommonParameters</span></span>
<span data-ttu-id="41fc1-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41fc1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41fc1-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41fc1-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41fc1-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41fc1-189">INPUTS</span></span>

### <span data-ttu-id="41fc1-190">System. String</span><span class="sxs-lookup"><span data-stu-id="41fc1-190">System.String</span></span>

### <span data-ttu-id="41fc1-191">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="41fc1-191">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="41fc1-192">Microsoft. Azure. Commands. SQL. Audit. model. AuditActionGroups []</span><span class="sxs-lookup"><span data-stu-id="41fc1-192">Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]</span></span>

### <span data-ttu-id="41fc1-193">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="41fc1-193">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="41fc1-194">System. GUID</span><span class="sxs-lookup"><span data-stu-id="41fc1-194">System.Guid</span></span>

### <span data-ttu-id="41fc1-195">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="41fc1-195">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="41fc1-196">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41fc1-196">OUTPUTS</span></span>

### <span data-ttu-id="41fc1-197">Microsoft. Azure. Commands. SQL. Audit. model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="41fc1-197">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="41fc1-198">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41fc1-198">NOTES</span></span>

## <span data-ttu-id="41fc1-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41fc1-199">RELATED LINKS</span></span>
