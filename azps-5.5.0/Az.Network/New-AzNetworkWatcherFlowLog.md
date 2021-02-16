---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherFlowLog.md
ms.openlocfilehash: 3828318840d10e5d88ebda6327ad17b9126bf03d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414241"
---
# <span data-ttu-id="98cce-101">New-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="98cce-101">New-AzNetworkWatcherFlowLog</span></span>

## <span data-ttu-id="98cce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98cce-102">SYNOPSIS</span></span>
<span data-ttu-id="98cce-103">Utwórz lub zaktualizuj zasób dziennika przepływu dla określonej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="98cce-103">Create or update a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="98cce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="98cce-104">SYNTAX</span></span>

### <span data-ttu-id="98cce-105">SetByName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="98cce-105">SetByName (Default)</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98cce-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="98cce-106">SetByResource</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98cce-107">SetByResourceWithTA</span><span class="sxs-lookup"><span data-stu-id="98cce-107">SetByResourceWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcher <PSNetworkWatcher> -Name <String> -TargetResourceId <String>
 -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98cce-108">SetByNameWithTA</span><span class="sxs-lookup"><span data-stu-id="98cce-108">SetByNameWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -NetworkWatcherName <String> -ResourceGroupName <String> -Name <String>
 -TargetResourceId <String> -StorageId <String> -Enabled <Boolean> [-EnableRetention <Boolean>]
 [-RetentionPolicyDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-EnableTrafficAnalytics]
 [-TrafficAnalyticsWorkspaceId <String>] [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98cce-109">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="98cce-109">SetByLocation</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98cce-110">SetByLocationWithTA</span><span class="sxs-lookup"><span data-stu-id="98cce-110">SetByLocationWithTA</span></span>
```
New-AzNetworkWatcherFlowLog -Location <String> -Name <String> -TargetResourceId <String> -StorageId <String>
 -Enabled <Boolean> [-EnableRetention <Boolean>] [-RetentionPolicyDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-EnableTrafficAnalytics] [-TrafficAnalyticsWorkspaceId <String>]
 [-TrafficAnalyticsInterval <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98cce-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="98cce-111">DESCRIPTION</span></span>
<span data-ttu-id="98cce-112">New-AzNetworkWatcherFlowLog tworzy lub aktualizuje zasób dziennika przepływu dla określonej grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="98cce-112">New-AzNetworkWatcherFlowLog command creates or updates a flow log resource for the specified network security group.</span></span>

## <span data-ttu-id="98cce-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="98cce-113">EXAMPLES</span></span>

### <span data-ttu-id="98cce-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="98cce-114">Example 1</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $true -EnableRetention $true -RetentionPolicyDays 5 -FormatVersion 2 -EnableTrafficAnalytics -TrafficAnalyticsWorkspaceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace
```

<span data-ttu-id="98cce-115">Name : pstest Id : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState : Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled : True RetentionPolicy : { "Days": 5, "Enabled": true } Format : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="98cce-115">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : True RetentionPolicy            : { "Days": 5, "Enabled": true } Format                     : { "Type": "JSON", "Version": 2 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": true, "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb", "workspaceRegion": "eastus", "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegr oups/flowlogsv2demo/providers/Microsoft.OperationalInsights/workspaces/MyWorkspace", "trafficAnalyticsInterval": 60 } }</span></span>

### <span data-ttu-id="98cce-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="98cce-116">Example 2</span></span>
```powershell
PS C:\> New-AzNetworkWatcherFlowLog -Location eastus -Name pstest -TargetResourceId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/MyFlowLog/providers/Microsoft.Network/networkSecurityGroups/MyNSG -StorageId /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/FlowLogsV2Demo/providers/Microsoft.Storage/storageAccounts/MyStorage -Enabled $false -EnableTrafficAnalytics:$false
```

<span data-ttu-id="98cce-117">Jeśli chcesz wyłączyć zasób flowLog, dla którego skonfigurowano funkcję TrafficAnalytics, musisz również wyłączyć funkcję TrafficAnalytics.</span><span class="sxs-lookup"><span data-stu-id="98cce-117">If you want to disable flowLog resource for which TrafficAnalytics is configured, it is necessary to disable TrafficAnalytics as well.</span></span> <span data-ttu-id="98cce-118">Można to zrobić tak, jak w przykładzie 2.</span><span class="sxs-lookup"><span data-stu-id="98cce-118">It can be done like in the example 2.</span></span>

<span data-ttu-id="98cce-119">Nazwa: identyfikator pstest : /subscriptions/bbbbbb-bbbb-bbbb-bbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag: W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState: Succeeded Location : eastus TargetResourceId : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId: /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled: False RetentionPolicy: { "Days": { "Days": 0, "Enabled": false } Format: { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration: { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span><span class="sxs-lookup"><span data-stu-id="98cce-119">Name                       : pstest Id                         : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/provid ers/Microsoft.Network/networkWatchers/NetworkWatcher_eastus/FlowLogs/pstest Etag                       : W/"f6047360-d797-4ca6-a9ec-28b5aec5c768" ProvisioningState          : Succeeded Location                   : eastus TargetResourceId           : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/MyFlowLog/provide rs/Microsoft.Network/networkSecurityGroups/MyNSG StorageId                  : /subscriptions/56abfbd6-ec72-4ce9-831f-bc2b6f2c5505/resourceGroups/FlowLogsV2Demo/provider s/Microsoft.Storage/storageAccounts/MySTorage Enabled                    : False RetentionPolicy            : { "Days": 0, "Enabled": false } Format                     : { "Type": "JSON", "Version": 1 } FlowAnalyticsConfiguration : { "networkWatcherFlowAnalyticsConfiguration": { "enabled": false, "trafficAnalyticsInterval": 60 } }</span></span>

## <span data-ttu-id="98cce-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98cce-120">PARAMETERS</span></span>

### <span data-ttu-id="98cce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98cce-121">-DefaultProfile</span></span>
<span data-ttu-id="98cce-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="98cce-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98cce-123">— włączone</span><span class="sxs-lookup"><span data-stu-id="98cce-123">-Enabled</span></span>
<span data-ttu-id="98cce-124">Oflaguj, aby włączyć/wyłączyć rejestrowanie przepływu.</span><span class="sxs-lookup"><span data-stu-id="98cce-124">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-125">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="98cce-125">-EnableRetention</span></span>
<span data-ttu-id="98cce-126">Oflaguj, aby włączyć/wyłączyć przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="98cce-126">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-127">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="98cce-127">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="98cce-128">Oflaguj, aby włączyć/wyłączyć funkcję TrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="98cce-128">Flag to enable/disable TrafficAnalytics</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-129">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="98cce-129">-Force</span></span>
<span data-ttu-id="98cce-130">Nie pytaj o potwierdzenie, czy chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="98cce-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="98cce-131">-FormatType</span><span class="sxs-lookup"><span data-stu-id="98cce-131">-FormatType</span></span>
<span data-ttu-id="98cce-132">Typ pliku dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="98cce-132">The file type of flow log.</span></span>
<span data-ttu-id="98cce-133">Obecnie jedyną obsługiwaną wartością jest "JSON".</span><span class="sxs-lookup"><span data-stu-id="98cce-133">The only supported value now is 'JSON'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-134">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="98cce-134">-FormatVersion</span></span>
<span data-ttu-id="98cce-135">Wersja (poprawka) dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="98cce-135">The version (revision) of the flow log.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-136">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98cce-136">-Location</span></span>
<span data-ttu-id="98cce-137">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="98cce-137">Location of the network watcher.</span></span>

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

### <span data-ttu-id="98cce-138">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="98cce-138">-Name</span></span>
<span data-ttu-id="98cce-139">Nazwa dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="98cce-139">The flow log name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FlowLogName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-140">- NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98cce-140">-NetworkWatcher</span></span>
<span data-ttu-id="98cce-141">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="98cce-141">The network watcher resource.</span></span>

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

### <span data-ttu-id="98cce-142">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="98cce-142">-NetworkWatcherName</span></span>
<span data-ttu-id="98cce-143">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="98cce-143">The name of network watcher.</span></span>

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

### <span data-ttu-id="98cce-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98cce-144">-ResourceGroupName</span></span>
<span data-ttu-id="98cce-145">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="98cce-145">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="98cce-146">-RetentionPolicyDays</span><span class="sxs-lookup"><span data-stu-id="98cce-146">-RetentionPolicyDays</span></span>
<span data-ttu-id="98cce-147">Liczba dni, przez które mają być zachowywane rekordy dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="98cce-147">Number of days to retain flow log records.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-148">- StorageId</span><span class="sxs-lookup"><span data-stu-id="98cce-148">-StorageId</span></span>
<span data-ttu-id="98cce-149">Identyfikator konta magazynu służącego do przechowywania dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="98cce-149">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-150">— Tag</span><span class="sxs-lookup"><span data-stu-id="98cce-150">-Tag</span></span>
<span data-ttu-id="98cce-151">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="98cce-151">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="98cce-152">-TargetResourceId</span></span>
<span data-ttu-id="98cce-153">Identyfikator grupy zabezpieczeń sieci, do której zostanie zastosowany dziennik przepływu.</span><span class="sxs-lookup"><span data-stu-id="98cce-153">ID of network security group to which flow log will be applied.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-154">- TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="98cce-154">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="98cce-155">Interwał w minutach, który określa, jak często usługa TA powinna wykonać analizę przepływu.</span><span class="sxs-lookup"><span data-stu-id="98cce-155">The interval in minutes which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: Int32
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-156">-TrafficAnalyticsWorkspaceId</span><span class="sxs-lookup"><span data-stu-id="98cce-156">-TrafficAnalyticsWorkspaceId</span></span>
<span data-ttu-id="98cce-157">Identyfikator zasobu dołączonego obszaru roboczego.</span><span class="sxs-lookup"><span data-stu-id="98cce-157">Resource Id of the attached workspace.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceWithTA, SetByNameWithTA, SetByLocationWithTA
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98cce-158">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98cce-158">-Confirm</span></span>
<span data-ttu-id="98cce-159">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98cce-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98cce-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98cce-160">-WhatIf</span></span>
<span data-ttu-id="98cce-161">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98cce-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98cce-162">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="98cce-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98cce-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98cce-163">CommonParameters</span></span>
<span data-ttu-id="98cce-164">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98cce-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98cce-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98cce-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98cce-166">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98cce-166">INPUTS</span></span>

### <span data-ttu-id="98cce-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98cce-167">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="98cce-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="98cce-168">OUTPUTS</span></span>

### <span data-ttu-id="98cce-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span><span class="sxs-lookup"><span data-stu-id="98cce-169">Microsoft.Azure.Commands.Network.Models.PSFlowLogResource</span></span>

## <span data-ttu-id="98cce-170">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="98cce-170">NOTES</span></span>

## <span data-ttu-id="98cce-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98cce-171">RELATED LINKS</span></span>

[<span data-ttu-id="98cce-172">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98cce-172">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="98cce-173">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98cce-173">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="98cce-174">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="98cce-174">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="98cce-175">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="98cce-175">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="98cce-176">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="98cce-176">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="98cce-177">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="98cce-177">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="98cce-178">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="98cce-178">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="98cce-179">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98cce-179">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98cce-180">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="98cce-180">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="98cce-181">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98cce-181">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98cce-182">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98cce-182">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98cce-183">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="98cce-183">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="98cce-184">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="98cce-184">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="98cce-185">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="98cce-185">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="98cce-186">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="98cce-186">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="98cce-187">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98cce-187">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98cce-188">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98cce-188">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98cce-189">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98cce-189">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98cce-190">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="98cce-190">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="98cce-191">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98cce-191">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98cce-192">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98cce-192">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98cce-193">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="98cce-193">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="98cce-194">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="98cce-194">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="98cce-195">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="98cce-195">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="98cce-196">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="98cce-196">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="98cce-197">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="98cce-197">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="98cce-198">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="98cce-198">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="98cce-199">Get-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="98cce-199">Get-AzNetworkWatcherFlowLog</span></span>](./Get-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="98cce-200">Set-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="98cce-200">Set-AzNetworkWatcherFlowLog</span></span>](./Set-AzNetworkWatcherFlowLog.md)

[<span data-ttu-id="98cce-201">Remove-AzNetworkWatcherFlowLog</span><span class="sxs-lookup"><span data-stu-id="98cce-201">Remove-AzNetworkWatcherFlowLog</span></span>](./Remove-AzNetworkWatcherFlowLog.md)
