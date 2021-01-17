---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 5d1c561af678086671927d3782a1fafbd9de503b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365547"
---
# <span data-ttu-id="7d930-101">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d930-101">Get-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="7d930-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d930-102">SYNOPSIS</span></span>
<span data-ttu-id="7d930-103">Get-AzLoadBalancerBackendAddressPool pobiera co najmniej jeden zestaw adresów zaplecza skojarzony z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d930-103">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span> 

## <span data-ttu-id="7d930-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d930-104">SYNTAX</span></span>

### <span data-ttu-id="7d930-105">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d930-105">GetByNameParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -LoadBalancerName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d930-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d930-106">GetByParentObjectParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool [-Name <String>] -LoadBalancer <PSLoadBalancer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d930-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d930-107">GetByResourceIdParameterSet</span></span>
```
Get-AzLoadBalancerBackendAddressPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d930-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d930-108">DESCRIPTION</span></span>
<span data-ttu-id="7d930-109">Get-AzLoadBalancerBackendAddressPool pobiera co najmniej jeden zestaw adresów zaplecza skojarzony z modułem równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d930-109">Get-AzLoadBalancerBackendAddressPool retrieves one or more backend address pools associated with a load balancer.</span></span>

## <span data-ttu-id="7d930-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d930-110">EXAMPLES</span></span>

### <span data-ttu-id="7d930-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7d930-111">Example 1</span></span>
```powershell
## Get single backend under loadbalancer
PS C:\> $lb = Get-AzLoadBalancer -ResourceGroupName $resourceGroup -Name $loadBalancerName
```

```powershell
## Get all backends under loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool
```
### <span data-ttu-id="7d930-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7d930-112">Example 2</span></span>
```powershell
#Get specific backend from loadbalancer
PS C:\> $lb | Get-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="7d930-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7d930-113">Example 3</span></span>
```powershell
#Get a backend by resource Id
PS C:\> Get-AzLoadBalancerBackendAddressPool -ResourceId $backendPool1.Id
```

## <span data-ttu-id="7d930-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d930-114">PARAMETERS</span></span>

### <span data-ttu-id="7d930-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d930-115">-DefaultProfile</span></span>
<span data-ttu-id="7d930-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d930-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d930-117">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="7d930-117">-LoadBalancer</span></span>
<span data-ttu-id="7d930-118">{{Opis modułu równoważenia obciążenia}}</span><span class="sxs-lookup"><span data-stu-id="7d930-118">{{ Fill LoadBalancer Description }}</span></span>

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

### <span data-ttu-id="7d930-119">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="7d930-119">-LoadBalancerName</span></span>
<span data-ttu-id="7d930-120">Nazwa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d930-120">The name of the load balancer.</span></span>

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

### <span data-ttu-id="7d930-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7d930-121">-Name</span></span>
<span data-ttu-id="7d930-122">Nazwa puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="7d930-122">The name of the backend address pool.</span></span>

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

### <span data-ttu-id="7d930-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d930-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d930-124">Nazwa grupy zasobów modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7d930-124">The resource group name of the load balancer.</span></span>

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

### <span data-ttu-id="7d930-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d930-125">-ResourceId</span></span>

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

### <span data-ttu-id="7d930-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d930-126">CommonParameters</span></span>
<span data-ttu-id="7d930-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d930-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d930-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d930-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d930-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d930-129">INPUTS</span></span>

### <span data-ttu-id="7d930-130">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7d930-130">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="7d930-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7d930-131">System.String</span></span>

## <span data-ttu-id="7d930-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d930-132">OUTPUTS</span></span>

### <span data-ttu-id="7d930-133">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="7d930-133">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="7d930-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d930-134">NOTES</span></span>

## <span data-ttu-id="7d930-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d930-135">RELATED LINKS</span></span>
