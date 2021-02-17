---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: c59034dcd587c9fee3ce6a4a7699670c77ea372f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415380"
---
# <span data-ttu-id="19768-101">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="19768-101">Set-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="19768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19768-102">SYNOPSIS</span></span>
<span data-ttu-id="19768-103">Aktualizuje zasób dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="19768-103">Updates flow log resource.</span></span>

## <span data-ttu-id="19768-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19768-104">SYNTAX</span></span>

### <span data-ttu-id="19768-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="19768-105">SetByName (Default)</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="19768-106">SetByResource</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="19768-107">SetByResourceWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="19768-108">SetByNameWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="19768-109">SetByLocation</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="19768-110">SetByLocationWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-111">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="19768-111">SetByResourceId</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-112">SetByResourceIdWithTA</span><span class="sxs-lookup"><span data-stu-id="19768-112">SetByResourceIdWithTA</span></span>
```
Set-AzNetworkWatcherFlowLog -ResourceId <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-113">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="19768-113">SetByInputObject</span></span>
```
Set-AzNetworkWatcherFlowLog -InputObject <PSFlowLogResource> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19768-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="19768-114">DESCRIPTION</span></span>
<span data-ttu-id="19768-115">Aktualizuje zasób dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="19768-115">Updates flow log resource.</span></span>

## <span data-ttu-id="19768-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19768-116">EXAMPLES</span></span>

### <span data-ttu-id="19768-117">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="19768-117">Example 1</span></span>
```powershell
PS C:\> $flowLog = Get-AzNetworkWatcherFlowLog -Location eastus -Name pstest
PS C:\> $flowLog.Enabled = $true
PS C:\> $flowLog.Format.Version = 2
PS C:\> $flowLog | Set-AzNetworkWatcherFlowLog -Force
```

<span data-ttu-id="19768-118">Nazwa: identyfikator pstest : /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag: W /"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState: Succeeded Location : eastus TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/bbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled: True RetentionPolicy: { "Days": 0, "Enabled": false } Format: { "Type": "JSON", "Wersja": 2 } FlowAnalyticsConfiguration: {}</span><span class="sxs-lookup"><span data-stu-id="19768-118">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"e939e1e6-1509-4d7a-9e89-1ea532f6f222" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MyStorage Enabled                    : True RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : {}</span></span>

## <span data-ttu-id="19768-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19768-119">PARAMETERS</span></span>

### <span data-ttu-id="19768-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19768-120">-DefaultProfile</span></span>
<span data-ttu-id="19768-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="19768-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-122">— włączone</span><span class="sxs-lookup"><span data-stu-id="19768-122">-Enabled</span></span>
<span data-ttu-id="19768-123">Oflaguj, aby włączyć/wyłączyć rejestrowanie przepływu.</span><span class="sxs-lookup"><span data-stu-id="19768-123">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-124">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="19768-124">-EnableRetention</span></span>
<span data-ttu-id="19768-125">Oflaguj, aby włączyć/wyłączyć przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="19768-125">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-126">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="19768-126">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="19768-127">Oflaguj, aby włączyć/wyłączyć funkcję TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="19768-127">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-128">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="19768-128">-Force</span></span>
<span data-ttu-id="19768-129">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="19768-129">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-130">-FormatType</span><span class="sxs-lookup"><span data-stu-id="19768-130">-FormatType</span></span>
<span data-ttu-id="19768-131">Typ pliku dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="19768-131">The file type of flow log.</span></span>
<span data-ttu-id="19768-132">Obecnie jedyną obsługiwaną wartością jest "JSON".</span><span class="sxs-lookup"><span data-stu-id="19768-132">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-133">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="19768-133">-FormatVersion</span></span>
<span data-ttu-id="19768-134">Wersja (poprawka) dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="19768-134">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19768-135">-InputObject</span></span>
<span data-ttu-id="19768-136">Obiekt przepływu.</span><span class="sxs-lookup"><span data-stu-id="19768-136">Flow lof object.</span></span>

```yaml
Type: PSFlowLogResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19768-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="19768-137">-Location</span></span>
<span data-ttu-id="19768-138">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="19768-138">Location of the network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByLocation, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="19768-139">-Name</span></span>
<span data-ttu-id="19768-140">Nazwa dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="19768-140">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-141">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19768-141">-NetworkWatcher</span></span>
<span data-ttu-id="19768-142">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="19768-142">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource, SetByResourceWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19768-143">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="19768-143">-NetworkWatcherName</span></span>
<span data-ttu-id="19768-144">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="19768-144">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19768-145">-ResourceGroupName</span></span>
<span data-ttu-id="19768-146">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="19768-146">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByNameWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19768-147">-ResourceId</span></span>
<span data-ttu-id="19768-148">Identyfikator zasobu FlowLog.</span><span class="sxs-lookup"><span data-stu-id="19768-148">FlowLog resource ID.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19768-149">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="19768-149">-RetentionPolicyDays</span></span>
<span data-ttu-id="19768-150">Liczba dni, przez które mają być zachowywane rekordy dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="19768-150">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-151">- StorageId</span><span class="sxs-lookup"><span data-stu-id="19768-151">-StorageId</span></span>
<span data-ttu-id="19768-152">Identyfikator konta magazynu służącego do przechowywania dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="19768-152">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-153">— Tag</span><span class="sxs-lookup"><span data-stu-id="19768-153">-Tag</span></span>
<span data-ttu-id="19768-154">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="19768-154">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-155">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="19768-155">-TargetResourceId</span></span>
<span data-ttu-id="19768-156">Identyfikator grupy zabezpieczeń sieci, do której zostanie zastosowany dziennik przepływu.</span><span class="sxs-lookup"><span data-stu-id="19768-156">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: SetByName, SetByResource, SetByResourceWithTA, SetByNameWithTA, SetByLocation, SetByLocationWithTA, SetByResourceId, SetByResourceIdWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-157">- TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="19768-157">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="19768-158">Interwał w minutach, który określa, jak często usługa TA powinna wykonać analizę przepływu.</span><span class="sxs-lookup"><span data-stu-id="19768-158">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-159">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="19768-159">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="19768-160">Identyfikator zasobu dołączonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="19768-160">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA, SetByResourceIdWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19768-161">-Confirm</span></span>
<span data-ttu-id="19768-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="19768-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19768-163">-WhatIf</span></span>
<span data-ttu-id="19768-164">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19768-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19768-165">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="19768-165">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19768-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19768-166">CommonParameters</span></span>
<span data-ttu-id="19768-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19768-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19768-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19768-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19768-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19768-169">INPUTS</span></span>

### <span data-ttu-id="19768-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19768-170">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="19768-171">System.String</span><span class="sxs-lookup"><span data-stu-id="19768-171">System.String</span></span>

### <span data-ttu-id="19768-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="19768-172">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="19768-173">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19768-173">OUTPUTS</span></span>

### <span data-ttu-id="19768-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="19768-174">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="19768-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19768-175">NOTES</span></span>

## <span data-ttu-id="19768-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19768-176">RELATED LINKS</span></span>

[<span data-ttu-id="19768-177">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19768-177">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="19768-178">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19768-178">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="19768-179">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="19768-179">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="19768-180">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="19768-180">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="19768-181">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="19768-181">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="19768-182">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="19768-182">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="19768-183">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="19768-183">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="19768-184">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19768-184">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19768-185">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="19768-185">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="19768-186">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19768-186">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19768-187">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19768-187">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19768-188">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="19768-188">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="19768-189">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="19768-189">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="19768-190">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="19768-190">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="19768-191">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="19768-191">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="19768-192">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="19768-192">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="19768-193">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="19768-193">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="19768-194">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="19768-194">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="19768-195">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="19768-195">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="19768-196">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="19768-196">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="19768-197">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="19768-197">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="19768-198">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="19768-198">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="19768-199">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="19768-199">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="19768-200">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="19768-200">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="19768-201">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="19768-201">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="19768-202">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="19768-202">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="19768-203">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="19768-203">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="19768-204">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="19768-204">New-AzNetworkWatcherFlowLog</span></span>](./New-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="19768-205">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="19768-205">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="19768-206">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="19768-206">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
