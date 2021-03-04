---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 72afb446b41143348b9feaa7e1b465a41d2b9cbe
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956833"
---
# <span data-ttu-id="b34fd-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b34fd-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="b34fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b34fd-102">SYNOPSIS</span></span>
<span data-ttu-id="b34fd-103">Get-AzLoadBalancerBackendAddressPool pobiera co najmniej jedną pulę adresów zaplecza skojarzoną z równoważeniem obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b34fd-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="b34fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b34fd-104">SYNTAX</span></span>

### <span data-ttu-id="b34fd-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b34fd-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b34fd-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b34fd-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b34fd-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b34fd-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b34fd-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b34fd-108">DESCRIPTION</span></span>
<span data-ttu-id="b34fd-109">Get-AzLoadBalancerBackendAddressPool pobiera co najmniej jedną pulę adresów zaplecza skojarzoną z równoważeniem obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b34fd-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="b34fd-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b34fd-110">EXAMPLES</span></span>

### <span data-ttu-id="b34fd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b34fd-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="b34fd-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b34fd-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="b34fd-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b34fd-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="b34fd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b34fd-114">PARAMETERS</span></span>

### <span data-ttu-id="b34fd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b34fd-115">-DefaultProfile</span></span>
<span data-ttu-id="b34fd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b34fd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34fd-117">-LoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b34fd-117">-LoadBalancer</span></span>
<span data-ttu-id="b34fd-118">{{ Fill LoadBalancer Description }}</span><span class="sxs-lookup"><span data-stu-id="b34fd-118">{{ Fill LoadBalancer Description }}</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b34fd-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="b34fd-119">-LoadBalancerName</span></span>
<span data-ttu-id="b34fd-120">Nazwa urządzenia do równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b34fd-120">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34fd-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b34fd-121">-Name</span></span>
<span data-ttu-id="b34fd-122">Nazwa puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b34fd-122">The name of the backend address pool.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b34fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="b34fd-124">Nazwa grupy zasobów dla równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="b34fd-124">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b34fd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b34fd-125">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b34fd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b34fd-126">CommonParameters</span></span>
<span data-ttu-id="b34fd-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b34fd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b34fd-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b34fd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b34fd-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b34fd-129">INPUTS</span></span>

### <span data-ttu-id="b34fd-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="b34fd-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="b34fd-131">System.String</span><span class="sxs-lookup"><span data-stu-id="b34fd-131">System.String</span></span>

## <span data-ttu-id="b34fd-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b34fd-132">OUTPUTS</span></span>

### <span data-ttu-id="b34fd-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b34fd-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="b34fd-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b34fd-134">NOTES</span></span>

## <span data-ttu-id="b34fd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b34fd-135">RELATED LINKS</span></span>
