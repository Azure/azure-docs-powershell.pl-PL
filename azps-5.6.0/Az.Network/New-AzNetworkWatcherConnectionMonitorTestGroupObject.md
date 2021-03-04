---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: 4ab9feb0d99bc808cfabb481baf81bb12e050f28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958410"
---
# <span data-ttu-id="ba3df-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="ba3df-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="ba3df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba3df-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3df-103">Utwórz grupę testową monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="ba3df-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="ba3df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba3df-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba3df-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba3df-105">DESCRIPTION</span></span>
<span data-ttu-id="ba3df-106">Polecenie New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet tworzy grupę testową monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="ba3df-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="ba3df-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba3df-107">EXAMPLES</span></span>

### <span data-ttu-id="ba3df-108">Przykład 1. Tworzenie grupy testowej z 2 testConfigurations, w source i 2 punktami końcowymi docelowymi</span><span class="sxs-lookup"><span data-stu-id="ba3df-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="ba3df-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba3df-109">PARAMETERS</span></span>

### <span data-ttu-id="ba3df-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3df-110">-DefaultProfile</span></span>
<span data-ttu-id="ba3df-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3df-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba3df-112">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="ba3df-112">-Destination</span></span>
<span data-ttu-id="ba3df-113">Lista punktów końcowych docelowych.</span><span class="sxs-lookup"><span data-stu-id="ba3df-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3df-114">- Wyłącz</span><span class="sxs-lookup"><span data-stu-id="ba3df-114">-Disable</span></span>
<span data-ttu-id="ba3df-115">Flaga wskazująca, czy grupa testowa jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="ba3df-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="ba3df-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ba3df-116">-Name</span></span>
<span data-ttu-id="ba3df-117">Nazwa grupy testowej.</span><span class="sxs-lookup"><span data-stu-id="ba3df-117">The test group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3df-118">— Źródło</span><span class="sxs-lookup"><span data-stu-id="ba3df-118">-Source</span></span>
<span data-ttu-id="ba3df-119">Lista źródłowych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="ba3df-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3df-120">- TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="ba3df-120">-TestConfiguration</span></span>
<span data-ttu-id="ba3df-121">Lista konfiguracji testowej.</span><span class="sxs-lookup"><span data-stu-id="ba3df-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3df-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba3df-122">-Confirm</span></span>
<span data-ttu-id="ba3df-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba3df-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba3df-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba3df-124">-WhatIf</span></span>
<span data-ttu-id="ba3df-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba3df-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba3df-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ba3df-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba3df-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3df-127">CommonParameters</span></span>
<span data-ttu-id="ba3df-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba3df-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3df-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba3df-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3df-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba3df-130">INPUTS</span></span>

### <span data-ttu-id="ba3df-131">Brak</span><span class="sxs-lookup"><span data-stu-id="ba3df-131">None</span></span>

## <span data-ttu-id="ba3df-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba3df-132">OUTPUTS</span></span>

### <span data-ttu-id="ba3df-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="ba3df-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="ba3df-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba3df-134">NOTES</span></span>

## <span data-ttu-id="ba3df-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba3df-135">RELATED LINKS</span></span>
