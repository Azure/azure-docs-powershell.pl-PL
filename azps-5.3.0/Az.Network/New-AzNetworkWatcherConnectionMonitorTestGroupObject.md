---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379057"
---
# <span data-ttu-id="a3035-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="a3035-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="a3035-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a3035-102">SYNOPSIS</span></span>
<span data-ttu-id="a3035-103">Tworzenie grupy testowej monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="a3035-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="a3035-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a3035-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3035-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a3035-105">DESCRIPTION</span></span>
<span data-ttu-id="a3035-106">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorTestGroupObject tworzy grupę testową monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="a3035-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="a3035-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a3035-107">EXAMPLES</span></span>

### <span data-ttu-id="a3035-108">Przykład 1. Tworzenie grupy testowej z dwoma punktami końcowymi 2 testConfigurations, w źródłowym i 2 docelowym</span><span class="sxs-lookup"><span data-stu-id="a3035-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="a3035-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a3035-109">PARAMETERS</span></span>

### <span data-ttu-id="a3035-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3035-110">-DefaultProfile</span></span>
<span data-ttu-id="a3035-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a3035-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3035-112">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="a3035-112">-Destination</span></span>
<span data-ttu-id="a3035-113">Lista docelowych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="a3035-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="a3035-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="a3035-114">-Disable</span></span>
<span data-ttu-id="a3035-115">Flaga wskazująca, czy grupa testowa jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="a3035-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="a3035-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a3035-116">-Name</span></span>
<span data-ttu-id="a3035-117">Nazwa grupy testowej.</span><span class="sxs-lookup"><span data-stu-id="a3035-117">The test group name.</span></span>

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

### <span data-ttu-id="a3035-118">-Source</span><span class="sxs-lookup"><span data-stu-id="a3035-118">-Source</span></span>
<span data-ttu-id="a3035-119">Lista źródłowych punktów końcowych.</span><span class="sxs-lookup"><span data-stu-id="a3035-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="a3035-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="a3035-120">-TestConfiguration</span></span>
<span data-ttu-id="a3035-121">Lista konfiguracji testu.</span><span class="sxs-lookup"><span data-stu-id="a3035-121">List of test configuration.</span></span>

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

### <span data-ttu-id="a3035-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a3035-122">-Confirm</span></span>
<span data-ttu-id="a3035-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3035-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3035-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3035-124">-WhatIf</span></span>
<span data-ttu-id="a3035-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3035-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3035-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a3035-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3035-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3035-127">CommonParameters</span></span>
<span data-ttu-id="a3035-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3035-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3035-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3035-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3035-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a3035-130">INPUTS</span></span>

### <span data-ttu-id="a3035-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a3035-131">None</span></span>

## <span data-ttu-id="a3035-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a3035-132">OUTPUTS</span></span>

### <span data-ttu-id="a3035-133">Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="a3035-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="a3035-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a3035-134">NOTES</span></span>

## <span data-ttu-id="a3035-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a3035-135">RELATED LINKS</span></span>
