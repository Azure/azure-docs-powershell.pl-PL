---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: c6ec48d0f2a69a0414699c04a82caa64319cf0dd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403548"
---
# <span data-ttu-id="ac705-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ac705-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="ac705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac705-102">SYNOPSIS</span></span>
<span data-ttu-id="ac705-103">Konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="ac705-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="ac705-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ac705-104">SYNTAX</span></span>

### <span data-ttu-id="ac705-105">SetFlowlogByResourceWithoutTA (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ac705-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac705-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="ac705-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac705-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="ac705-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac705-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="ac705-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac705-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="ac705-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac705-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="ac705-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac705-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="ac705-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac705-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="ac705-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac705-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="ac705-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ac705-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="ac705-114">DESCRIPTION</span></span>
<span data-ttu-id="ac705-115">Ta Set-AzNetworkWatcherConfigFlowLog konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="ac705-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="ac705-116">Do właściwości, które należy skonfigurować, należą: czy dla udostępnianego zasobu włączono rejestrowanie przepływu, skonfigurowane konto magazynu do wysyłania dzienników, format rejestrowania przepływu i zasady przechowywania dla dzienników.</span><span class="sxs-lookup"><span data-stu-id="ac705-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="ac705-117">Obecnie grupy zabezpieczeń sieci są obsługiwane w przypadku rejestrowania przepływu.</span><span class="sxs-lookup"><span data-stu-id="ac705-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="ac705-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ac705-118">EXAMPLES</span></span>

### <span data-ttu-id="ac705-119">Przykład 1. Konfigurowanie rejestrowania przepływu dla określonego serwera NSG</span><span class="sxs-lookup"><span data-stu-id="ac705-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="ac705-120">W tym przykładzie konfigurujemy stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ac705-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="ac705-121">W odpowiedzi widać, że określona funkcja NSG ma włączoną funkcję rejestrowania przepływu, domyślny format i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="ac705-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="ac705-122">Przykład 2. Konfigurowanie rejestrowania przepływu dla określonego serwera NSG i ustawianie wersji rejestrowania przepływu na wartość 2.</span><span class="sxs-lookup"><span data-stu-id="ac705-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="ac705-123">W tym przykładzie konfigurujemy rejestrowanie przepływu w grupie zabezpieczeń sieci (NSG, Network Security Group) z określonymi dziennikami w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="ac705-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="ac705-124">W odpowiedzi widać, że dla określonego serwera NSG włączono rejestrowanie przepływu, ustawiono format i nie skonfigurowano żadnych zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="ac705-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="ac705-125">Jeśli region nie obsługuje określonej wersji, aplikacja Network Watcher zapisze domyślną obsługiwaną wersję w regionie.</span><span class="sxs-lookup"><span data-stu-id="ac705-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="ac705-126">Przykład 3. Konfigurowanie rejestrowania przepływu i analizy ruchu dla określonego serwera NSG</span><span class="sxs-lookup"><span data-stu-id="ac705-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="ac705-127">W tym przykładzie konfigurujemy stan rejestrowania przepływu i analizę ruchu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ac705-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="ac705-128">W odpowiedzi widać, że określona NSG ma włączone rejestrowanie przepływu i analizę ruchu, format domyślny i nie są ustawione żadne zasady przechowywania.</span><span class="sxs-lookup"><span data-stu-id="ac705-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="ac705-129">Przykład 4. Wyłączanie analizy ruchu dla określonego serwera NSG ze skonfigurowanym rejestrowaniem przepływu i analizą ruchu</span><span class="sxs-lookup"><span data-stu-id="ac705-129">Example 4: Disable Traffic Analytics for a Specified NSG with Flow Logging and Traffic Analytics configured</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
PS C:\> $workspace = Get-AzOperationalInsightsWorkspace -Name WorkspaceName -ResourceGroupName WorkspaceRg
PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics -Workspace $workspace -TrafficAnalyticsInterval 60


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID -EnableTrafficAnalytics:$false -Workspace $workspace

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
              "enabled": false,
              "workspaceId": "bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb",
              "workspaceRegion": "WorkspaceLocation",
              "workspaceResourceId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourcegroups/WorkspaceRg/providers/microsoft.operationalinsights/workspaces/WorkspaceName",
          "TrafficAnalyticsInterval": 60
            }
          }
```

<span data-ttu-id="ac705-130">W tym przykładzie wyłączyliśmy analizę ruchu dla grupy zabezpieczeń sieci, która ma skonfigurowane wcześniej rejestrowanie przepływu i analizę ruchu.</span><span class="sxs-lookup"><span data-stu-id="ac705-130">In this example we disable Traffic Analytics for a Network Security Group which has flow logging and Traffic Analytics configured earlier.</span></span> <span data-ttu-id="ac705-131">W odpowiedzi widać, że określona funkcja NSG ma włączoną funkcję rejestrowania przepływu, ale funkcja Analizy ruchu jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="ac705-131">In the response, we see the specified NSG has flow logging enabled but Traffic Analytics disabled.</span></span>

## <span data-ttu-id="ac705-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac705-132">PARAMETERS</span></span>

### <span data-ttu-id="ac705-133">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ac705-133">-AsJob</span></span>
<span data-ttu-id="ac705-134">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ac705-134">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac705-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac705-135">-DefaultProfile</span></span>
<span data-ttu-id="ac705-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac705-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac705-137">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="ac705-137">-EnableFlowLog</span></span>
<span data-ttu-id="ac705-138">Oflaguj, aby włączyć/wyłączyć rejestrowanie przepływu.</span><span class="sxs-lookup"><span data-stu-id="ac705-138">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="ac705-139">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="ac705-139">-EnableRetention</span></span>
<span data-ttu-id="ac705-140">Oflaguj, aby włączyć/wyłączyć przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="ac705-140">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="ac705-141">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="ac705-141">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="ac705-142">Oflaguj, aby włączyć/wyłączyć przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="ac705-142">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="ac705-143">-FormatType</span><span class="sxs-lookup"><span data-stu-id="ac705-143">-FormatType</span></span>
<span data-ttu-id="ac705-144">Typ formatu dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="ac705-144">Type of flow log format.</span></span>

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

### <span data-ttu-id="ac705-145">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="ac705-145">-FormatVersion</span></span>
<span data-ttu-id="ac705-146">Wersja formatu dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="ac705-146">Version of flow log format.</span></span>

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

### <span data-ttu-id="ac705-147">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ac705-147">-Location</span></span>
<span data-ttu-id="ac705-148">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="ac705-148">Location of the network watcher.</span></span>

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

### <span data-ttu-id="ac705-149">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac705-149">-NetworkWatcher</span></span>
<span data-ttu-id="ac705-150">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="ac705-150">The network watcher resource.</span></span>

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

### <span data-ttu-id="ac705-151">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="ac705-151">-NetworkWatcherName</span></span>
<span data-ttu-id="ac705-152">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="ac705-152">The name of network watcher.</span></span>

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

### <span data-ttu-id="ac705-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac705-153">-ResourceGroupName</span></span>
<span data-ttu-id="ac705-154">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="ac705-154">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="ac705-155">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ac705-155">-RetentionInDays</span></span>
<span data-ttu-id="ac705-156">Liczba dni, przez które mają być zachowywane rekordy dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="ac705-156">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="ac705-157">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ac705-157">-StorageAccountId</span></span>
<span data-ttu-id="ac705-158">Identyfikator konta magazynu służącego do przechowywania dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="ac705-158">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="ac705-159">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="ac705-159">-TargetResourceId</span></span>
<span data-ttu-id="ac705-160">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="ac705-160">The target resource ID.</span></span>

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

### <span data-ttu-id="ac705-161">- TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="ac705-161">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="ac705-162">Pobiera lub ustawia interwał (w minutach), który określa, jak często usługa TA powinna wykonać analizę przepływu.</span><span class="sxs-lookup"><span data-stu-id="ac705-162">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span> <span data-ttu-id="ac705-163">Obsługiwane wartości to 10 i 60 minut.</span><span class="sxs-lookup"><span data-stu-id="ac705-163">Supported values are 10 and 60 minutes.</span></span>

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

### <span data-ttu-id="ac705-164">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="ac705-164">-Workspace</span></span>
<span data-ttu-id="ac705-165">Obiekt WS używany do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="ac705-165">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="ac705-166">- WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="ac705-166">-WorkspaceGUID</span></span>
<span data-ttu-id="ac705-167">Identyfikator GUID WS używany do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="ac705-167">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="ac705-168">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="ac705-168">-WorkspaceLocation</span></span>
<span data-ttu-id="ac705-169">Azure Region WS, który jest używany do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="ac705-169">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="ac705-170">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="ac705-170">-WorkspaceResourceId</span></span>
<span data-ttu-id="ac705-171">Subskrypcja WS, która jest używana do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="ac705-171">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="ac705-172">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ac705-172">-Confirm</span></span>
<span data-ttu-id="ac705-173">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ac705-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac705-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac705-174">-WhatIf</span></span>
<span data-ttu-id="ac705-175">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac705-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ac705-176">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ac705-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac705-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac705-177">CommonParameters</span></span>
<span data-ttu-id="ac705-178">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac705-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac705-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac705-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac705-180">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac705-180">INPUTS</span></span>

### <span data-ttu-id="ac705-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac705-181">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="ac705-182">System.String</span><span class="sxs-lookup"><span data-stu-id="ac705-182">System.String</span></span>

### <span data-ttu-id="ac705-183">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ac705-183">System.Boolean</span></span>

### <span data-ttu-id="ac705-184">System.Int32</span><span class="sxs-lookup"><span data-stu-id="ac705-184">System.Int32</span></span>

### <span data-ttu-id="ac705-185">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ac705-185">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ac705-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="ac705-186">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="ac705-187">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac705-187">OUTPUTS</span></span>

### <span data-ttu-id="ac705-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="ac705-188">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="ac705-189">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ac705-189">NOTES</span></span>
<span data-ttu-id="ac705-190">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="ac705-190">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="ac705-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac705-191">RELATED LINKS</span></span>

[<span data-ttu-id="ac705-192">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac705-192">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="ac705-193">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac705-193">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="ac705-194">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="ac705-194">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="ac705-195">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="ac705-195">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="ac705-196">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="ac705-196">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="ac705-197">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="ac705-197">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="ac705-198">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="ac705-198">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="ac705-199">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac705-199">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac705-200">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="ac705-200">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="ac705-201">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac705-201">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac705-202">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac705-202">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac705-203">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac705-203">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="ac705-204">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="ac705-204">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="ac705-205">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="ac705-205">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="ac705-206">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="ac705-206">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="ac705-207">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ac705-207">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ac705-208">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ac705-208">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ac705-209">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ac705-209">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ac705-210">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="ac705-210">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="ac705-211">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ac705-211">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ac705-212">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ac705-212">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="ac705-213">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="ac705-213">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="ac705-214">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="ac705-214">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="ac705-215">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="ac705-215">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="ac705-216">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="ac705-216">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="ac705-217">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="ac705-217">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="ac705-218">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="ac705-218">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
