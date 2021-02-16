---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: 55e98b23f4da1adf641bcf2a3ce7ced95cf5befd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402681"
---
# <span data-ttu-id="d51d0-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d51d0-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="d51d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d51d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d51d0-103">Konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d51d0-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="d51d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d51d0-104">SYNTAX</span></span>

### <span data-ttu-id="d51d0-105">SetFlowlogByResourceWithoutTA (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d51d0-105">SetFlowlogByResourceWithoutTA (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51d0-106">SetFlowlogByResourceWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="d51d0-106">SetFlowlogByResourceWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51d0-107">SetFlowlogByResourceWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="d51d0-107">SetFlowlogByResourceWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d51d0-108">SetFlowlogByNameWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="d51d0-108">SetFlowlogByNameWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -Workspace <IOperationalInsightWorkspace> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51d0-109">SetFlowlogByNameWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="d51d0-109">SetFlowlogByNameWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics]
 -WorkspaceResourceId <String> -WorkspaceGUID <String> -WorkspaceLocation <String>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d51d0-110">SetFlowlogByNameWithoutTA</span><span class="sxs-lookup"><span data-stu-id="d51d0-110">SetFlowlogByNameWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-FormatType <String>] [-FormatVersion <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51d0-111">SetFlowlogByLocationWithTAByResource</span><span class="sxs-lookup"><span data-stu-id="d51d0-111">SetFlowlogByLocationWithTAByResource</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -Workspace <IOperationalInsightWorkspace>
 [-TrafficAnalyticsInterval <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d51d0-112">SetFlowlogByLocationWithTAByDetails</span><span class="sxs-lookup"><span data-stu-id="d51d0-112">SetFlowlogByLocationWithTAByDetails</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-EnableTrafficAnalytics] -WorkspaceResourceId <String>
 -WorkspaceGUID <String> -WorkspaceLocation <String> [-TrafficAnalyticsInterval <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d51d0-113">SetFlowlogByLocationWithoutTA</span><span class="sxs-lookup"><span data-stu-id="d51d0-113">SetFlowlogByLocationWithoutTA</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -Location <String> -TargetResourceId <String> -EnableFlowLog <Boolean>
 -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>] [-FormatType <String>]
 [-FormatVersion <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d51d0-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="d51d0-114">DESCRIPTION</span></span>
<span data-ttu-id="d51d0-115">Ta Set-AzNetworkWatcherConfigFlowLog konfiguruje rejestrowanie przepływu dla zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d51d0-115">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="d51d0-116">Do właściwości, które należy skonfigurować, należą: czy dla udostępnianego zasobu włączono rejestrowanie przepływu, skonfigurowane konto magazynu do wysyłania dzienników, format rejestrowania przepływu i zasady przechowywania dla dzienników.</span><span class="sxs-lookup"><span data-stu-id="d51d0-116">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, the flow logging format, and the retention policy for the logs.</span></span> <span data-ttu-id="d51d0-117">Obecnie grupy zabezpieczeń sieci są obsługiwane do rejestrowania przepływu.</span><span class="sxs-lookup"><span data-stu-id="d51d0-117">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="d51d0-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d51d0-118">EXAMPLES</span></span>

### <span data-ttu-id="d51d0-119">Przykład 1. Konfigurowanie rejestrowania przepływu dla określonego serwera NSG</span><span class="sxs-lookup"><span data-stu-id="d51d0-119">Example 1: Configure Flow Logging for a Specified NSG</span></span>
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

<span data-ttu-id="d51d0-120">W tym przykładzie konfigurujemy stan rejestrowania przepływu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d51d0-120">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="d51d0-121">W odpowiedzi widać, że określona funkcja NSG ma włączoną funkcję rejestrowania przepływu, domyślny format i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d51d0-121">In the response, we see the specified NSG has flow logging enabled, default format, and no retention policy set.</span></span>

### <span data-ttu-id="d51d0-122">Przykład 2. Konfigurowanie rejestrowania przepływu dla określonego serwera NSG i ustawianie wersji rejestrowania przepływu na wartość 2.</span><span class="sxs-lookup"><span data-stu-id="d51d0-122">Example 2: Configure Flow Logging for a Specified NSG and set the version of flow logging to 2.</span></span>
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

<span data-ttu-id="d51d0-123">W tym przykładzie konfigurujemy rejestrowanie przepływu w grupie zabezpieczeń sieci (NSG, Network Security Group) z określonymi dziennikami w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="d51d0-123">In this example, we configure flow logging on a Network Security Group (NSG) with version 2 logs specified.</span></span> <span data-ttu-id="d51d0-124">W odpowiedzi widać, że dla określonego serwera NSG włączono rejestrowanie przepływu, ustawiono format i nie skonfigurowano żadnych zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d51d0-124">In the response, we see the specified NSG has flow logging enabled, the format is set, and there is no retention policy configured.</span></span> <span data-ttu-id="d51d0-125">Jeśli region nie obsługuje określonej wersji, aplikacja Network Watcher zapisze domyślną obsługiwaną wersję w regionie.</span><span class="sxs-lookup"><span data-stu-id="d51d0-125">If the region does not support version you specified, Network Watcher will write the default supported version in the region.</span></span>

### <span data-ttu-id="d51d0-126">Przykład 3. Konfigurowanie rejestrowania przepływu i analizy ruchu dla określonego serwera NSG</span><span class="sxs-lookup"><span data-stu-id="d51d0-126">Example 3: Configure Flow Logging and Traffic Analytics for a Specified NSG</span></span>
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

<span data-ttu-id="d51d0-127">W tym przykładzie konfigurujemy stan rejestrowania przepływu i analizę ruchu dla grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d51d0-127">In this example we configure flow logging status and Traffic Analytics for a Network Security Group.</span></span> <span data-ttu-id="d51d0-128">W odpowiedzi widać, że dla określonego serwera NSG włączono rejestrowanie przepływu i analizę ruchu, format domyślny i nie ustawiono zasad przechowywania.</span><span class="sxs-lookup"><span data-stu-id="d51d0-128">In the response, we see the specified NSG has flow logging and Traffic Analytics enabled, default format, and no retention policy set.</span></span>

## <span data-ttu-id="d51d0-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d51d0-129">PARAMETERS</span></span>

### <span data-ttu-id="d51d0-130">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d51d0-130">-AsJob</span></span>
<span data-ttu-id="d51d0-131">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d51d0-131">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d51d0-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51d0-132">-DefaultProfile</span></span>
<span data-ttu-id="d51d0-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d51d0-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d51d0-134">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="d51d0-134">-EnableFlowLog</span></span>
<span data-ttu-id="d51d0-135">Oflaguj, aby włączyć/wyłączyć rejestrowanie przepływu.</span><span class="sxs-lookup"><span data-stu-id="d51d0-135">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="d51d0-136">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="d51d0-136">-EnableRetention</span></span>
<span data-ttu-id="d51d0-137">Oflaguj, aby włączyć/wyłączyć przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="d51d0-137">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="d51d0-138">-EnableTrafficAnalytics</span><span class="sxs-lookup"><span data-stu-id="d51d0-138">-EnableTrafficAnalytics</span></span>
<span data-ttu-id="d51d0-139">Oflaguj, aby włączyć/wyłączyć przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="d51d0-139">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="d51d0-140">-FormatType</span><span class="sxs-lookup"><span data-stu-id="d51d0-140">-FormatType</span></span>
<span data-ttu-id="d51d0-141">Typ formatu dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="d51d0-141">Type of flow log format.</span></span>

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

### <span data-ttu-id="d51d0-142">-FormatVersion</span><span class="sxs-lookup"><span data-stu-id="d51d0-142">-FormatVersion</span></span>
<span data-ttu-id="d51d0-143">Wersja formatu dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="d51d0-143">Version of flow log format.</span></span>

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

### <span data-ttu-id="d51d0-144">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d51d0-144">-Location</span></span>
<span data-ttu-id="d51d0-145">Lokalizacja czujki sieci.</span><span class="sxs-lookup"><span data-stu-id="d51d0-145">Location of the network watcher.</span></span>

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

### <span data-ttu-id="d51d0-146">— NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d51d0-146">-NetworkWatcher</span></span>
<span data-ttu-id="d51d0-147">Zasób obserwowania sieci.</span><span class="sxs-lookup"><span data-stu-id="d51d0-147">The network watcher resource.</span></span>

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

### <span data-ttu-id="d51d0-148">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d51d0-148">-NetworkWatcherName</span></span>
<span data-ttu-id="d51d0-149">Nazwa osoby oglądacej sieć.</span><span class="sxs-lookup"><span data-stu-id="d51d0-149">The name of network watcher.</span></span>

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

### <span data-ttu-id="d51d0-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d51d0-150">-ResourceGroupName</span></span>
<span data-ttu-id="d51d0-151">Nazwa grupy zasobów obserwowanych sieci.</span><span class="sxs-lookup"><span data-stu-id="d51d0-151">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="d51d0-152">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d51d0-152">-RetentionInDays</span></span>
<span data-ttu-id="d51d0-153">Liczba dni, przez które mają być zachowywane rekordy dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="d51d0-153">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="d51d0-154">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d51d0-154">-StorageAccountId</span></span>
<span data-ttu-id="d51d0-155">Identyfikator konta magazynu służącego do przechowywania dziennika przepływów.</span><span class="sxs-lookup"><span data-stu-id="d51d0-155">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="d51d0-156">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d51d0-156">-TargetResourceId</span></span>
<span data-ttu-id="d51d0-157">Identyfikator zasobu docelowego.</span><span class="sxs-lookup"><span data-stu-id="d51d0-157">The target resource ID.</span></span>

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

### <span data-ttu-id="d51d0-158">- TrafficAnalyticsInterval</span><span class="sxs-lookup"><span data-stu-id="d51d0-158">-TrafficAnalyticsInterval</span></span>
<span data-ttu-id="d51d0-159">Pobiera lub ustawia interwał (w minutach), który określa, jak często usługa TA powinna wykonać analizę przepływu.</span><span class="sxs-lookup"><span data-stu-id="d51d0-159">Gets or sets the interval (in minutes) which would decide how frequently TA service should do flow analytics.</span></span>

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

### <span data-ttu-id="d51d0-160">— Obszar roboczy</span><span class="sxs-lookup"><span data-stu-id="d51d0-160">-Workspace</span></span>
<span data-ttu-id="d51d0-161">Obiekt WS używany do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="d51d0-161">The WS object which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="d51d0-162">- WorkspaceGUID</span><span class="sxs-lookup"><span data-stu-id="d51d0-162">-WorkspaceGUID</span></span>
<span data-ttu-id="d51d0-163">Identyfikator GUID WS używany do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="d51d0-163">GUID of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="d51d0-164">-WorkspaceLocation</span><span class="sxs-lookup"><span data-stu-id="d51d0-164">-WorkspaceLocation</span></span>
<span data-ttu-id="d51d0-165">Azure Region WS, który jest używany do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="d51d0-165">Azure Region of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="d51d0-166">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="d51d0-166">-WorkspaceResourceId</span></span>
<span data-ttu-id="d51d0-167">Subskrypcja WS, która jest używana do przechowywania danych analizy ruchu.</span><span class="sxs-lookup"><span data-stu-id="d51d0-167">Subscription of the WS which is used to store the traffic analytics data.</span></span>

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

### <span data-ttu-id="d51d0-168">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d51d0-168">-Confirm</span></span>
<span data-ttu-id="d51d0-169">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d51d0-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51d0-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51d0-170">-WhatIf</span></span>
<span data-ttu-id="d51d0-171">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d51d0-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d51d0-172">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d51d0-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51d0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51d0-173">CommonParameters</span></span>
<span data-ttu-id="d51d0-174">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d51d0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51d0-175">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51d0-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51d0-176">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d51d0-176">INPUTS</span></span>

### <span data-ttu-id="d51d0-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d51d0-177">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="d51d0-178">System.String</span><span class="sxs-lookup"><span data-stu-id="d51d0-178">System.String</span></span>

### <span data-ttu-id="d51d0-179">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d51d0-179">System.Boolean</span></span>

### <span data-ttu-id="d51d0-180">System.Int32</span><span class="sxs-lookup"><span data-stu-id="d51d0-180">System.Int32</span></span>

### <span data-ttu-id="d51d0-181">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d51d0-181">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d51d0-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span><span class="sxs-lookup"><span data-stu-id="d51d0-182">Microsoft.Azure.Management.Internal.Network.Common.IOperationalInsightWorkspace</span></span>

## <span data-ttu-id="d51d0-183">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d51d0-183">OUTPUTS</span></span>

### <span data-ttu-id="d51d0-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="d51d0-184">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="d51d0-185">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d51d0-185">NOTES</span></span>
<span data-ttu-id="d51d0-186">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span><span class="sxs-lookup"><span data-stu-id="d51d0-186">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="d51d0-187">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d51d0-187">RELATED LINKS</span></span>

[<span data-ttu-id="d51d0-188">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d51d0-188">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d51d0-189">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d51d0-189">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d51d0-190">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d51d0-190">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d51d0-191">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="d51d0-191">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="d51d0-192">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d51d0-192">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d51d0-193">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d51d0-193">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d51d0-194">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d51d0-194">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d51d0-195">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d51d0-195">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d51d0-196">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d51d0-196">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d51d0-197">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d51d0-197">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d51d0-198">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d51d0-198">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d51d0-199">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d51d0-199">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d51d0-200">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="d51d0-200">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="d51d0-201">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d51d0-201">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d51d0-202">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="d51d0-202">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="d51d0-203">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d51d0-203">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d51d0-204">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d51d0-204">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d51d0-205">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d51d0-205">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d51d0-206">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="d51d0-206">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="d51d0-207">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d51d0-207">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d51d0-208">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d51d0-208">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="d51d0-209">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="d51d0-209">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="d51d0-210">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="d51d0-210">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="d51d0-211">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d51d0-211">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="d51d0-212">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="d51d0-212">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="d51d0-213">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="d51d0-213">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="d51d0-214">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="d51d0-214">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)
