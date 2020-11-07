---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAuditing.md
ms.openlocfilehash: ba225571780d4d09dfd5ecc1b47132462468b734
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707917"
---
# <span data-ttu-id="62ca6-101">Get-AzSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="62ca6-101">Get-AzSqlServerAuditing</span></span>

## <span data-ttu-id="62ca6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="62ca6-103">Pobiera ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62ca6-103">Gets the auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="62ca6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62ca6-104">SYNTAX</span></span>

### <span data-ttu-id="62ca6-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="62ca6-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca6-106">EventHubSet</span><span class="sxs-lookup"><span data-stu-id="62ca6-106">EventHubSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca6-107">LogAnalyticsSet</span><span class="sxs-lookup"><span data-stu-id="62ca6-107">LogAnalyticsSet</span></span>
```
Get-AzSqlServerAuditing [-ResourceGroupName] <String> [-ServerName] <String> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca6-108">BlobStorageByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="62ca6-108">BlobStorageByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-BlobStorage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca6-109">EventHubByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="62ca6-109">EventHubByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-EventHub]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ca6-110">LogAnalyticsByParentResourceSet</span><span class="sxs-lookup"><span data-stu-id="62ca6-110">LogAnalyticsByParentResourceSet</span></span>
```
Get-AzSqlServerAuditing -InputObject <AzureSqlServerModel> [-LogAnalytics]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ca6-111">Opis</span><span class="sxs-lookup"><span data-stu-id="62ca6-111">DESCRIPTION</span></span>
<span data-ttu-id="62ca6-112">Polecenie cmdlet **Get-AzSqlServerAuditing** pobiera ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="62ca6-112">The **Get-AzSqlServerAuditing** cmdlet gets the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="62ca6-113">Określ parametry *ResourceGroupName* i *nazwa_serwera* identyfikujące serwer.</span><span class="sxs-lookup"><span data-stu-id="62ca6-113">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="62ca6-114">Miejsce docelowe dzienników inspekcji jest określane przez określenie jednego z następujących parametrów przełącznika: BlobStorage, LogAnalytics lub EventHub (jeśli nie jest określona, wartość domyślna to BlobStorage).</span><span class="sxs-lookup"><span data-stu-id="62ca6-114">The audit logs destination is determined by specifying one of the following switch parameters: BlobStorage, LogAnalytics or EventHub (if none is specified, the default is BlobStorage).</span></span>

## <span data-ttu-id="62ca6-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62ca6-115">EXAMPLES</span></span>

### <span data-ttu-id="62ca6-116">Przykład 1: uzyskiwanie ustawień inspekcji magazynu obiektów BLOB dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="62ca6-116">Example 1: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
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

### <span data-ttu-id="62ca6-117">Przykład 2: uzyskiwanie ustawień inspekcji magazynu obiektów BLOB dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="62ca6-117">Example 2: Get the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -BlobStorage
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

### <span data-ttu-id="62ca6-118">Przykład 3: uzyskiwanie, za pośrednictwem rurociągu, ustawienia inspekcji magazynu obiektów BLOB w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="62ca6-118">Example 3: Get, through pipeline, the blob storage auditing settings of an Azure SQL server</span></span>
```
PS C:\> Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Get-AzSqlServerAuditing -BlobStorage
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

### <span data-ttu-id="62ca6-119">Przykład 4: uzyskiwanie ustawień inspekcji centrum zdarzeń dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="62ca6-119">Example 4: Get the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="62ca6-120">Przykład 5: Get, za pośrednictwem rurociągu — ustawienia inspekcji centrum zdarzeń programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="62ca6-120">Example 5: Get, through pipeline, the event hub auditing settings of an Azure SQL server</span></span>
```
PS C:\>$server = Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
PS C:\>$server | Get-AzSqlServerAuditing -EventHub
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName                   : resourcegroup01
ServerName                          : server01
AuditState                          : Enabled
PredicateExpression                 : statement <> 'select 1'
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
```

### <span data-ttu-id="62ca6-121">Przykład 6: Pobieranie ustawień inspekcji analizy dzienników programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="62ca6-121">Example 6: Get the log analytics auditing settings of an Azure SQL server</span></span>
```
PS C:\>Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01" -LogAnalytics
AuditActionGroup    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                       BATCH_COMPLETED_GROUP, ...}
ResourceGroupName   : resourcegroup01
ServerName          : server01
AuditState          : Enabled
PredicateExpression : statement <> 'select 1'
WorkspaceResourceId : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="62ca6-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62ca6-122">PARAMETERS</span></span>

### <span data-ttu-id="62ca6-123">-BlobStorage</span><span class="sxs-lookup"><span data-stu-id="62ca6-123">-BlobStorage</span></span>
<span data-ttu-id="62ca6-124">Określa, że miejsce docelowe dziennika inspekcji jest magazynem obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="62ca6-124">Specifies that audit logs destination is blob storage</span></span>

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

### <span data-ttu-id="62ca6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ca6-125">-DefaultProfile</span></span>
<span data-ttu-id="62ca6-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62ca6-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62ca6-127">— EventHub</span><span class="sxs-lookup"><span data-stu-id="62ca6-127">-EventHub</span></span>
<span data-ttu-id="62ca6-128">Określa, że miejscem docelowym dziennika inspekcji jest centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="62ca6-128">Specifies that audit logs destination is event hub</span></span>

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

### <span data-ttu-id="62ca6-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="62ca6-129">-InputObject</span></span>
<span data-ttu-id="62ca6-130">Obiekt serwera do zarządzania zasadami inspekcji.</span><span class="sxs-lookup"><span data-stu-id="62ca6-130">The server object to manage its audit policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel
Parameter Sets: BlobStorageByParentResourceSet, EventHubByParentResourceSet, LogAnalyticsByParentResourceSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62ca6-131">-LogAnalytics</span><span class="sxs-lookup"><span data-stu-id="62ca6-131">-LogAnalytics</span></span>
<span data-ttu-id="62ca6-132">Określa, że miejscem docelowym dziennika inspekcji jest Analiza dzienników</span><span class="sxs-lookup"><span data-stu-id="62ca6-132">Specifies that audit logs destination is log analytics</span></span>

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

### <span data-ttu-id="62ca6-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ca6-133">-ResourceGroupName</span></span>
<span data-ttu-id="62ca6-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62ca6-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="62ca6-135">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="62ca6-135">-ServerName</span></span>
<span data-ttu-id="62ca6-136">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="62ca6-136">SQL server name.</span></span>

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

### <span data-ttu-id="62ca6-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62ca6-137">-Confirm</span></span>
<span data-ttu-id="62ca6-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ca6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ca6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ca6-139">-WhatIf</span></span>
<span data-ttu-id="62ca6-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ca6-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="62ca6-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62ca6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ca6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ca6-142">CommonParameters</span></span>
<span data-ttu-id="62ca6-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ca6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ca6-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62ca6-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ca6-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ca6-145">INPUTS</span></span>

### <span data-ttu-id="62ca6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="62ca6-146">System.String</span></span>

### <span data-ttu-id="62ca6-147">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="62ca6-147">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="62ca6-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="62ca6-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="62ca6-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62ca6-149">OUTPUTS</span></span>

### <span data-ttu-id="62ca6-150">Microsoft. Azure. Commands. SQL. Audit. model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="62ca6-150">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="62ca6-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62ca6-151">NOTES</span></span>

## <span data-ttu-id="62ca6-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62ca6-152">RELATED LINKS</span></span>
