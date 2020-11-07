---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 4a64226f5445c77c262f1c0521a58d4f3f00ac99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708950"
---
# <span data-ttu-id="cdb61-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cdb61-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="cdb61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cdb61-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb61-103">Konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="cdb61-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="cdb61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cdb61-104">SYNTAX</span></span>

### <span data-ttu-id="cdb61-105">SetFlowlogByResourceWithoutTA (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cdb61-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb61-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="cdb61-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb61-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="cdb61-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb61-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="cdb61-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb61-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="cdb61-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb61-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="cdb61-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb61-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="cdb61-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb61-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="cdb61-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb61-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="cdb61-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cdb61-114">Opis</span><span class="sxs-lookup"><span data-stu-id="cdb61-114">DESCRIPTION</span></span>
<span data-ttu-id="cdb61-115">Set-AzNetworkWatcherConfigFlowLog konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="cdb61-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="cdb61-116">Właściwości do skonfigurowania: czy rejestrowanie przepływu jest włączone dla dostarczanego zasobu, skonfigurowane konto magazynu, w którym mają być wysyłane dzienniki, format rejestrowania przepływu oraz zasady przechowywania dzienników.</span><span class="sxs-lookup"><span data-stu-id="cdb61-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="cdb61-117">W przypadku rejestrowania przepływów są obsługiwane obecnie grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="cdb61-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="cdb61-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cdb61-118">EXAMPLES</span></span>

### <span data-ttu-id="cdb61-119">Przykład 1: Konfigurowanie rejestrowania przepływu dla określonego NSG</span><span class="sxs-lookup"><span data-stu-id="cdb61-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
```

<span data-ttu-id="cdb61-120">W tym przykładzie skonfigurowano stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="cdb61-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="cdb61-121">W odpowiedzi widać, że określony NSG ma włączone rejestrowanie przepływu, format domyślny i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="cdb61-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="cdb61-122">Przykład 2: Konfigurowanie rejestrowania przepływu dla określonego NSG i Ustawianie wersji rejestrowania przepływu na 2.</span><span class="sxs-lookup"><span data-stu-id="cdb61-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -FormatVersion 2

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 2
                   }
```

<span data-ttu-id="cdb61-123">W tym przykładzie skonfigurowano rejestrowanie przepływu w grupie zabezpieczeń sieci (NSG) z określonymi dziennikami w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="cdb61-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="cdb61-124">W odpowiedzi widać, że określony NSG ma włączone rejestrowanie przepływu, jest ustawiany format i nie skonfigurowano zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="cdb61-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="cdb61-125">Jeśli region nie obsługuje określonej wersji, obserwator sieci zapisze domyślną obsługiwaną wersję w regionie.</span><span class="sxs-lookup"><span data-stu-id="cdb61-125">If the region does not support version you specificed, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="cdb61-126">Przykład 3: Konfigurowanie rejestrowania przepływu i analizy ruchu dla określonego NSG</span><span class="sxs-lookup"><span data-stu-id="cdb61-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
Format           : {
                     "Type ": "Json",
                     "Version": 1
                   }
FlowAnalyticsConfiguration : {
            "networkWatcherFlowAnalyticsConfiguration": {
              "enabled": true,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
              "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="cdb61-127">W tym przykładzie skonfigurowano stan rejestrowania przepływu i analizy ruchu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="cdb61-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="cdb61-128">W odpowiedzi widać, że określony NSG ma włączone rejestrowanie przepływów oraz Analiza ruchu, format domyślny i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="cdb61-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="cdb61-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdb61-129">PARAMETERS</span></span>

### <span data-ttu-id="cdb61-130">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cdb61-130">-AsJob</span></span>
<span data-ttu-id="cdb61-131">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cdb61-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdb61-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb61-132">-DefaultProfile</span></span>
<span data-ttu-id="cdb61-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb61-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb61-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="cdb61-134">-EnableFlowLog</span></span>
<span data-ttu-id="cdb61-135">Flaga włączenia/wyłączenia rejestrowania przepływu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-135">Flag to enable/disable flow logging.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="cdb61-136">-EnableRetention</span></span>
<span data-ttu-id="cdb61-137">Flaga włączenia/wyłączenia przechowywania.</span><span class="sxs-lookup"><span data-stu-id="cdb61-137">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="cdb61-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="cdb61-139">Flaga włączenia/wyłączenia przechowywania.</span><span class="sxs-lookup"><span data-stu-id="cdb61-139">Flag to enable/disable retention.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases: EnableTA

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="cdb61-140">-FormatType</span></span>
<span data-ttu-id="cdb61-141">Typ dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-141">Type of flow log format.</span></span>

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

### <span data-ttu-id="cdb61-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="cdb61-142">-FormatVersion</span></span>
<span data-ttu-id="cdb61-143">Wersja formatu dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-143">Version of flow log format.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-144">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cdb61-144">-Location</span></span>
<span data-ttu-id="cdb61-145">Lokalizacja obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cdb61-145">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails, SetFlowlogByLocationWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-146">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb61-146">-NetworkWatcher</span></span>
<span data-ttu-id="cdb61-147">Zasób obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cdb61-147">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetFlowlogByResourceWithoutTA, SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cdb61-148">-NetworkWatcherName</span></span>
<span data-ttu-id="cdb61-149">Nazwa obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cdb61-149">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb61-150">-ResourceGroupName</span></span>
<span data-ttu-id="cdb61-151">Nazwa grupy zasobów obserwatora sieci.</span><span class="sxs-lookup"><span data-stu-id="cdb61-151">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByNameWithoutTA
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cdb61-152">-RetentionInDays</span></span>
<span data-ttu-id="cdb61-153">Liczba dni przechowywania rekordów dziennika przepływu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-153">Number of days to retain flow log records.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cdb61-154">-StorageAccountId</span></span>
<span data-ttu-id="cdb61-155">Identyfikator konta magazynu, które służy do przechowywania dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="cdb61-155">ID of the storage account which is used to store the flow log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb61-156">-TargetResourceId</span></span>
<span data-ttu-id="cdb61-157">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="cdb61-157">The target resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-158">-TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="cdb61-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="cdb61-159">Pobiera lub ustawia interwał (w minutach), który decyduje o tym, jak często usługa TA ma wykonywać analizy przepływu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

```yaml
Type: System.Int32
Parameter Sets: SetFlowlogByResourceWithTAByResource, SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByResource, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByResource, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-160">-Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="cdb61-160">-Workspace</span></span>
<span data-ttu-id="cdb61-161">Obiekt WS służący do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-161">The WS object which is used to store the traffic analytics data.</span></span>

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByResourceWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace
Parameter Sets: SetFlowlogByNameWithTAByResource, SetFlowlogByLocationWithTAByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-162">-WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="cdb61-162">-WorkspaceGUID</span></span>
<span data-ttu-id="cdb61-163">Identyfikator GUID protokołu WS służący do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="cdb61-164">-WorkspaceLocation</span></span>
<span data-ttu-id="cdb61-165">Obszar Azure w usłudze WS służący do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb61-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="cdb61-167">Abonament protokołu WS służącego do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="cdb61-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

```yaml
Type: System.String
Parameter Sets: SetFlowlogByResourceWithTAByDetails, SetFlowlogByNameWithTAByDetails, SetFlowlogByLocationWithTAByDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb61-168">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdb61-168">-Confirm</span></span>
<span data-ttu-id="cdb61-169">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdb61-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb61-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb61-170">-WhatIf</span></span>
<span data-ttu-id="cdb61-171">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdb61-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdb61-172">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cdb61-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb61-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb61-173">CommonParameters</span></span>
<span data-ttu-id="cdb61-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb61-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb61-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb61-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb61-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdb61-176">INPUTS</span></span>

### <span data-ttu-id="cdb61-177">Microsoft. Azure. Commands. Network. models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb61-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cdb61-178">System. String</span><span class="sxs-lookup"><span data-stu-id="cdb61-178">System.String</span></span>

### <span data-ttu-id="cdb61-179">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cdb61-179">System.Boolean</span></span>

### <span data-ttu-id="cdb61-180">System. Int32</span><span class="sxs-lookup"><span data-stu-id="cdb61-180">System.Int32</span></span>

### <span data-ttu-id="cdb61-181">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="cdb61-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="cdb61-182">Microsoft. Azure. Management. Internal. Network. Common. IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="cdb61-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="cdb61-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cdb61-183">OUTPUTS</span></span>

### <span data-ttu-id="cdb61-184">Microsoft. Azure. Commands. Network. models. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="cdb61-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="cdb61-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cdb61-185">NOTES</span></span>
<span data-ttu-id="cdb61-186">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking, monitor, przepływ, dzienniki, flowlog, rejestrowanie</span><span class="sxs-lookup"><span data-stu-id="cdb61-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="cdb61-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdb61-187">RELATED LINKS</span></span>

[<span data-ttu-id="cdb61-188">Nowe — AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb61-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cdb61-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb61-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cdb61-190">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cdb61-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cdb61-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cdb61-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cdb61-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cdb61-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cdb61-193">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cdb61-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cdb61-194">Start — AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cdb61-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cdb61-195">Nowe — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb61-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb61-196">Nowe — AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cdb61-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cdb61-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb61-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb61-198">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb61-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb61-199">Zatrzymaj — AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cdb61-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cdb61-200">Nowe — AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cdb61-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cdb61-201">Test — AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cdb61-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cdb61-202">Test — AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cdb61-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cdb61-203">Zatrzymaj — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb61-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb61-204">Start — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb61-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb61-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb61-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb61-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cdb61-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cdb61-207">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb61-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb61-208">Nowe — AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb61-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cdb61-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cdb61-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cdb61-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cdb61-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cdb61-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cdb61-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cdb61-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cdb61-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cdb61-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cdb61-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="cdb61-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cdb61-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)