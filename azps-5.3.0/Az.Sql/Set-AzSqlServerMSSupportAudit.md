---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 623f52f1de9370c679f6df09b6cf05c50f38ca6b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499398"
---
# <span data-ttu-id="cc180-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="cc180-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="cc180-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cc180-102">SYNOPSIS</span></span>
<span data-ttu-id="cc180-103">Zmienia ustawienia inspekcji operacji pomocy technicznej firmy Microsoft dotyczące programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cc180-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="cc180-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cc180-104">SYNTAX</span></span>

### <span data-ttu-id="cc180-105">ServerParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cc180-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc180-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc180-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc180-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cc180-107">DESCRIPTION</span></span>
<span data-ttu-id="cc180-108">Polecenie cmdlet **Set-AzSqlServerMSSupportAudit** powoduje zmianę ustawień inspekcji operacji pomocy technicznej firmy Microsoft dla programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cc180-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="cc180-109">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="cc180-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="cc180-110">Gdy magazyn obiektów BLOB jest miejscem docelowym dla dzienników inspekcji, określ parametr *StorageAccountResourceId* , aby określić konto magazynu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cc180-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="cc180-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cc180-111">EXAMPLES</span></span>

### <span data-ttu-id="cc180-112">Przykład 1: Włączanie zasad inspekcji operacji pomocy technicznej Microsoft dotyczących magazynu obiektów BLOB dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc180-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="cc180-113">Przykład 2: wyłączanie zasad inspekcji operacji pomocy technicznej firmy Microsoft w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc180-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="cc180-114">Przykład 3: Włączanie zasad inspekcji operacji pomocy technicznej Microsoft dotyczących usługi centrum zdarzeń w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc180-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="cc180-115">Przykład 4: wyłączanie zasad inspekcji usług centrum zdarzeń w usłudze Microsoft dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc180-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="cc180-116">Przykład 5: Włączanie zasad inspekcji operacji pomocy technicznej dla usługi Microsoft log w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc180-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="cc180-117">Przykład 6: wyłączenie zasad inspekcji operacji pomocy technicznej dla usługi Microsoft log w usłudze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc180-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="cc180-118">Przykład 7: wyłączanie, za pośrednictwem rurociągu, zasady inspekcji operacji pomocy technicznej firmy Microsoft dotyczące usługi SQL Server</span><span class="sxs-lookup"><span data-stu-id="cc180-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="cc180-119">Przykład 8: wyłączanie wysyłania rekordów inspekcji operacji pomocy technicznej firmy Microsoft w usłudze Azure SQL Server do magazynu obiektów blob i włączanie wysyłania ich do analizy dzienników.</span><span class="sxs-lookup"><span data-stu-id="cc180-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="cc180-120">Przykład 9: Włączanie wysyłania rekordów inspekcji operacji pomocy technicznej firmy Microsoft w programie Azure SQL Server do magazynu obiektów blob, centrum zdarzeń i analizy dzienników.</span><span class="sxs-lookup"><span data-stu-id="cc180-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="cc180-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cc180-121">PARAMETERS</span></span>

### <span data-ttu-id="cc180-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc180-122">-AsJob</span></span>
<span data-ttu-id="cc180-123">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cc180-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc180-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="cc180-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="cc180-125">Wskazuje, czy Magazyn obiektów BLOB jest miejscem docelowym dla rekordów inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc180-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="cc180-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc180-126">-DefaultProfile</span></span>
<span data-ttu-id="cc180-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cc180-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc180-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="cc180-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="cc180-129">Identyfikator zasobu dla reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="cc180-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="cc180-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="cc180-130">-EventHubName</span></span>
<span data-ttu-id="cc180-131">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="cc180-131">The name of the event hub.</span></span> <span data-ttu-id="cc180-132">Jeśli w trakcie dostarczania EventHubAuthorizationRuleResourceId zostanie wybrana opcja Brak, zostanie wybrany domyślny centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="cc180-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="cc180-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="cc180-133">-EventHubTargetState</span></span>
<span data-ttu-id="cc180-134">Wskazuje, czy centrum zdarzeń jest miejscem docelowym dla rekordów inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc180-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="cc180-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="cc180-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="cc180-136">Wskazuje, czy Analiza dzienników jest lokalizacją docelową dla rekordów inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc180-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="cc180-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc180-137">-PassThru</span></span>
<span data-ttu-id="cc180-138">Określa, czy na końcu wykonania polecenia cmdlet mają być wyprowadzane zasady inspekcji działań pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc180-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="cc180-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc180-139">-ResourceGroupName</span></span>
<span data-ttu-id="cc180-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cc180-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="cc180-141">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="cc180-141">-ServerName</span></span>
<span data-ttu-id="cc180-142">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="cc180-142">SQL server name.</span></span>

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

### <span data-ttu-id="cc180-143">-Serverobject</span><span class="sxs-lookup"><span data-stu-id="cc180-143">-ServerObject</span></span>
<span data-ttu-id="cc180-144">Obiekt serwera do zarządzania zasadami inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc180-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="cc180-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cc180-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="cc180-146">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="cc180-146">The storage account resource id</span></span>

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

### <span data-ttu-id="cc180-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="cc180-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="cc180-148">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analiza dziennika) dla obszaru roboczego analizy dzienników, do którego chcesz wysłać dzienniki inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="cc180-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="cc180-149">Przykład:/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="cc180-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="cc180-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cc180-150">-Confirm</span></span>
<span data-ttu-id="cc180-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc180-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc180-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc180-152">-WhatIf</span></span>
<span data-ttu-id="cc180-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc180-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc180-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cc180-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc180-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc180-155">CommonParameters</span></span>
<span data-ttu-id="cc180-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc180-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc180-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc180-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc180-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cc180-158">INPUTS</span></span>

### <span data-ttu-id="cc180-159">System. String</span><span class="sxs-lookup"><span data-stu-id="cc180-159">System.String</span></span>

### <span data-ttu-id="cc180-160">Microsoft. Azure. Commands. SQL. Server. model. AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="cc180-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="cc180-161">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cc180-161">System.Guid</span></span>

### <span data-ttu-id="cc180-162">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cc180-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cc180-163">Microsoft. Azure. Commands. SQL. Audit. model. ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="cc180-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="cc180-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cc180-164">OUTPUTS</span></span>

### <span data-ttu-id="cc180-165">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc180-165">System.Boolean</span></span>

## <span data-ttu-id="cc180-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cc180-166">NOTES</span></span>

## <span data-ttu-id="cc180-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cc180-167">RELATED LINKS</span></span>
