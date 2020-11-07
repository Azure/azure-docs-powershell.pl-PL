---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: ac1057159de6f3028bd599183dc5c411155f14e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708010"
---
# <span data-ttu-id="877d4-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="877d4-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="877d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="877d4-102">SYNOPSIS</span></span>
<span data-ttu-id="877d4-103">Pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="877d4-103">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="877d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="877d4-104">SYNTAX</span></span>

### <span data-ttu-id="877d4-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="877d4-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="877d4-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="877d4-106">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="877d4-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="877d4-107">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="877d4-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="877d4-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="877d4-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="877d4-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="877d4-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="877d4-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="877d4-111">Opis</span><span class="sxs-lookup"><span data-stu-id="877d4-111">DESCRIPTION</span></span>
<span data-ttu-id="877d4-112">Polecenie cmdlet **Get-AzSqlDatabaseAuditing** pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="877d4-112">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="877d4-113">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="877d4-113">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="877d4-114">Miejsce docelowe dzienników inspekcji jest określane przez określenie jednego z następujących parametrów przełącznika: BlobStorage, LogAnalytics lub EventHub (jeśli nie jest określona, wartość domyślna to BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="877d4-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="877d4-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="877d4-115">EXAMPLES</span></span>

### <span data-ttu-id="877d4-116">Przykład 1: uzyskiwanie ustawień inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="877d4-116">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="877d4-117">Przykład 2: uzyskiwanie ustawień inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="877d4-117">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorage
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="877d4-118">Przykład 3: uzyskiwanie, za pośrednictwem rurociągu, ustawienia inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="877d4-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
```
PS C:\> Get-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" | Get-AzSqlDatabaseAuditing
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

### <span data-ttu-id="877d4-119">Przykład 4: uzyskiwanie ustawień inspekcji centrum zdarzeń bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="877d4-119">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="877d4-120">Przykład 5: Get, za pośrednictwem rurociągu ustawienia inspekcji centrum zdarzeń bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="877d4-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
```
PS C:\>$database = Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
PS C:\>$database | Get-AzSqlDatabaseAuditing -EventHub
DatabaseName                        : database01
AuditAction                         : {}
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
PredicateExpression                 : statement <> 'select 1'
```

### <span data-ttu-id="877d4-121">Przykład 6: Pobieranie ustawień inspekcji analizy dzienników bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="877d4-121">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -LogAnalytics
DatabaseName        : database01
AuditAction         : {}
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="877d4-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="877d4-122">PARAMETERS</span></span>

### <span data-ttu-id="877d4-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="877d4-123">-BlobStorage</span></span>
<span data-ttu-id="877d4-124">Określa, że miejsce docelowe dziennika inspekcji jest magazynem obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="877d4-124">Specifies that audit logs destination is blob storage</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameterSet, BlobStorageByParentResourceSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d4-125">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="877d4-125">-DatabaseName</span></span>
<span data-ttu-id="877d4-126">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="877d4-126">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="877d4-127">-DefaultProfile</span></span>
<span data-ttu-id="877d4-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="877d4-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="877d4-129">— EventHub</span><span class="sxs-lookup"><span data-stu-id="877d4-129">-EventHub</span></span>
<span data-ttu-id="877d4-130">Określa, że miejscem docelowym dziennika inspekcji jest centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="877d4-130">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="877d4-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="877d4-131">-InputObject</span></span>
<span data-ttu-id="877d4-132">Obiekt bazy danych do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="877d4-132">The database object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="877d4-133">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="877d4-133">-LogAnalytics</span></span>
<span data-ttu-id="877d4-134">Określa, że miejscem docelowym dziennika inspekcji jest Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="877d4-134">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="877d4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="877d4-135">-ResourceGroupName</span></span>
<span data-ttu-id="877d4-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="877d4-136">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d4-137">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="877d4-137">-ServerName</span></span>
<span data-ttu-id="877d4-138">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="877d4-138">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet, EventHubSet, LogAnalyticsSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="877d4-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="877d4-139">-Confirm</span></span>
<span data-ttu-id="877d4-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="877d4-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="877d4-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="877d4-141">-WhatIf</span></span>
<span data-ttu-id="877d4-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="877d4-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="877d4-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="877d4-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="877d4-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="877d4-144">CommonParameters</span></span>
<span data-ttu-id="877d4-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="877d4-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="877d4-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="877d4-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="877d4-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="877d4-147">INPUTS</span></span>

### <span data-ttu-id="877d4-148">System. String</span><span class="sxs-lookup"><span data-stu-id="877d4-148">System.String</span></span>

### <span data-ttu-id="877d4-149">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="877d4-149">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="877d4-150">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="877d4-150">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="877d4-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="877d4-151">OUTPUTS</span></span>

### <span data-ttu-id="877d4-152">Microsoft. Azure. Commands. SQL. Audit. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="877d4-152">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="877d4-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="877d4-153">NOTES</span></span>

## <span data-ttu-id="877d4-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="877d4-154">RELATED LINKS</span></span>
