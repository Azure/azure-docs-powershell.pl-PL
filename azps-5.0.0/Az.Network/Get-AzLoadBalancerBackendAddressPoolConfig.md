---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F421174A-B138-45EB-AF84-CB3CE5870F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspoolconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPoolConfig.md
ms.openlocfilehash: f6acd469c49df7e67e8aa9bf00faf4952a33eb79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225195"
---
# <span data-ttu-id="c3c28-101">Get-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3c28-101">Get-AzLoadBalancerBackendAddressPoolConfig</span></span>

## <span data-ttu-id="c3c28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3c28-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c28-103">Pobiera konfigurację puli adresów zaplecza modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c3c28-103">Gets a backend address pool configuration for a load balancer.</span></span>

## <span data-ttu-id="c3c28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3c28-104">SYNTAX</span></span>

```
Get-AzLoadBalancerBackendAddressPoolConfig -LoadBalancer <PSLoadBalancer> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3c28-105">DESCRIPTION</span></span>
<span data-ttu-id="c3c28-106">Polecenie cmdlet **Get-AzLoadBalancerBackendAddressPoolConfig** pobiera pojedynczą pulę adresów zaplecza lub listę pul adresów zaplecza w ramach modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c3c28-106">The **Get-AzLoadBalancerBackendAddressPoolConfig** cmdlet gets a single backend address pool or a list of backend address pools within a load balancer.</span></span>

## <span data-ttu-id="c3c28-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3c28-107">EXAMPLES</span></span>

### <span data-ttu-id="c3c28-108">Przykład 1: pobieranie puli adresów zaplecza</span><span class="sxs-lookup"><span data-stu-id="c3c28-108">Example 1: Get the backend address pool</span></span>
```
PS C:\>$loadbalancer = Get-AzLoadBalancer -Name "MyLoadBalancer" -ResourceGroupName "MyResourceGroup"
PS C:\> Get-AzLoadBalancerBackendAddressPoolConfig -Name "BackendAddressPool02" -LoadBalancer $loadbalancer
```

<span data-ttu-id="c3c28-109">Pierwsze polecenie uzyskuje istniejące Równoważenie obciążenia o nazwie MyLoadBalancer w grupie zasób o nazwie moja grupa, a następnie zapisuje je w zmiennej $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="c3c28-109">The first command gets an existing load balancer named MyLoadBalancer in the resource group named MyResourceGroup, and then stores it in the $loadbalancer variable.</span></span>
<span data-ttu-id="c3c28-110">Drugie polecenie pobiera skojarzoną konfigurację puli adresów zaplecza o nazwie BackendAddressPool02 dla modułu równoważenia obciążenia w $loadbalancer.</span><span class="sxs-lookup"><span data-stu-id="c3c28-110">The second command gets the associated backend address pool configuration named BackendAddressPool02 for the load balancer in $loadbalancer.</span></span>

## <span data-ttu-id="c3c28-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3c28-111">PARAMETERS</span></span>

### <span data-ttu-id="c3c28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c28-112">-DefaultProfile</span></span>
<span data-ttu-id="c3c28-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3c28-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3c28-114">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="c3c28-114">-LoadBalancer</span></span>
<span data-ttu-id="c3c28-115">Określa moduł równoważenia obciążenia skojarzony z pulą adresów zaplecza, aby uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="c3c28-115">Specifies the load balancer that is associated with the backend address pool to get.</span></span>

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

### <span data-ttu-id="c3c28-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3c28-116">-Name</span></span>
<span data-ttu-id="c3c28-117">Określa nazwę modułu równoważenia obciążenia zawierającego pulę adresów zaplecza, która ma zostać pozyskana.</span><span class="sxs-lookup"><span data-stu-id="c3c28-117">Specifies the name of the load balancer that contains the backend address pool to get.</span></span>

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

### <span data-ttu-id="c3c28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c28-118">CommonParameters</span></span>
<span data-ttu-id="c3c28-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3c28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c28-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3c28-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c28-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3c28-121">INPUTS</span></span>

### <span data-ttu-id="c3c28-122">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3c28-122">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

## <span data-ttu-id="c3c28-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3c28-123">OUTPUTS</span></span>

### <span data-ttu-id="c3c28-124">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c3c28-124">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="c3c28-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3c28-125">NOTES</span></span>

## <span data-ttu-id="c3c28-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3c28-126">RELATED LINKS</span></span>

[<span data-ttu-id="c3c28-127">Dodaj-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3c28-127">Add-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Add-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c3c28-128">Get-AzLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="c3c28-128">Get-AzLoadBalancer</span></span>](./Get-AzLoadBalancer.md)

[<span data-ttu-id="c3c28-129">Nowe — AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3c28-129">New-AzLoadBalancerBackendAddressPoolConfig</span></span>](./New-AzLoadBalancerBackendAddressPoolConfig.md)

[<span data-ttu-id="c3c28-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span><span class="sxs-lookup"><span data-stu-id="c3c28-130">Remove-AzLoadBalancerBackendAddressPoolConfig</span></span>](./Remove-AzLoadBalancerBackendAddressPoolConfig.md)


