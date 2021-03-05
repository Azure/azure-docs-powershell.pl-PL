---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlServerMSSupportAudit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerMSSupportAudit.md
ms.openlocfilehash: 6e101beb73b68427f806fdae3fa2406082a9b47a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985573"
---
# <span data-ttu-id="1e4f8-101">Set-AzSqlServerMSSupportAudit</span><span class="sxs-lookup"><span data-stu-id="1e4f8-101">Set-AzSqlServerMSSupportAudit</span></span>

## <span data-ttu-id="1e4f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4f8-103">Zmienia ustawienia inspekcji operacji pomocy technicznej firmy Microsoft na serwerze Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-103">Changes the Microsoft support operations auditing settings of an Azure SQL server.</span></span>

## <span data-ttu-id="1e4f8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e4f8-104">SYNTAX</span></span>

### <span data-ttu-id="1e4f8-105">ServerParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1e4f8-105">ServerParameterSet (Default)</span></span>
```
Set-AzSqlServerMSSupportAudit
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>] [-EventHubAuthorizationRuleResourceId <String>]
 [-LogAnalyticsTargetState <String>] [-WorkspaceResourceId <String>]
 [-PassThru] [-ResourceGroupName] <String> [-ServerName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4f8-106">ServerObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e4f8-106">ServerObjectParameterSet</span></span>
```
Set-AzSqlServerMSSupportAudit [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-EventHubTargetState <String>] [-EventHubName <String>]
 [-EventHubAuthorizationRuleResourceId <String>] [-LogAnalyticsTargetState <String>]
 [-WorkspaceResourceId <String>] [-PassThru] -ServerObject <AzureSqlServerModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e4f8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e4f8-107">DESCRIPTION</span></span>
<span data-ttu-id="1e4f8-108">Polecenie **cmdlet Set-AzSqlServerMSSupportAudit** zmienia ustawienia inspekcji operacji pomocy technicznej firmy Microsoft serwera AZURE SQL.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-108">The **Set-AzSqlServerMSSupportAudit** cmdlet changes the  Microsoft support operations auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1e4f8-109">Aby użyć polecenia cmdlet, określ serwer za pomocą parametrów *ResourceGroupName* i *ServerName.*</span><span class="sxs-lookup"><span data-stu-id="1e4f8-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="1e4f8-110">Jeśli magazyn obiektów blob jest miejscem docelowym dzienników inspekcji, określ parametr *StorageAccountResourceId* w celu określenia konta magazynu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs.</span></span>

## <span data-ttu-id="1e4f8-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e4f8-111">EXAMPLES</span></span>

### <span data-ttu-id="1e4f8-112">Przykład 1. Włączanie zasad inspekcji inspekcji operacji obsługi magazynu obiektów blob firmy Microsoft na serwerze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1e4f8-112">Example 1: Enable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### <span data-ttu-id="1e4f8-113">Przykład 2. Wyłączenie zasad inspekcji inspekcji operacji obsługi magazynu obiektów blob programu Microsoft Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1e4f8-113">Example 2: Disable the blob storage Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1e4f8-114">Przykład 3. Włączanie zasad inspekcji inspekcji operacji w centrum zdarzeń firmy Microsoft na serwerze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1e4f8-114">Example 3: Enable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId"
```

### <span data-ttu-id="1e4f8-115">Przykład 4. Wyłączenie zasad inspekcji inspekcji operacji pomocy technicznej centrum zdarzeń firmy Microsoft na serwerze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1e4f8-115">Example 4: Disable the event hub Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventHubTargetState Disabled
```

### <span data-ttu-id="1e4f8-116">Przykład 5. Włączanie zasad inspekcji inspekcji operacji obsługi dzienników firmy Microsoft na serwerze Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="1e4f8-116">Example 5: Enable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### <span data-ttu-id="1e4f8-117">Przykład 6. Wyłączenie zasad inspekcji inspekcji operacji obsługi dzienników firmy Microsoft na serwerze Azure SQL</span><span class="sxs-lookup"><span data-stu-id="1e4f8-117">Example 6: Disable the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1e4f8-118">Przykład 7. Wyłączanie za pośrednictwem potoku zasad inspekcji inspekcji operacji obsługi logów programu Azure SQL Server przez firmę Microsoft</span><span class="sxs-lookup"><span data-stu-id="1e4f8-118">Example 7: Disable, through pipeline, the log analytics Microsoft support operations auditing policy of an Azure SQL server</span></span>
```powershell
PS C:\>Get-AzSqlServer -ResourceGroupName "ResourceGroup01" -ServerName "Server01" | Set-AzSqlServerMSSupportAudit -LogAnalyticsTargetState Disabled
```

### <span data-ttu-id="1e4f8-119">Przykład 8. Wyłączanie wysyłania rekordów inspekcji operacji pomocy technicznej firmy Microsoft w serwerze Azure SQL do magazynu obiektów blob i włączanie wysyłania ich do analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-119">Example 8: Disable sending Microsoft support operations audit records of an Azure SQL server to blob storage, and enable sending them to log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -LogAnalyticsTargetState Enabled -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2" -BlobStorageTargetState Disabled
```

### <span data-ttu-id="1e4f8-120">Przykład 9. Umożliwianie wysyłania rekordów inspekcji działań pomocy technicznej firmy Microsoft w programie Azure SQL Server do magazynu obiektów blob, centrum zdarzeń i analizy dziennika.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-120">Example 9: Enable sending Microsoft support operations audit records of an Azure SQL server to blob storage, event hub and log analytics.</span></span>
```powershell
PS C:\>Set-AzSqlServerMSSupportAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -EventHubTargetState Enabled -EventHubName "EventHubName" -EventHubAuthorizationRuleResourceId "EventHubAuthorizationRuleResourceId" -LogAnalyticsTargetState Enabled  -WorkspaceResourceId "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

## <span data-ttu-id="1e4f8-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e4f8-121">PARAMETERS</span></span>

### <span data-ttu-id="1e4f8-122">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1e4f8-122">-AsJob</span></span>
<span data-ttu-id="1e4f8-123">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1e4f8-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e4f8-124">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="1e4f8-124">-BlobStorageTargetState</span></span>
<span data-ttu-id="1e4f8-125">Wskazuje, czy magazyn obiektów blob jest miejscem docelowym rekordów inspekcji działań pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-125">Indicates whether blob storage is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1e4f8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4f8-126">-DefaultProfile</span></span>
<span data-ttu-id="1e4f8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e4f8-128">-EventHubAuthorizationRuleResourceId</span><span class="sxs-lookup"><span data-stu-id="1e4f8-128">-EventHubAuthorizationRuleResourceId</span></span>
<span data-ttu-id="1e4f8-129">Identyfikator zasobu reguły autoryzacji centrum zdarzeń</span><span class="sxs-lookup"><span data-stu-id="1e4f8-129">The resource Id for the event hub authorization rule</span></span>

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

### <span data-ttu-id="1e4f8-130">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="1e4f8-130">-EventHubName</span></span>
<span data-ttu-id="1e4f8-131">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-131">The name of the event hub.</span></span> <span data-ttu-id="1e4f8-132">Jeśli podczas dostarczania wartości EventHubAuthorizationRuleResourceId nie zostanie określone żadne, zostanie wybrane domyślne centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-132">If none is specified when providing EventHubAuthorizationRuleResourceId, the default event hub will be selected.</span></span>

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

### <span data-ttu-id="1e4f8-133">-EventHubTargetState</span><span class="sxs-lookup"><span data-stu-id="1e4f8-133">-EventHubTargetState</span></span>
<span data-ttu-id="1e4f8-134">Wskazuje, czy centrum zdarzeń jest miejscem docelowym rekordów inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-134">Indicates whether event hub is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1e4f8-135">-LogAnalyticsTargetState</span><span class="sxs-lookup"><span data-stu-id="1e4f8-135">-LogAnalyticsTargetState</span></span>
<span data-ttu-id="1e4f8-136">Wskazuje, czy analiza dziennika jest miejscem docelowym rekordów inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-136">Indicates whether log analytics is a destination for Microsoft support operations audit records.</span></span>

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

### <span data-ttu-id="1e4f8-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e4f8-137">-PassThru</span></span>
<span data-ttu-id="1e4f8-138">Określa, czy zasady inspekcji inspekcji pomocy technicznej firmy Microsoft mają być wyprowadzone po zakończeniu wykonywania polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-138">Specifies whether to output the Microsoft support operations auditing policy at end of cmdlet execution</span></span>

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

### <span data-ttu-id="1e4f8-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4f8-139">-ResourceGroupName</span></span>
<span data-ttu-id="1e4f8-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="1e4f8-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1e4f8-141">-ServerName</span></span>
<span data-ttu-id="1e4f8-142">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-142">SQL server name.</span></span>

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

### <span data-ttu-id="1e4f8-143">-ServerObject</span><span class="sxs-lookup"><span data-stu-id="1e4f8-143">-ServerObject</span></span>
<span data-ttu-id="1e4f8-144">Obiekt serwera do zarządzania zasadami inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-144">The server object to manage its Microsoft support operations audit policy.</span></span>

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

### <span data-ttu-id="1e4f8-145">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1e4f8-145">-StorageAccountResourceId</span></span>
<span data-ttu-id="1e4f8-146">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1e4f8-146">The storage account resource id</span></span>

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

### <span data-ttu-id="1e4f8-147">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="1e4f8-147">-WorkspaceResourceId</span></span>
<span data-ttu-id="1e4f8-148">Identyfikator obszaru roboczego (identyfikator zasobu obszaru roboczego analizy dziennika) dla obszaru roboczego analizy dziennika, do którego chcesz wysłać dzienniki inspekcji operacji pomocy technicznej firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-148">The workspace ID (resource ID of a Log Analytics workspace) for a Log Analytics workspace to which you would like to send Microsoft support operations Audit Logs.</span></span> <span data-ttu-id="1e4f8-149">Przykład: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span><span class="sxs-lookup"><span data-stu-id="1e4f8-149">Example: /subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2</span></span>

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

### <span data-ttu-id="1e4f8-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e4f8-150">-Confirm</span></span>
<span data-ttu-id="1e4f8-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e4f8-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e4f8-152">-WhatIf</span></span>
<span data-ttu-id="1e4f8-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e4f8-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e4f8-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4f8-155">CommonParameters</span></span>
<span data-ttu-id="1e4f8-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4f8-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4f8-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e4f8-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4f8-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e4f8-158">INPUTS</span></span>

### <span data-ttu-id="1e4f8-159">System.String</span><span class="sxs-lookup"><span data-stu-id="1e4f8-159">System.String</span></span>

### <span data-ttu-id="1e4f8-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span><span class="sxs-lookup"><span data-stu-id="1e4f8-160">Microsoft.Azure.Commands.Sql.Server.Model.AzureSqlServerModel</span></span>

### <span data-ttu-id="1e4f8-161">System.Guid</span><span class="sxs-lookup"><span data-stu-id="1e4f8-161">System.Guid</span></span>

### <span data-ttu-id="1e4f8-162">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1e4f8-162">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1e4f8-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span><span class="sxs-lookup"><span data-stu-id="1e4f8-163">Microsoft.Azure.Commands.Sql.Auditing.Model.ServerDevOpsAuditModel</span></span>

## <span data-ttu-id="1e4f8-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e4f8-164">OUTPUTS</span></span>

### <span data-ttu-id="1e4f8-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1e4f8-165">System.Boolean</span></span>

## <span data-ttu-id="1e4f8-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e4f8-166">NOTES</span></span>

## <span data-ttu-id="1e4f8-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e4f8-167">RELATED LINKS</span></span>
