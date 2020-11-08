---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 78F356F6-A621-4C27-B9CC-D103E74B3A33
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancer.md
ms.openlocfilehash: 767f725633560d79cb19e1caad61c08772107b42
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234335"
---
# <span data-ttu-id="d60b1-101">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d60b1-101">Get-AzLoadBalancer</span></span>

## <span data-ttu-id="d60b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d60b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d60b1-103">Pobiera moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d60b1-103">Gets a load balancer.</span></span>

## <span data-ttu-id="d60b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d60b1-104">SYNTAX</span></span>

### <span data-ttu-id="d60b1-105">NOEXPAND (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d60b1-105">NoExpand (Default)</span></span>
```
Get-AzLoadBalancer [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d60b1-106">Większa</span><span class="sxs-lookup"><span data-stu-id="d60b1-106">Expand</span></span>
```
Get-AzLoadBalancer -ResourceGroupName <String> -Name <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d60b1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d60b1-107">DESCRIPTION</span></span>
<span data-ttu-id="d60b1-108">Polecenie cmdlet **Get-AzLoadBalancer** pobiera jeden lub więcej modułów równoważenia obciążenia platformy Azure, które znajdują się w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="d60b1-108">The **Get-AzLoadBalancer** cmdlet gets one or more Azure load balancers that are contained in a resource group.</span></span>

## <span data-ttu-id="d60b1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d60b1-109">EXAMPLES</span></span>

### <span data-ttu-id="d60b1-110">Przykład 1: uzyskiwanie modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="d60b1-110">Example 1: Get a load balancer</span></span>
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="d60b1-111">To polecenie uzyskuje usługę równoważenia obciążenia o nazwie MyLoadBalancer.</span><span class="sxs-lookup"><span data-stu-id="d60b1-111">This command gets the load balancer named MyLoadBalancer.</span></span>
<span data-ttu-id="d60b1-112">Aby można było uruchomić to polecenie cmdlet, musi istnieć moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="d60b1-112">A load balancer must exist before you can run this cmdlet.</span></span>

### <span data-ttu-id="d60b1-113">Przykład 2: Wyświetlanie listy modułów równoważenia obciążenia przy użyciu funkcji filtrowania</span><span class="sxs-lookup"><span data-stu-id="d60b1-113">Example 2: List load balancers using filtering</span></span>
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
                             "Name": "Basic"
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
                             "Name": "Basic"
                           }
```

<span data-ttu-id="d60b1-114">To polecenie pobiera wszystkie moduły równoważenia obciążenia o nazwie rozpoczynającej się od tekstu "MyLoadBalancer".</span><span class="sxs-lookup"><span data-stu-id="d60b1-114">This command gets all load balancers with a name that starts with "MyLoadBalancer"</span></span>

## <span data-ttu-id="d60b1-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d60b1-115">PARAMETERS</span></span>

### <span data-ttu-id="d60b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d60b1-116">-DefaultProfile</span></span>
<span data-ttu-id="d60b1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d60b1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d60b1-118">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="d60b1-118">-ExpandResource</span></span>
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

### <span data-ttu-id="d60b1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d60b1-119">-Name</span></span>
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

### <span data-ttu-id="d60b1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d60b1-120">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d60b1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d60b1-121">CommonParameters</span></span>
<span data-ttu-id="d60b1-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d60b1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d60b1-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d60b1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d60b1-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d60b1-124">INPUTS</span></span>

### <span data-ttu-id="d60b1-125">System. String</span><span class="sxs-lookup"><span data-stu-id="d60b1-125">System.String</span></span>

## <span data-ttu-id="d60b1-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d60b1-126">OUTPUTS</span></span>

### <span data-ttu-id="d60b1-127">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d60b1-127">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="d60b1-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d60b1-128">NOTES</span></span>

## <span data-ttu-id="d60b1-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d60b1-129">RELATED LINKS</span></span>

[<span data-ttu-id="d60b1-130">Nowe — AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d60b1-130">New-AzLoadBalancer</span></span>](./New-AzLoadBalancer.md)

[<span data-ttu-id="d60b1-131">Remove-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d60b1-131">Remove-AzLoadBalancer</span></span>](./Remove-AzLoadBalancer.md)

[<span data-ttu-id="d60b1-132">Set-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="d60b1-132">Set-AzLoadBalancer</span></span>](./Set-AzLoadBalancer.md)


