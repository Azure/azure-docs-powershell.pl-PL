---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: dd887874540a216cc826f807059e6534b99e28f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179882"
---
# <span data-ttu-id="1f89c-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f89c-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="1f89c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f89c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f89c-103">Pobiera równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1f89c-103">Gets a load balancer.</span></span>

## <span data-ttu-id="1f89c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f89c-104">SYNTAX</span></span>

### <span data-ttu-id="1f89c-105">NoExpand (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1f89c-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f89c-106">Rozwiń</span><span class="sxs-lookup"><span data-stu-id="1f89c-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f89c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f89c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f89c-108">Polecenie **cmdlet Get-AzLoadBalancer** pobiera co najmniej jedno narzędzie do równoważenia obciążenia platformy Azure, które są zawarte w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="1f89c-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="1f89c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f89c-109">EXAMPLES</span></span>

### <span data-ttu-id="1f89c-110">Przykład 1. Uzyskiwanie równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="1f89c-110">Example 1: Get a load balancer</span></span>
```
PS C:\> Get-AzLoadBalancer -Name "MyLoadBalancer1" -ResourceGroupName "MyResourceGroup"

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="1f89c-111">To polecenie pobiera równoważenie obciążenia o nazwie MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="1f89c-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="1f89c-112">Aby można było uruchomić to polecenie cmdlet, musi istnieć równoważenie obciążenia.</span><span class="sxs-lookup"><span data-stu-id="1f89c-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="1f89c-113">Przykład 2. Lista elementów równoważenia obciążenia przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="1f89c-113">Example 2: List load balancers using filtering</span></span>
```
PS C:\> Get-AzLoadBalancer -Name MyLoadBalancer*

Name                     : MyLoadBalancer1
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }

Name                     : MyLoadBalancer2
ResourceGroupName        : MyResourceGroup
Location                 : australiaeast
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/MyResourceGroup/providers/M
                           icrosoft.Network/loadBalancers/MyLoadBalancer2
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
FrontendIpConfigurations : []
BackendAddressPools      : []
LoadBalancingRules       : []
Probes                   : []
InboundNatRules          : []
InboundNatPools          : []
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
```

<span data-ttu-id="1f89c-114">To polecenie pobiera wszystkie równoważenie obciążenia o nazwie, która zaczyna się od "MyLoadBalancer"</span><span class="sxs-lookup"><span data-stu-id="1f89c-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="1f89c-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f89c-115">PARAMETERS</span></span>

### <span data-ttu-id="1f89c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f89c-116">-DefaultProfile</span></span>
<span data-ttu-id="1f89c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f89c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f89c-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="1f89c-118">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f89c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f89c-119">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1f89c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f89c-120">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="1f89c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f89c-121">CommonParameters</span></span>
<span data-ttu-id="1f89c-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f89c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f89c-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f89c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f89c-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f89c-124">INPUTS</span></span>

### <span data-ttu-id="1f89c-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1f89c-125">System.String</span></span>

## <span data-ttu-id="1f89c-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f89c-126">OUTPUTS</span></span>

### <span data-ttu-id="1f89c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f89c-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="1f89c-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f89c-128">NOTES</span></span>

## <span data-ttu-id="1f89c-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f89c-129">RELATED LINKS</span></span>

[<span data-ttu-id="1f89c-130">New-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f89c-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="1f89c-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f89c-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="1f89c-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="1f89c-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


