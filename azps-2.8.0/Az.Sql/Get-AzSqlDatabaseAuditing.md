---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseAuditing.md
ms.openlocfilehash: 641ab27f75950a2c15035a7787346250a41f9ab9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887082"
---
# <span data-ttu-id="951d6-101">Get-AzSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="951d6-101">Get-AzSqlDatabaseAuditing</span></span>

## <span data-ttu-id="951d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="951d6-102">SYNOPSIS</span></span>
<span data-ttu-id="951d6-103">**Ważne: to polecenie cmdlet jest przestarzałe, polecenie [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) zamienia je.**</span><span class="sxs-lookup"><span data-stu-id="951d6-103">**Important: This cmdlet is deprecated, [Get-AzSqlDatbaseAudit](https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseaudit) is replacing it.**</span></span>

<span data-ttu-id="951d6-104">Pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="951d6-104">Gets the auditing settings of an Azure SQL database.</span></span>

## <span data-ttu-id="951d6-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="951d6-105">SYNTAX</span></span>

### <span data-ttu-id="951d6-106">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="951d6-106">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-BlobStorage] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951d6-107">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="951d6-107">EventHubSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-EventHub] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951d6-108">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="951d6-108">LogAnalyticsSet</span></span>
```
Get-AzSqlDatabaseAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-DatabaseName] <String>
 [-LogAnalytics] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951d6-109">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="951d6-109">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951d6-110">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="951d6-110">EventHubByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="951d6-111">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="951d6-111">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlDatabaseAuditing -InputObject <AzureSqlDatabaseModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="951d6-112">Opis</span><span class="sxs-lookup"><span data-stu-id="951d6-112">DESCRIPTION</span></span>
<span data-ttu-id="951d6-113">Polecenie cmdlet **Get-AzSqlDatabaseAuditing** pobiera ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="951d6-113">The **Get-AzSqlDatabaseAuditing** cmdlet gets the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="951d6-114">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="951d6-114">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="951d6-115">Miejsce docelowe dzienników inspekcji jest określane przez określenie jednego z następujących parametrów przełącznika: BlobStorage, LogAnalytics lub EventHub (jeśli nie jest określona, wartość domyślna to BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="951d6-115">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="951d6-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="951d6-116">EXAMPLES</span></span>

### <span data-ttu-id="951d6-117">Przykład 1: uzyskiwanie ustawień inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="951d6-117">Example 1: Get the blob storage auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="951d6-118">Przykład 2: uzyskiwanie ustawień inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="951d6-118">Example 2: Get the blob storage auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="951d6-119">Przykład 3: uzyskiwanie, za pośrednictwem rurociągu, ustawienia inspekcji magazynu obiektów BLOB bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="951d6-119">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="951d6-120">Przykład 4: uzyskiwanie ustawień inspekcji centrum zdarzeń bazy danych Azure SQL</span><span class="sxs-lookup"><span data-stu-id="951d6-120">Example 4: Get the event hub auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="951d6-121">Przykład 5: Get, za pośrednictwem rurociągu ustawienia inspekcji centrum zdarzeń bazy danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="951d6-121">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL database</span></span>
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

### <span data-ttu-id="951d6-122">Przykład 6: Pobieranie ustawień inspekcji analizy dzienników bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="951d6-122">Example 6: Get the log analytics auditing settings of an Azure SQL database</span></span>
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

## <span data-ttu-id="951d6-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="951d6-123">PARAMETERS</span></span>

### <span data-ttu-id="951d6-124">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="951d6-124">-BlobStorage</span></span>
<span data-ttu-id="951d6-125">Określa, że miejsce docelowe dziennika inspekcji jest magazynem obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="951d6-125">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="951d6-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="951d6-126">-DatabaseName</span></span>
<span data-ttu-id="951d6-127">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="951d6-127">SQL Database name.</span></span>

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

### <span data-ttu-id="951d6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="951d6-128">-DefaultProfile</span></span>
<span data-ttu-id="951d6-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="951d6-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="951d6-130">— EventHub</span><span class="sxs-lookup"><span data-stu-id="951d6-130">-EventHub</span></span>
<span data-ttu-id="951d6-131">Określa, że miejscem docelowym dziennika inspekcji jest centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="951d6-131">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="951d6-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="951d6-132">-InputObject</span></span>
<span data-ttu-id="951d6-133">Obiekt bazy danych do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="951d6-133">The database object to manage its audit policy.</span></span>

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

### <span data-ttu-id="951d6-134">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="951d6-134">-LogAnalytics</span></span>
<span data-ttu-id="951d6-135">Określa, że miejscem docelowym dziennika inspekcji jest Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="951d6-135">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="951d6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="951d6-136">-ResourceGroupName</span></span>
<span data-ttu-id="951d6-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="951d6-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="951d6-138">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="951d6-138">-ServerName</span></span>
<span data-ttu-id="951d6-139">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="951d6-139">SQL server name.</span></span>

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

### <span data-ttu-id="951d6-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="951d6-140">-Confirm</span></span>
<span data-ttu-id="951d6-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="951d6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="951d6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="951d6-142">-WhatIf</span></span>
<span data-ttu-id="951d6-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="951d6-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="951d6-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="951d6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="951d6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="951d6-145">CommonParameters</span></span>
<span data-ttu-id="951d6-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="951d6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="951d6-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="951d6-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="951d6-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="951d6-148">INPUTS</span></span>

### <span data-ttu-id="951d6-149">System. String</span><span class="sxs-lookup"><span data-stu-id="951d6-149">System.String</span></span>

### <span data-ttu-id="951d6-150">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="951d6-150">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="951d6-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="951d6-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="951d6-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="951d6-152">OUTPUTS</span></span>

### <span data-ttu-id="951d6-153">Microsoft. Azure. Commands. SQL. Audit. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="951d6-153">Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="951d6-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="951d6-154">NOTES</span></span>

## <span data-ttu-id="951d6-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="951d6-155">RELATED LINKS</span></span>
