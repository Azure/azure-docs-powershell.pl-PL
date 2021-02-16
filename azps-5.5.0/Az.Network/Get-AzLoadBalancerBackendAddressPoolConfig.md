---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189762"
---
# <span data-ttu-id="43d34-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43d34-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="43d34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43d34-102">SYNOPSIS</span></span>
<span data-ttu-id="43d34-103">Pobiera konfigurację puli adresów zaplecza dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="43d34-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="43d34-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="43d34-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43d34-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="43d34-105">DESCRIPTION</span></span>
<span data-ttu-id="43d34-106">Polecenie **cmdlet Get-AzLoadBalancerBackendAddressPoolConfig** pobiera jedną pulę adresów zaplecza lub listę pul adresów zaplecza w ramach równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="43d34-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="43d34-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="43d34-107">EXAMPLES</span></span>

### <span data-ttu-id="43d34-108">Przykład 1. Uzyskiwanie puli adresów zaplecza</span><span class="sxs-lookup"><span data-stu-id="43d34-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="43d34-109">Pierwsze polecenie pobiera istniejące polecenie równoważenia obciążenia o nazwie MyLoadBalancer w grupie zasobów o nazwie MyResourceGroup, a następnie przechowuje je w $loadbalancer danych.</span><span class="sxs-lookup"><span data-stu-id="43d34-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="43d34-110">Drugie polecenie pobiera skojarzoną konfigurację puli adresów zaplecza o nazwie BackendAddressPool02 dla równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="43d34-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="43d34-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43d34-111">PARAMETERS</span></span>

### <span data-ttu-id="43d34-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d34-112">-DefaultProfile</span></span>
<span data-ttu-id="43d34-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="43d34-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43d34-114">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43d34-114">-LoadBalancer</span></span>
<span data-ttu-id="43d34-115">Określa, jaka wartość zostanie skojarzona z pulą adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="43d34-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLoadBalancer
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43d34-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="43d34-116">-Name</span></span>
<span data-ttu-id="43d34-117">Określa nazwę serwera równoważenia obciążenia, który zawiera pulę adresów zaplecza do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="43d34-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="43d34-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d34-118">CommonParameters</span></span>
<span data-ttu-id="43d34-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d34-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d34-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="43d34-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d34-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43d34-121">INPUTS</span></span>

### <span data-ttu-id="43d34-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43d34-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="43d34-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43d34-123">OUTPUTS</span></span>

### <span data-ttu-id="43d34-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="43d34-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="43d34-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="43d34-125">NOTES</span></span>

## <span data-ttu-id="43d34-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43d34-126">RELATED LINKS</span></span>

[<span data-ttu-id="43d34-127">Add-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43d34-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="43d34-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="43d34-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="43d34-129">New-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43d34-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="43d34-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="43d34-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


