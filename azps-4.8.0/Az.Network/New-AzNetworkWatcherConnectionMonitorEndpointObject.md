---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorendpointobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorEndpointObject.md
ms.openlocfilehash: 58e26de74abb46234f6985c3973b5bbe494bd0ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94219484"
---
# <span data-ttu-id="3097e-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="3097e-101">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="3097e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3097e-102">SYNOPSIS</span></span>
<span data-ttu-id="3097e-103">Tworzy punkt końcowy monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="3097e-103">Creates connection monitor endpoint.</span></span>

## <span data-ttu-id="3097e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3097e-104">SYNTAX</span></span>

### <span data-ttu-id="3097e-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="3097e-105">SetByResourceId</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] -ResourceId <String>
 [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3097e-106">SetByAddress</span><span class="sxs-lookup"><span data-stu-id="3097e-106">SetByAddress</span></span>
```
New-AzNetworkWatcherConnectionMonitorEndpointObject [-Name <String>] [-Address <String>] [-FilterType <String>]
 [-FilterItem <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3097e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3097e-107">DESCRIPTION</span></span>
<span data-ttu-id="3097e-108">Polecenie cmdlet New-AzNetworkWatcherConnectionMonitorEndpointObject powoduje utworzenie punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="3097e-108">New-AzNetworkWatcherConnectionMonitorEndpointObject cmdlet creates connection monitor endpoint.</span></span>

## <span data-ttu-id="3097e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3097e-109">EXAMPLES</span></span>

### <span data-ttu-id="3097e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3097e-110">Example 1</span></span>
```powershell
PS C:\>$MySrcResourceId1 = "/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace"
PS C:\>$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type "AgentAddress" -Address "WIN-P0HGNDO2S1B"
PS C:\>$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name "workspaceEndpoint" -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

<span data-ttu-id="3097e-111">Nazwa: workspaceEndpoint ResourceId:/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address: Filter: {"Type": "," Items ": [{" typ ":" AgentAddress "," Address ":" WIN-P0HGNDO2S1B "}]}</span><span class="sxs-lookup"><span data-stu-id="3097e-111">Name       : workspaceEndpoint ResourceId : /subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace Address    : Filter     : { "Type": "Include", "Items": [ { "Type": "AgentAddress", "Address": "WIN-P0HGNDO2S1B" } ] }</span></span>

## <span data-ttu-id="3097e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3097e-112">PARAMETERS</span></span>

### <span data-ttu-id="3097e-113">-Address (adres)</span><span class="sxs-lookup"><span data-stu-id="3097e-113">-Address</span></span>
<span data-ttu-id="3097e-114">Adres punktu końcowego monitora połączenia (adres IP lub nazwa domeny).</span><span class="sxs-lookup"><span data-stu-id="3097e-114">Address of the connection monitor endpoint (IP or domain name).</span></span>

```yaml
Type: System.String
Parameter Sets: SetByAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3097e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3097e-115">-DefaultProfile</span></span>
<span data-ttu-id="3097e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3097e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3097e-117">-FilterItem</span><span class="sxs-lookup"><span data-stu-id="3097e-117">-FilterItem</span></span>
<span data-ttu-id="3097e-118">Lista elementów w filtrze.</span><span class="sxs-lookup"><span data-stu-id="3097e-118">List of items in the filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointFilterItem]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3097e-119">-FilterType</span><span class="sxs-lookup"><span data-stu-id="3097e-119">-FilterType</span></span>
<span data-ttu-id="3097e-120">Zachowanie filtru punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="3097e-120">The behavior of the endpoint filter.</span></span> <span data-ttu-id="3097e-121">Obecnie jest obsługiwana tylko "Dołączanie".</span><span class="sxs-lookup"><span data-stu-id="3097e-121">Currently only 'Include' is supported.</span></span>

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

### <span data-ttu-id="3097e-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3097e-122">-Name</span></span>
<span data-ttu-id="3097e-123">Nazwa punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="3097e-123">The name of the connection monitor endpoint.</span></span>

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

### <span data-ttu-id="3097e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3097e-124">-ResourceId</span></span>
<span data-ttu-id="3097e-125">Identyfikator zasobu punktu końcowego monitora połączenia.</span><span class="sxs-lookup"><span data-stu-id="3097e-125">Resource ID of the connection monitor endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3097e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3097e-126">-Confirm</span></span>
<span data-ttu-id="3097e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3097e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3097e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3097e-128">-WhatIf</span></span>
<span data-ttu-id="3097e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3097e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3097e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3097e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3097e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3097e-131">CommonParameters</span></span>
<span data-ttu-id="3097e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3097e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3097e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3097e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3097e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3097e-134">INPUTS</span></span>

### <span data-ttu-id="3097e-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3097e-135">None</span></span>

## <span data-ttu-id="3097e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3097e-136">OUTPUTS</span></span>

### <span data-ttu-id="3097e-137">Microsoft. Azure. Commands. Network. models. PSNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="3097e-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject</span></span>

## <span data-ttu-id="3097e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3097e-138">NOTES</span></span>

## <span data-ttu-id="3097e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3097e-139">RELATED LINKS</span></span>
