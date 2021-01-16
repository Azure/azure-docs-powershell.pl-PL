---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azloadbalancerbackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzLoadBalancerBackendAddressPool.md
ms.openlocfilehash: 691a45899480485f35164d4f18aea1595f70fbc9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322322"
---
# <span data-ttu-id="3dedf-101">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3dedf-101">Remove-AzLoadBalancerBackendAddressPool</span></span>

## <span data-ttu-id="3dedf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dedf-102">SYNOPSIS</span></span>
<span data-ttu-id="3dedf-103">Usuwa pulę zaplecza z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3dedf-103">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="3dedf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dedf-104">SYNTAX</span></span>

### <span data-ttu-id="3dedf-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dedf-105">DeleteByNameParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -ResourceGroupName <String> -Name <String> [-LoadBalancerName <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dedf-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool -Name <String> [-LoadBalancerName <String>]
 -LoadBalancer <PSLoadBalancer> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3dedf-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dedf-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] [-InputObject <PSBackendAddressPool>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dedf-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3dedf-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzLoadBalancerBackendAddressPool [-LoadBalancerName <String>] -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dedf-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3dedf-109">DESCRIPTION</span></span>
<span data-ttu-id="3dedf-110">Usuwa pulę zaplecza z modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3dedf-110">Removes a backend pool from a load balancer</span></span>

## <span data-ttu-id="3dedf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dedf-111">EXAMPLES</span></span>

### <span data-ttu-id="3dedf-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3dedf-112">Example 1</span></span>
```powershell
##removing by passing lb object via pipeline
PS C:\> $lb | Remove-AzLoadBalancerBackendAddressPool -Name $backendPool1
```

### <span data-ttu-id="3dedf-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="3dedf-113">Example 2</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -InputObject $backendPoolObject
```

### <span data-ttu-id="3dedf-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="3dedf-114">Example 3</span></span>
```powershell
##removing by passing input object
PS C:\> Remove-AzLoadBalancerBackendAddressPool -ResourceId $backendPoolObject.Id
```

## <span data-ttu-id="3dedf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dedf-115">PARAMETERS</span></span>

### <span data-ttu-id="3dedf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dedf-116">-DefaultProfile</span></span>
<span data-ttu-id="3dedf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dedf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dedf-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3dedf-118">-InputObject</span></span>
<span data-ttu-id="3dedf-119">Pula adresów zaplecza do usunięcia</span><span class="sxs-lookup"><span data-stu-id="3dedf-119">The backend address pool to remove</span></span>

```yaml
Type: PSBackendAddressPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-120">-Moduł równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="3dedf-120">-LoadBalancer</span></span>
<span data-ttu-id="3dedf-121">Zasób modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3dedf-121">The load balancer resource.</span></span>

```yaml
Type: PSLoadBalancer
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-122">-LoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="3dedf-122">-LoadBalancerName</span></span>
<span data-ttu-id="3dedf-123">Nazwa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3dedf-123">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3dedf-124">-Name</span></span>
<span data-ttu-id="3dedf-125">Nazwa modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3dedf-125">The name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dedf-126">-PassThru</span></span>
<span data-ttu-id="3dedf-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3dedf-127">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dedf-128">-ResourceGroupName</span></span>
<span data-ttu-id="3dedf-129">Nazwa grupy zasobów modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="3dedf-129">The resource group name of the load balancer.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dedf-130">-ResourceId</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3dedf-131">-Confirm</span></span>
<span data-ttu-id="3dedf-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dedf-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dedf-133">-WhatIf</span></span>
<span data-ttu-id="3dedf-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dedf-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dedf-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3dedf-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dedf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dedf-136">CommonParameters</span></span>
<span data-ttu-id="3dedf-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dedf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dedf-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dedf-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dedf-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dedf-139">INPUTS</span></span>

### <span data-ttu-id="3dedf-140">Microsoft. Azure. Commands. Network. models. PSLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3dedf-140">Microsoft.Azure.Commands.Network.Models.PSLoadBalancer</span></span>

### <span data-ttu-id="3dedf-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3dedf-141">System.String</span></span>

## <span data-ttu-id="3dedf-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dedf-142">OUTPUTS</span></span>

### <span data-ttu-id="3dedf-143">Microsoft. Azure. Commands. Network. models. PSBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="3dedf-143">Microsoft.Azure.Commands.Network.Models.PSBackendAddressPool</span></span>

## <span data-ttu-id="3dedf-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dedf-144">NOTES</span></span>

## <span data-ttu-id="3dedf-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dedf-145">RELATED LINKS</span></span>
